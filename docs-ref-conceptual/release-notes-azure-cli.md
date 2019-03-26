---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/15/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 4337f2203841d6247e4b487d245138424c63e448
ms.sourcegitcommit: 71c0ccd475524cf4d6db45bba8139fef3262d764
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "58175135"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="b0184-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="b0184-103">Azure CLI release notes</span></span>
## <a name="march-12-2019"></a><span data-ttu-id="b0184-104">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="b0184-104">March 12, 2019</span></span>

<span data-ttu-id="b0184-105">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="b0184-105">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="b0184-106">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-106">Core</span></span>

* <span data-ttu-id="b0184-107">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-107">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-108">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-108">ACR</span></span>

* <span data-ttu-id="b0184-109">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-109">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-110">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-110">ACS</span></span>

* <span data-ttu-id="b0184-111">`aks browse` に対する `--listen-address` 引数は、`kubectl` がサポートしない場合は無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-111">Changed to ignore `--listen-address` argument to `aks browse` if `kubectl` doesn't support it</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-112">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-112">AppService</span></span>

* <span data-ttu-id="b0184-113">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-113">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="b0184-114">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-114">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="b0184-115">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-115">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="b0184-116">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-116">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="b0184-117">Botservice</span><span class="sxs-lookup"><span data-stu-id="b0184-117">Botservice</span></span>

* <span data-ttu-id="b0184-118">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-118">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="b0184-119">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-119">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="b0184-120">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-120">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="b0184-121">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-121">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="b0184-122">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-122">Container</span></span>

* <span data-ttu-id="b0184-123">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-123">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="b0184-124">EventHub</span><span class="sxs-lookup"><span data-stu-id="b0184-124">EventHub</span></span>

* <span data-ttu-id="b0184-125">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-125">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="b0184-126">Find</span><span class="sxs-lookup"><span data-stu-id="b0184-126">Find</span></span>

* <span data-ttu-id="b0184-127">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="b0184-127">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b0184-128">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b0184-128">HDInsight</span></span>

* <span data-ttu-id="b0184-129">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-129">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="b0184-130">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-130">Network</span></span>

* <span data-ttu-id="b0184-131">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-131">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0184-132">Rdbms</span><span class="sxs-lookup"><span data-stu-id="b0184-132">Rdbms</span></span>

* <span data-ttu-id="b0184-133">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="b0184-133">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="b0184-134">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-134">Role</span></span>

* <span data-ttu-id="b0184-135">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-135">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="b0184-136">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-136">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b0184-137">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b0184-137">Service Fabric</span></span>

* <span data-ttu-id="b0184-138">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-138">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="b0184-139">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="b0184-139">February 26, 2019</span></span>

<span data-ttu-id="b0184-140">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="b0184-140">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="b0184-141">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-141">Core</span></span>

* <span data-ttu-id="b0184-142">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-142">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-143">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-143">ACR</span></span>

* <span data-ttu-id="b0184-144">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-144">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="b0184-145">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-145">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-146">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-146">ACS</span></span>

* <span data-ttu-id="b0184-147">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-147">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-148">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-148">AppService</span></span>

* <span data-ttu-id="b0184-149">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-149">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-150">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-150">Batch</span></span>
* <span data-ttu-id="b0184-151">[破壊的変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-151">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="b0184-152">[破壊的変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-152">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="b0184-153">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-153">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="b0184-154">[破壊的変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-154">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="b0184-155">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-155">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="b0184-156">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="b0184-156">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0184-157">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0184-157">CosmosDB</span></span>

* <span data-ttu-id="b0184-158">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-158">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="b0184-159">Kusto</span><span class="sxs-lookup"><span data-stu-id="b0184-159">Kusto</span></span>

* <span data-ttu-id="b0184-160">[破壊的変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-160">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="b0184-161">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-161">Network</span></span>

* <span data-ttu-id="b0184-162">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-162">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="b0184-163">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-163">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="b0184-164">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-164">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="b0184-165">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-165">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="b0184-166">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-166">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="b0184-167">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-167">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="b0184-168">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-168">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-169">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-169">Resource</span></span>

* <span data-ttu-id="b0184-170">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-170">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="b0184-171">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-171">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="b0184-172">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-172">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="b0184-173">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-173">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="b0184-174">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-174">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="b0184-175">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-175">Role</span></span>

* <span data-ttu-id="b0184-176">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-176">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-177">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-177">VM</span></span>

* <span data-ttu-id="b0184-178">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-178">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="b0184-179">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="b0184-179">February 12, 2019</span></span>

<span data-ttu-id="b0184-180">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="b0184-180">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="b0184-181">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-181">Core</span></span>

* <span data-ttu-id="b0184-182">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-182">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="b0184-183">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-183">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-184">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-184">ACR</span></span>
* <span data-ttu-id="b0184-185">[破壊的変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-185">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="b0184-186">[破壊的変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-186">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-187">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-187">ACS</span></span>
* <span data-ttu-id="b0184-188">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-188">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="b0184-189">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-189">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="b0184-190">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-190">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="b0184-191">AMS</span><span class="sxs-lookup"><span data-stu-id="b0184-191">AMS</span></span>
* <span data-ttu-id="b0184-192">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-192">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="b0184-193">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-193">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-194">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-194">Appservice</span></span>
* <span data-ttu-id="b0184-195">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-195">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="b0184-196">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-196">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="b0184-197">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-197">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="b0184-198">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-198">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="b0184-199">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-199">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="b0184-200">Botservice</span><span class="sxs-lookup"><span data-stu-id="b0184-200">Botservice</span></span>
* <span data-ttu-id="b0184-201">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-201">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="b0184-202">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-202">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="b0184-203">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-203">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="b0184-204">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-204">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="b0184-205">[非推奨] `--proj-file-path` を優先して、`--proj-name` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-205">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="b0184-206">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-206">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="b0184-207">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-207">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="b0184-208">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-208">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="b0184-209">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="b0184-209">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="b0184-210">8.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-210">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="b0184-211">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b0184-211">Key Vault</span></span>
* <span data-ttu-id="b0184-212">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-212">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-213">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-213">Monitor</span></span>
* <span data-ttu-id="b0184-214">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-214">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="b0184-215">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-215">Network</span></span>
* <span data-ttu-id="b0184-216">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-216">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="b0184-217">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-217">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="b0184-218">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-218">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="b0184-219">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-219">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="b0184-220">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="b0184-220">Policy Insights</span></span>
* <span data-ttu-id="b0184-221">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-221">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0184-222">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0184-222">RDBMS</span></span>
* <span data-ttu-id="b0184-223">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-223">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="b0184-224">Redis</span><span class="sxs-lookup"><span data-stu-id="b0184-224">Redis</span></span>
* <span data-ttu-id="b0184-225">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-225">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="b0184-226">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-226">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="b0184-227">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-227">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="b0184-228">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-228">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="b0184-229">[破壊的変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-229">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="b0184-230">[破壊的変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0184-230">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="b0184-231">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-231">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="b0184-232">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-232">Role</span></span>
* <span data-ttu-id="b0184-233">[破壊的変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="b0184-233">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="b0184-234">SQL VM</span><span class="sxs-lookup"><span data-stu-id="b0184-234">SQL VM</span></span>
* <span data-ttu-id="b0184-235">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-235">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-236">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-236">VM</span></span>
* <span data-ttu-id="b0184-237">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-237">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="b0184-238">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-238">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="b0184-239">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-239">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="b0184-240">[破壊的変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="b0184-240">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="b0184-241">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b0184-241">January 31, 2019</span></span>

<span data-ttu-id="b0184-242">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="b0184-242">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="b0184-243">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-243">Core</span></span>

* <span data-ttu-id="b0184-244">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="b0184-244">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="b0184-245">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b0184-245">January 28, 2019</span></span>

<span data-ttu-id="b0184-246">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="b0184-246">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-247">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-247">ACR</span></span>
* <span data-ttu-id="b0184-248">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-248">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-249">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-249">ACS</span></span>
* <span data-ttu-id="b0184-250">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-250">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="b0184-251">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-251">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="b0184-252">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-252">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="b0184-253">AMS</span><span class="sxs-lookup"><span data-stu-id="b0184-253">AMS</span></span>
* <span data-ttu-id="b0184-254">[破壊的変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-254">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="b0184-255">[破壊的変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-255">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-256">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-256">Appservice</span></span>
* <span data-ttu-id="b0184-257">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-257">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="b0184-258">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-258">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="b0184-259">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-259">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="b0184-260">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-260">Container</span></span>
* <span data-ttu-id="b0184-261">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-261">Added `container start` command</span></span>
* <span data-ttu-id="b0184-262">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-262">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="b0184-263">EventGrid</span><span class="sxs-lookup"><span data-stu-id="b0184-263">EventGrid</span></span>
* <span data-ttu-id="b0184-264">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-264">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="b0184-265">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-265">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="b0184-266">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-266">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="b0184-267">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-267">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="b0184-268">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="b0184-268">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b0184-269">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b0184-269">HDInsight</span></span>
* <span data-ttu-id="b0184-270">[破壊的変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-270">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="b0184-271">[破壊的変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-271">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="b0184-272">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-272">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="b0184-273">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-273">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="b0184-274">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-274">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="b0184-275">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-275">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="b0184-276">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-276">IoT</span></span>
* <span data-ttu-id="b0184-277">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-277">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="b0184-278">Kusto</span><span class="sxs-lookup"><span data-stu-id="b0184-278">Kusto</span></span>
* <span data-ttu-id="b0184-279">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b0184-279">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-280">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-280">Monitor</span></span>
* <span data-ttu-id="b0184-281">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-281">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="b0184-282">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-282">Profile</span></span>
* <span data-ttu-id="b0184-283">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-283">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="b0184-284">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-284">Network</span></span>
* <span data-ttu-id="b0184-285">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-285">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="b0184-286">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-286">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-287">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-287">Resource</span></span>
* <span data-ttu-id="b0184-288">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-288">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="b0184-289">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-289">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="b0184-290">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="b0184-290">SQL Virtual Machine</span></span>
* <span data-ttu-id="b0184-291">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b0184-291">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-292">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-292">Storage</span></span>
* <span data-ttu-id="b0184-293">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-293">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="b0184-294">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="b0184-294">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-295">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-295">VM</span></span>
* <span data-ttu-id="b0184-296">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-296">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="b0184-297">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-297">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="b0184-298">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="b0184-298">January 15, 2019</span></span>

<span data-ttu-id="b0184-299">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="b0184-299">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-300">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-300">ACR</span></span>
* <span data-ttu-id="b0184-301">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-301">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="b0184-302">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-302">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="b0184-303">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-303">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="b0184-304">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-304">ACS</span></span>
* <span data-ttu-id="b0184-305">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-305">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-306">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-306">Appservice</span></span>
* <span data-ttu-id="b0184-307">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-307">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="b0184-308">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-308">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="b0184-309">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-309">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="b0184-310">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-310">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="b0184-311">Botservice</span><span class="sxs-lookup"><span data-stu-id="b0184-311">Botservice</span></span>
* <span data-ttu-id="b0184-312">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-312">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="b0184-313">構成</span><span class="sxs-lookup"><span data-stu-id="b0184-313">Configure</span></span>
* <span data-ttu-id="b0184-314">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-314">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0184-315">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0184-315">CosmosDB</span></span>
* <span data-ttu-id="b0184-316">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-316">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b0184-317">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b0184-317">HDInsight</span></span>
* <span data-ttu-id="b0184-318">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-318">Added commands for managing applications</span></span>
* <span data-ttu-id="b0184-319">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-319">Added commands for managing script actions</span></span>
* <span data-ttu-id="b0184-320">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-320">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="b0184-321">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-321">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="b0184-322">[破壊的変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-322">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="b0184-323">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-323">Network</span></span>
* <span data-ttu-id="b0184-324">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-324">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="b0184-325">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-325">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="b0184-326">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-326">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="b0184-327">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-327">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="b0184-328">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-328">Role</span></span>
* <span data-ttu-id="b0184-329">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="b0184-329">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="b0184-330">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="b0184-330">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="b0184-331">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b0184-331">Security</span></span>
* <span data-ttu-id="b0184-332">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-332">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-333">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-333">Storage</span></span>
* <span data-ttu-id="b0184-334">[破壊的変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-334">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="b0184-335">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b0184-335">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="b0184-336">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-336">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="b0184-337">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-337">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="b0184-338">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-338">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-339">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-339">VM</span></span>
* <span data-ttu-id="b0184-340">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-340">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="b0184-341">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-341">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="b0184-342">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-342">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="b0184-343">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-343">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="b0184-344">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-344">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="b0184-345">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-345">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="b0184-346">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="b0184-346">December 20, 2018</span></span>

<span data-ttu-id="b0184-347">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="b0184-347">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="b0184-348">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-348">Appservice</span></span>
* <span data-ttu-id="b0184-349">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-349">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="b0184-350">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-350">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="b0184-351">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-351">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="b0184-352">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="b0184-352">IoTCentral</span></span>
* <span data-ttu-id="b0184-353">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-353">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="b0184-354">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-354">Role</span></span>
* <span data-ttu-id="b0184-355">[破壊的変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-355">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-356">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-356">SQL</span></span>
* <span data-ttu-id="b0184-357">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-357">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-358">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-358">VM</span></span>
* <span data-ttu-id="b0184-359">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-359">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="b0184-360">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="b0184-360">December 18, 2018</span></span>

<span data-ttu-id="b0184-361">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="b0184-361">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="b0184-362">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-362">ACR</span></span>
* <span data-ttu-id="b0184-363">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-363">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="b0184-364">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="b0184-364">Condensed the table layout for task list</span></span>
* <span data-ttu-id="b0184-365">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-365">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-366">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-366">ACS</span></span>
* <span data-ttu-id="b0184-367">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-367">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="b0184-368">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-368">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="b0184-369">[非推奨] `az acs` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-369">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="b0184-370">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="b0184-370">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="b0184-371">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-371">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="b0184-372">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-372">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-373">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-373">Appservice</span></span>
* <span data-ttu-id="b0184-374">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-374">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="b0184-375">Botservice</span><span class="sxs-lookup"><span data-stu-id="b0184-375">Botservice</span></span>
* <span data-ttu-id="b0184-376">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-376">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="b0184-377">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-377">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="b0184-378">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-378">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="b0184-379">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="b0184-379">Reduced Kudu network calls</span></span>
* <span data-ttu-id="b0184-380">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-380">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="b0184-381">消費</span><span class="sxs-lookup"><span data-stu-id="b0184-381">Consumption</span></span>
* <span data-ttu-id="b0184-382">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-382">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0184-383">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0184-383">CosmosDB</span></span>
* <span data-ttu-id="b0184-384">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-384">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="b0184-385">マップ</span><span class="sxs-lookup"><span data-stu-id="b0184-385">Maps</span></span>
* <span data-ttu-id="b0184-386">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-386">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="b0184-387">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-387">Network</span></span>
* <span data-ttu-id="b0184-388">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-388">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="b0184-389">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-389">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-390">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-390">Resource</span></span>
* <span data-ttu-id="b0184-391">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-391">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="b0184-392">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-392">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-393">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-393">Storage</span></span>
*  <span data-ttu-id="b0184-394">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-394">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-395">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-395">VM</span></span>
* <span data-ttu-id="b0184-396">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-396">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="b0184-397">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="b0184-397">December 4, 2018</span></span>

<span data-ttu-id="b0184-398">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="b0184-398">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="b0184-399">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-399">Core</span></span>
* <span data-ttu-id="b0184-400">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-400">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="b0184-401">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-401">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-402">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-402">Appservice</span></span>
* <span data-ttu-id="b0184-403">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-403">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="b0184-404">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-404">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="b0184-405">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-405">Network</span></span>
* <span data-ttu-id="b0184-406">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-406">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="b0184-407">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-407">Role</span></span>
* <span data-ttu-id="b0184-408">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-408">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="b0184-409">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-409">VM</span></span>
* <span data-ttu-id="b0184-410">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-410">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="b0184-411">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-411">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="b0184-412">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-412">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="b0184-413">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-413">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="b0184-414">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="b0184-414">November 20, 2018</span></span>

<span data-ttu-id="b0184-415">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="b0184-415">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="b0184-416">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-416">Core</span></span>
* <span data-ttu-id="b0184-417">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-417">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-418">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-418">ACR</span></span>
* <span data-ttu-id="b0184-419">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-419">Added context token to task step</span></span>
* <span data-ttu-id="b0184-420">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-420">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="b0184-421">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-421">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-422">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-422">Appservice</span></span>
* <span data-ttu-id="b0184-423">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-423">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="b0184-424">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-424">Updated the default `node_version`.</span></span> <span data-ttu-id="b0184-425">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="b0184-425">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="b0184-426">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-426">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="b0184-427">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-427">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="b0184-428">IotCentral</span><span class="sxs-lookup"><span data-stu-id="b0184-428">IotCentral</span></span>
* <span data-ttu-id="b0184-429">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-429">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0184-430">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0184-430">KeyVault</span></span>
* <span data-ttu-id="b0184-431">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-431">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="b0184-432">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-432">Network</span></span>
* <span data-ttu-id="b0184-433">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-433">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="b0184-434">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-434">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="b0184-435">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-435">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="b0184-436">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-436">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0184-437">Rdbms</span><span class="sxs-lookup"><span data-stu-id="b0184-437">Rdbms</span></span>
* <span data-ttu-id="b0184-438">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-438">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="b0184-439">Rbac</span><span class="sxs-lookup"><span data-stu-id="b0184-439">Rbac</span></span>
* <span data-ttu-id="b0184-440">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-440">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="b0184-441">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-441">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="b0184-442">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-442">Storage</span></span>
* <span data-ttu-id="b0184-443">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-443">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="b0184-444">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-444">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="b0184-445">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-445">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="b0184-446">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="b0184-446">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-447">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-447">VM</span></span>
* <span data-ttu-id="b0184-448">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-448">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="b0184-449">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-449">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="b0184-450">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="b0184-450">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="b0184-451">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-451">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="b0184-452">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-452">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="b0184-453">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-453">Added `snapshot wait` command</span></span>
* <span data-ttu-id="b0184-454">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-454">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="b0184-455">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="b0184-455">November 6, 2018</span></span>

<span data-ttu-id="b0184-456">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="b0184-456">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="b0184-457">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-457">Core</span></span>
* <span data-ttu-id="b0184-458">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-458">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-459">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-459">ACR</span></span>
* <span data-ttu-id="b0184-460">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-460">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="b0184-461">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-461">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-462">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-462">ACS</span></span>
* <span data-ttu-id="b0184-463">[破壊的変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-463">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="b0184-464">Advisor</span><span class="sxs-lookup"><span data-stu-id="b0184-464">Advisor</span></span>
* <span data-ttu-id="b0184-465">GA リリース</span><span class="sxs-lookup"><span data-stu-id="b0184-465">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="b0184-466">AMS</span><span class="sxs-lookup"><span data-stu-id="b0184-466">AMS</span></span>
* <span data-ttu-id="b0184-467">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-467">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="b0184-468">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-468">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="b0184-469">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-469">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="b0184-470">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-470">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="b0184-471">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-471">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="b0184-472">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-472">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="b0184-473">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-473">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="b0184-474">[破壊的変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="b0184-474">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="b0184-475">[破壊的変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-475">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="b0184-476">[破壊的変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-476">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="b0184-477">[破壊的変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="b0184-477">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="b0184-478">[破壊的変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="b0184-478">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="b0184-479">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="b0184-479">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="b0184-480">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="b0184-480">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="b0184-481">[破壊的変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-481">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="b0184-482">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b0184-482">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="b0184-483">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="b0184-483">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-484">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-484">AppService</span></span>
* <span data-ttu-id="b0184-485">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-485">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="b0184-486">構成</span><span class="sxs-lookup"><span data-stu-id="b0184-486">Configure</span></span>
* <span data-ttu-id="b0184-487">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-487">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="b0184-488">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-488">Container</span></span>
* <span data-ttu-id="b0184-489">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-489">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="b0184-490">EventHub</span><span class="sxs-lookup"><span data-stu-id="b0184-490">EventHub</span></span>
* <span data-ttu-id="b0184-491">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-491">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-492">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-492">Interactive</span></span>
* <span data-ttu-id="b0184-493">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="b0184-493">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-494">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-494">Monitor</span></span>
* <span data-ttu-id="b0184-495">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-495">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="b0184-496">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-496">Network</span></span>
* <span data-ttu-id="b0184-497">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-497">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="b0184-498">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-498">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="b0184-499">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-499">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="b0184-500">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-500">Profile</span></span>
* <span data-ttu-id="b0184-501">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-501">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0184-502">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0184-502">RDBMS</span></span>
* <span data-ttu-id="b0184-503">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-503">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-504">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-504">Resource</span></span>
* <span data-ttu-id="b0184-505">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-505">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="b0184-506">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-506">Role</span></span>
* <span data-ttu-id="b0184-507">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-507">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="b0184-508">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-508">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="b0184-509">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-509">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-510">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-510">Storage</span></span>
* <span data-ttu-id="b0184-511">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="b0184-511">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-512">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-512">VM</span></span>
* <span data-ttu-id="b0184-513">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-513">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="b0184-514">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-514">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="b0184-515">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-515">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="b0184-516">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-516">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="b0184-517">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="b0184-517">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="b0184-518">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-518">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="b0184-519">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="b0184-519">October 23, 2018</span></span>

<span data-ttu-id="b0184-520">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="b0184-520">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="b0184-521">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-521">Core</span></span>
* <span data-ttu-id="b0184-522">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-522">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="b0184-523">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-523">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-524">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-524">ACR</span></span>
* <span data-ttu-id="b0184-525">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-525">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="b0184-526">CDN</span><span class="sxs-lookup"><span data-stu-id="b0184-526">CDN</span></span>
* <span data-ttu-id="b0184-527">[破壊的変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="b0184-527">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="b0184-528">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-528">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="b0184-529">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-529">Container</span></span>
* <span data-ttu-id="b0184-530">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-530">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="b0184-531">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-531">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="b0184-532">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-532">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="b0184-533">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-533">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="b0184-534">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-534">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="b0184-535">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-535">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="b0184-536">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-536">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0184-537">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0184-537">CosmosDB</span></span>
* <span data-ttu-id="b0184-538">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-538">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-539">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-539">Interactive</span></span>
* <span data-ttu-id="b0184-540">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-540">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="b0184-541">IoT Central</span><span class="sxs-lookup"><span data-stu-id="b0184-541">IoT Central</span></span>
* <span data-ttu-id="b0184-542">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-542">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="b0184-543">[破壊的変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="b0184-543">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-544">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-544">Monitor</span></span>
* <span data-ttu-id="b0184-545">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="b0184-545">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="b0184-546">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-546">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="b0184-547">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-547">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="b0184-548">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-548">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="b0184-549">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-549">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="b0184-550">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-550">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="b0184-551">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="b0184-551">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="b0184-552">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-552">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="b0184-553">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-553">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="b0184-554">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-554">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="b0184-555">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-555">Network</span></span>
* <span data-ttu-id="b0184-556">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-556">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="b0184-557">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-557">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="b0184-558">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b0184-558">ServiceBus</span></span>
* <span data-ttu-id="b0184-559">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-559">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-560">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-560">SQL</span></span>
* <span data-ttu-id="b0184-561">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-561">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-562">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-562">Storage</span></span>
* <span data-ttu-id="b0184-563">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-563">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="b0184-564">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-564">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-565">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-565">VM</span></span>
* <span data-ttu-id="b0184-566">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="b0184-566">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="b0184-567">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-567">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="b0184-568">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-568">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="b0184-569">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="b0184-569">October 16, 2018</span></span>

<span data-ttu-id="b0184-570">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="b0184-570">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-571">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-571">VM</span></span>
* <span data-ttu-id="b0184-572">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-572">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="b0184-573">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="b0184-573">October 9, 2018</span></span>

<span data-ttu-id="b0184-574">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="b0184-574">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="b0184-575">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-575">Core</span></span>
* <span data-ttu-id="b0184-576">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-576">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-577">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-577">ACR</span></span>
* <span data-ttu-id="b0184-578">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-578">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-579">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-579">ACS</span></span>
* <span data-ttu-id="b0184-580">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="b0184-580">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="b0184-581">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-581">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="b0184-582">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-582">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="b0184-583">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-583">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="b0184-584">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-584">Container</span></span>
* <span data-ttu-id="b0184-585">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-585">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="b0184-586">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-586">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="b0184-587">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="b0184-587">Event Hub</span></span>
* <span data-ttu-id="b0184-588">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-588">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="b0184-589">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-589">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="b0184-590">Extensions</span><span class="sxs-lookup"><span data-stu-id="b0184-590">Extensions</span></span>
* <span data-ttu-id="b0184-591">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-591">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b0184-592">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b0184-592">HDInsight</span></span>
* <span data-ttu-id="b0184-593">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-593">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="b0184-594">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-594">IoT</span></span>
* <span data-ttu-id="b0184-595">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-595">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0184-596">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0184-596">KeyVault</span></span>
* <span data-ttu-id="b0184-597">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-597">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="b0184-598">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-598">Network</span></span>
* <span data-ttu-id="b0184-599">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="b0184-599">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="b0184-600">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="b0184-600">See #6052</span></span>
* <span data-ttu-id="b0184-601">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-601">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="b0184-602">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="b0184-602">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="b0184-603">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-603">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="b0184-604">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-604">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="b0184-605">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-605">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="b0184-606">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-606">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="b0184-607">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-607">Role</span></span>
* <span data-ttu-id="b0184-608">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-608">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="b0184-609">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-609">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="b0184-610">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-610">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="b0184-611">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-611">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="b0184-612">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b0184-612">Service Bus</span></span>
* <span data-ttu-id="b0184-613">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-613">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-614">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-614">VM</span></span>
* <span data-ttu-id="b0184-615">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-615">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="b0184-616">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-616">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="b0184-617">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-617">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="b0184-618">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-618">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="b0184-619">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-619">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="b0184-620">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-620">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="b0184-621">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="b0184-621">September 21, 2018</span></span>

<span data-ttu-id="b0184-622">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="b0184-622">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-623">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-623">ACR</span></span>
* <span data-ttu-id="b0184-624">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-624">Added ACR Task commands</span></span>
* <span data-ttu-id="b0184-625">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-625">Added quick run command</span></span>
* <span data-ttu-id="b0184-626">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-626">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="b0184-627">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-627">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="b0184-628">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-628">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="b0184-629">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-629">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-630">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-630">ACS</span></span>
* <span data-ttu-id="b0184-631">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-631">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="b0184-632">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-632">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-633">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-633">AppService</span></span>

* <span data-ttu-id="b0184-634">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-634">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="b0184-635">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-635">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="b0184-636">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-636">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="b0184-637">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-637">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-638">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-638">Batch</span></span>
* <span data-ttu-id="b0184-639">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-639">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="b0184-640">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-640">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="b0184-641">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-641">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="b0184-642">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-642">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b0184-643">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b0184-643">Batch AI</span></span> 
* <span data-ttu-id="b0184-644">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-644">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b0184-645">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b0184-645">Cognitive Services</span></span>
* <span data-ttu-id="b0184-646">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-646">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="b0184-647">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-647">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="b0184-648">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-648">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="b0184-649">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-649">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="b0184-650">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-650">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="b0184-651">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-651">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="b0184-652">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-652">Container</span></span>
* <span data-ttu-id="b0184-653">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-653">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="b0184-654">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-654">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="b0184-655">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-655">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="b0184-656">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-656">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="b0184-657">DataLake</span><span class="sxs-lookup"><span data-stu-id="b0184-657">Datalake</span></span>
* <span data-ttu-id="b0184-658">仮想ネットワーク ルール用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-658">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="b0184-659">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="b0184-659">Interactive Shell</span></span>
* <span data-ttu-id="b0184-660">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-660">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="b0184-661">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-661">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="b0184-662">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-662">IoT</span></span>
* <span data-ttu-id="b0184-663">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-663">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="b0184-664">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b0184-664">Key Vault</span></span>
* <span data-ttu-id="b0184-665">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-665">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="b0184-666">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-666">Network</span></span>
* <span data-ttu-id="b0184-667">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-667">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="b0184-668">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-668">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="b0184-669">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-669">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="b0184-670">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-670">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="b0184-671">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-671">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="b0184-672">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-672">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="b0184-673">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b0184-673">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="b0184-674">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-674">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="b0184-675">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-675">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="b0184-676">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-676">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="b0184-677">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-677">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="b0184-678">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-678">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="b0184-679">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-679">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="b0184-680">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="b0184-680">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="b0184-681">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-681">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="b0184-682">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-682">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="b0184-683">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-683">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="b0184-684">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-684">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0184-685">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0184-685">RDBMS</span></span>
* <span data-ttu-id="b0184-686">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-686">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="b0184-687">予約</span><span class="sxs-lookup"><span data-stu-id="b0184-687">Reservation</span></span>
* <span data-ttu-id="b0184-688">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-688">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="b0184-689">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-689">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="b0184-690">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="b0184-690">Manage App</span></span>
* <span data-ttu-id="b0184-691">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-691">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="b0184-692">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-692">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="b0184-693">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-693">Role</span></span>
* <span data-ttu-id="b0184-694">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-694">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="b0184-695">SignalR</span><span class="sxs-lookup"><span data-stu-id="b0184-695">SignalR</span></span>
* <span data-ttu-id="b0184-696">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-696">First release</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-697">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-697">Storage</span></span>
* <span data-ttu-id="b0184-698">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-698">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="b0184-699">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-699">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-700">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-700">VM</span></span>
* <span data-ttu-id="b0184-701">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="b0184-701">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="b0184-702">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-702">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="b0184-703">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b0184-703">August 28, 2018</span></span>

<span data-ttu-id="b0184-704">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="b0184-704">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="b0184-705">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-705">Core</span></span>

* <span data-ttu-id="b0184-706">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-706">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="b0184-707">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-707">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-708">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-708">ACR</span></span>

* <span data-ttu-id="b0184-709">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-709">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="b0184-710">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-710">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-711">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-711">ACS</span></span>

* <span data-ttu-id="b0184-712">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-712">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="b0184-713">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-713">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-714">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-714">AppService</span></span>

* <span data-ttu-id="b0184-715">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-715">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="b0184-716">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-716">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="b0184-717">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-717">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="b0184-718">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b0184-718">Backup</span></span>

* <span data-ttu-id="b0184-719">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-719">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="b0184-720">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="b0184-720">Bot Service</span></span>

* <span data-ttu-id="b0184-721">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="b0184-721">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b0184-722">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b0184-722">Cognitive Services</span></span>

* <span data-ttu-id="b0184-723">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-723">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="b0184-724">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-724">IoT</span></span>

* <span data-ttu-id="b0184-725">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-725">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-726">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-726">Monitor</span></span>

* <span data-ttu-id="b0184-727">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-727">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="b0184-728">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-728">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="b0184-729">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-729">Network</span></span>

* <span data-ttu-id="b0184-730">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-730">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-731">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-731">Resource</span></span>

* <span data-ttu-id="b0184-732">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-732">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-733">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-733">Storage</span></span>

* <span data-ttu-id="b0184-734">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-734">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-735">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-735">VM</span></span>

* <span data-ttu-id="b0184-736">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-736">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="b0184-737">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-737">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="b0184-738">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="b0184-738">Auguest 14, 2018</span></span>

<span data-ttu-id="b0184-739">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="b0184-739">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="b0184-740">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-740">Core</span></span>

* <span data-ttu-id="b0184-741">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-741">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="b0184-742">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-742">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="b0184-743">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="b0184-743">Telemetry</span></span>

* <span data-ttu-id="b0184-744">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-744">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-745">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-745">ACR</span></span>

* <span data-ttu-id="b0184-746">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-746">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="b0184-747">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-747">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-748">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-748">ACS</span></span>

* <span data-ttu-id="b0184-749">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-749">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="b0184-750">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-750">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="b0184-751">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-751">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="b0184-752">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-752">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="b0184-753">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-753">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="b0184-754">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-754">AppService</span></span>

* <span data-ttu-id="b0184-755">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-755">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="b0184-756">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-756">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="b0184-757">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b0184-757">BatchAI</span></span>

* <span data-ttu-id="b0184-758">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-758">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="b0184-759">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-759">Container</span></span>

* <span data-ttu-id="b0184-760">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-760">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="b0184-761">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-761">IoT</span></span>

* <span data-ttu-id="b0184-762">[破壊的変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-762">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="b0184-763">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-763">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="b0184-764">Iot Central</span><span class="sxs-lookup"><span data-stu-id="b0184-764">Iot Central</span></span>

* <span data-ttu-id="b0184-765">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-765">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0184-766">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0184-766">KeyVault</span></span>


* <span data-ttu-id="b0184-767">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-767">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="b0184-768">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-768">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="b0184-769">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-769">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="b0184-770">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-770">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="b0184-771">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-771">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="b0184-772">リレー</span><span class="sxs-lookup"><span data-stu-id="b0184-772">Relay</span></span>

* <span data-ttu-id="b0184-773">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-773">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-774">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-774">Sql</span></span>

* <span data-ttu-id="b0184-775">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-775">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-776">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-776">Storage</span></span>

* <span data-ttu-id="b0184-777">[破壊的変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="b0184-777">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="b0184-778">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-778">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="b0184-779">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="b0184-779">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="b0184-780">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-780">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="b0184-781">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-781">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-782">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-782">VM</span></span>

* <span data-ttu-id="b0184-783">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-783">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="b0184-784">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="b0184-784">July 31, 2018</span></span>

<span data-ttu-id="b0184-785">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="b0184-785">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-786">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-786">ACR</span></span>

* <span data-ttu-id="b0184-787">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-787">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="b0184-788">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-788">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-789">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-789">ACS</span></span>

* <span data-ttu-id="b0184-790">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-790">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-791">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-791">Batch</span></span>

* <span data-ttu-id="b0184-792">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-792">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="b0184-793">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-793">Container</span></span>

* <span data-ttu-id="b0184-794">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-794">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="b0184-795">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-795">Network</span></span>

* <span data-ttu-id="b0184-796">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-796">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="b0184-797">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-797">Resource</span></span>

* <span data-ttu-id="b0184-798">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-798">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="b0184-799">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-799">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="b0184-800">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-800">Role</span></span>

* <span data-ttu-id="b0184-801">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-801">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="b0184-802">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-802">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="b0184-803">Search</span><span class="sxs-lookup"><span data-stu-id="b0184-803">Search</span></span>

* <span data-ttu-id="b0184-804">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-804">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="b0184-805">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b0184-805">Service Bus</span></span>

* <span data-ttu-id="b0184-806">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-806">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="b0184-807">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-807">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="b0184-808">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="b0184-808">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="b0184-809">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="b0184-809">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-810">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-810">Storage</span></span>

* <span data-ttu-id="b0184-811">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-811">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="b0184-812">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="b0184-812">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-813">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-813">VM</span></span>

* <span data-ttu-id="b0184-814">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-814">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="b0184-815">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-815">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="b0184-816">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-816">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="b0184-817">[破壊的変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-817">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="b0184-818">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="b0184-818">July 18, 2018</span></span>

<span data-ttu-id="b0184-819">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="b0184-819">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="b0184-820">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-820">Core</span></span>

* <span data-ttu-id="b0184-821">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-821">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="b0184-822">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-822">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="b0184-823">[破壊的変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-823">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-824">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-824">ACR</span></span>

* <span data-ttu-id="b0184-825">[破壊的変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-825">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="b0184-826">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-826">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="b0184-827">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-827">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="b0184-828">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-828">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-829">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-829">ACS</span></span>

* <span data-ttu-id="b0184-830">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-830">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-831">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-831">AppService</span></span>

* <span data-ttu-id="b0184-832">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-832">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-833">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-833">Batch</span></span>

* <span data-ttu-id="b0184-834">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-834">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="b0184-835">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-835">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b0184-836">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b0184-836">Batch AI</span></span>

* <span data-ttu-id="b0184-837">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-837">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="b0184-838">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-838">Container</span></span>

* <span data-ttu-id="b0184-839">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-839">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="b0184-840">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-840">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="b0184-841">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-841">Network</span></span>

* <span data-ttu-id="b0184-842">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-842">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="b0184-843">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-843">Added `network nic wait`</span></span>
* <span data-ttu-id="b0184-844">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-844">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="b0184-845">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-845">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="b0184-846">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-846">Resource</span></span>

* <span data-ttu-id="b0184-847">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-847">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="b0184-848">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-848">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="b0184-849">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-849">Added `deployment wait` command</span></span>
* <span data-ttu-id="b0184-850">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-850">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-851">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-851">SQL</span></span>

* <span data-ttu-id="b0184-852">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-852">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="b0184-853">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-853">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="b0184-854">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="b0184-854">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-855">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-855">Storage</span></span>

* <span data-ttu-id="b0184-856">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-856">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-857">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-857">VM</span></span>

* <span data-ttu-id="b0184-858">[破壊的変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-858">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="b0184-859">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-859">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="b0184-860">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-860">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="b0184-861">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b0184-861">July 3, 2018</span></span>

<span data-ttu-id="b0184-862">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="b0184-862">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="b0184-863">AKS</span><span class="sxs-lookup"><span data-stu-id="b0184-863">AKS</span></span>

* <span data-ttu-id="b0184-864">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-864">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="b0184-865">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b0184-865">July 3, 2018</span></span>

<span data-ttu-id="b0184-866">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="b0184-866">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="b0184-867">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-867">Core</span></span>

* <span data-ttu-id="b0184-868">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-868">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-869">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-869">ACR</span></span>

* <span data-ttu-id="b0184-870">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-870">Added polling build status</span></span>
* <span data-ttu-id="b0184-871">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-871">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="b0184-872">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-872">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-873">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-873">ACS</span></span>

* <span data-ttu-id="b0184-874">[破壊的変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-874">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="b0184-875">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-875">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="b0184-876">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-876">Updated options for `aks browse` command.</span></span> <span data-ttu-id="b0184-877">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-877">Added `--listen-port` support</span></span>
* <span data-ttu-id="b0184-878">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-878">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="b0184-879">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="b0184-879">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="b0184-880">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-880">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-881">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-881">AppService</span></span>

* <span data-ttu-id="b0184-882">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-882">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="b0184-883">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-883">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="b0184-884">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b0184-884">Backup</span></span>

* <span data-ttu-id="b0184-885">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-885">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="b0184-886">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b0184-886">BatchAI</span></span>

* <span data-ttu-id="b0184-887">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-887">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="b0184-888">クラウド</span><span class="sxs-lookup"><span data-stu-id="b0184-888">Cloud</span></span>

* <span data-ttu-id="b0184-889">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-889">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="b0184-890">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-890">Container</span></span>

* <span data-ttu-id="b0184-891">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-891">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="b0184-892">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-892">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="b0184-893">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-893">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="b0184-894">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0184-894">Extension</span></span>

* <span data-ttu-id="b0184-895">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-895">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="b0184-896">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-896">Network</span></span>

* <span data-ttu-id="b0184-897">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-897">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0184-898">Rdbms</span><span class="sxs-lookup"><span data-stu-id="b0184-898">Rdbms</span></span>

* <span data-ttu-id="b0184-899">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-899">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-900">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-900">Resource</span></span>

* <span data-ttu-id="b0184-901">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-901">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-902">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-902">VM</span></span>

* <span data-ttu-id="b0184-903">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-903">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="b0184-904">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="b0184-904">June 25, 2018</span></span>

<span data-ttu-id="b0184-905">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="b0184-905">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="b0184-906">CLI</span><span class="sxs-lookup"><span data-stu-id="b0184-906">CLI</span></span>

* <span data-ttu-id="b0184-907">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-907">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="b0184-908">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="b0184-908">June 19, 2018</span></span>

<span data-ttu-id="b0184-909">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="b0184-909">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="b0184-910">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-910">Core</span></span>

* <span data-ttu-id="b0184-911">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-911">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-912">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-912">ACR</span></span>

* <span data-ttu-id="b0184-913">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-913">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="b0184-914">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-914">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-915">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-915">ACS</span></span>

* <span data-ttu-id="b0184-916">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-916">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="b0184-917">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-917">Added `--update` support</span></span>
* <span data-ttu-id="b0184-918">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-918">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="b0184-919">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="b0184-919">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="b0184-920">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-920">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="b0184-921">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-921">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="b0184-922">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-922">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="b0184-923">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-923">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-924">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-924">AppService</span></span>

* <span data-ttu-id="b0184-925">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-925">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="b0184-926">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-926">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-927">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-927">Batch</span></span>

* <span data-ttu-id="b0184-928">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-928">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b0184-929">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b0184-929">Batch AI</span></span>

* <span data-ttu-id="b0184-930">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-930">Added support for workspaces.</span></span> <span data-ttu-id="b0184-931">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="b0184-931">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="b0184-932">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-932">Added support for experiments.</span></span> <span data-ttu-id="b0184-933">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="b0184-933">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="b0184-934">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-934">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="b0184-935">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-935">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="b0184-936">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="b0184-936">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="b0184-937">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-937">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="b0184-938">[破壊的変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="b0184-938">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="b0184-939">[破壊的変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="b0184-939">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="b0184-940">[破壊的変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-940">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="b0184-941">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="b0184-941">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="b0184-942">[破壊的変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-942">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="b0184-943">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="b0184-943">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="b0184-944">[破壊的変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-944">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="b0184-945">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="b0184-945">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="b0184-946">[破壊的変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-946">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="b0184-947">[破壊的変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-947">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="b0184-948">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-948">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="b0184-949">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-949">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="b0184-950">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-950">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="b0184-951">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-951">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="b0184-952">マップ</span><span class="sxs-lookup"><span data-stu-id="b0184-952">Maps</span></span>

* <span data-ttu-id="b0184-953">[破壊的変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-953">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="b0184-954">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-954">Network</span></span>

* <span data-ttu-id="b0184-955">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="b0184-955">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="b0184-956">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-956">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="b0184-957">#6502</span><span class="sxs-lookup"><span data-stu-id="b0184-957">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="b0184-958">Reservations</span><span class="sxs-lookup"><span data-stu-id="b0184-958">Reservations</span></span>

* <span data-ttu-id="b0184-959">[破壊的変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-959">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="b0184-960">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-960">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="b0184-961">[破壊的変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-961">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="b0184-962">[破壊的変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-962">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="b0184-963">[破壊的変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-963">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="b0184-964">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-964">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="b0184-965">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-965">Role</span></span>

* <span data-ttu-id="b0184-966">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-966">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-967">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-967">SQL</span></span>

* <span data-ttu-id="b0184-968">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-968">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-969">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-969">Storage</span></span>

* <span data-ttu-id="b0184-970">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="b0184-970">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-971">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-971">VM</span></span>

* <span data-ttu-id="b0184-972">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-972">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="b0184-973">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-973">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="b0184-974">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-974">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="b0184-975">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b0184-975">June 13, 2018</span></span>

<span data-ttu-id="b0184-976">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="b0184-976">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="b0184-977">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-977">Core</span></span>

* <span data-ttu-id="b0184-978">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-978">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="b0184-979">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b0184-979">June 13, 2018</span></span>

<span data-ttu-id="b0184-980">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="b0184-980">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="b0184-981">AKS</span><span class="sxs-lookup"><span data-stu-id="b0184-981">AKS</span></span>

* <span data-ttu-id="b0184-982">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-982">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="b0184-983">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-983">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="b0184-984">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-984">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="b0184-985">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-985">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="b0184-986">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-986">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-987">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-987">AppService</span></span>

* <span data-ttu-id="b0184-988">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-988">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="b0184-989">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b0184-989">June 5, 2018</span></span>

<span data-ttu-id="b0184-990">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="b0184-990">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-991">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-991">Interactive</span></span>

* <span data-ttu-id="b0184-992">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-992">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="b0184-993">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b0184-993">June 5, 2018</span></span>

<span data-ttu-id="b0184-994">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="b0184-994">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="b0184-995">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-995">Core</span></span>

* <span data-ttu-id="b0184-996">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-996">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="b0184-997">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-997">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-998">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-998">ACR</span></span>

* <span data-ttu-id="b0184-999">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-999">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="b0184-1000">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1000">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="b0184-1001">AKS</span><span class="sxs-lookup"><span data-stu-id="b0184-1001">AKS</span></span>

* <span data-ttu-id="b0184-1002">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1002">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-1003">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-1003">Batch</span></span>

* <span data-ttu-id="b0184-1004">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1004">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="b0184-1005">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-1005">IOT</span></span>

* <span data-ttu-id="b0184-1006">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1006">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1007">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1007">Network</span></span>

* <span data-ttu-id="b0184-1008">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1008">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="b0184-1009">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="b0184-1009">Policy Insights</span></span>

* <span data-ttu-id="b0184-1010">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-1010">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="b0184-1011">ARM</span><span class="sxs-lookup"><span data-stu-id="b0184-1011">ARM</span></span>

* <span data-ttu-id="b0184-1012">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1012">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-1013">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-1013">SQL</span></span>

* <span data-ttu-id="b0184-1014">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1014">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="b0184-1015">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1015">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="b0184-1016">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1016">Storage</span></span>

* <span data-ttu-id="b0184-1017">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1017">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1018">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1018">VM</span></span>

* <span data-ttu-id="b0184-1019">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1019">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="b0184-1020">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1020">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="b0184-1021">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1021">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="b0184-1022">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1022">May 22, 2018</span></span>

<span data-ttu-id="b0184-1023">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="b0184-1023">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="b0184-1024">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1024">Core</span></span>

* <span data-ttu-id="b0184-1025">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1025">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1026">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1026">ACS</span></span>

* <span data-ttu-id="b0184-1027">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1027">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="b0184-1028">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1028">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1029">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-1029">AppService</span></span>

* <span data-ttu-id="b0184-1030">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1030">Improved generic update commands</span></span>
* <span data-ttu-id="b0184-1031">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1031">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="b0184-1032">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-1032">Container</span></span>

* <span data-ttu-id="b0184-1033">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1033">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="b0184-1034">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1034">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="b0184-1035">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0184-1035">Extension</span></span>

* <span data-ttu-id="b0184-1036">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1036">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-1037">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-1037">Interactive</span></span>

* <span data-ttu-id="b0184-1038">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1038">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="b0184-1039">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1039">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0184-1040">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0184-1040">KeyVault</span></span>

* <span data-ttu-id="b0184-1041">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1041">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1042">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1042">Network</span></span>

* <span data-ttu-id="b0184-1043">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1043">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="b0184-1044">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1044">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-1045">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-1045">SQL</span></span>

* <span data-ttu-id="b0184-1046">[破壊的変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1046">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="b0184-1047">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1047">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="b0184-1048">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1048">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="b0184-1049">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1049">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="b0184-1050">[破壊的変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1050">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="b0184-1051">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="b0184-1051">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="b0184-1052">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b0184-1052">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="b0184-1053">`edition`</span><span class="sxs-lookup"><span data-stu-id="b0184-1053">`edition`.</span></span> <span data-ttu-id="b0184-1054">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b0184-1054">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="b0184-1055">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="b0184-1055">`elasticPoolName`.</span></span> <span data-ttu-id="b0184-1056">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b0184-1056">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="b0184-1057">[破壊的変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1057">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="b0184-1058">`edition`</span><span class="sxs-lookup"><span data-stu-id="b0184-1058">`edition`.</span></span> <span data-ttu-id="b0184-1059">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b0184-1059">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="b0184-1060">`dtu`</span><span class="sxs-lookup"><span data-stu-id="b0184-1060">`dtu`.</span></span> <span data-ttu-id="b0184-1061">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b0184-1061">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="b0184-1062">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="b0184-1062">`databaseDtuMin`.</span></span> <span data-ttu-id="b0184-1063">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b0184-1063">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="b0184-1064">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="b0184-1064">`databaseDtuMax`.</span></span> <span data-ttu-id="b0184-1065">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b0184-1065">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="b0184-1066">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1066">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="b0184-1067">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1067">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1068">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1068">Storage</span></span>

* <span data-ttu-id="b0184-1069">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1069">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="b0184-1070">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1070">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1071">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1071">VM</span></span>

* <span data-ttu-id="b0184-1072">[破壊的変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1072">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="b0184-1073">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="b0184-1073">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="b0184-1074">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1074">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="b0184-1075">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1075">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="b0184-1076">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1076">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="b0184-1077">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1077">May 7, 2018</span></span>

<span data-ttu-id="b0184-1078">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="b0184-1078">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="b0184-1079">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1079">Core</span></span>

* <span data-ttu-id="b0184-1080">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1080">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="b0184-1081">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1081">Added limited support for positional arguments</span></span>
* <span data-ttu-id="b0184-1082">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1082">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="b0184-1083">#5591</span><span class="sxs-lookup"><span data-stu-id="b0184-1083">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="b0184-1084">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1084">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="b0184-1085">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="b0184-1085">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="b0184-1086">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1086">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="b0184-1087">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1087">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="b0184-1088">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1088">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-1089">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-1089">ACR</span></span>

* <span data-ttu-id="b0184-1090">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1090">Added ACR Build commands</span></span>
* <span data-ttu-id="b0184-1091">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1091">Improved resource not found error messages</span></span>
* <span data-ttu-id="b0184-1092">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1092">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="b0184-1093">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1093">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="b0184-1094">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1094">Improved repository commands error messages</span></span>
* <span data-ttu-id="b0184-1095">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1095">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1096">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1096">ACS</span></span>

* <span data-ttu-id="b0184-1097">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1097">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="b0184-1098">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1098">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="b0184-1099">AMS</span><span class="sxs-lookup"><span data-stu-id="b0184-1099">AMS</span></span>

* <span data-ttu-id="b0184-1100">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="b0184-1100">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1101">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1101">Appservice</span></span>

* <span data-ttu-id="b0184-1102">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1102">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="b0184-1103">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1103">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="b0184-1104">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1104">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="b0184-1105">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1105">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b0184-1106">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b0184-1106">Batch AI</span></span>

* <span data-ttu-id="b0184-1107">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1107">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b0184-1108">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b0184-1108">Cognitive Services</span></span>

* <span data-ttu-id="b0184-1109">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1109">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="b0184-1110">消費</span><span class="sxs-lookup"><span data-stu-id="b0184-1110">Consumption</span></span>

* <span data-ttu-id="b0184-1111">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1111">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="b0184-1112">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-1112">Container</span></span>

* <span data-ttu-id="b0184-1113">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1113">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="b0184-1114">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0184-1114">Cosmos DB</span></span>

* <span data-ttu-id="b0184-1115">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1115">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="b0184-1116">DMS</span><span class="sxs-lookup"><span data-stu-id="b0184-1116">DMS</span></span>

* <span data-ttu-id="b0184-1117">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1117">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="b0184-1118">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0184-1118">Extension</span></span>

* <span data-ttu-id="b0184-1119">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1119">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-1120">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-1120">Interactive</span></span>

* <span data-ttu-id="b0184-1121">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1121">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="b0184-1122">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1122">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="b0184-1123">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1123">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="b0184-1124">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1124">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="b0184-1125">ラボ</span><span class="sxs-lookup"><span data-stu-id="b0184-1125">Lab</span></span>

* <span data-ttu-id="b0184-1126">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1126">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1127">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1127">Network</span></span>

* <span data-ttu-id="b0184-1128">[破壊的変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1128">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="b0184-1129">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-1129">Profile</span></span>

* <span data-ttu-id="b0184-1130">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1130">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="b0184-1131">[破壊的変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1131">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="b0184-1132">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1132">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="b0184-1133">Redis</span><span class="sxs-lookup"><span data-stu-id="b0184-1133">Redis</span></span>

* <span data-ttu-id="b0184-1134">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1134">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="b0184-1135">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1135">Deprecated `redis list-all`.</span></span> <span data-ttu-id="b0184-1136">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="b0184-1136">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="b0184-1137">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1137">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="b0184-1138">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1138">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="b0184-1139">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-1139">Role</span></span>

* <span data-ttu-id="b0184-1140">[破壊的変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1140">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1141">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1141">Storage</span></span>

* <span data-ttu-id="b0184-1142">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="b0184-1142">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="b0184-1143">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1143">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="b0184-1144">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="b0184-1144">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="b0184-1145">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="b0184-1145">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="b0184-1146">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1146">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1147">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1147">VM</span></span>

* <span data-ttu-id="b0184-1148">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1148">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="b0184-1149">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1149">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="b0184-1150">[破壊的変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="b0184-1150">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="b0184-1151">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1151">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="b0184-1152">[破壊的変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1152">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="b0184-1153">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1153">Added write accelerator support</span></span>
* <span data-ttu-id="b0184-1154">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1154">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="b0184-1155">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1155">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="b0184-1156">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1156">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="b0184-1157">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1157">April 10, 2018</span></span>

<span data-ttu-id="b0184-1158">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="b0184-1158">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-1159">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-1159">ACR</span></span>

* <span data-ttu-id="b0184-1160">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1160">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1161">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1161">ACS</span></span>

* <span data-ttu-id="b0184-1162">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1162">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1163">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1163">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="b0184-1165">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1165">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="b0184-1166">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b0184-1166">BatchAI</span></span>

* <span data-ttu-id="b0184-1167">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1167">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="b0184-1168">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="b0184-1168">Job level mounting</span></span>
  - <span data-ttu-id="b0184-1169">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="b0184-1169">Environment variables with secret values</span></span>
  - <span data-ttu-id="b0184-1170">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="b0184-1170">Performance counters settings</span></span>
  - <span data-ttu-id="b0184-1171">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="b0184-1171">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="b0184-1172">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="b0184-1172">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="b0184-1173">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="b0184-1173">Usage and limits reporting</span></span>
  - <span data-ttu-id="b0184-1174">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="b0184-1174">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="b0184-1175">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="b0184-1175">Support for custom images</span></span>
  - <span data-ttu-id="b0184-1176">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1176">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="b0184-1177">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-1177">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="b0184-1178">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="b0184-1178">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="b0184-1179">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="b0184-1179">National clouds are supported</span></span>
* <span data-ttu-id="b0184-1180">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1180">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="b0184-1181">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1181">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="b0184-1182">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1182">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="b0184-1183">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1183">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="b0184-1184">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="b0184-1184">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="b0184-1185">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="b0184-1185">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="b0184-1186">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1186">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="b0184-1187">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1187">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="b0184-1188">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="b0184-1188">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="b0184-1189">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1189">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="b0184-1190">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1190">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="b0184-1191">[破壊的変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1191">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="b0184-1192">[破壊的変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1192">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="b0184-1193">課金</span><span class="sxs-lookup"><span data-stu-id="b0184-1193">Billing</span></span>

* <span data-ttu-id="b0184-1194">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1194">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="b0184-1195">消費</span><span class="sxs-lookup"><span data-stu-id="b0184-1195">Consumption</span></span>

* <span data-ttu-id="b0184-1196">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1196">Added `marketplace` commands</span></span>
* <span data-ttu-id="b0184-1197">[破壊的変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1197">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="b0184-1198">[破壊的変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1198">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="b0184-1199">[破壊的変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1199">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="b0184-1200">[破壊的変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1200">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="b0184-1201">[破壊的変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1201">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="b0184-1202">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-1202">Container</span></span>

* <span data-ttu-id="b0184-1203">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1203">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="b0184-1204">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1204">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="b0184-1205">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0184-1205">Extension</span></span>

* <span data-ttu-id="b0184-1206">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1206">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-1207">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-1207">Interactive</span></span>

* <span data-ttu-id="b0184-1208">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1208">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="b0184-1209">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1209">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="b0184-1210">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1210">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1211">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1211">Network</span></span>

* <span data-ttu-id="b0184-1212">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1212">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="b0184-1213">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1213">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="b0184-1214">#4910</span><span class="sxs-lookup"><span data-stu-id="b0184-1214">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="b0184-1215">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1215">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="b0184-1216">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="b0184-1216">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="b0184-1217">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1217">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="b0184-1218">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1218">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="b0184-1219">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1219">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="b0184-1220">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-1220">Profile</span></span>

* <span data-ttu-id="b0184-1221">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1221">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="b0184-1222">[破壊的変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1222">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0184-1223">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0184-1223">RDBMS</span></span>

* <span data-ttu-id="b0184-1224">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1224">Added `georestore` command</span></span>
* <span data-ttu-id="b0184-1225">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1225">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1226">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1226">Resource</span></span>

* <span data-ttu-id="b0184-1227">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1227">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="b0184-1228">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1228">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-1229">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-1229">SQL</span></span>

* <span data-ttu-id="b0184-1230">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1230">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1231">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1231">Storage</span></span>

* <span data-ttu-id="b0184-1232">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1232">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1233">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1233">VM</span></span>

* <span data-ttu-id="b0184-1234">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1234">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="b0184-1235">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1235">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="b0184-1237">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1237">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="b0184-1238">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1238">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="b0184-1239">#5718</span><span class="sxs-lookup"><span data-stu-id="b0184-1239">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="b0184-1240">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1240">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="b0184-1241">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1241">March 27, 2018</span></span>

<span data-ttu-id="b0184-1242">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="b0184-1242">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="b0184-1243">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1243">Core</span></span>

* <span data-ttu-id="b0184-1244">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="b0184-1244">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1245">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1245">ACS</span></span>

* <span data-ttu-id="b0184-1246">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1246">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1247">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1247">Appservice</span></span>

* <span data-ttu-id="b0184-1248">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1248">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="b0184-1249">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1249">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="b0184-1250">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b0184-1250">Backup</span></span>

* <span data-ttu-id="b0184-1251">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1251">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="b0184-1252">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="b0184-1252">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="b0184-1253">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1253">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="b0184-1254">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1254">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="b0184-1255">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-1255">Container</span></span>

* <span data-ttu-id="b0184-1256">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1256">Added `container exec` command.</span></span> <span data-ttu-id="b0184-1257">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="b0184-1257">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="b0184-1258">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="b0184-1258">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="b0184-1259">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0184-1259">Extension</span></span>

* <span data-ttu-id="b0184-1260">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1260">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="b0184-1261">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1261">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="b0184-1262">[破壊的変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1262">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-1263">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-1263">Interactive</span></span>

* <span data-ttu-id="b0184-1264">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1264">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="b0184-1265">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1265">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="b0184-1266">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="b0184-1266">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="b0184-1267">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1267">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="b0184-1268">ラボ</span><span class="sxs-lookup"><span data-stu-id="b0184-1268">Lab</span></span>

* <span data-ttu-id="b0184-1269">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1269">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-1270">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-1270">Monitor</span></span>

* <span data-ttu-id="b0184-1271">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="b0184-1271">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="b0184-1272">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="b0184-1272">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="b0184-1273">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="b0184-1273">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1274">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1274">Network</span></span>

* <span data-ttu-id="b0184-1275">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1275">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="b0184-1276">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-1276">Profile</span></span>

* <span data-ttu-id="b0184-1277">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1277">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0184-1278">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0184-1278">RDBMS</span></span>

* <span data-ttu-id="b0184-1279">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1279">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1280">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1280">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="b0184-1282">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-1282">Role</span></span>

* <span data-ttu-id="b0184-1283">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1283">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="b0184-1284">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1284">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="b0184-1285">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1285">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="b0184-1286">[破壊的変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1286">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="b0184-1287">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1287">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1288">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1288">Storage</span></span>

* <span data-ttu-id="b0184-1289">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1289">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="b0184-1290">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="b0184-1290">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1291">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1291">VM</span></span>

* <span data-ttu-id="b0184-1292">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1292">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="b0184-1293">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1293">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="b0184-1294">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1294">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="b0184-1295">[破壊的変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1295">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="b0184-1296">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1296">March 13, 2018</span></span>

<span data-ttu-id="b0184-1297">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="b0184-1297">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-1298">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-1298">ACR</span></span>

* <span data-ttu-id="b0184-1299">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1299">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="b0184-1300">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1300">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="b0184-1301">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1301">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1302">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1302">ACS</span></span>

* <span data-ttu-id="b0184-1303">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1303">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="b0184-1304">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1304">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="b0184-1305">Advisor</span><span class="sxs-lookup"><span data-stu-id="b0184-1305">Advisor</span></span>

* <span data-ttu-id="b0184-1306">[破壊的変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1306">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="b0184-1307">[破壊的変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1307">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="b0184-1308">[破壊的変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1308">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="b0184-1309">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1309">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="b0184-1310">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1310">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1311">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1311">Appservice</span></span>

* <span data-ttu-id="b0184-1312">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1312">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="b0184-1313">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1313">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="b0184-1314">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="b0184-1314">Eventhubs</span></span>

* <span data-ttu-id="b0184-1315">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-1315">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="b0184-1316">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0184-1316">Extension</span></span>

* <span data-ttu-id="b0184-1317">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1317">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-1318">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-1318">Interactive</span></span>

* <span data-ttu-id="b0184-1319">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="b0184-1319">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="b0184-1320">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="b0184-1320">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="b0184-1321">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="b0184-1321">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="b0184-1322">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1322">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-1323">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-1323">Monitor</span></span>

* <span data-ttu-id="b0184-1324">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1324">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="b0184-1325">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1325">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="b0184-1326">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1326">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="b0184-1327">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1327">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1328">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1328">Network</span></span>

* <span data-ttu-id="b0184-1329">[破壊的変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1329">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="b0184-1330">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1330">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="b0184-1331">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1331">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="b0184-1332">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1332">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="b0184-1333">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-1333">Profile</span></span>

* <span data-ttu-id="b0184-1334">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1334">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="b0184-1335">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1335">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0184-1336">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0184-1336">RDBMS</span></span>

* <span data-ttu-id="b0184-1337">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1337">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="b0184-1338">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b0184-1338">Service Bus</span></span>

* <span data-ttu-id="b0184-1339">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-1339">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1340">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1340">Storage</span></span>

* <span data-ttu-id="b0184-1341">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1341">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="b0184-1342">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1342">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1343">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1343">VM</span></span>

* <span data-ttu-id="b0184-1344">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1344">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="b0184-1345">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1345">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="b0184-1346">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1346">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="b0184-1347">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1347">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="b0184-1348">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1348">February 27, 2018</span></span>

<span data-ttu-id="b0184-1349">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="b0184-1349">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="b0184-1350">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1350">Core</span></span>

* <span data-ttu-id="b0184-1351">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="b0184-1351">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="b0184-1352">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1352">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="b0184-1353">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1353">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1354">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1354">ACS</span></span>

* <span data-ttu-id="b0184-1355">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1355">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="b0184-1356">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="b0184-1356">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="b0184-1357">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1357">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="b0184-1358">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1358">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1359">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1359">Appservice</span></span>

* <span data-ttu-id="b0184-1360">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="b0184-1360">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="b0184-1361">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="b0184-1361">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b0184-1362">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b0184-1362">Cognitive Services</span></span>

* <span data-ttu-id="b0184-1363">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1363">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="b0184-1364">消費</span><span class="sxs-lookup"><span data-stu-id="b0184-1364">Consumption</span></span>

* <span data-ttu-id="b0184-1365">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1365">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="b0184-1366">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1366">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="b0184-1367">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-1367">Container</span></span>

* <span data-ttu-id="b0184-1368">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1368">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1369">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1369">Network</span></span>

* <span data-ttu-id="b0184-1370">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="b0184-1370">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1371">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1371">Resource</span></span>

* <span data-ttu-id="b0184-1372">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1372">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="b0184-1373">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-1373">Role</span></span>

* <span data-ttu-id="b0184-1374">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1374">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-1375">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-1375">SQL</span></span>

* <span data-ttu-id="b0184-1376">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1376">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1377">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1377">Storage</span></span>

* <span data-ttu-id="b0184-1378">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1378">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1379">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1379">VM</span></span>

* <span data-ttu-id="b0184-1380">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1380">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="b0184-1381">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1381">February 13, 2018</span></span>

<span data-ttu-id="b0184-1382">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="b0184-1382">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="b0184-1383">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1383">Core</span></span>

* <span data-ttu-id="b0184-1384">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1384">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1385">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1385">ACS</span></span>

* <span data-ttu-id="b0184-1386">[破壊的変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1386">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="b0184-1387">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1387">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="b0184-1388">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1388">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="b0184-1389">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1389">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="b0184-1390">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1390">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="b0184-1391">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1391">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="b0184-1392">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1392">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="b0184-1393">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="b0184-1393">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1394">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1394">Appservice</span></span>

* <span data-ttu-id="b0184-1395">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1395">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="b0184-1396">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1396">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="b0184-1397">CDN</span><span class="sxs-lookup"><span data-stu-id="b0184-1397">CDN</span></span>

* <span data-ttu-id="b0184-1398">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1398">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="b0184-1399">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-1399">Container</span></span>

* <span data-ttu-id="b0184-1400">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1400">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="b0184-1401">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1401">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0184-1402">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0184-1402">CosmosDB</span></span>

* <span data-ttu-id="b0184-1403">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1403">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="b0184-1404">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0184-1404">Extension</span></span>

* <span data-ttu-id="b0184-1405">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1405">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="b0184-1406">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1406">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="b0184-1407">フィードバック</span><span class="sxs-lookup"><span data-stu-id="b0184-1407">Feedback</span></span>

* <span data-ttu-id="b0184-1408">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1408">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-1409">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-1409">Interactive</span></span>

* <span data-ttu-id="b0184-1410">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1410">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="b0184-1411">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1411">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="b0184-1412">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-1412">IoT</span></span>

* <span data-ttu-id="b0184-1413">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1413">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="b0184-1414">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1414">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="b0184-1415">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1415">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="b0184-1416">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1416">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-1417">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-1417">Monitor</span></span>

* <span data-ttu-id="b0184-1418">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1418">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1419">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1419">Network</span></span>

* <span data-ttu-id="b0184-1420">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1420">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="b0184-1421">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-1421">Profile</span></span>

* <span data-ttu-id="b0184-1422">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1422">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1423">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1423">Resource</span></span>

* <span data-ttu-id="b0184-1424">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1424">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="b0184-1425">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-1425">Role</span></span>

* <span data-ttu-id="b0184-1426">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1426">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-1427">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-1427">SQL</span></span>

* <span data-ttu-id="b0184-1428">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1428">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="b0184-1429">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1429">Added `sql db rename`</span></span>
* <span data-ttu-id="b0184-1430">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1430">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1431">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1431">Storage</span></span>

* <span data-ttu-id="b0184-1432">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1432">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1433">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1433">VM</span></span>

* <span data-ttu-id="b0184-1434">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1434">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="b0184-1435">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1435">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="b0184-1436">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="b0184-1436">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="b0184-1437">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1437">January 31, 2018</span></span>

<span data-ttu-id="b0184-1438">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="b0184-1438">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="b0184-1439">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1439">Core</span></span>

* <span data-ttu-id="b0184-1440">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1440">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="b0184-1441">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1441">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="b0184-1442">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1442">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="b0184-1443">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="b0184-1443">Use `--verbose` to see</span></span>
* <span data-ttu-id="b0184-1444">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="b0184-1444">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1445">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1445">ACS</span></span>

* <span data-ttu-id="b0184-1446">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1446">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="b0184-1447">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1447">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1448">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1448">Appservice</span></span>

* <span data-ttu-id="b0184-1449">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="b0184-1449">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="b0184-1450">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1450">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="b0184-1451">CDN</span><span class="sxs-lookup"><span data-stu-id="b0184-1451">CDN</span></span>

* <span data-ttu-id="b0184-1452">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1452">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0184-1453">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0184-1453">CosmosDB</span></span>

* <span data-ttu-id="b0184-1454">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1454">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-1455">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-1455">Interactive</span></span>

* <span data-ttu-id="b0184-1456">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1456">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1457">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1457">Network</span></span>

* <span data-ttu-id="b0184-1458">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1458">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="b0184-1459">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1459">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="b0184-1460">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1460">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="b0184-1461">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1461">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="b0184-1462">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1462">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="b0184-1463">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1463">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="b0184-1464">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1464">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="b0184-1465">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1465">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="b0184-1466">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1466">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="b0184-1467">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1467">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="b0184-1468">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-1468">Profile</span></span>

* <span data-ttu-id="b0184-1469">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1469">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1470">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1470">Resource</span></span>

* <span data-ttu-id="b0184-1471">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1471">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1472">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1472">Storage</span></span>

* <span data-ttu-id="b0184-1473">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1473">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="b0184-1474">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1474">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="b0184-1475">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1475">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="b0184-1476">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1476">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="b0184-1477">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1477">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1478">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1478">VM</span></span>

* <span data-ttu-id="b0184-1479">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1479">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="b0184-1480">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1480">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="b0184-1481">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1481">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="b0184-1482">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1482">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="b0184-1483">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1483">January 17, 2018</span></span>

<span data-ttu-id="b0184-1484">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="b0184-1484">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-1485">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-1485">ACR</span></span>

* <span data-ttu-id="b0184-1486">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1486">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="b0184-1487">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1487">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1488">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1488">ACS</span></span>

* <span data-ttu-id="b0184-1489">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1489">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="b0184-1490">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1490">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1491">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1491">Appservice</span></span>

* <span data-ttu-id="b0184-1492">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1492">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="b0184-1493">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1493">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="b0184-1494">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1494">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="b0184-1495">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b0184-1495">Backup</span></span>

* <span data-ttu-id="b0184-1496">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1496">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="b0184-1497">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1497">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="b0184-1498">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1498">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="b0184-1499">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1499">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="b0184-1500">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1500">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-1501">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-1501">Batch</span></span>

* <span data-ttu-id="b0184-1502">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1502">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="b0184-1503">クラウド</span><span class="sxs-lookup"><span data-stu-id="b0184-1503">Cloud</span></span>

* <span data-ttu-id="b0184-1504">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1504">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="b0184-1505">消費</span><span class="sxs-lookup"><span data-stu-id="b0184-1505">Consumption</span></span>

* <span data-ttu-id="b0184-1506">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1506">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="b0184-1507">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b0184-1507">Event Grid</span></span>

* <span data-ttu-id="b0184-1508">[破壊的変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1508">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="b0184-1509">[破壊的変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1509">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="b0184-1510">[破壊的変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1510">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="b0184-1511">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b0184-1511">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="b0184-1512">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1512">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="b0184-1513">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1513">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="b0184-1514">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1514">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="b0184-1515">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1515">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-1516">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0184-1516">Interactive</span></span>

* <span data-ttu-id="b0184-1517">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1517">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="b0184-1518">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1518">Fixed errors on startup</span></span>
* <span data-ttu-id="b0184-1519">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1519">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="b0184-1520">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-1520">IoT</span></span>

* <span data-ttu-id="b0184-1521">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1521">Added support for device provisioning service</span></span>
* <span data-ttu-id="b0184-1522">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1522">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="b0184-1523">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1523">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-1524">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-1524">Monitor</span></span>

* <span data-ttu-id="b0184-1525">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1525">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="b0184-1526">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1526">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="b0184-1527">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1527">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1528">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1528">Network</span></span>

* <span data-ttu-id="b0184-1529">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1529">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="b0184-1530">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1530">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="b0184-1531">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-1531">Profile</span></span>

* <span data-ttu-id="b0184-1532">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1532">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="b0184-1533">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-1533">Role</span></span>

* <span data-ttu-id="b0184-1534">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1534">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b0184-1535">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b0184-1535">Service Fabric</span></span>

* <span data-ttu-id="b0184-1536">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1536">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="b0184-1537">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1537">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1538">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1538">VM</span></span>

* <span data-ttu-id="b0184-1539">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="b0184-1539">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="b0184-1540">[破壊的変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1540">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="b0184-1541">[破壊的変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1541">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="b0184-1542">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1542">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="b0184-1543">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1543">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="b0184-1544">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1544">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="b0184-1545">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1545">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="b0184-1546">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1546">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="b0184-1547">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1547">December 19, 2017</span></span>

<span data-ttu-id="b0184-1548">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="b0184-1548">Version 2.0.23</span></span>

* <span data-ttu-id="b0184-1549">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1549">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="b0184-1550">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-1550">Container</span></span>

* <span data-ttu-id="b0184-1551">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1551">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1552">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1552">Network</span></span>

* <span data-ttu-id="b0184-1553">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1553">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="b0184-1554">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1554">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1555">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1555">Storage</span></span>

* <span data-ttu-id="b0184-1556">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1556">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1557">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1557">VM</span></span>

* <span data-ttu-id="b0184-1558">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1558">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="b0184-1559">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1559">December 5, 2017</span></span>

<span data-ttu-id="b0184-1560">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="b0184-1560">Version 2.0.22</span></span>

* <span data-ttu-id="b0184-1561">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1561">Removed `az component` commands.</span></span> <span data-ttu-id="b0184-1562">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b0184-1562">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="b0184-1563">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1563">Core</span></span>
* <span data-ttu-id="b0184-1564">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1564">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="b0184-1565">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1565">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1566">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1566">ACS</span></span>

* <span data-ttu-id="b0184-1567">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1567">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="b0184-1568">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1568">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="b0184-1569">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1569">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="b0184-1570">Advisor</span><span class="sxs-lookup"><span data-stu-id="b0184-1570">Advisor</span></span>

* <span data-ttu-id="b0184-1571">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-1571">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1572">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1572">Appservice</span></span>

* <span data-ttu-id="b0184-1573">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1573">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="b0184-1574">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1574">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="b0184-1575">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1575">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="b0184-1576">消費</span><span class="sxs-lookup"><span data-stu-id="b0184-1576">Consumption</span></span>

* <span data-ttu-id="b0184-1577">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1577">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="b0184-1578">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-1578">Container</span></span>

* <span data-ttu-id="b0184-1579">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1579">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-1580">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-1580">Monitor</span></span>

* <span data-ttu-id="b0184-1581">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1581">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1582">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1582">Resource</span></span>

* <span data-ttu-id="b0184-1583">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1583">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="b0184-1584">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-1584">Role</span></span>

* <span data-ttu-id="b0184-1585">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1585">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="b0184-1586">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1586">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="b0184-1587">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1587">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-1588">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-1588">SQL</span></span>

* <span data-ttu-id="b0184-1589">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1589">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="b0184-1590">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1590">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1591">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1591">VM</span></span>

* <span data-ttu-id="b0184-1592">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1592">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="b0184-1593">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1593">November 14, 2017</span></span>

<span data-ttu-id="b0184-1594">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="b0184-1594">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-1595">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-1595">ACR</span></span>

* <span data-ttu-id="b0184-1596">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1596">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="b0184-1597">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1597">ACS</span></span>

* <span data-ttu-id="b0184-1598">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1598">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="b0184-1599">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1599">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="b0184-1600">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1600">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="b0184-1601">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1601">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="b0184-1602">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1602">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1603">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1603">Appservice</span></span>

* <span data-ttu-id="b0184-1604">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1604">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="b0184-1605">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1605">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="b0184-1606">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1606">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="b0184-1607">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1607">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="b0184-1608">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1608">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="b0184-1609">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="b0184-1609">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-1610">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-1610">Batch</span></span>

* <span data-ttu-id="b0184-1611">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1611">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="b0184-1612">Batchai</span><span class="sxs-lookup"><span data-stu-id="b0184-1612">Batchai</span></span>

* <span data-ttu-id="b0184-1613">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1613">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="b0184-1614">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1614">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="b0184-1615">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1615">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="b0184-1616">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1616">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="b0184-1617">クラウド</span><span class="sxs-lookup"><span data-stu-id="b0184-1617">Cloud</span></span>

* <span data-ttu-id="b0184-1618">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1618">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="b0184-1619">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-1619">Container</span></span>

* <span data-ttu-id="b0184-1620">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1620">Added support to open multiple ports</span></span>
* <span data-ttu-id="b0184-1621">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1621">Added container group restart policy</span></span>
* <span data-ttu-id="b0184-1622">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1622">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="b0184-1623">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1623">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b0184-1624">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b0184-1624">Data Lake Analytics</span></span>

* <span data-ttu-id="b0184-1625">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1625">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b0184-1626">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b0184-1626">Data Lake Store</span></span>

* <span data-ttu-id="b0184-1627">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1627">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="b0184-1628">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0184-1628">Extension</span></span>

* <span data-ttu-id="b0184-1629">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1629">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="b0184-1630">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1630">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="b0184-1631">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-1631">IoT</span></span>

* <span data-ttu-id="b0184-1632">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1632">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-1633">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-1633">Monitor</span></span>

* <span data-ttu-id="b0184-1634">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1634">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1635">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1635">Network</span></span>

* <span data-ttu-id="b0184-1636">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1636">Added support for CAA DNS records</span></span>
* <span data-ttu-id="b0184-1637">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1637">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="b0184-1638">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1638">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="b0184-1639">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1639">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="b0184-1640">Reservations</span><span class="sxs-lookup"><span data-stu-id="b0184-1640">Reservations</span></span>

* <span data-ttu-id="b0184-1641">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b0184-1641">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1642">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1642">Resource</span></span>

* <span data-ttu-id="b0184-1643">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1643">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-1644">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-1644">SQL</span></span>

* <span data-ttu-id="b0184-1645">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1645">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1646">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1646">Storage</span></span>

* <span data-ttu-id="b0184-1647">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1647">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="b0184-1648">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1648">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="b0184-1649">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1649">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="b0184-1650">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1650">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="b0184-1651">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1651">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="b0184-1652">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1652">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="b0184-1653">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1653">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1654">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1654">VM</span></span>

* <span data-ttu-id="b0184-1655">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1655">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="b0184-1656">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1656">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="b0184-1657">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1657">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="b0184-1658">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1658">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="b0184-1659">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1659">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="b0184-1660">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1660">October 24, 2017</span></span>

<span data-ttu-id="b0184-1661">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="b0184-1661">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="b0184-1662">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1662">Core</span></span>

* <span data-ttu-id="b0184-1663">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1663">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-1664">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-1664">ACR</span></span>

* <span data-ttu-id="b0184-1665">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1665">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="b0184-1666">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1666">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="b0184-1667">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1667">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1668">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1668">ACS</span></span>

* <span data-ttu-id="b0184-1669">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1669">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="b0184-1670">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1670">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1671">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1671">Appservice</span></span>

* <span data-ttu-id="b0184-1672">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1672">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="b0184-1673">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b0184-1673">Component</span></span>

* <span data-ttu-id="b0184-1674">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1674">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-1675">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-1675">Monitor</span></span>

* <span data-ttu-id="b0184-1676">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1676">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1677">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1677">Resource</span></span>

* <span data-ttu-id="b0184-1678">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1678">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="b0184-1679">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1679">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1680">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1680">VM</span></span>

* <span data-ttu-id="b0184-1681">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1681">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="b0184-1682">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1682">October 9, 2017</span></span>

<span data-ttu-id="b0184-1683">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="b0184-1683">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="b0184-1684">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1684">Core</span></span>

* <span data-ttu-id="b0184-1685">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1685">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1686">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1686">Appservice</span></span>

* <span data-ttu-id="b0184-1687">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1687">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-1688">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-1688">Batch</span></span>

* <span data-ttu-id="b0184-1689">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1689">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="b0184-1690">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1690">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="b0184-1691">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1691">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="b0184-1692">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1692">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="b0184-1693">Batchai</span><span class="sxs-lookup"><span data-stu-id="b0184-1693">Batchai</span></span>

* <span data-ttu-id="b0184-1694">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-1694">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0184-1695">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0184-1695">Keyvault</span></span>

* <span data-ttu-id="b0184-1696">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1696">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="b0184-1697">(#4448)</span><span class="sxs-lookup"><span data-stu-id="b0184-1697">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="b0184-1698">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1698">Network</span></span>

* <span data-ttu-id="b0184-1699">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1699">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="b0184-1700">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1700">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1701">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1701">Resource</span></span>

* <span data-ttu-id="b0184-1702">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1702">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="b0184-1703">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1703">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="b0184-1704">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1704">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="b0184-1705">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1705">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-1706">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-1706">Sql</span></span>

* <span data-ttu-id="b0184-1707">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1707">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="b0184-1708">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1708">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="b0184-1709">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1709">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1710">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1710">Storage</span></span>

* <span data-ttu-id="b0184-1711">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1711">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1712">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1712">Vm</span></span>

* <span data-ttu-id="b0184-1713">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1713">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="b0184-1714">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1714">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="b0184-1715">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1715">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="b0184-1716">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1716">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="b0184-1717">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1717">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="b0184-1718">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1718">September 22, 2017</span></span>

<span data-ttu-id="b0184-1719">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="b0184-1719">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1720">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1720">Resource</span></span>

* <span data-ttu-id="b0184-1721">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1721">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="b0184-1722">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1722">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="b0184-1723">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1723">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="b0184-1724">[破壊的変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1724">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1725">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1725">Network</span></span>

* <span data-ttu-id="b0184-1726">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1726">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="b0184-1727">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1727">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="b0184-1728">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1728">Added `asg` application security group commands</span></span>
* <span data-ttu-id="b0184-1729">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1729">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="b0184-1730">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1730">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="b0184-1731">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1731">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="b0184-1732">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1732">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1733">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1733">Storage</span></span>

* <span data-ttu-id="b0184-1734">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1734">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="b0184-1735">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="b0184-1735">Eventgrid</span></span>

* <span data-ttu-id="b0184-1736">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1736">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-1737">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-1737">SQL</span></span>

* <span data-ttu-id="b0184-1738">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1738">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="b0184-1739">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="b0184-1739">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="b0184-1740">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1740">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0184-1741">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0184-1741">Keyvault</span></span>

* <span data-ttu-id="b0184-1742">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1742">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1743">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1743">VM</span></span>

* <span data-ttu-id="b0184-1744">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1744">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="b0184-1745">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1745">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="b0184-1746">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1746">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="b0184-1747">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1747">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="b0184-1748">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1748">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="b0184-1749">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1749">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1750">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1750">ACS</span></span>

* <span data-ttu-id="b0184-1751">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1751">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1752">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1752">Appservice</span></span>

* <span data-ttu-id="b0184-1753">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1753">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="b0184-1754">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b0184-1754">Backup</span></span>

* <span data-ttu-id="b0184-1755">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b0184-1755">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="b0184-1756">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1756">September 11, 2017</span></span>

<span data-ttu-id="b0184-1757">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="b0184-1757">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="b0184-1758">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1758">Core</span></span>

* <span data-ttu-id="b0184-1759">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1759">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="b0184-1760">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1760">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1761">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1761">Acs</span></span>

* <span data-ttu-id="b0184-1762">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1762">Added `acs list-locations` command</span></span>
* <span data-ttu-id="b0184-1763">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1763">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1764">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1764">Appservice</span></span>

* <span data-ttu-id="b0184-1765">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1765">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="b0184-1766">CDN</span><span class="sxs-lookup"><span data-stu-id="b0184-1766">CDN</span></span>

* <span data-ttu-id="b0184-1767">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1767">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="b0184-1768">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0184-1768">Extension</span></span>

* <span data-ttu-id="b0184-1769">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-1769">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0184-1770">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0184-1770">Keyvault</span></span>

* <span data-ttu-id="b0184-1771">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1771">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1772">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1772">Network</span></span>

* <span data-ttu-id="b0184-1773">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1773">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="b0184-1774">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1774">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="b0184-1775">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1775">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="b0184-1776">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1776">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="b0184-1777">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1777">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-1778">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-1778">Resource</span></span>

* <span data-ttu-id="b0184-1779">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b0184-1779">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="b0184-1780">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b0184-1780">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="b0184-1781">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b0184-1781">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="b0184-1782">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1782">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-1783">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-1783">SQL</span></span>

* <span data-ttu-id="b0184-1784">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1784">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1785">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1785">VM</span></span>

* <span data-ttu-id="b0184-1786">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="b0184-1786">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="b0184-1787">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="b0184-1787">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="b0184-1788">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1788">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="b0184-1789">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="b0184-1789">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="b0184-1790">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="b0184-1790">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="b0184-1791">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1791">August 31, 2017</span></span>

<span data-ttu-id="b0184-1792">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="b0184-1792">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0184-1793">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0184-1793">Keyvault</span></span>

* <span data-ttu-id="b0184-1794">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1794">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="b0184-1795">SF</span><span class="sxs-lookup"><span data-stu-id="b0184-1795">Sf</span></span>

* <span data-ttu-id="b0184-1796">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="b0184-1796">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1797">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1797">Storage</span></span>

* <span data-ttu-id="b0184-1798">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1798">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="b0184-1799">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="b0184-1799">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="b0184-1800">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1800">August 28, 2017</span></span>

<span data-ttu-id="b0184-1801">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="b0184-1801">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="b0184-1802">CLI</span><span class="sxs-lookup"><span data-stu-id="b0184-1802">CLI</span></span>

* <span data-ttu-id="b0184-1803">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1803">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1804">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1804">ACS</span></span>

* <span data-ttu-id="b0184-1805">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1805">Corrected preview regions</span></span>
* <span data-ttu-id="b0184-1806">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1806">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="b0184-1807">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1807">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1808">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1808">Appservice</span></span>

* <span data-ttu-id="b0184-1809">[破壊的変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1809">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="b0184-1810">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1810">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="b0184-1811">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1811">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="b0184-1812">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1812">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="b0184-1813">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="b0184-1813">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="b0184-1814">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-1814">IoT</span></span>

* <span data-ttu-id="b0184-1815">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1815">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1816">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1816">Network</span></span>

* <span data-ttu-id="b0184-1817">[破壊的変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1817">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="b0184-1818">[破壊的変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1818">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="b0184-1819">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1819">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="b0184-1820">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1820">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="b0184-1821">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1821">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="b0184-1822">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-1822">Profile</span></span>

* <span data-ttu-id="b0184-1823">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1823">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b0184-1824">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b0184-1824">Service Fabric</span></span>

* <span data-ttu-id="b0184-1825">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b0184-1825">Preview release</span></span>
* <span data-ttu-id="b0184-1826">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1826">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="b0184-1827">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1827">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="b0184-1828">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1828">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1829">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1829">Storage</span></span>

* <span data-ttu-id="b0184-1830">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1830">Enabled setting blob tier</span></span>
* <span data-ttu-id="b0184-1831">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1831">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="b0184-1832">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1832">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="b0184-1833">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1833">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="b0184-1834">[破壊的変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1834">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="b0184-1835">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="b0184-1835">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1836">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1836">VM</span></span>

* <span data-ttu-id="b0184-1837">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1837">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="b0184-1838">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1838">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="b0184-1839">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1839">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="b0184-1840">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1840">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="b0184-1841">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1841">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="b0184-1842">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1842">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="b0184-1843">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1843">August 15, 2017</span></span>

<span data-ttu-id="b0184-1844">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="b0184-1844">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1845">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1845">ACS</span></span>

* <span data-ttu-id="b0184-1846">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1846">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1847">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1847">Appservice</span></span>

* <span data-ttu-id="b0184-1848">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1848">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="b0184-1849">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b0184-1849">Event Grid</span></span>

* <span data-ttu-id="b0184-1850">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1850">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="b0184-1851">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1851">August 11, 2017</span></span>

<span data-ttu-id="b0184-1852">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="b0184-1852">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1853">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1853">ACS</span></span>

* <span data-ttu-id="b0184-1854">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1854">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-1855">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-1855">Batch</span></span>

* <span data-ttu-id="b0184-1856">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1856">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="b0184-1857">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1857">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="b0184-1858">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1858">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="b0184-1859">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1859">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="b0184-1860">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-1860">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="b0184-1861">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1861">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="b0184-1862">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b0184-1862">Component</span></span>

* <span data-ttu-id="b0184-1863">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1863">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="b0184-1864">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0184-1864">Container</span></span>

* <span data-ttu-id="b0184-1865">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1865">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="b0184-1866">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b0184-1866">Data Lake Store</span></span>

* <span data-ttu-id="b0184-1867">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1867">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="b0184-1868">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b0184-1868">Event Grid</span></span>

* <span data-ttu-id="b0184-1869">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-1869">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1870">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1870">Network</span></span>

* <span data-ttu-id="b0184-1871">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1871">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="b0184-1872">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1872">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="b0184-1873">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1873">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="b0184-1874">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1874">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="b0184-1875">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-1875">Profile</span></span>

* <span data-ttu-id="b0184-1876">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1876">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-1877">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-1877">Storage</span></span>

* <span data-ttu-id="b0184-1878">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="b0184-1878">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-1879">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-1879">VM</span></span>

* <span data-ttu-id="b0184-1880">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1880">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="b0184-1881">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1881">Exposed `list-skus` command</span></span>
* <span data-ttu-id="b0184-1882">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-1882">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="b0184-1883">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="b0184-1883">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="b0184-1884">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1884">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="b0184-1885">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b0184-1885">July 28, 2017</span></span>

<span data-ttu-id="b0184-1886">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="b0184-1886">Version 2.0.12</span></span>

* <span data-ttu-id="b0184-1887">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1887">Added container commands</span></span>
* <span data-ttu-id="b0184-1888">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1888">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="b0184-1889">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-1889">Core</span></span>

* <span data-ttu-id="b0184-1890">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="b0184-1890">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="b0184-1891">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1891">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="b0184-1892">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="b0184-1892">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="b0184-1893">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="b0184-1893">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="b0184-1894">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="b0184-1894">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="b0184-1895">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="b0184-1895">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="b0184-1896">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="b0184-1896">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="b0184-1897">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="b0184-1897">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="b0184-1898">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="b0184-1898">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="b0184-1899">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="b0184-1899">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="b0184-1900">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="b0184-1900">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="b0184-1901">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="b0184-1901">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="b0184-1902">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1902">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="b0184-1903">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1903">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="b0184-1904">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-1904">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="b0184-1905">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="b0184-1905">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="b0184-1906">ACR</span><span class="sxs-lookup"><span data-stu-id="b0184-1906">ACR</span></span>

* <span data-ttu-id="b0184-1907">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1907">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="b0184-1908">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-1908">Support SKU update for managed registries</span></span>
* <span data-ttu-id="b0184-1909">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1909">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="b0184-1910">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1910">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="b0184-1911">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1911">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="b0184-1912">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1912">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-1913">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-1913">ACS</span></span>

* <span data-ttu-id="b0184-1914">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-1914">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-1915">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0184-1915">Appservice</span></span>

* <span data-ttu-id="b0184-1916">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1916">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="b0184-1917">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-1917">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="b0184-1918">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="b0184-1918">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="b0184-1919">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="b0184-1919">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="b0184-1920">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="b0184-1920">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="b0184-1921">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="b0184-1921">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="b0184-1922">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="b0184-1922">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="b0184-1923">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="b0184-1923">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="b0184-1924">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1924">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="b0184-1925">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b0184-1925">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="b0184-1926">Batch</span><span class="sxs-lookup"><span data-stu-id="b0184-1926">Batch</span></span>

* <span data-ttu-id="b0184-1927">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1927">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="b0184-1928">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1928">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="b0184-1929">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1929">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="b0184-1930">CDN</span><span class="sxs-lookup"><span data-stu-id="b0184-1930">CDN</span></span>

* <span data-ttu-id="b0184-1931">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1931">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="b0184-1932">クラウド</span><span class="sxs-lookup"><span data-stu-id="b0184-1932">Cloud</span></span>

* <span data-ttu-id="b0184-1933">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1933">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="b0184-1934">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="b0184-1934">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="b0184-1935">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-1935">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="b0184-1936">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1936">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="b0184-1937">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1937">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0184-1938">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0184-1938">CosmosDB</span></span>

* <span data-ttu-id="b0184-1939">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1939">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="b0184-1940">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1940">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b0184-1941">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b0184-1941">Data Lake Analytics</span></span>

* <span data-ttu-id="b0184-1942">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1942">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="b0184-1943">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1943">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="b0184-1944">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1944">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b0184-1945">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b0184-1945">Data Lake Store</span></span>

* <span data-ttu-id="b0184-1946">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1946">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="b0184-1947">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1947">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="b0184-1948">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1948">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="b0184-1949">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="b0184-1949">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="b0184-1950">対話</span><span class="sxs-lookup"><span data-stu-id="b0184-1950">Interactive</span></span>

* <span data-ttu-id="b0184-1951">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1951">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="b0184-1952">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="b0184-1952">Increased test coverage</span></span>
* <span data-ttu-id="b0184-1953">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1953">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="b0184-1954">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="b0184-1954">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="b0184-1955">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="b0184-1955">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="b0184-1956">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="b0184-1956">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="b0184-1957">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="b0184-1957">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="b0184-1958">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1958">Added `--progress` flag</span></span>
* <span data-ttu-id="b0184-1959">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1959">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="b0184-1960">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="b0184-1960">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="b0184-1961">IoT</span><span class="sxs-lookup"><span data-stu-id="b0184-1961">IoT</span></span>

* <span data-ttu-id="b0184-1962">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1962">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="b0184-1963">(#3934)</span><span class="sxs-lookup"><span data-stu-id="b0184-1963">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="b0184-1964">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b0184-1964">Key vault</span></span>

* <span data-ttu-id="b0184-1965">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1965">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="b0184-1966">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b0184-1966">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="b0184-1967">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b0184-1967">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="b0184-1968">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b0184-1968">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="b0184-1969">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b0184-1969">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="b0184-1970">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="b0184-1970">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="b0184-1971">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1971">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="b0184-1972">(#3307)</span><span class="sxs-lookup"><span data-stu-id="b0184-1972">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="b0184-1973">ラボ</span><span class="sxs-lookup"><span data-stu-id="b0184-1973">Lab</span></span>

* <span data-ttu-id="b0184-1974">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1974">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="b0184-1975">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1975">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-1976">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-1976">Monitor</span></span>

* <span data-ttu-id="b0184-1977">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="b0184-1977">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="b0184-1978">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1978">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="b0184-1979">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1979">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="b0184-1980">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1980">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="b0184-1981">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1981">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="b0184-1982">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0184-1982">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="b0184-1983">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1983">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="b0184-1984">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="b0184-1984">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="b0184-1985">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1985">`location` no longer required</span></span>
  * <span data-ttu-id="b0184-1986">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="b0184-1986">Add name and ID support for target</span></span>
  * <span data-ttu-id="b0184-1987">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="b0184-1987">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="b0184-1988">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-1988">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="b0184-1989">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-1989">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="b0184-1990">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="b0184-1990">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="b0184-1991">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-1991">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="b0184-1992">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1992">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="b0184-1993">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-1993">Network</span></span>

* <span data-ttu-id="b0184-1994">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1994">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="b0184-1995">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1995">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="b0184-1996">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1996">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="b0184-1997">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1997">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="b0184-1998">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1998">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="b0184-1999">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-1999">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="b0184-2000">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2000">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="b0184-2001">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2001">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="b0184-2002">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2002">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="b0184-2003">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2003">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="b0184-2004">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2004">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="b0184-2005">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2005">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="b0184-2006">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2006">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="b0184-2007">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2007">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="b0184-2008">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2008">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="b0184-2009">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2009">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="b0184-2010">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2010">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="b0184-2011">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2011">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="b0184-2012">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2012">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="b0184-2013">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2013">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="b0184-2014">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2014">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="b0184-2015">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2015">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="b0184-2016">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2016">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="b0184-2017">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b0184-2017">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="b0184-2018">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b0184-2018">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="b0184-2019">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b0184-2019">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="b0184-2020">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b0184-2020">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="b0184-2021">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-2021">Profile</span></span>

* <span data-ttu-id="b0184-2022">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-2022">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="b0184-2023">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-2023">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="b0184-2024">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="b0184-2024">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="b0184-2025">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2025">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="b0184-2026">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-2026">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0184-2027">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0184-2027">RDBMS</span></span>

* <span data-ttu-id="b0184-2028">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="b0184-2028">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="b0184-2029">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="b0184-2029">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="b0184-2030">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="b0184-2030">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="b0184-2031">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="b0184-2031">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-2032">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-2032">Resource</span></span>

* <span data-ttu-id="b0184-2033">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2033">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="b0184-2034">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2034">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="b0184-2035">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2035">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="b0184-2036">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-2036">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="b0184-2037">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="b0184-2037">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="b0184-2038">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2038">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="b0184-2039">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="b0184-2039">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="b0184-2040">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2040">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="b0184-2041">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-2041">Role</span></span>

* <span data-ttu-id="b0184-2042">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-2042">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="b0184-2043">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="b0184-2043">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="b0184-2044">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="b0184-2044">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="b0184-2045">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="b0184-2045">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="b0184-2046">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2046">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b0184-2047">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b0184-2047">Service Fabric</span></span>
* <span data-ttu-id="b0184-2048">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="b0184-2048">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="b0184-2049">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="b0184-2049">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="b0184-2050">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="b0184-2050">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-2051">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-2051">SQL</span></span>

* <span data-ttu-id="b0184-2052">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2052">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="b0184-2053">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2053">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="b0184-2054">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2054">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-2055">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-2055">Storage</span></span>

* <span data-ttu-id="b0184-2056">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="b0184-2056">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="b0184-2057">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-2057">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="b0184-2058">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="b0184-2058">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="b0184-2059">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="b0184-2059">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="b0184-2060">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="b0184-2060">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="b0184-2061">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="b0184-2061">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-2062">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-2062">VM</span></span>

* <span data-ttu-id="b0184-2063">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-2063">Support configuring nsg</span></span>
* <span data-ttu-id="b0184-2064">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2064">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="b0184-2065">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0184-2065">Support managed service identities</span></span>
* <span data-ttu-id="b0184-2066">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2066">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="b0184-2067">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="b0184-2067">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="b0184-2068">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="b0184-2068">May 10, 2017</span></span>

<span data-ttu-id="b0184-2069">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="b0184-2069">Version 2.0.6</span></span>

* <span data-ttu-id="b0184-2070">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2070">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="b0184-2071">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2071">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="b0184-2072">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2072">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="b0184-2073">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2073">Include Cognitive Services module</span></span>
* <span data-ttu-id="b0184-2074">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2074">Include Service Fabric module</span></span>
* <span data-ttu-id="b0184-2075">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="b0184-2075">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="b0184-2076">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2076">Add support for CDN commands</span></span>
* <span data-ttu-id="b0184-2077">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2077">Remove Container module</span></span>
* <span data-ttu-id="b0184-2078">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="b0184-2078">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="b0184-2079">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="b0184-2079">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="b0184-2080">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-2080">Core</span></span>

* <span data-ttu-id="b0184-2081">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="b0184-2081">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="b0184-2082">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="b0184-2082">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="b0184-2083">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="b0184-2083">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="b0184-2084">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="b0184-2084">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="b0184-2085">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="b0184-2085">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="b0184-2086">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="b0184-2086">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="b0184-2087">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="b0184-2087">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="b0184-2088">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="b0184-2088">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="b0184-2089">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="b0184-2089">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="b0184-2090">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="b0184-2090">core: Improved performance</span></span>
* <span data-ttu-id="b0184-2091">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="b0184-2091">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="b0184-2092">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="b0184-2092">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-2093">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-2093">ACS</span></span>

* <span data-ttu-id="b0184-2094">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2094">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="b0184-2095">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2095">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="b0184-2096">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2096">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="b0184-2097">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="b0184-2097">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-2098">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-2098">AppService</span></span>

* <span data-ttu-id="b0184-2099">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2099">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="b0184-2100">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2100">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="b0184-2101">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="b0184-2101">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="b0184-2102">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2102">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="b0184-2103">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2103">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="b0184-2104">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="b0184-2104">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="b0184-2105">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="b0184-2105">support slot swap with preview</span></span>
* <span data-ttu-id="b0184-2106">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="b0184-2106">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="b0184-2107">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="b0184-2107">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0184-2108">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0184-2108">CosmosDB</span></span>

* <span data-ttu-id="b0184-2109">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2109">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="b0184-2110">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2110">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="b0184-2111">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2111">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="b0184-2112">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2112">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b0184-2113">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b0184-2113">Data Lake Analytics</span></span>

* <span data-ttu-id="b0184-2114">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2114">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="b0184-2115">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="b0184-2115">Add support for new catalog item type: package.</span></span> <span data-ttu-id="b0184-2116">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="b0184-2116">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="b0184-2117">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="b0184-2117">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="b0184-2118">テーブル</span><span class="sxs-lookup"><span data-stu-id="b0184-2118">Table</span></span>
  * <span data-ttu-id="b0184-2119">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="b0184-2119">Table valued function</span></span>
  * <span data-ttu-id="b0184-2120">表示</span><span class="sxs-lookup"><span data-stu-id="b0184-2120">View</span></span>
  * <span data-ttu-id="b0184-2121">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="b0184-2121">Table Statistics.</span></span> <span data-ttu-id="b0184-2122">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="b0184-2122">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b0184-2123">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b0184-2123">Data Lake Store</span></span>

* <span data-ttu-id="b0184-2124">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2124">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="b0184-2125">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="b0184-2125">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="b0184-2126">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="b0184-2126">missed help for access show.</span></span> <span data-ttu-id="b0184-2127">追加しました </span><span class="sxs-lookup"><span data-stu-id="b0184-2127">adding it.</span></span> <span data-ttu-id="b0184-2128">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="b0184-2128">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="b0184-2129">検索</span><span class="sxs-lookup"><span data-stu-id="b0184-2129">Find</span></span>

* <span data-ttu-id="b0184-2130">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="b0184-2130">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0184-2131">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0184-2131">KeyVault</span></span>

* <span data-ttu-id="b0184-2132">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2132">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="b0184-2133">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2133">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="b0184-2134">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="b0184-2134">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="b0184-2135">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2135">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="b0184-2136">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="b0184-2136">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="b0184-2137">ラボ</span><span class="sxs-lookup"><span data-stu-id="b0184-2137">Lab</span></span>

* <span data-ttu-id="b0184-2138">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2138">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="b0184-2139">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2139">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="b0184-2140">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2140">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="b0184-2141">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2141">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="b0184-2142">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2142">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="b0184-2143">監視</span><span class="sxs-lookup"><span data-stu-id="b0184-2143">Monitor</span></span>

* <span data-ttu-id="b0184-2144">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="b0184-2144">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="b0184-2145">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="b0184-2145">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="b0184-2146">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-2146">Network</span></span>

* <span data-ttu-id="b0184-2147">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2147">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="b0184-2148">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2148">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="b0184-2149">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2149">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="b0184-2150">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2150">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="b0184-2151">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2151">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="b0184-2152">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2152">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="b0184-2153">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2153">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="b0184-2154">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2154">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="b0184-2155">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2155">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="b0184-2156">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2156">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="b0184-2157">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2157">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="b0184-2158">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2158">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="b0184-2159">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2159">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="b0184-2160">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2160">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="b0184-2161">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0184-2161">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="b0184-2162">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2162">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="b0184-2163">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0184-2163">Profile</span></span>

* <span data-ttu-id="b0184-2164">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="b0184-2164">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="b0184-2165">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="b0184-2165">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="b0184-2166">Redis</span><span class="sxs-lookup"><span data-stu-id="b0184-2166">Redis</span></span>

* <span data-ttu-id="b0184-2167">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2167">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="b0184-2168">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2168">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="b0184-2169">リソース</span><span class="sxs-lookup"><span data-stu-id="b0184-2169">Resource</span></span>

* <span data-ttu-id="b0184-2170">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="b0184-2170">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="b0184-2171">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="b0184-2171">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="b0184-2172">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="b0184-2172">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="b0184-2173">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="b0184-2173">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="b0184-2174">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="b0184-2174">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="b0184-2175">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="b0184-2175">Add docs for az lock update.</span></span> <span data-ttu-id="b0184-2176">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="b0184-2176">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="b0184-2177">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="b0184-2177">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="b0184-2178">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="b0184-2178">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="b0184-2179">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="b0184-2179">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="b0184-2180">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="b0184-2180">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="b0184-2181">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="b0184-2181">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="b0184-2182">Role</span><span class="sxs-lookup"><span data-stu-id="b0184-2182">Role</span></span>

* <span data-ttu-id="b0184-2183">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="b0184-2183">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="b0184-2184">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="b0184-2184">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="b0184-2185">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="b0184-2185">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="b0184-2186">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="b0184-2186">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="b0184-2187">SQL</span><span class="sxs-lookup"><span data-stu-id="b0184-2187">SQL</span></span>

* <span data-ttu-id="b0184-2188">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0184-2188">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="b0184-2189">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="b0184-2189">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="b0184-2190">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-2190">Storage</span></span>

* <span data-ttu-id="b0184-2191">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="b0184-2191">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="b0184-2192">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2192">Add support for incremental blob copy</span></span>
* <span data-ttu-id="b0184-2193">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2193">Add support for large block blob upload</span></span>
* <span data-ttu-id="b0184-2194">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="b0184-2194">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-2195">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-2195">VM</span></span>

* <span data-ttu-id="b0184-2196">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="b0184-2196">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="b0184-2197">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="b0184-2197">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="b0184-2198">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="b0184-2198">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="b0184-2199">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="b0184-2199">az vm/vmss disk</span></span>
  3. <span data-ttu-id="b0184-2200">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="b0184-2200">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="b0184-2201">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="b0184-2201">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="b0184-2202">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="b0184-2202">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="b0184-2203">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b0184-2203">April 3, 2017</span></span>

<span data-ttu-id="b0184-2204">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="b0184-2204">Version 2.0.2</span></span>

<span data-ttu-id="b0184-2205">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="b0184-2205">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="b0184-2206">コア</span><span class="sxs-lookup"><span data-stu-id="b0184-2206">Core</span></span>

* <span data-ttu-id="b0184-2207">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="b0184-2207">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="b0184-2208">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="b0184-2208">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="b0184-2209">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="b0184-2209">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="b0184-2210">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="b0184-2210">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="b0184-2211">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="b0184-2211">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="b0184-2212">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="b0184-2212">Add prompting for missing template parameters.</span></span> <span data-ttu-id="b0184-2213">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="b0184-2213">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="b0184-2214">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="b0184-2214">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="b0184-2215">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="b0184-2215">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="b0184-2216">ACS</span><span class="sxs-lookup"><span data-stu-id="b0184-2216">ACS</span></span>

* <span data-ttu-id="b0184-2217">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="b0184-2217">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="b0184-2218">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="b0184-2218">Add support for ssh key password prompting.</span></span> <span data-ttu-id="b0184-2219">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="b0184-2219">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="b0184-2220">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="b0184-2220">Add support for windows clusters.</span></span> <span data-ttu-id="b0184-2221">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="b0184-2221">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="b0184-2222">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="b0184-2222">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="b0184-2223">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="b0184-2223">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="b0184-2224">AppService</span><span class="sxs-lookup"><span data-stu-id="b0184-2224">AppService</span></span>

* <span data-ttu-id="b0184-2225">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="b0184-2225">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="b0184-2226">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="b0184-2226">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="b0184-2227">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="b0184-2227">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="b0184-2228">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="b0184-2228">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="b0184-2229">DataLake</span><span class="sxs-lookup"><span data-stu-id="b0184-2229">DataLake</span></span>

* <span data-ttu-id="b0184-2230">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-2230">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="b0184-2231">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0184-2231">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="b0184-2232">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="b0184-2232">DocuemntDB</span></span>

* <span data-ttu-id="b0184-2233">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="b0184-2233">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="b0184-2234">VM</span><span class="sxs-lookup"><span data-stu-id="b0184-2234">VM</span></span>

* <span data-ttu-id="b0184-2235">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="b0184-2235">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="b0184-2236">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="b0184-2236">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="b0184-2237">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="b0184-2237">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="b0184-2238">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="b0184-2238">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="b0184-2239">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="b0184-2239">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="b0184-2240">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="b0184-2240">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="b0184-2241">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="b0184-2241">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="b0184-2242">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b0184-2242">February 27, 2017</span></span>

<span data-ttu-id="b0184-2243">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="b0184-2243">Version 2.0.0</span></span>

<span data-ttu-id="b0184-2244">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="b0184-2244">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="b0184-2245">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="b0184-2245">Container Service (acs)</span></span>
- <span data-ttu-id="b0184-2246">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="b0184-2246">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="b0184-2247">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0184-2247">Networking</span></span>
- <span data-ttu-id="b0184-2248">Storage</span><span class="sxs-lookup"><span data-stu-id="b0184-2248">Storage</span></span>

<span data-ttu-id="b0184-2249">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="b0184-2249">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="b0184-2250">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="b0184-2250">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="b0184-2251">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="b0184-2251">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="b0184-2252">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="b0184-2252">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="b0184-2253">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="b0184-2253">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="b0184-2254">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="b0184-2254">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="b0184-2255">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="b0184-2255">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="b0184-2256">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="b0184-2256">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="b0184-2257">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="b0184-2257">Provide feedback from the command line with the `az feedback` command</span></span>

