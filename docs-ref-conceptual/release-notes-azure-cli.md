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
ms.openlocfilehash: 9f35084eeecab491e5be63eb856b0bb64a6157d0
ms.sourcegitcommit: 9fb008f2802ca6a58f33e01263bf55a80d01f031
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/27/2019
ms.locfileid: "56891213"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="b0c9c-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="b0c9c-103">Azure CLI release notes</span></span>
## <a name="february-26-2019"></a><span data-ttu-id="b0c9c-104">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-104">February 26, 2019</span></span>

<span data-ttu-id="b0c9c-105">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="b0c9c-105">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-106">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-106">Core</span></span>

* <span data-ttu-id="b0c9c-107">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-107">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-108">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-108">ACR</span></span>

* <span data-ttu-id="b0c9c-109">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-109">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="b0c9c-110">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-110">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-111">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-111">ACS</span></span>

* <span data-ttu-id="b0c9c-112">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-112">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-113">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-113">AppService</span></span>

* <span data-ttu-id="b0c9c-114">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-114">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-115">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-115">Batch</span></span>
* <span data-ttu-id="b0c9c-116">[破壊的変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-116">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="b0c9c-117">[破壊的変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-117">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="b0c9c-118">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-118">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="b0c9c-119">[破壊的変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-119">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="b0c9c-120">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-120">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="b0c9c-121">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-121">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0c9c-122">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0c9c-122">CosmosDB</span></span>

* <span data-ttu-id="b0c9c-123">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-123">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="b0c9c-124">Kusto</span><span class="sxs-lookup"><span data-stu-id="b0c9c-124">Kusto</span></span>

* <span data-ttu-id="b0c9c-125">[破壊的変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-125">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-126">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-126">Network</span></span>

* <span data-ttu-id="b0c9c-127">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-127">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="b0c9c-128">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-128">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="b0c9c-129">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-129">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="b0c9c-130">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-130">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="b0c9c-131">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-131">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="b0c9c-132">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-132">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="b0c9c-133">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-133">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-134">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-134">Resource</span></span>

* <span data-ttu-id="b0c9c-135">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-135">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="b0c9c-136">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-136">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="b0c9c-137">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-137">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="b0c9c-138">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-138">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="b0c9c-139">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-139">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-140">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-140">Role</span></span>

* <span data-ttu-id="b0c9c-141">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-141">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-142">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-142">VM</span></span>

* <span data-ttu-id="b0c9c-143">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-143">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="b0c9c-144">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-144">February 12, 2019</span></span>

<span data-ttu-id="b0c9c-145">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="b0c9c-145">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-146">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-146">Core</span></span>

* <span data-ttu-id="b0c9c-147">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-147">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="b0c9c-148">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-148">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-149">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-149">ACR</span></span>
* <span data-ttu-id="b0c9c-150">[破壊的変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-150">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="b0c9c-151">[破壊的変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-151">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-152">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-152">ACS</span></span>
* <span data-ttu-id="b0c9c-153">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-153">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="b0c9c-154">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-154">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="b0c9c-155">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-155">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="b0c9c-156">AMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-156">AMS</span></span>
* <span data-ttu-id="b0c9c-157">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-157">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="b0c9c-158">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-158">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-159">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-159">Appservice</span></span>
* <span data-ttu-id="b0c9c-160">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-160">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="b0c9c-161">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-161">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="b0c9c-162">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-162">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="b0c9c-163">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-163">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="b0c9c-164">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-164">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="b0c9c-165">Botservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-165">Botservice</span></span>
* <span data-ttu-id="b0c9c-166">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-166">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="b0c9c-167">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-167">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="b0c9c-168">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-168">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="b0c9c-169">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-169">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="b0c9c-170">[非推奨] `--proj-file-path` を優先して、`--proj-name` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-170">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="b0c9c-171">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-171">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="b0c9c-172">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-172">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="b0c9c-173">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-173">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="b0c9c-174">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="b0c9c-174">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="b0c9c-175">8.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-175">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="b0c9c-176">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-176">Key Vault</span></span>
* <span data-ttu-id="b0c9c-177">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-177">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-178">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-178">Monitor</span></span>
* <span data-ttu-id="b0c9c-179">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-179">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-180">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-180">Network</span></span>
* <span data-ttu-id="b0c9c-181">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-181">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="b0c9c-182">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-182">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="b0c9c-183">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-183">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="b0c9c-184">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-184">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="b0c9c-185">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="b0c9c-185">Policy Insights</span></span>
* <span data-ttu-id="b0c9c-186">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-186">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0c9c-187">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-187">RDBMS</span></span>
* <span data-ttu-id="b0c9c-188">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-188">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="b0c9c-189">Redis</span><span class="sxs-lookup"><span data-stu-id="b0c9c-189">Redis</span></span>
* <span data-ttu-id="b0c9c-190">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-190">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="b0c9c-191">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-191">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="b0c9c-192">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-192">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="b0c9c-193">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-193">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="b0c9c-194">[破壊的変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-194">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="b0c9c-195">[破壊的変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-195">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="b0c9c-196">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-196">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-197">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-197">Role</span></span>
* <span data-ttu-id="b0c9c-198">[破壊的変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-198">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="b0c9c-199">SQL VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-199">SQL VM</span></span>
* <span data-ttu-id="b0c9c-200">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-200">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-201">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-201">VM</span></span>
* <span data-ttu-id="b0c9c-202">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-202">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="b0c9c-203">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-203">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="b0c9c-204">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-204">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="b0c9c-205">[破壊的変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-205">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="b0c9c-206">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-206">January 31, 2019</span></span>

<span data-ttu-id="b0c9c-207">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="b0c9c-207">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-208">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-208">Core</span></span>

* <span data-ttu-id="b0c9c-209">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-209">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="b0c9c-210">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-210">January 28, 2019</span></span>

<span data-ttu-id="b0c9c-211">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="b0c9c-211">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-212">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-212">ACR</span></span>
* <span data-ttu-id="b0c9c-213">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-213">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-214">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-214">ACS</span></span>
* <span data-ttu-id="b0c9c-215">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-215">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="b0c9c-216">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-216">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="b0c9c-217">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-217">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="b0c9c-218">AMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-218">AMS</span></span>
* <span data-ttu-id="b0c9c-219">[破壊的変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-219">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="b0c9c-220">[破壊的変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-220">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-221">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-221">Appservice</span></span>
* <span data-ttu-id="b0c9c-222">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-222">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="b0c9c-223">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-223">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="b0c9c-224">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-224">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-225">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-225">Container</span></span>
* <span data-ttu-id="b0c9c-226">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-226">Added `container start` command</span></span>
* <span data-ttu-id="b0c9c-227">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-227">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="b0c9c-228">EventGrid</span><span class="sxs-lookup"><span data-stu-id="b0c9c-228">EventGrid</span></span>
* <span data-ttu-id="b0c9c-229">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-229">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="b0c9c-230">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-230">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="b0c9c-231">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-231">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="b0c9c-232">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-232">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="b0c9c-233">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-233">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b0c9c-234">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b0c9c-234">HDInsight</span></span>
* <span data-ttu-id="b0c9c-235">[破壊的変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-235">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="b0c9c-236">[破壊的変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-236">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="b0c9c-237">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-237">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="b0c9c-238">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-238">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="b0c9c-239">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-239">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="b0c9c-240">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-240">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="b0c9c-241">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-241">IoT</span></span>
* <span data-ttu-id="b0c9c-242">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-242">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="b0c9c-243">Kusto</span><span class="sxs-lookup"><span data-stu-id="b0c9c-243">Kusto</span></span>
* <span data-ttu-id="b0c9c-244">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-244">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-245">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-245">Monitor</span></span>
* <span data-ttu-id="b0c9c-246">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-246">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="b0c9c-247">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-247">Profile</span></span>
* <span data-ttu-id="b0c9c-248">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-248">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-249">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-249">Network</span></span>
* <span data-ttu-id="b0c9c-250">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-250">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="b0c9c-251">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-251">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-252">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-252">Resource</span></span>
* <span data-ttu-id="b0c9c-253">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-253">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="b0c9c-254">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-254">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="b0c9c-255">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="b0c9c-255">SQL Virtual Machine</span></span>
* <span data-ttu-id="b0c9c-256">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-256">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-257">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-257">Storage</span></span>
* <span data-ttu-id="b0c9c-258">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-258">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="b0c9c-259">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-259">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-260">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-260">VM</span></span>
* <span data-ttu-id="b0c9c-261">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-261">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="b0c9c-262">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-262">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="b0c9c-263">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-263">January 15, 2019</span></span>

<span data-ttu-id="b0c9c-264">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="b0c9c-264">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-265">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-265">ACR</span></span>
* <span data-ttu-id="b0c9c-266">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-266">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="b0c9c-267">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-267">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="b0c9c-268">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-268">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="b0c9c-269">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-269">ACS</span></span>
* <span data-ttu-id="b0c9c-270">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-270">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-271">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-271">Appservice</span></span>
* <span data-ttu-id="b0c9c-272">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-272">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="b0c9c-273">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-273">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="b0c9c-274">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-274">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="b0c9c-275">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-275">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="b0c9c-276">Botservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-276">Botservice</span></span>
* <span data-ttu-id="b0c9c-277">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-277">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="b0c9c-278">構成</span><span class="sxs-lookup"><span data-stu-id="b0c9c-278">Configure</span></span>
* <span data-ttu-id="b0c9c-279">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-279">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0c9c-280">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0c9c-280">CosmosDB</span></span>
* <span data-ttu-id="b0c9c-281">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-281">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b0c9c-282">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b0c9c-282">HDInsight</span></span>
* <span data-ttu-id="b0c9c-283">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-283">Added commands for managing applications</span></span>
* <span data-ttu-id="b0c9c-284">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-284">Added commands for managing script actions</span></span>
* <span data-ttu-id="b0c9c-285">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-285">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="b0c9c-286">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-286">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="b0c9c-287">[破壊的変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-287">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-288">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-288">Network</span></span>
* <span data-ttu-id="b0c9c-289">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-289">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="b0c9c-290">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-290">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="b0c9c-291">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-291">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="b0c9c-292">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-292">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-293">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-293">Role</span></span>
* <span data-ttu-id="b0c9c-294">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-294">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="b0c9c-295">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="b0c9c-295">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="b0c9c-296">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-296">Security</span></span>
* <span data-ttu-id="b0c9c-297">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-297">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-298">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-298">Storage</span></span>
* <span data-ttu-id="b0c9c-299">[破壊的変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-299">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="b0c9c-300">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b0c9c-300">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="b0c9c-301">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-301">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="b0c9c-302">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-302">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="b0c9c-303">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-303">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-304">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-304">VM</span></span>
* <span data-ttu-id="b0c9c-305">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-305">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="b0c9c-306">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-306">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="b0c9c-307">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-307">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="b0c9c-308">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-308">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="b0c9c-309">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-309">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="b0c9c-310">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-310">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="b0c9c-311">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-311">December 20, 2018</span></span>

<span data-ttu-id="b0c9c-312">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="b0c9c-312">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="b0c9c-313">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-313">Appservice</span></span>
* <span data-ttu-id="b0c9c-314">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-314">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="b0c9c-315">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-315">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="b0c9c-316">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-316">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="b0c9c-317">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="b0c9c-317">IoTCentral</span></span>
* <span data-ttu-id="b0c9c-318">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-318">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-319">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-319">Role</span></span>
* <span data-ttu-id="b0c9c-320">[破壊的変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-320">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-321">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-321">SQL</span></span>
* <span data-ttu-id="b0c9c-322">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-322">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-323">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-323">VM</span></span>
* <span data-ttu-id="b0c9c-324">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-324">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="b0c9c-325">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-325">December 18, 2018</span></span>

<span data-ttu-id="b0c9c-326">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="b0c9c-326">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="b0c9c-327">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-327">ACR</span></span>
* <span data-ttu-id="b0c9c-328">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-328">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="b0c9c-329">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-329">Condensed the table layout for task list</span></span>
* <span data-ttu-id="b0c9c-330">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-330">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-331">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-331">ACS</span></span>
* <span data-ttu-id="b0c9c-332">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-332">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="b0c9c-333">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-333">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="b0c9c-334">[非推奨] `az acs` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-334">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="b0c9c-335">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="b0c9c-335">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="b0c9c-336">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-336">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="b0c9c-337">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-337">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-338">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-338">Appservice</span></span>
* <span data-ttu-id="b0c9c-339">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-339">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="b0c9c-340">Botservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-340">Botservice</span></span>
* <span data-ttu-id="b0c9c-341">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-341">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="b0c9c-342">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-342">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="b0c9c-343">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-343">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="b0c9c-344">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-344">Reduced Kudu network calls</span></span>
* <span data-ttu-id="b0c9c-345">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-345">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="b0c9c-346">消費</span><span class="sxs-lookup"><span data-stu-id="b0c9c-346">Consumption</span></span>
* <span data-ttu-id="b0c9c-347">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-347">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0c9c-348">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0c9c-348">CosmosDB</span></span>
* <span data-ttu-id="b0c9c-349">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-349">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="b0c9c-350">マップ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-350">Maps</span></span>
* <span data-ttu-id="b0c9c-351">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-351">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-352">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-352">Network</span></span>
* <span data-ttu-id="b0c9c-353">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-353">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="b0c9c-354">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-354">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-355">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-355">Resource</span></span>
* <span data-ttu-id="b0c9c-356">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-356">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="b0c9c-357">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-357">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-358">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-358">Storage</span></span>
*  <span data-ttu-id="b0c9c-359">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-359">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-360">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-360">VM</span></span>
* <span data-ttu-id="b0c9c-361">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-361">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="b0c9c-362">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-362">December 4, 2018</span></span>

<span data-ttu-id="b0c9c-363">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="b0c9c-363">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="b0c9c-364">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-364">Core</span></span>
* <span data-ttu-id="b0c9c-365">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-365">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="b0c9c-366">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-366">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-367">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-367">Appservice</span></span>
* <span data-ttu-id="b0c9c-368">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-368">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="b0c9c-369">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-369">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-370">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-370">Network</span></span>
* <span data-ttu-id="b0c9c-371">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-371">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-372">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-372">Role</span></span>
* <span data-ttu-id="b0c9c-373">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-373">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="b0c9c-374">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-374">VM</span></span>
* <span data-ttu-id="b0c9c-375">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-375">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="b0c9c-376">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-376">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="b0c9c-377">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-377">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="b0c9c-378">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-378">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="b0c9c-379">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-379">November 20, 2018</span></span>

<span data-ttu-id="b0c9c-380">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="b0c9c-380">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="b0c9c-381">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-381">Core</span></span>
* <span data-ttu-id="b0c9c-382">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-382">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-383">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-383">ACR</span></span>
* <span data-ttu-id="b0c9c-384">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-384">Added context token to task step</span></span>
* <span data-ttu-id="b0c9c-385">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-385">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="b0c9c-386">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-386">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-387">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-387">Appservice</span></span>
* <span data-ttu-id="b0c9c-388">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-388">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="b0c9c-389">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-389">Updated the default `node_version`.</span></span> <span data-ttu-id="b0c9c-390">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-390">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="b0c9c-391">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-391">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="b0c9c-392">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-392">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="b0c9c-393">IotCentral</span><span class="sxs-lookup"><span data-stu-id="b0c9c-393">IotCentral</span></span>
* <span data-ttu-id="b0c9c-394">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-394">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0c9c-395">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-395">KeyVault</span></span>
* <span data-ttu-id="b0c9c-396">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-396">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-397">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-397">Network</span></span>
* <span data-ttu-id="b0c9c-398">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-398">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="b0c9c-399">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-399">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="b0c9c-400">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-400">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="b0c9c-401">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-401">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0c9c-402">Rdbms</span><span class="sxs-lookup"><span data-stu-id="b0c9c-402">Rdbms</span></span>
* <span data-ttu-id="b0c9c-403">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-403">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="b0c9c-404">Rbac</span><span class="sxs-lookup"><span data-stu-id="b0c9c-404">Rbac</span></span>
* <span data-ttu-id="b0c9c-405">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-405">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="b0c9c-406">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-406">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="b0c9c-407">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-407">Storage</span></span>
* <span data-ttu-id="b0c9c-408">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-408">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="b0c9c-409">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-409">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="b0c9c-410">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-410">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="b0c9c-411">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-411">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-412">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-412">VM</span></span>
* <span data-ttu-id="b0c9c-413">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-413">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="b0c9c-414">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-414">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="b0c9c-415">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-415">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="b0c9c-416">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-416">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="b0c9c-417">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-417">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="b0c9c-418">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-418">Added `snapshot wait` command</span></span>
* <span data-ttu-id="b0c9c-419">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-419">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="b0c9c-420">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-420">November 6, 2018</span></span>

<span data-ttu-id="b0c9c-421">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="b0c9c-421">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-422">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-422">Core</span></span>
* <span data-ttu-id="b0c9c-423">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-423">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-424">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-424">ACR</span></span>
* <span data-ttu-id="b0c9c-425">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-425">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="b0c9c-426">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-426">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-427">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-427">ACS</span></span>
* <span data-ttu-id="b0c9c-428">[破壊的変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-428">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="b0c9c-429">Advisor</span><span class="sxs-lookup"><span data-stu-id="b0c9c-429">Advisor</span></span>
* <span data-ttu-id="b0c9c-430">GA リリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-430">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="b0c9c-431">AMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-431">AMS</span></span>
* <span data-ttu-id="b0c9c-432">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-432">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="b0c9c-433">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-433">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="b0c9c-434">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-434">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="b0c9c-435">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-435">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="b0c9c-436">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-436">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="b0c9c-437">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-437">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="b0c9c-438">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-438">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="b0c9c-439">[破壊的変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-439">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="b0c9c-440">[破壊的変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-440">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="b0c9c-441">[破壊的変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-441">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="b0c9c-442">[破壊的変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-442">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="b0c9c-443">[破壊的変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-443">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="b0c9c-444">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-444">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="b0c9c-445">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-445">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="b0c9c-446">[破壊的変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-446">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="b0c9c-447">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-447">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="b0c9c-448">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-448">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-449">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-449">AppService</span></span>
* <span data-ttu-id="b0c9c-450">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-450">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="b0c9c-451">構成</span><span class="sxs-lookup"><span data-stu-id="b0c9c-451">Configure</span></span>
* <span data-ttu-id="b0c9c-452">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-452">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-453">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-453">Container</span></span>
* <span data-ttu-id="b0c9c-454">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-454">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="b0c9c-455">EventHub</span><span class="sxs-lookup"><span data-stu-id="b0c9c-455">EventHub</span></span>
* <span data-ttu-id="b0c9c-456">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-456">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-457">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-457">Interactive</span></span>
* <span data-ttu-id="b0c9c-458">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="b0c9c-458">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-459">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-459">Monitor</span></span>
* <span data-ttu-id="b0c9c-460">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-460">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-461">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-461">Network</span></span>
* <span data-ttu-id="b0c9c-462">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-462">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="b0c9c-463">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-463">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="b0c9c-464">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-464">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="b0c9c-465">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-465">Profile</span></span>
* <span data-ttu-id="b0c9c-466">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-466">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0c9c-467">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-467">RDBMS</span></span>
* <span data-ttu-id="b0c9c-468">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-468">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-469">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-469">Resource</span></span>
* <span data-ttu-id="b0c9c-470">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-470">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-471">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-471">Role</span></span>
* <span data-ttu-id="b0c9c-472">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-472">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="b0c9c-473">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-473">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="b0c9c-474">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-474">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-475">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-475">Storage</span></span>
* <span data-ttu-id="b0c9c-476">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-476">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-477">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-477">VM</span></span>
* <span data-ttu-id="b0c9c-478">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-478">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="b0c9c-479">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-479">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="b0c9c-480">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-480">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="b0c9c-481">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-481">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="b0c9c-482">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="b0c9c-482">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="b0c9c-483">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-483">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="b0c9c-484">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-484">October 23, 2018</span></span>

<span data-ttu-id="b0c9c-485">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="b0c9c-485">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-486">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-486">Core</span></span>
* <span data-ttu-id="b0c9c-487">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-487">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="b0c9c-488">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-488">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-489">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-489">ACR</span></span>
* <span data-ttu-id="b0c9c-490">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-490">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="b0c9c-491">CDN</span><span class="sxs-lookup"><span data-stu-id="b0c9c-491">CDN</span></span>
* <span data-ttu-id="b0c9c-492">[破壊的変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-492">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="b0c9c-493">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-493">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-494">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-494">Container</span></span>
* <span data-ttu-id="b0c9c-495">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-495">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="b0c9c-496">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-496">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="b0c9c-497">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-497">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="b0c9c-498">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-498">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="b0c9c-499">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-499">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="b0c9c-500">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-500">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="b0c9c-501">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-501">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0c9c-502">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0c9c-502">CosmosDB</span></span>
* <span data-ttu-id="b0c9c-503">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-503">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-504">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-504">Interactive</span></span>
* <span data-ttu-id="b0c9c-505">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-505">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="b0c9c-506">IoT Central</span><span class="sxs-lookup"><span data-stu-id="b0c9c-506">IoT Central</span></span>
* <span data-ttu-id="b0c9c-507">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-507">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="b0c9c-508">[破壊的変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-508">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-509">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-509">Monitor</span></span>
* <span data-ttu-id="b0c9c-510">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="b0c9c-510">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="b0c9c-511">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-511">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="b0c9c-512">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-512">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="b0c9c-513">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-513">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="b0c9c-514">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-514">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="b0c9c-515">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-515">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="b0c9c-516">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="b0c9c-516">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="b0c9c-517">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-517">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="b0c9c-518">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-518">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="b0c9c-519">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-519">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-520">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-520">Network</span></span>
* <span data-ttu-id="b0c9c-521">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-521">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="b0c9c-522">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-522">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="b0c9c-523">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b0c9c-523">ServiceBus</span></span>
* <span data-ttu-id="b0c9c-524">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-524">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-525">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-525">SQL</span></span>
* <span data-ttu-id="b0c9c-526">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-526">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-527">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-527">Storage</span></span>
* <span data-ttu-id="b0c9c-528">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-528">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="b0c9c-529">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-529">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-530">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-530">VM</span></span>
* <span data-ttu-id="b0c9c-531">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-531">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="b0c9c-532">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-532">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="b0c9c-533">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-533">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="b0c9c-534">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-534">October 16, 2018</span></span>

<span data-ttu-id="b0c9c-535">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="b0c9c-535">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-536">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-536">VM</span></span>
* <span data-ttu-id="b0c9c-537">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-537">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="b0c9c-538">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-538">October 9, 2018</span></span>

<span data-ttu-id="b0c9c-539">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="b0c9c-539">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-540">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-540">Core</span></span>
* <span data-ttu-id="b0c9c-541">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-541">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-542">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-542">ACR</span></span>
* <span data-ttu-id="b0c9c-543">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-543">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-544">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-544">ACS</span></span>
* <span data-ttu-id="b0c9c-545">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="b0c9c-545">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="b0c9c-546">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-546">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="b0c9c-547">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-547">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="b0c9c-548">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-548">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-549">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-549">Container</span></span>
* <span data-ttu-id="b0c9c-550">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-550">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="b0c9c-551">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-551">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="b0c9c-552">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-552">Event Hub</span></span>
* <span data-ttu-id="b0c9c-553">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-553">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="b0c9c-554">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-554">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="b0c9c-555">Extensions</span><span class="sxs-lookup"><span data-stu-id="b0c9c-555">Extensions</span></span>
* <span data-ttu-id="b0c9c-556">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-556">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b0c9c-557">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b0c9c-557">HDInsight</span></span>
* <span data-ttu-id="b0c9c-558">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-558">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="b0c9c-559">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-559">IoT</span></span>
* <span data-ttu-id="b0c9c-560">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-560">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0c9c-561">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-561">KeyVault</span></span>
* <span data-ttu-id="b0c9c-562">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-562">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-563">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-563">Network</span></span>
* <span data-ttu-id="b0c9c-564">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-564">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="b0c9c-565">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="b0c9c-565">See #6052</span></span>
* <span data-ttu-id="b0c9c-566">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-566">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="b0c9c-567">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-567">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="b0c9c-568">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-568">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="b0c9c-569">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-569">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="b0c9c-570">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-570">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="b0c9c-571">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-571">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-572">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-572">Role</span></span>
* <span data-ttu-id="b0c9c-573">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-573">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="b0c9c-574">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-574">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="b0c9c-575">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-575">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="b0c9c-576">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-576">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="b0c9c-577">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b0c9c-577">Service Bus</span></span>
* <span data-ttu-id="b0c9c-578">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-578">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-579">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-579">VM</span></span>
* <span data-ttu-id="b0c9c-580">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-580">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="b0c9c-581">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-581">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="b0c9c-582">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-582">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="b0c9c-583">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-583">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="b0c9c-584">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-584">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="b0c9c-585">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-585">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="b0c9c-586">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-586">September 21, 2018</span></span>

<span data-ttu-id="b0c9c-587">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="b0c9c-587">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-588">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-588">ACR</span></span>
* <span data-ttu-id="b0c9c-589">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-589">Added ACR Task commands</span></span>
* <span data-ttu-id="b0c9c-590">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-590">Added quick run command</span></span>
* <span data-ttu-id="b0c9c-591">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-591">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="b0c9c-592">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-592">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="b0c9c-593">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-593">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="b0c9c-594">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-594">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-595">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-595">ACS</span></span>
* <span data-ttu-id="b0c9c-596">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-596">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="b0c9c-597">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-597">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-598">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-598">AppService</span></span>

* <span data-ttu-id="b0c9c-599">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-599">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="b0c9c-600">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-600">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="b0c9c-601">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-601">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="b0c9c-602">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-602">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-603">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-603">Batch</span></span>
* <span data-ttu-id="b0c9c-604">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-604">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="b0c9c-605">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-605">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="b0c9c-606">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-606">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="b0c9c-607">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-607">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b0c9c-608">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b0c9c-608">Batch AI</span></span> 
* <span data-ttu-id="b0c9c-609">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-609">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b0c9c-610">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b0c9c-610">Cognitive Services</span></span>
* <span data-ttu-id="b0c9c-611">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-611">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="b0c9c-612">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-612">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="b0c9c-613">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-613">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="b0c9c-614">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-614">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="b0c9c-615">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-615">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="b0c9c-616">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-616">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-617">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-617">Container</span></span>
* <span data-ttu-id="b0c9c-618">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-618">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="b0c9c-619">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-619">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="b0c9c-620">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-620">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="b0c9c-621">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-621">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="b0c9c-622">DataLake</span><span class="sxs-lookup"><span data-stu-id="b0c9c-622">Datalake</span></span>
* <span data-ttu-id="b0c9c-623">仮想ネットワーク ルール用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-623">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="b0c9c-624">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-624">Interactive Shell</span></span>
* <span data-ttu-id="b0c9c-625">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-625">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="b0c9c-626">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-626">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="b0c9c-627">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-627">IoT</span></span>
* <span data-ttu-id="b0c9c-628">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-628">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="b0c9c-629">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-629">Key Vault</span></span>
* <span data-ttu-id="b0c9c-630">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-630">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-631">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-631">Network</span></span>
* <span data-ttu-id="b0c9c-632">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-632">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="b0c9c-633">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-633">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="b0c9c-634">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-634">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="b0c9c-635">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-635">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="b0c9c-636">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-636">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="b0c9c-637">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-637">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="b0c9c-638">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-638">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="b0c9c-639">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-639">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="b0c9c-640">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-640">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="b0c9c-641">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-641">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="b0c9c-642">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-642">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="b0c9c-643">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-643">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="b0c9c-644">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-644">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="b0c9c-645">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-645">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="b0c9c-646">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-646">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="b0c9c-647">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-647">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="b0c9c-648">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-648">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="b0c9c-649">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-649">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0c9c-650">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-650">RDBMS</span></span>
* <span data-ttu-id="b0c9c-651">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-651">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="b0c9c-652">予約</span><span class="sxs-lookup"><span data-stu-id="b0c9c-652">Reservation</span></span>
* <span data-ttu-id="b0c9c-653">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-653">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="b0c9c-654">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-654">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="b0c9c-655">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="b0c9c-655">Manage App</span></span>
* <span data-ttu-id="b0c9c-656">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-656">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="b0c9c-657">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-657">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-658">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-658">Role</span></span>
* <span data-ttu-id="b0c9c-659">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-659">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="b0c9c-660">SignalR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-660">SignalR</span></span>
* <span data-ttu-id="b0c9c-661">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-661">First release</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-662">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-662">Storage</span></span>
* <span data-ttu-id="b0c9c-663">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-663">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="b0c9c-664">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-664">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-665">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-665">VM</span></span>
* <span data-ttu-id="b0c9c-666">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-666">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="b0c9c-667">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-667">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="b0c9c-668">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-668">August 28, 2018</span></span>

<span data-ttu-id="b0c9c-669">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="b0c9c-669">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-670">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-670">Core</span></span>

* <span data-ttu-id="b0c9c-671">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-671">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="b0c9c-672">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-672">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-673">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-673">ACR</span></span>

* <span data-ttu-id="b0c9c-674">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-674">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="b0c9c-675">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-675">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-676">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-676">ACS</span></span>

* <span data-ttu-id="b0c9c-677">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-677">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="b0c9c-678">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-678">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-679">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-679">AppService</span></span>

* <span data-ttu-id="b0c9c-680">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-680">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="b0c9c-681">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-681">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="b0c9c-682">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-682">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="b0c9c-683">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-683">Backup</span></span>

* <span data-ttu-id="b0c9c-684">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-684">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="b0c9c-685">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="b0c9c-685">Bot Service</span></span>

* <span data-ttu-id="b0c9c-686">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-686">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b0c9c-687">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b0c9c-687">Cognitive Services</span></span>

* <span data-ttu-id="b0c9c-688">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-688">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="b0c9c-689">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-689">IoT</span></span>

* <span data-ttu-id="b0c9c-690">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-690">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-691">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-691">Monitor</span></span>

* <span data-ttu-id="b0c9c-692">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-692">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="b0c9c-693">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-693">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-694">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-694">Network</span></span>

* <span data-ttu-id="b0c9c-695">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-695">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-696">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-696">Resource</span></span>

* <span data-ttu-id="b0c9c-697">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-697">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-698">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-698">Storage</span></span>

* <span data-ttu-id="b0c9c-699">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-699">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-700">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-700">VM</span></span>

* <span data-ttu-id="b0c9c-701">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-701">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="b0c9c-702">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-702">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="b0c9c-703">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-703">Auguest 14, 2018</span></span>

<span data-ttu-id="b0c9c-704">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="b0c9c-704">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-705">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-705">Core</span></span>

* <span data-ttu-id="b0c9c-706">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-706">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="b0c9c-707">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-707">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="b0c9c-708">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-708">Telemetry</span></span>

* <span data-ttu-id="b0c9c-709">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-709">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-710">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-710">ACR</span></span>

* <span data-ttu-id="b0c9c-711">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-711">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="b0c9c-712">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-712">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-713">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-713">ACS</span></span>

* <span data-ttu-id="b0c9c-714">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-714">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="b0c9c-715">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-715">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="b0c9c-716">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-716">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="b0c9c-717">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-717">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="b0c9c-718">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-718">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="b0c9c-719">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-719">AppService</span></span>

* <span data-ttu-id="b0c9c-720">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-720">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="b0c9c-721">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-721">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="b0c9c-722">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b0c9c-722">BatchAI</span></span>

* <span data-ttu-id="b0c9c-723">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-723">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="b0c9c-724">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-724">Container</span></span>

* <span data-ttu-id="b0c9c-725">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-725">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="b0c9c-726">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-726">IoT</span></span>

* <span data-ttu-id="b0c9c-727">[破壊的変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-727">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="b0c9c-728">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-728">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="b0c9c-729">Iot Central</span><span class="sxs-lookup"><span data-stu-id="b0c9c-729">Iot Central</span></span>

* <span data-ttu-id="b0c9c-730">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-730">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0c9c-731">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-731">KeyVault</span></span>


* <span data-ttu-id="b0c9c-732">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-732">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="b0c9c-733">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-733">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="b0c9c-734">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-734">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="b0c9c-735">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-735">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="b0c9c-736">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-736">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="b0c9c-737">リレー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-737">Relay</span></span>

* <span data-ttu-id="b0c9c-738">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-738">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-739">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-739">Sql</span></span>

* <span data-ttu-id="b0c9c-740">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-740">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-741">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-741">Storage</span></span>

* <span data-ttu-id="b0c9c-742">[破壊的変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-742">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="b0c9c-743">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-743">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="b0c9c-744">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-744">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="b0c9c-745">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-745">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="b0c9c-746">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-746">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-747">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-747">VM</span></span>

* <span data-ttu-id="b0c9c-748">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-748">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="b0c9c-749">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-749">July 31, 2018</span></span>

<span data-ttu-id="b0c9c-750">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="b0c9c-750">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-751">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-751">ACR</span></span>

* <span data-ttu-id="b0c9c-752">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-752">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="b0c9c-753">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-753">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-754">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-754">ACS</span></span>

* <span data-ttu-id="b0c9c-755">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-755">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-756">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-756">Batch</span></span>

* <span data-ttu-id="b0c9c-757">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-757">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-758">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-758">Container</span></span>

* <span data-ttu-id="b0c9c-759">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-759">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-760">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-760">Network</span></span>

* <span data-ttu-id="b0c9c-761">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-761">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="b0c9c-762">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-762">Resource</span></span>

* <span data-ttu-id="b0c9c-763">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-763">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="b0c9c-764">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-764">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-765">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-765">Role</span></span>

* <span data-ttu-id="b0c9c-766">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-766">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="b0c9c-767">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-767">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="b0c9c-768">Search</span><span class="sxs-lookup"><span data-stu-id="b0c9c-768">Search</span></span>

* <span data-ttu-id="b0c9c-769">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-769">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="b0c9c-770">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b0c9c-770">Service Bus</span></span>

* <span data-ttu-id="b0c9c-771">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-771">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="b0c9c-772">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-772">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="b0c9c-773">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-773">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="b0c9c-774">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-774">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-775">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-775">Storage</span></span>

* <span data-ttu-id="b0c9c-776">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-776">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="b0c9c-777">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-777">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-778">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-778">VM</span></span>

* <span data-ttu-id="b0c9c-779">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-779">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="b0c9c-780">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-780">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="b0c9c-781">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-781">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="b0c9c-782">[破壊的変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-782">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="b0c9c-783">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-783">July 18, 2018</span></span>

<span data-ttu-id="b0c9c-784">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="b0c9c-784">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-785">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-785">Core</span></span>

* <span data-ttu-id="b0c9c-786">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-786">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="b0c9c-787">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-787">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="b0c9c-788">[破壊的変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-788">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-789">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-789">ACR</span></span>

* <span data-ttu-id="b0c9c-790">[破壊的変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-790">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="b0c9c-791">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-791">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="b0c9c-792">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-792">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="b0c9c-793">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-793">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-794">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-794">ACS</span></span>

* <span data-ttu-id="b0c9c-795">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-795">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-796">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-796">AppService</span></span>

* <span data-ttu-id="b0c9c-797">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-797">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-798">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-798">Batch</span></span>

* <span data-ttu-id="b0c9c-799">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-799">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="b0c9c-800">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-800">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b0c9c-801">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b0c9c-801">Batch AI</span></span>

* <span data-ttu-id="b0c9c-802">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-802">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-803">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-803">Container</span></span>

* <span data-ttu-id="b0c9c-804">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-804">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="b0c9c-805">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-805">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-806">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-806">Network</span></span>

* <span data-ttu-id="b0c9c-807">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-807">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="b0c9c-808">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-808">Added `network nic wait`</span></span>
* <span data-ttu-id="b0c9c-809">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-809">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="b0c9c-810">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-810">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="b0c9c-811">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-811">Resource</span></span>

* <span data-ttu-id="b0c9c-812">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-812">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="b0c9c-813">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-813">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="b0c9c-814">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-814">Added `deployment wait` command</span></span>
* <span data-ttu-id="b0c9c-815">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-815">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-816">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-816">SQL</span></span>

* <span data-ttu-id="b0c9c-817">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-817">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="b0c9c-818">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-818">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="b0c9c-819">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-819">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-820">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-820">Storage</span></span>

* <span data-ttu-id="b0c9c-821">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-821">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-822">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-822">VM</span></span>

* <span data-ttu-id="b0c9c-823">[破壊的変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-823">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="b0c9c-824">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-824">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="b0c9c-825">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-825">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="b0c9c-826">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-826">July 3, 2018</span></span>

<span data-ttu-id="b0c9c-827">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="b0c9c-827">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="b0c9c-828">AKS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-828">AKS</span></span>

* <span data-ttu-id="b0c9c-829">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-829">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="b0c9c-830">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-830">July 3, 2018</span></span>

<span data-ttu-id="b0c9c-831">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="b0c9c-831">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-832">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-832">Core</span></span>

* <span data-ttu-id="b0c9c-833">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-833">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-834">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-834">ACR</span></span>

* <span data-ttu-id="b0c9c-835">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-835">Added polling build status</span></span>
* <span data-ttu-id="b0c9c-836">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-836">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="b0c9c-837">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-837">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-838">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-838">ACS</span></span>

* <span data-ttu-id="b0c9c-839">[破壊的変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-839">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="b0c9c-840">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-840">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="b0c9c-841">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-841">Updated options for `aks browse` command.</span></span> <span data-ttu-id="b0c9c-842">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-842">Added `--listen-port` support</span></span>
* <span data-ttu-id="b0c9c-843">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-843">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="b0c9c-844">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-844">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="b0c9c-845">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-845">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-846">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-846">AppService</span></span>

* <span data-ttu-id="b0c9c-847">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-847">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="b0c9c-848">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-848">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="b0c9c-849">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-849">Backup</span></span>

* <span data-ttu-id="b0c9c-850">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-850">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="b0c9c-851">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b0c9c-851">BatchAI</span></span>

* <span data-ttu-id="b0c9c-852">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-852">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="b0c9c-853">クラウド</span><span class="sxs-lookup"><span data-stu-id="b0c9c-853">Cloud</span></span>

* <span data-ttu-id="b0c9c-854">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-854">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-855">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-855">Container</span></span>

* <span data-ttu-id="b0c9c-856">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-856">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="b0c9c-857">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-857">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="b0c9c-858">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-858">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="b0c9c-859">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0c9c-859">Extension</span></span>

* <span data-ttu-id="b0c9c-860">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-860">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-861">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-861">Network</span></span>

* <span data-ttu-id="b0c9c-862">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-862">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0c9c-863">Rdbms</span><span class="sxs-lookup"><span data-stu-id="b0c9c-863">Rdbms</span></span>

* <span data-ttu-id="b0c9c-864">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-864">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-865">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-865">Resource</span></span>

* <span data-ttu-id="b0c9c-866">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-866">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-867">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-867">VM</span></span>

* <span data-ttu-id="b0c9c-868">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-868">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="b0c9c-869">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-869">June 25, 2018</span></span>

<span data-ttu-id="b0c9c-870">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="b0c9c-870">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="b0c9c-871">CLI</span><span class="sxs-lookup"><span data-stu-id="b0c9c-871">CLI</span></span>

* <span data-ttu-id="b0c9c-872">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-872">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="b0c9c-873">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-873">June 19, 2018</span></span>

<span data-ttu-id="b0c9c-874">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="b0c9c-874">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-875">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-875">Core</span></span>

* <span data-ttu-id="b0c9c-876">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-876">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-877">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-877">ACR</span></span>

* <span data-ttu-id="b0c9c-878">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-878">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="b0c9c-879">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-879">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-880">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-880">ACS</span></span>

* <span data-ttu-id="b0c9c-881">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-881">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="b0c9c-882">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-882">Added `--update` support</span></span>
* <span data-ttu-id="b0c9c-883">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-883">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="b0c9c-884">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-884">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="b0c9c-885">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-885">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="b0c9c-886">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-886">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="b0c9c-887">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-887">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="b0c9c-888">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-888">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-889">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-889">AppService</span></span>

* <span data-ttu-id="b0c9c-890">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-890">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="b0c9c-891">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-891">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-892">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-892">Batch</span></span>

* <span data-ttu-id="b0c9c-893">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-893">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b0c9c-894">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b0c9c-894">Batch AI</span></span>

* <span data-ttu-id="b0c9c-895">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-895">Added support for workspaces.</span></span> <span data-ttu-id="b0c9c-896">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="b0c9c-896">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="b0c9c-897">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-897">Added support for experiments.</span></span> <span data-ttu-id="b0c9c-898">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="b0c9c-898">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="b0c9c-899">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-899">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="b0c9c-900">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-900">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="b0c9c-901">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-901">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="b0c9c-902">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-902">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="b0c9c-903">[破壊的変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="b0c9c-903">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="b0c9c-904">[破壊的変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="b0c9c-904">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="b0c9c-905">[破壊的変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-905">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="b0c9c-906">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-906">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="b0c9c-907">[破壊的変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-907">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="b0c9c-908">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-908">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="b0c9c-909">[破壊的変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-909">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="b0c9c-910">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-910">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="b0c9c-911">[破壊的変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-911">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="b0c9c-912">[破壊的変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-912">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="b0c9c-913">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-913">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="b0c9c-914">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-914">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="b0c9c-915">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-915">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="b0c9c-916">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-916">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="b0c9c-917">マップ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-917">Maps</span></span>

* <span data-ttu-id="b0c9c-918">[破壊的変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-918">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-919">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-919">Network</span></span>

* <span data-ttu-id="b0c9c-920">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-920">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="b0c9c-921">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-921">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="b0c9c-922">#6502</span><span class="sxs-lookup"><span data-stu-id="b0c9c-922">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="b0c9c-923">Reservations</span><span class="sxs-lookup"><span data-stu-id="b0c9c-923">Reservations</span></span>

* <span data-ttu-id="b0c9c-924">[破壊的変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-924">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="b0c9c-925">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-925">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="b0c9c-926">[破壊的変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-926">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="b0c9c-927">[破壊的変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-927">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="b0c9c-928">[破壊的変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-928">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="b0c9c-929">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-929">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-930">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-930">Role</span></span>

* <span data-ttu-id="b0c9c-931">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-931">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-932">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-932">SQL</span></span>

* <span data-ttu-id="b0c9c-933">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-933">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-934">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-934">Storage</span></span>

* <span data-ttu-id="b0c9c-935">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-935">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-936">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-936">VM</span></span>

* <span data-ttu-id="b0c9c-937">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-937">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="b0c9c-938">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-938">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="b0c9c-939">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-939">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="b0c9c-940">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-940">June 13, 2018</span></span>

<span data-ttu-id="b0c9c-941">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="b0c9c-941">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-942">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-942">Core</span></span>

* <span data-ttu-id="b0c9c-943">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-943">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="b0c9c-944">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-944">June 13, 2018</span></span>

<span data-ttu-id="b0c9c-945">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="b0c9c-945">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="b0c9c-946">AKS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-946">AKS</span></span>

* <span data-ttu-id="b0c9c-947">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-947">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="b0c9c-948">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-948">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="b0c9c-949">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-949">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="b0c9c-950">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-950">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="b0c9c-951">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-951">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-952">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-952">AppService</span></span>

* <span data-ttu-id="b0c9c-953">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-953">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="b0c9c-954">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-954">June 5, 2018</span></span>

<span data-ttu-id="b0c9c-955">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="b0c9c-955">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-956">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-956">Interactive</span></span>

* <span data-ttu-id="b0c9c-957">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-957">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="b0c9c-958">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-958">June 5, 2018</span></span>

<span data-ttu-id="b0c9c-959">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="b0c9c-959">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-960">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-960">Core</span></span>

* <span data-ttu-id="b0c9c-961">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-961">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="b0c9c-962">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-962">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-963">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-963">ACR</span></span>

* <span data-ttu-id="b0c9c-964">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-964">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="b0c9c-965">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-965">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="b0c9c-966">AKS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-966">AKS</span></span>

* <span data-ttu-id="b0c9c-967">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-967">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-968">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-968">Batch</span></span>

* <span data-ttu-id="b0c9c-969">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-969">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="b0c9c-970">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-970">IOT</span></span>

* <span data-ttu-id="b0c9c-971">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-971">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-972">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-972">Network</span></span>

* <span data-ttu-id="b0c9c-973">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-973">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="b0c9c-974">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="b0c9c-974">Policy Insights</span></span>

* <span data-ttu-id="b0c9c-975">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-975">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="b0c9c-976">ARM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-976">ARM</span></span>

* <span data-ttu-id="b0c9c-977">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-977">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-978">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-978">SQL</span></span>

* <span data-ttu-id="b0c9c-979">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-979">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="b0c9c-980">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-980">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="b0c9c-981">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-981">Storage</span></span>

* <span data-ttu-id="b0c9c-982">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-982">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-983">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-983">VM</span></span>

* <span data-ttu-id="b0c9c-984">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-984">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="b0c9c-985">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-985">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="b0c9c-986">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-986">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="b0c9c-987">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-987">May 22, 2018</span></span>

<span data-ttu-id="b0c9c-988">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="b0c9c-988">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-989">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-989">Core</span></span>

* <span data-ttu-id="b0c9c-990">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-990">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-991">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-991">ACS</span></span>

* <span data-ttu-id="b0c9c-992">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-992">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="b0c9c-993">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-993">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-994">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-994">AppService</span></span>

* <span data-ttu-id="b0c9c-995">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-995">Improved generic update commands</span></span>
* <span data-ttu-id="b0c9c-996">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-996">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-997">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-997">Container</span></span>

* <span data-ttu-id="b0c9c-998">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-998">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="b0c9c-999">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-999">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="b0c9c-1000">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1000">Extension</span></span>

* <span data-ttu-id="b0c9c-1001">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1001">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-1002">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1002">Interactive</span></span>

* <span data-ttu-id="b0c9c-1003">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1003">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="b0c9c-1004">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1004">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0c9c-1005">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1005">KeyVault</span></span>

* <span data-ttu-id="b0c9c-1006">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1006">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1007">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1007">Network</span></span>

* <span data-ttu-id="b0c9c-1008">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1008">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="b0c9c-1009">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1009">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-1010">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1010">SQL</span></span>

* <span data-ttu-id="b0c9c-1011">[破壊的変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1011">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="b0c9c-1012">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1012">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="b0c9c-1013">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1013">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="b0c9c-1014">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1014">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="b0c9c-1015">[破壊的変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1015">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="b0c9c-1016">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1016">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="b0c9c-1017">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1017">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="b0c9c-1018">`edition`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1018">`edition`.</span></span> <span data-ttu-id="b0c9c-1019">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1019">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="b0c9c-1020">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1020">`elasticPoolName`.</span></span> <span data-ttu-id="b0c9c-1021">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1021">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="b0c9c-1022">[破壊的変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1022">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="b0c9c-1023">`edition`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1023">`edition`.</span></span> <span data-ttu-id="b0c9c-1024">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1024">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="b0c9c-1025">`dtu`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1025">`dtu`.</span></span> <span data-ttu-id="b0c9c-1026">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1026">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="b0c9c-1027">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1027">`databaseDtuMin`.</span></span> <span data-ttu-id="b0c9c-1028">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1028">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="b0c9c-1029">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1029">`databaseDtuMax`.</span></span> <span data-ttu-id="b0c9c-1030">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1030">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="b0c9c-1031">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1031">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="b0c9c-1032">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1032">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1033">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1033">Storage</span></span>

* <span data-ttu-id="b0c9c-1034">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1034">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="b0c9c-1035">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1035">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1036">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1036">VM</span></span>

* <span data-ttu-id="b0c9c-1037">[破壊的変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1037">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="b0c9c-1038">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1038">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="b0c9c-1039">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1039">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="b0c9c-1040">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1040">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="b0c9c-1041">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1041">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="b0c9c-1042">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1042">May 7, 2018</span></span>

<span data-ttu-id="b0c9c-1043">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1043">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-1044">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1044">Core</span></span>

* <span data-ttu-id="b0c9c-1045">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1045">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="b0c9c-1046">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1046">Added limited support for positional arguments</span></span>
* <span data-ttu-id="b0c9c-1047">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1047">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="b0c9c-1048">#5591</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1048">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="b0c9c-1049">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1049">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="b0c9c-1050">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1050">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="b0c9c-1051">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1051">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="b0c9c-1052">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1052">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="b0c9c-1053">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1053">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-1054">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1054">ACR</span></span>

* <span data-ttu-id="b0c9c-1055">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1055">Added ACR Build commands</span></span>
* <span data-ttu-id="b0c9c-1056">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1056">Improved resource not found error messages</span></span>
* <span data-ttu-id="b0c9c-1057">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1057">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="b0c9c-1058">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1058">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="b0c9c-1059">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1059">Improved repository commands error messages</span></span>
* <span data-ttu-id="b0c9c-1060">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1060">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1061">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1061">ACS</span></span>

* <span data-ttu-id="b0c9c-1062">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1062">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="b0c9c-1063">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1063">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="b0c9c-1064">AMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1064">AMS</span></span>

* <span data-ttu-id="b0c9c-1065">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1065">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1066">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1066">Appservice</span></span>

* <span data-ttu-id="b0c9c-1067">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1067">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="b0c9c-1068">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1068">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="b0c9c-1069">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1069">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="b0c9c-1070">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1070">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b0c9c-1071">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1071">Batch AI</span></span>

* <span data-ttu-id="b0c9c-1072">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1072">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b0c9c-1073">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1073">Cognitive Services</span></span>

* <span data-ttu-id="b0c9c-1074">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1074">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="b0c9c-1075">消費</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1075">Consumption</span></span>

* <span data-ttu-id="b0c9c-1076">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1076">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-1077">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1077">Container</span></span>

* <span data-ttu-id="b0c9c-1078">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1078">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="b0c9c-1079">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1079">Cosmos DB</span></span>

* <span data-ttu-id="b0c9c-1080">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1080">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="b0c9c-1081">DMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1081">DMS</span></span>

* <span data-ttu-id="b0c9c-1082">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1082">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="b0c9c-1083">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1083">Extension</span></span>

* <span data-ttu-id="b0c9c-1084">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1084">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-1085">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1085">Interactive</span></span>

* <span data-ttu-id="b0c9c-1086">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1086">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="b0c9c-1087">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1087">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="b0c9c-1088">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1088">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="b0c9c-1089">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1089">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="b0c9c-1090">ラボ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1090">Lab</span></span>

* <span data-ttu-id="b0c9c-1091">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1091">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1092">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1092">Network</span></span>

* <span data-ttu-id="b0c9c-1093">[破壊的変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1093">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="b0c9c-1094">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1094">Profile</span></span>

* <span data-ttu-id="b0c9c-1095">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1095">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="b0c9c-1096">[破壊的変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1096">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="b0c9c-1097">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1097">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="b0c9c-1098">Redis</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1098">Redis</span></span>

* <span data-ttu-id="b0c9c-1099">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1099">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="b0c9c-1100">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1100">Deprecated `redis list-all`.</span></span> <span data-ttu-id="b0c9c-1101">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1101">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="b0c9c-1102">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1102">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="b0c9c-1103">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1103">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-1104">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1104">Role</span></span>

* <span data-ttu-id="b0c9c-1105">[破壊的変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1105">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1106">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1106">Storage</span></span>

* <span data-ttu-id="b0c9c-1107">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1107">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="b0c9c-1108">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1108">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="b0c9c-1109">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1109">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="b0c9c-1110">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1110">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="b0c9c-1111">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1111">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1112">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1112">VM</span></span>

* <span data-ttu-id="b0c9c-1113">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1113">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="b0c9c-1114">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1114">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="b0c9c-1115">[破壊的変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1115">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="b0c9c-1116">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1116">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="b0c9c-1117">[破壊的変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1117">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="b0c9c-1118">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1118">Added write accelerator support</span></span>
* <span data-ttu-id="b0c9c-1119">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1119">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="b0c9c-1120">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1120">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="b0c9c-1121">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1121">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="b0c9c-1122">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1122">April 10, 2018</span></span>

<span data-ttu-id="b0c9c-1123">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1123">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-1124">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1124">ACR</span></span>

* <span data-ttu-id="b0c9c-1125">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1125">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1126">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1126">ACS</span></span>

* <span data-ttu-id="b0c9c-1127">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1127">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1128">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1128">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="b0c9c-1130">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1130">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="b0c9c-1131">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1131">BatchAI</span></span>

* <span data-ttu-id="b0c9c-1132">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1132">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="b0c9c-1133">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1133">Job level mounting</span></span>
  - <span data-ttu-id="b0c9c-1134">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1134">Environment variables with secret values</span></span>
  - <span data-ttu-id="b0c9c-1135">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1135">Performance counters settings</span></span>
  - <span data-ttu-id="b0c9c-1136">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1136">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="b0c9c-1137">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1137">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="b0c9c-1138">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1138">Usage and limits reporting</span></span>
  - <span data-ttu-id="b0c9c-1139">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1139">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="b0c9c-1140">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1140">Support for custom images</span></span>
  - <span data-ttu-id="b0c9c-1141">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1141">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="b0c9c-1142">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1142">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="b0c9c-1143">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1143">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="b0c9c-1144">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1144">National clouds are supported</span></span>
* <span data-ttu-id="b0c9c-1145">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1145">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="b0c9c-1146">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1146">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="b0c9c-1147">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1147">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="b0c9c-1148">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1148">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="b0c9c-1149">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1149">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="b0c9c-1150">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1150">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="b0c9c-1151">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1151">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="b0c9c-1152">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1152">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="b0c9c-1153">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1153">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="b0c9c-1154">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1154">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="b0c9c-1155">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1155">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="b0c9c-1156">[破壊的変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1156">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="b0c9c-1157">[破壊的変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1157">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="b0c9c-1158">課金</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1158">Billing</span></span>

* <span data-ttu-id="b0c9c-1159">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1159">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="b0c9c-1160">消費</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1160">Consumption</span></span>

* <span data-ttu-id="b0c9c-1161">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1161">Added `marketplace` commands</span></span>
* <span data-ttu-id="b0c9c-1162">[破壊的変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1162">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="b0c9c-1163">[破壊的変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1163">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="b0c9c-1164">[破壊的変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1164">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="b0c9c-1165">[破壊的変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1165">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="b0c9c-1166">[破壊的変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1166">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-1167">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1167">Container</span></span>

* <span data-ttu-id="b0c9c-1168">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1168">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="b0c9c-1169">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1169">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="b0c9c-1170">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1170">Extension</span></span>

* <span data-ttu-id="b0c9c-1171">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1171">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-1172">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1172">Interactive</span></span>

* <span data-ttu-id="b0c9c-1173">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1173">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="b0c9c-1174">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1174">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="b0c9c-1175">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1175">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1176">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1176">Network</span></span>

* <span data-ttu-id="b0c9c-1177">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1177">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="b0c9c-1178">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1178">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="b0c9c-1179">#4910</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1179">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="b0c9c-1180">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1180">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="b0c9c-1181">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1181">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="b0c9c-1182">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1182">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="b0c9c-1183">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1183">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="b0c9c-1184">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1184">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="b0c9c-1185">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1185">Profile</span></span>

* <span data-ttu-id="b0c9c-1186">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1186">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="b0c9c-1187">[破壊的変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1187">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0c9c-1188">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1188">RDBMS</span></span>

* <span data-ttu-id="b0c9c-1189">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1189">Added `georestore` command</span></span>
* <span data-ttu-id="b0c9c-1190">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1190">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1191">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1191">Resource</span></span>

* <span data-ttu-id="b0c9c-1192">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1192">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="b0c9c-1193">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1193">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-1194">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1194">SQL</span></span>

* <span data-ttu-id="b0c9c-1195">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1195">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1196">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1196">Storage</span></span>

* <span data-ttu-id="b0c9c-1197">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1197">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1198">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1198">VM</span></span>

* <span data-ttu-id="b0c9c-1199">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1199">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="b0c9c-1200">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1200">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="b0c9c-1202">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1202">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="b0c9c-1203">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1203">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="b0c9c-1204">#5718</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1204">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="b0c9c-1205">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1205">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="b0c9c-1206">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1206">March 27, 2018</span></span>

<span data-ttu-id="b0c9c-1207">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1207">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-1208">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1208">Core</span></span>

* <span data-ttu-id="b0c9c-1209">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1209">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1210">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1210">ACS</span></span>

* <span data-ttu-id="b0c9c-1211">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1211">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1212">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1212">Appservice</span></span>

* <span data-ttu-id="b0c9c-1213">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1213">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="b0c9c-1214">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1214">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="b0c9c-1215">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1215">Backup</span></span>

* <span data-ttu-id="b0c9c-1216">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1216">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="b0c9c-1217">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1217">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="b0c9c-1218">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1218">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="b0c9c-1219">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1219">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-1220">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1220">Container</span></span>

* <span data-ttu-id="b0c9c-1221">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1221">Added `container exec` command.</span></span> <span data-ttu-id="b0c9c-1222">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1222">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="b0c9c-1223">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1223">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="b0c9c-1224">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1224">Extension</span></span>

* <span data-ttu-id="b0c9c-1225">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1225">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="b0c9c-1226">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1226">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="b0c9c-1227">[破壊的変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1227">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-1228">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1228">Interactive</span></span>

* <span data-ttu-id="b0c9c-1229">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1229">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="b0c9c-1230">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1230">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="b0c9c-1231">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1231">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="b0c9c-1232">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1232">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="b0c9c-1233">ラボ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1233">Lab</span></span>

* <span data-ttu-id="b0c9c-1234">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1234">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-1235">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1235">Monitor</span></span>

* <span data-ttu-id="b0c9c-1236">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1236">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="b0c9c-1237">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1237">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="b0c9c-1238">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1238">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1239">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1239">Network</span></span>

* <span data-ttu-id="b0c9c-1240">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1240">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="b0c9c-1241">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1241">Profile</span></span>

* <span data-ttu-id="b0c9c-1242">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1242">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0c9c-1243">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1243">RDBMS</span></span>

* <span data-ttu-id="b0c9c-1244">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1244">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1245">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1245">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="b0c9c-1247">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1247">Role</span></span>

* <span data-ttu-id="b0c9c-1248">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1248">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="b0c9c-1249">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1249">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="b0c9c-1250">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1250">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="b0c9c-1251">[破壊的変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1251">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="b0c9c-1252">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1252">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1253">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1253">Storage</span></span>

* <span data-ttu-id="b0c9c-1254">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1254">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="b0c9c-1255">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1255">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1256">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1256">VM</span></span>

* <span data-ttu-id="b0c9c-1257">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1257">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="b0c9c-1258">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1258">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="b0c9c-1259">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1259">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="b0c9c-1260">[破壊的変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1260">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="b0c9c-1261">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1261">March 13, 2018</span></span>

<span data-ttu-id="b0c9c-1262">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1262">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-1263">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1263">ACR</span></span>

* <span data-ttu-id="b0c9c-1264">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1264">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="b0c9c-1265">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1265">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="b0c9c-1266">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1266">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1267">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1267">ACS</span></span>

* <span data-ttu-id="b0c9c-1268">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1268">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="b0c9c-1269">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1269">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="b0c9c-1270">Advisor</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1270">Advisor</span></span>

* <span data-ttu-id="b0c9c-1271">[破壊的変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1271">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="b0c9c-1272">[破壊的変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1272">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="b0c9c-1273">[破壊的変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1273">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="b0c9c-1274">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1274">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="b0c9c-1275">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1275">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1276">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1276">Appservice</span></span>

* <span data-ttu-id="b0c9c-1277">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1277">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="b0c9c-1278">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1278">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="b0c9c-1279">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1279">Eventhubs</span></span>

* <span data-ttu-id="b0c9c-1280">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1280">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="b0c9c-1281">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1281">Extension</span></span>

* <span data-ttu-id="b0c9c-1282">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1282">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-1283">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1283">Interactive</span></span>

* <span data-ttu-id="b0c9c-1284">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1284">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="b0c9c-1285">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1285">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="b0c9c-1286">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1286">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="b0c9c-1287">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1287">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-1288">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1288">Monitor</span></span>

* <span data-ttu-id="b0c9c-1289">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1289">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="b0c9c-1290">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1290">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="b0c9c-1291">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1291">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="b0c9c-1292">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1292">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1293">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1293">Network</span></span>

* <span data-ttu-id="b0c9c-1294">[破壊的変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1294">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="b0c9c-1295">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1295">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="b0c9c-1296">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1296">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="b0c9c-1297">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1297">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="b0c9c-1298">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1298">Profile</span></span>

* <span data-ttu-id="b0c9c-1299">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1299">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="b0c9c-1300">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1300">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0c9c-1301">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1301">RDBMS</span></span>

* <span data-ttu-id="b0c9c-1302">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1302">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="b0c9c-1303">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1303">Service Bus</span></span>

* <span data-ttu-id="b0c9c-1304">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1304">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1305">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1305">Storage</span></span>

* <span data-ttu-id="b0c9c-1306">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1306">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="b0c9c-1307">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1307">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1308">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1308">VM</span></span>

* <span data-ttu-id="b0c9c-1309">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1309">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="b0c9c-1310">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1310">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="b0c9c-1311">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1311">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="b0c9c-1312">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1312">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="b0c9c-1313">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1313">February 27, 2018</span></span>

<span data-ttu-id="b0c9c-1314">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1314">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-1315">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1315">Core</span></span>

* <span data-ttu-id="b0c9c-1316">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1316">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="b0c9c-1317">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1317">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="b0c9c-1318">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1318">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1319">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1319">ACS</span></span>

* <span data-ttu-id="b0c9c-1320">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1320">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="b0c9c-1321">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1321">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="b0c9c-1322">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1322">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="b0c9c-1323">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1323">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1324">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1324">Appservice</span></span>

* <span data-ttu-id="b0c9c-1325">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1325">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="b0c9c-1326">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1326">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b0c9c-1327">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1327">Cognitive Services</span></span>

* <span data-ttu-id="b0c9c-1328">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1328">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="b0c9c-1329">消費</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1329">Consumption</span></span>

* <span data-ttu-id="b0c9c-1330">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1330">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="b0c9c-1331">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1331">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-1332">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1332">Container</span></span>

* <span data-ttu-id="b0c9c-1333">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1333">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1334">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1334">Network</span></span>

* <span data-ttu-id="b0c9c-1335">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1335">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1336">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1336">Resource</span></span>

* <span data-ttu-id="b0c9c-1337">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1337">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-1338">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1338">Role</span></span>

* <span data-ttu-id="b0c9c-1339">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1339">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-1340">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1340">SQL</span></span>

* <span data-ttu-id="b0c9c-1341">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1341">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1342">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1342">Storage</span></span>

* <span data-ttu-id="b0c9c-1343">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1343">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1344">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1344">VM</span></span>

* <span data-ttu-id="b0c9c-1345">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1345">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="b0c9c-1346">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1346">February 13, 2018</span></span>

<span data-ttu-id="b0c9c-1347">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1347">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-1348">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1348">Core</span></span>

* <span data-ttu-id="b0c9c-1349">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1349">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1350">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1350">ACS</span></span>

* <span data-ttu-id="b0c9c-1351">[破壊的変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1351">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="b0c9c-1352">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1352">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="b0c9c-1353">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1353">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="b0c9c-1354">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1354">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="b0c9c-1355">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1355">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="b0c9c-1356">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1356">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="b0c9c-1357">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1357">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="b0c9c-1358">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1358">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1359">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1359">Appservice</span></span>

* <span data-ttu-id="b0c9c-1360">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1360">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="b0c9c-1361">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1361">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="b0c9c-1362">CDN</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1362">CDN</span></span>

* <span data-ttu-id="b0c9c-1363">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1363">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-1364">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1364">Container</span></span>

* <span data-ttu-id="b0c9c-1365">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1365">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="b0c9c-1366">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1366">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0c9c-1367">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1367">CosmosDB</span></span>

* <span data-ttu-id="b0c9c-1368">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1368">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="b0c9c-1369">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1369">Extension</span></span>

* <span data-ttu-id="b0c9c-1370">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1370">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="b0c9c-1371">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1371">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="b0c9c-1372">フィードバック</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1372">Feedback</span></span>

* <span data-ttu-id="b0c9c-1373">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1373">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-1374">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1374">Interactive</span></span>

* <span data-ttu-id="b0c9c-1375">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1375">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="b0c9c-1376">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1376">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="b0c9c-1377">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1377">IoT</span></span>

* <span data-ttu-id="b0c9c-1378">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1378">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="b0c9c-1379">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1379">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="b0c9c-1380">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1380">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="b0c9c-1381">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1381">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-1382">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1382">Monitor</span></span>

* <span data-ttu-id="b0c9c-1383">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1383">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1384">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1384">Network</span></span>

* <span data-ttu-id="b0c9c-1385">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1385">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="b0c9c-1386">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1386">Profile</span></span>

* <span data-ttu-id="b0c9c-1387">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1387">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1388">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1388">Resource</span></span>

* <span data-ttu-id="b0c9c-1389">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1389">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-1390">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1390">Role</span></span>

* <span data-ttu-id="b0c9c-1391">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1391">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-1392">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1392">SQL</span></span>

* <span data-ttu-id="b0c9c-1393">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1393">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="b0c9c-1394">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1394">Added `sql db rename`</span></span>
* <span data-ttu-id="b0c9c-1395">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1395">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1396">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1396">Storage</span></span>

* <span data-ttu-id="b0c9c-1397">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1397">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1398">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1398">VM</span></span>

* <span data-ttu-id="b0c9c-1399">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1399">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="b0c9c-1400">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1400">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="b0c9c-1401">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1401">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="b0c9c-1402">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1402">January 31, 2018</span></span>

<span data-ttu-id="b0c9c-1403">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1403">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-1404">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1404">Core</span></span>

* <span data-ttu-id="b0c9c-1405">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1405">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="b0c9c-1406">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1406">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="b0c9c-1407">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1407">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="b0c9c-1408">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1408">Use `--verbose` to see</span></span>
* <span data-ttu-id="b0c9c-1409">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1409">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1410">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1410">ACS</span></span>

* <span data-ttu-id="b0c9c-1411">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1411">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="b0c9c-1412">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1412">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1413">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1413">Appservice</span></span>

* <span data-ttu-id="b0c9c-1414">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1414">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="b0c9c-1415">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1415">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="b0c9c-1416">CDN</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1416">CDN</span></span>

* <span data-ttu-id="b0c9c-1417">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1417">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0c9c-1418">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1418">CosmosDB</span></span>

* <span data-ttu-id="b0c9c-1419">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1419">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-1420">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1420">Interactive</span></span>

* <span data-ttu-id="b0c9c-1421">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1421">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1422">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1422">Network</span></span>

* <span data-ttu-id="b0c9c-1423">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1423">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="b0c9c-1424">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1424">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="b0c9c-1425">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1425">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="b0c9c-1426">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1426">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="b0c9c-1427">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1427">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="b0c9c-1428">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1428">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="b0c9c-1429">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1429">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="b0c9c-1430">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1430">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="b0c9c-1431">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1431">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="b0c9c-1432">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1432">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="b0c9c-1433">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1433">Profile</span></span>

* <span data-ttu-id="b0c9c-1434">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1434">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1435">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1435">Resource</span></span>

* <span data-ttu-id="b0c9c-1436">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1436">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1437">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1437">Storage</span></span>

* <span data-ttu-id="b0c9c-1438">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1438">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="b0c9c-1439">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1439">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="b0c9c-1440">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1440">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="b0c9c-1441">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1441">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="b0c9c-1442">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1442">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1443">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1443">VM</span></span>

* <span data-ttu-id="b0c9c-1444">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1444">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="b0c9c-1445">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1445">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="b0c9c-1446">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1446">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="b0c9c-1447">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1447">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="b0c9c-1448">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1448">January 17, 2018</span></span>

<span data-ttu-id="b0c9c-1449">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1449">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-1450">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1450">ACR</span></span>

* <span data-ttu-id="b0c9c-1451">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1451">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="b0c9c-1452">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1452">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1453">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1453">ACS</span></span>

* <span data-ttu-id="b0c9c-1454">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1454">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="b0c9c-1455">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1455">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1456">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1456">Appservice</span></span>

* <span data-ttu-id="b0c9c-1457">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1457">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="b0c9c-1458">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1458">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="b0c9c-1459">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1459">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="b0c9c-1460">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1460">Backup</span></span>

* <span data-ttu-id="b0c9c-1461">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1461">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="b0c9c-1462">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1462">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="b0c9c-1463">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1463">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="b0c9c-1464">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1464">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="b0c9c-1465">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1465">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-1466">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1466">Batch</span></span>

* <span data-ttu-id="b0c9c-1467">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1467">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="b0c9c-1468">クラウド</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1468">Cloud</span></span>

* <span data-ttu-id="b0c9c-1469">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1469">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="b0c9c-1470">消費</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1470">Consumption</span></span>

* <span data-ttu-id="b0c9c-1471">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1471">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="b0c9c-1472">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1472">Event Grid</span></span>

* <span data-ttu-id="b0c9c-1473">[破壊的変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1473">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="b0c9c-1474">[破壊的変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1474">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="b0c9c-1475">[破壊的変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1475">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="b0c9c-1476">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1476">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="b0c9c-1477">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1477">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="b0c9c-1478">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1478">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="b0c9c-1479">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1479">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="b0c9c-1480">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1480">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-1481">Interactive</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1481">Interactive</span></span>

* <span data-ttu-id="b0c9c-1482">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1482">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="b0c9c-1483">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1483">Fixed errors on startup</span></span>
* <span data-ttu-id="b0c9c-1484">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1484">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="b0c9c-1485">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1485">IoT</span></span>

* <span data-ttu-id="b0c9c-1486">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1486">Added support for device provisioning service</span></span>
* <span data-ttu-id="b0c9c-1487">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1487">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="b0c9c-1488">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1488">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-1489">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1489">Monitor</span></span>

* <span data-ttu-id="b0c9c-1490">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1490">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="b0c9c-1491">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1491">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="b0c9c-1492">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1492">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1493">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1493">Network</span></span>

* <span data-ttu-id="b0c9c-1494">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1494">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="b0c9c-1495">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1495">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="b0c9c-1496">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1496">Profile</span></span>

* <span data-ttu-id="b0c9c-1497">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1497">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-1498">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1498">Role</span></span>

* <span data-ttu-id="b0c9c-1499">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1499">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b0c9c-1500">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1500">Service Fabric</span></span>

* <span data-ttu-id="b0c9c-1501">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1501">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="b0c9c-1502">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1502">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1503">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1503">VM</span></span>

* <span data-ttu-id="b0c9c-1504">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1504">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="b0c9c-1505">[破壊的変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1505">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="b0c9c-1506">[破壊的変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1506">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="b0c9c-1507">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1507">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="b0c9c-1508">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1508">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="b0c9c-1509">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1509">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="b0c9c-1510">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1510">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="b0c9c-1511">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1511">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="b0c9c-1512">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1512">December 19, 2017</span></span>

<span data-ttu-id="b0c9c-1513">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1513">Version 2.0.23</span></span>

* <span data-ttu-id="b0c9c-1514">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1514">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-1515">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1515">Container</span></span>

* <span data-ttu-id="b0c9c-1516">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1516">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1517">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1517">Network</span></span>

* <span data-ttu-id="b0c9c-1518">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1518">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="b0c9c-1519">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1519">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1520">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1520">Storage</span></span>

* <span data-ttu-id="b0c9c-1521">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1521">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1522">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1522">VM</span></span>

* <span data-ttu-id="b0c9c-1523">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1523">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="b0c9c-1524">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1524">December 5, 2017</span></span>

<span data-ttu-id="b0c9c-1525">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1525">Version 2.0.22</span></span>

* <span data-ttu-id="b0c9c-1526">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1526">Removed `az component` commands.</span></span> <span data-ttu-id="b0c9c-1527">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1527">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-1528">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1528">Core</span></span>
* <span data-ttu-id="b0c9c-1529">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1529">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="b0c9c-1530">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1530">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1531">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1531">ACS</span></span>

* <span data-ttu-id="b0c9c-1532">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1532">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="b0c9c-1533">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1533">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="b0c9c-1534">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1534">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="b0c9c-1535">Advisor</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1535">Advisor</span></span>

* <span data-ttu-id="b0c9c-1536">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1536">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1537">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1537">Appservice</span></span>

* <span data-ttu-id="b0c9c-1538">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1538">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="b0c9c-1539">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1539">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="b0c9c-1540">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1540">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="b0c9c-1541">消費</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1541">Consumption</span></span>

* <span data-ttu-id="b0c9c-1542">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1542">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-1543">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1543">Container</span></span>

* <span data-ttu-id="b0c9c-1544">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1544">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-1545">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1545">Monitor</span></span>

* <span data-ttu-id="b0c9c-1546">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1546">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1547">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1547">Resource</span></span>

* <span data-ttu-id="b0c9c-1548">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1548">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-1549">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1549">Role</span></span>

* <span data-ttu-id="b0c9c-1550">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1550">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="b0c9c-1551">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1551">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="b0c9c-1552">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1552">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-1553">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1553">SQL</span></span>

* <span data-ttu-id="b0c9c-1554">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1554">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="b0c9c-1555">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1555">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1556">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1556">VM</span></span>

* <span data-ttu-id="b0c9c-1557">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1557">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="b0c9c-1558">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1558">November 14, 2017</span></span>

<span data-ttu-id="b0c9c-1559">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1559">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-1560">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1560">ACR</span></span>

* <span data-ttu-id="b0c9c-1561">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1561">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="b0c9c-1562">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1562">ACS</span></span>

* <span data-ttu-id="b0c9c-1563">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1563">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="b0c9c-1564">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1564">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="b0c9c-1565">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1565">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="b0c9c-1566">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1566">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="b0c9c-1567">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1567">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1568">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1568">Appservice</span></span>

* <span data-ttu-id="b0c9c-1569">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1569">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="b0c9c-1570">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1570">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="b0c9c-1571">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1571">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="b0c9c-1572">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1572">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="b0c9c-1573">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1573">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="b0c9c-1574">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1574">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-1575">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1575">Batch</span></span>

* <span data-ttu-id="b0c9c-1576">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1576">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="b0c9c-1577">Batchai</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1577">Batchai</span></span>

* <span data-ttu-id="b0c9c-1578">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1578">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="b0c9c-1579">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1579">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="b0c9c-1580">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1580">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="b0c9c-1581">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1581">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="b0c9c-1582">クラウド</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1582">Cloud</span></span>

* <span data-ttu-id="b0c9c-1583">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1583">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-1584">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1584">Container</span></span>

* <span data-ttu-id="b0c9c-1585">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1585">Added support to open multiple ports</span></span>
* <span data-ttu-id="b0c9c-1586">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1586">Added container group restart policy</span></span>
* <span data-ttu-id="b0c9c-1587">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1587">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="b0c9c-1588">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1588">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b0c9c-1589">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1589">Data Lake Analytics</span></span>

* <span data-ttu-id="b0c9c-1590">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1590">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b0c9c-1591">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1591">Data Lake Store</span></span>

* <span data-ttu-id="b0c9c-1592">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1592">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="b0c9c-1593">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1593">Extension</span></span>

* <span data-ttu-id="b0c9c-1594">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1594">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="b0c9c-1595">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1595">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="b0c9c-1596">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1596">IoT</span></span>

* <span data-ttu-id="b0c9c-1597">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1597">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-1598">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1598">Monitor</span></span>

* <span data-ttu-id="b0c9c-1599">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1599">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1600">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1600">Network</span></span>

* <span data-ttu-id="b0c9c-1601">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1601">Added support for CAA DNS records</span></span>
* <span data-ttu-id="b0c9c-1602">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1602">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="b0c9c-1603">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1603">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="b0c9c-1604">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1604">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="b0c9c-1605">Reservations</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1605">Reservations</span></span>

* <span data-ttu-id="b0c9c-1606">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1606">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1607">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1607">Resource</span></span>

* <span data-ttu-id="b0c9c-1608">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1608">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-1609">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1609">SQL</span></span>

* <span data-ttu-id="b0c9c-1610">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1610">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1611">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1611">Storage</span></span>

* <span data-ttu-id="b0c9c-1612">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1612">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="b0c9c-1613">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1613">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="b0c9c-1614">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1614">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="b0c9c-1615">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1615">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="b0c9c-1616">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1616">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="b0c9c-1617">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1617">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="b0c9c-1618">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1618">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1619">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1619">VM</span></span>

* <span data-ttu-id="b0c9c-1620">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1620">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="b0c9c-1621">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1621">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="b0c9c-1622">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1622">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="b0c9c-1623">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1623">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="b0c9c-1624">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1624">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="b0c9c-1625">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1625">October 24, 2017</span></span>

<span data-ttu-id="b0c9c-1626">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1626">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-1627">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1627">Core</span></span>

* <span data-ttu-id="b0c9c-1628">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1628">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-1629">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1629">ACR</span></span>

* <span data-ttu-id="b0c9c-1630">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1630">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="b0c9c-1631">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1631">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="b0c9c-1632">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1632">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1633">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1633">ACS</span></span>

* <span data-ttu-id="b0c9c-1634">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1634">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="b0c9c-1635">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1635">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1636">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1636">Appservice</span></span>

* <span data-ttu-id="b0c9c-1637">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1637">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="b0c9c-1638">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1638">Component</span></span>

* <span data-ttu-id="b0c9c-1639">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1639">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-1640">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1640">Monitor</span></span>

* <span data-ttu-id="b0c9c-1641">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1641">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1642">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1642">Resource</span></span>

* <span data-ttu-id="b0c9c-1643">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1643">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="b0c9c-1644">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1644">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1645">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1645">VM</span></span>

* <span data-ttu-id="b0c9c-1646">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1646">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="b0c9c-1647">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1647">October 9, 2017</span></span>

<span data-ttu-id="b0c9c-1648">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1648">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-1649">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1649">Core</span></span>

* <span data-ttu-id="b0c9c-1650">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1650">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1651">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1651">Appservice</span></span>

* <span data-ttu-id="b0c9c-1652">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1652">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-1653">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1653">Batch</span></span>

* <span data-ttu-id="b0c9c-1654">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1654">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="b0c9c-1655">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1655">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="b0c9c-1656">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1656">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="b0c9c-1657">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1657">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="b0c9c-1658">Batchai</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1658">Batchai</span></span>

* <span data-ttu-id="b0c9c-1659">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1659">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0c9c-1660">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1660">Keyvault</span></span>

* <span data-ttu-id="b0c9c-1661">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1661">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="b0c9c-1662">(#4448)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1662">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="b0c9c-1663">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1663">Network</span></span>

* <span data-ttu-id="b0c9c-1664">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1664">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="b0c9c-1665">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1665">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1666">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1666">Resource</span></span>

* <span data-ttu-id="b0c9c-1667">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1667">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="b0c9c-1668">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1668">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="b0c9c-1669">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1669">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="b0c9c-1670">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1670">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-1671">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1671">Sql</span></span>

* <span data-ttu-id="b0c9c-1672">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1672">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="b0c9c-1673">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1673">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="b0c9c-1674">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1674">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1675">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1675">Storage</span></span>

* <span data-ttu-id="b0c9c-1676">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1676">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1677">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1677">Vm</span></span>

* <span data-ttu-id="b0c9c-1678">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1678">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="b0c9c-1679">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1679">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="b0c9c-1680">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1680">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="b0c9c-1681">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1681">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="b0c9c-1682">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1682">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="b0c9c-1683">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1683">September 22, 2017</span></span>

<span data-ttu-id="b0c9c-1684">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1684">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1685">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1685">Resource</span></span>

* <span data-ttu-id="b0c9c-1686">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1686">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="b0c9c-1687">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1687">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="b0c9c-1688">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1688">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="b0c9c-1689">[破壊的変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1689">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1690">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1690">Network</span></span>

* <span data-ttu-id="b0c9c-1691">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1691">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="b0c9c-1692">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1692">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="b0c9c-1693">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1693">Added `asg` application security group commands</span></span>
* <span data-ttu-id="b0c9c-1694">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1694">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="b0c9c-1695">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1695">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="b0c9c-1696">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1696">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="b0c9c-1697">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1697">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1698">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1698">Storage</span></span>

* <span data-ttu-id="b0c9c-1699">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1699">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="b0c9c-1700">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1700">Eventgrid</span></span>

* <span data-ttu-id="b0c9c-1701">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1701">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-1702">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1702">SQL</span></span>

* <span data-ttu-id="b0c9c-1703">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1703">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="b0c9c-1704">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1704">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="b0c9c-1705">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1705">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0c9c-1706">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1706">Keyvault</span></span>

* <span data-ttu-id="b0c9c-1707">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1707">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1708">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1708">VM</span></span>

* <span data-ttu-id="b0c9c-1709">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1709">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="b0c9c-1710">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1710">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="b0c9c-1711">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1711">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="b0c9c-1712">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1712">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="b0c9c-1713">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1713">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="b0c9c-1714">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1714">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1715">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1715">ACS</span></span>

* <span data-ttu-id="b0c9c-1716">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1716">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1717">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1717">Appservice</span></span>

* <span data-ttu-id="b0c9c-1718">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1718">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="b0c9c-1719">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1719">Backup</span></span>

* <span data-ttu-id="b0c9c-1720">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1720">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="b0c9c-1721">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1721">September 11, 2017</span></span>

<span data-ttu-id="b0c9c-1722">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1722">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="b0c9c-1723">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1723">Core</span></span>

* <span data-ttu-id="b0c9c-1724">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1724">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="b0c9c-1725">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1725">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1726">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1726">Acs</span></span>

* <span data-ttu-id="b0c9c-1727">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1727">Added `acs list-locations` command</span></span>
* <span data-ttu-id="b0c9c-1728">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1728">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1729">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1729">Appservice</span></span>

* <span data-ttu-id="b0c9c-1730">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1730">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="b0c9c-1731">CDN</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1731">CDN</span></span>

* <span data-ttu-id="b0c9c-1732">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1732">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="b0c9c-1733">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1733">Extension</span></span>

* <span data-ttu-id="b0c9c-1734">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1734">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0c9c-1735">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1735">Keyvault</span></span>

* <span data-ttu-id="b0c9c-1736">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1736">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1737">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1737">Network</span></span>

* <span data-ttu-id="b0c9c-1738">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1738">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="b0c9c-1739">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1739">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="b0c9c-1740">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1740">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="b0c9c-1741">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1741">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="b0c9c-1742">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1742">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1743">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1743">Resource</span></span>

* <span data-ttu-id="b0c9c-1744">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1744">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="b0c9c-1745">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1745">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="b0c9c-1746">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1746">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="b0c9c-1747">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1747">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-1748">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1748">SQL</span></span>

* <span data-ttu-id="b0c9c-1749">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1749">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1750">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1750">VM</span></span>

* <span data-ttu-id="b0c9c-1751">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1751">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="b0c9c-1752">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1752">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="b0c9c-1753">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1753">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="b0c9c-1754">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1754">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="b0c9c-1755">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1755">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="b0c9c-1756">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1756">August 31, 2017</span></span>

<span data-ttu-id="b0c9c-1757">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1757">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0c9c-1758">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1758">Keyvault</span></span>

* <span data-ttu-id="b0c9c-1759">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1759">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="b0c9c-1760">SF</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1760">Sf</span></span>

* <span data-ttu-id="b0c9c-1761">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1761">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1762">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1762">Storage</span></span>

* <span data-ttu-id="b0c9c-1763">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1763">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="b0c9c-1764">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1764">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="b0c9c-1765">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1765">August 28, 2017</span></span>

<span data-ttu-id="b0c9c-1766">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1766">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="b0c9c-1767">CLI</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1767">CLI</span></span>

* <span data-ttu-id="b0c9c-1768">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1768">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1769">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1769">ACS</span></span>

* <span data-ttu-id="b0c9c-1770">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1770">Corrected preview regions</span></span>
* <span data-ttu-id="b0c9c-1771">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1771">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="b0c9c-1772">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1772">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1773">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1773">Appservice</span></span>

* <span data-ttu-id="b0c9c-1774">[破壊的変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1774">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="b0c9c-1775">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1775">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="b0c9c-1776">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1776">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="b0c9c-1777">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1777">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="b0c9c-1778">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1778">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="b0c9c-1779">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1779">IoT</span></span>

* <span data-ttu-id="b0c9c-1780">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1780">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1781">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1781">Network</span></span>

* <span data-ttu-id="b0c9c-1782">[破壊的変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1782">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="b0c9c-1783">[破壊的変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1783">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="b0c9c-1784">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1784">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="b0c9c-1785">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1785">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="b0c9c-1786">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1786">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="b0c9c-1787">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1787">Profile</span></span>

* <span data-ttu-id="b0c9c-1788">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1788">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b0c9c-1789">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1789">Service Fabric</span></span>

* <span data-ttu-id="b0c9c-1790">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1790">Preview release</span></span>
* <span data-ttu-id="b0c9c-1791">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1791">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="b0c9c-1792">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1792">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="b0c9c-1793">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1793">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1794">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1794">Storage</span></span>

* <span data-ttu-id="b0c9c-1795">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1795">Enabled setting blob tier</span></span>
* <span data-ttu-id="b0c9c-1796">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1796">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="b0c9c-1797">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1797">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="b0c9c-1798">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1798">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="b0c9c-1799">[破壊的変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1799">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="b0c9c-1800">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1800">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1801">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1801">VM</span></span>

* <span data-ttu-id="b0c9c-1802">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1802">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="b0c9c-1803">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1803">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="b0c9c-1804">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1804">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="b0c9c-1805">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1805">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="b0c9c-1806">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1806">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="b0c9c-1807">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1807">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="b0c9c-1808">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1808">August 15, 2017</span></span>

<span data-ttu-id="b0c9c-1809">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1809">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1810">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1810">ACS</span></span>

* <span data-ttu-id="b0c9c-1811">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1811">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1812">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1812">Appservice</span></span>

* <span data-ttu-id="b0c9c-1813">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1813">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="b0c9c-1814">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1814">Event Grid</span></span>

* <span data-ttu-id="b0c9c-1815">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1815">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="b0c9c-1816">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1816">August 11, 2017</span></span>

<span data-ttu-id="b0c9c-1817">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1817">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1818">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1818">ACS</span></span>

* <span data-ttu-id="b0c9c-1819">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1819">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-1820">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1820">Batch</span></span>

* <span data-ttu-id="b0c9c-1821">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1821">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="b0c9c-1822">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1822">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="b0c9c-1823">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1823">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="b0c9c-1824">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1824">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="b0c9c-1825">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1825">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="b0c9c-1826">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1826">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="b0c9c-1827">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1827">Component</span></span>

* <span data-ttu-id="b0c9c-1828">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1828">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="b0c9c-1829">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1829">Container</span></span>

* <span data-ttu-id="b0c9c-1830">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1830">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="b0c9c-1831">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1831">Data Lake Store</span></span>

* <span data-ttu-id="b0c9c-1832">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1832">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="b0c9c-1833">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1833">Event Grid</span></span>

* <span data-ttu-id="b0c9c-1834">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1834">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1835">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1835">Network</span></span>

* <span data-ttu-id="b0c9c-1836">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1836">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="b0c9c-1837">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1837">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="b0c9c-1838">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1838">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="b0c9c-1839">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1839">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="b0c9c-1840">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1840">Profile</span></span>

* <span data-ttu-id="b0c9c-1841">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1841">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-1842">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1842">Storage</span></span>

* <span data-ttu-id="b0c9c-1843">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1843">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-1844">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1844">VM</span></span>

* <span data-ttu-id="b0c9c-1845">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1845">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="b0c9c-1846">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1846">Exposed `list-skus` command</span></span>
* <span data-ttu-id="b0c9c-1847">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1847">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="b0c9c-1848">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1848">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="b0c9c-1849">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1849">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="b0c9c-1850">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1850">July 28, 2017</span></span>

<span data-ttu-id="b0c9c-1851">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1851">Version 2.0.12</span></span>

* <span data-ttu-id="b0c9c-1852">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1852">Added container commands</span></span>
* <span data-ttu-id="b0c9c-1853">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1853">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="b0c9c-1854">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1854">Core</span></span>

* <span data-ttu-id="b0c9c-1855">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1855">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="b0c9c-1856">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1856">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="b0c9c-1857">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1857">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="b0c9c-1858">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1858">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="b0c9c-1859">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1859">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="b0c9c-1860">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1860">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="b0c9c-1861">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1861">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="b0c9c-1862">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1862">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="b0c9c-1863">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1863">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="b0c9c-1864">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1864">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="b0c9c-1865">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1865">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="b0c9c-1866">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1866">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="b0c9c-1867">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1867">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="b0c9c-1868">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1868">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="b0c9c-1869">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1869">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="b0c9c-1870">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1870">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="b0c9c-1871">ACR</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1871">ACR</span></span>

* <span data-ttu-id="b0c9c-1872">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1872">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="b0c9c-1873">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1873">Support SKU update for managed registries</span></span>
* <span data-ttu-id="b0c9c-1874">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1874">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="b0c9c-1875">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1875">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="b0c9c-1876">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1876">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="b0c9c-1877">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1877">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-1878">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1878">ACS</span></span>

* <span data-ttu-id="b0c9c-1879">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1879">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-1880">Appservice</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1880">Appservice</span></span>

* <span data-ttu-id="b0c9c-1881">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1881">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="b0c9c-1882">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1882">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="b0c9c-1883">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1883">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="b0c9c-1884">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1884">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="b0c9c-1885">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1885">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="b0c9c-1886">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1886">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="b0c9c-1887">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1887">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="b0c9c-1888">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1888">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="b0c9c-1889">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1889">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="b0c9c-1890">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1890">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="b0c9c-1891">Batch</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1891">Batch</span></span>

* <span data-ttu-id="b0c9c-1892">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1892">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="b0c9c-1893">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1893">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="b0c9c-1894">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1894">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="b0c9c-1895">CDN</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1895">CDN</span></span>

* <span data-ttu-id="b0c9c-1896">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1896">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="b0c9c-1897">クラウド</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1897">Cloud</span></span>

* <span data-ttu-id="b0c9c-1898">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1898">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="b0c9c-1899">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1899">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="b0c9c-1900">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1900">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="b0c9c-1901">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1901">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="b0c9c-1902">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1902">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0c9c-1903">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1903">CosmosDB</span></span>

* <span data-ttu-id="b0c9c-1904">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1904">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="b0c9c-1905">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1905">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b0c9c-1906">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1906">Data Lake Analytics</span></span>

* <span data-ttu-id="b0c9c-1907">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1907">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="b0c9c-1908">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1908">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="b0c9c-1909">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1909">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b0c9c-1910">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1910">Data Lake Store</span></span>

* <span data-ttu-id="b0c9c-1911">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1911">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="b0c9c-1912">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1912">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="b0c9c-1913">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1913">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="b0c9c-1914">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1914">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="b0c9c-1915">対話</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1915">Interactive</span></span>

* <span data-ttu-id="b0c9c-1916">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1916">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="b0c9c-1917">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1917">Increased test coverage</span></span>
* <span data-ttu-id="b0c9c-1918">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1918">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="b0c9c-1919">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1919">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="b0c9c-1920">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1920">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="b0c9c-1921">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1921">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="b0c9c-1922">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1922">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="b0c9c-1923">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1923">Added `--progress` flag</span></span>
* <span data-ttu-id="b0c9c-1924">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1924">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="b0c9c-1925">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1925">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="b0c9c-1926">IoT</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1926">IoT</span></span>

* <span data-ttu-id="b0c9c-1927">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1927">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="b0c9c-1928">(#3934)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1928">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="b0c9c-1929">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1929">Key vault</span></span>

* <span data-ttu-id="b0c9c-1930">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1930">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="b0c9c-1931">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1931">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="b0c9c-1932">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1932">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="b0c9c-1933">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1933">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="b0c9c-1934">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1934">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="b0c9c-1935">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1935">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="b0c9c-1936">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1936">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="b0c9c-1937">(#3307)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1937">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="b0c9c-1938">ラボ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1938">Lab</span></span>

* <span data-ttu-id="b0c9c-1939">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1939">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="b0c9c-1940">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1940">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-1941">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1941">Monitor</span></span>

* <span data-ttu-id="b0c9c-1942">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1942">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="b0c9c-1943">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1943">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="b0c9c-1944">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1944">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="b0c9c-1945">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1945">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="b0c9c-1946">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1946">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="b0c9c-1947">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1947">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="b0c9c-1948">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1948">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="b0c9c-1949">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1949">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="b0c9c-1950">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1950">`location` no longer required</span></span>
  * <span data-ttu-id="b0c9c-1951">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1951">Add name and ID support for target</span></span>
  * <span data-ttu-id="b0c9c-1952">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1952">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="b0c9c-1953">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1953">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="b0c9c-1954">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1954">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="b0c9c-1955">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1955">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="b0c9c-1956">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1956">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="b0c9c-1957">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1957">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-1958">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1958">Network</span></span>

* <span data-ttu-id="b0c9c-1959">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1959">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="b0c9c-1960">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1960">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="b0c9c-1961">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1961">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="b0c9c-1962">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1962">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="b0c9c-1963">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1963">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="b0c9c-1964">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1964">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="b0c9c-1965">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1965">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="b0c9c-1966">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1966">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="b0c9c-1967">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1967">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="b0c9c-1968">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1968">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="b0c9c-1969">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1969">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="b0c9c-1970">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1970">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="b0c9c-1971">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1971">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="b0c9c-1972">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1972">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="b0c9c-1973">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1973">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="b0c9c-1974">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1974">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="b0c9c-1975">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1975">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="b0c9c-1976">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1976">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="b0c9c-1977">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1977">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="b0c9c-1978">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1978">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="b0c9c-1979">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1979">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="b0c9c-1980">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1980">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="b0c9c-1981">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1981">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="b0c9c-1982">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1982">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="b0c9c-1983">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1983">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="b0c9c-1984">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1984">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="b0c9c-1985">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1985">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="b0c9c-1986">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1986">Profile</span></span>

* <span data-ttu-id="b0c9c-1987">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1987">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="b0c9c-1988">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1988">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="b0c9c-1989">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1989">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="b0c9c-1990">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1990">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="b0c9c-1991">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1991">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="b0c9c-1992">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1992">RDBMS</span></span>

* <span data-ttu-id="b0c9c-1993">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1993">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="b0c9c-1994">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1994">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="b0c9c-1995">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1995">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="b0c9c-1996">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1996">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-1997">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1997">Resource</span></span>

* <span data-ttu-id="b0c9c-1998">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1998">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="b0c9c-1999">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-1999">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="b0c9c-2000">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2000">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="b0c9c-2001">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2001">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="b0c9c-2002">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2002">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="b0c9c-2003">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2003">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="b0c9c-2004">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2004">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="b0c9c-2005">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2005">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-2006">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2006">Role</span></span>

* <span data-ttu-id="b0c9c-2007">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2007">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="b0c9c-2008">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2008">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="b0c9c-2009">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2009">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="b0c9c-2010">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2010">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="b0c9c-2011">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2011">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b0c9c-2012">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2012">Service Fabric</span></span>
* <span data-ttu-id="b0c9c-2013">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2013">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="b0c9c-2014">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2014">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="b0c9c-2015">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2015">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-2016">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2016">SQL</span></span>

* <span data-ttu-id="b0c9c-2017">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2017">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="b0c9c-2018">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2018">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="b0c9c-2019">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2019">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-2020">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2020">Storage</span></span>

* <span data-ttu-id="b0c9c-2021">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2021">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="b0c9c-2022">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2022">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="b0c9c-2023">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2023">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="b0c9c-2024">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2024">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="b0c9c-2025">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2025">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="b0c9c-2026">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2026">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-2027">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2027">VM</span></span>

* <span data-ttu-id="b0c9c-2028">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2028">Support configuring nsg</span></span>
* <span data-ttu-id="b0c9c-2029">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2029">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="b0c9c-2030">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2030">Support managed service identities</span></span>
* <span data-ttu-id="b0c9c-2031">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2031">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="b0c9c-2032">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2032">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="b0c9c-2033">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2033">May 10, 2017</span></span>

<span data-ttu-id="b0c9c-2034">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2034">Version 2.0.6</span></span>

* <span data-ttu-id="b0c9c-2035">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2035">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="b0c9c-2036">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2036">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="b0c9c-2037">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2037">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="b0c9c-2038">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2038">Include Cognitive Services module</span></span>
* <span data-ttu-id="b0c9c-2039">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2039">Include Service Fabric module</span></span>
* <span data-ttu-id="b0c9c-2040">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2040">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="b0c9c-2041">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2041">Add support for CDN commands</span></span>
* <span data-ttu-id="b0c9c-2042">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2042">Remove Container module</span></span>
* <span data-ttu-id="b0c9c-2043">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2043">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="b0c9c-2044">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2044">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="b0c9c-2045">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2045">Core</span></span>

* <span data-ttu-id="b0c9c-2046">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2046">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="b0c9c-2047">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2047">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="b0c9c-2048">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2048">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="b0c9c-2049">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2049">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="b0c9c-2050">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2050">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="b0c9c-2051">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2051">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="b0c9c-2052">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2052">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="b0c9c-2053">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2053">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="b0c9c-2054">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2054">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="b0c9c-2055">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2055">core: Improved performance</span></span>
* <span data-ttu-id="b0c9c-2056">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2056">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="b0c9c-2057">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2057">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-2058">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2058">ACS</span></span>

* <span data-ttu-id="b0c9c-2059">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2059">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="b0c9c-2060">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2060">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="b0c9c-2061">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2061">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="b0c9c-2062">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2062">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-2063">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2063">AppService</span></span>

* <span data-ttu-id="b0c9c-2064">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2064">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="b0c9c-2065">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2065">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="b0c9c-2066">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2066">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="b0c9c-2067">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2067">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="b0c9c-2068">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2068">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="b0c9c-2069">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2069">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="b0c9c-2070">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2070">support slot swap with preview</span></span>
* <span data-ttu-id="b0c9c-2071">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2071">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="b0c9c-2072">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2072">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b0c9c-2073">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2073">CosmosDB</span></span>

* <span data-ttu-id="b0c9c-2074">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2074">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="b0c9c-2075">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2075">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="b0c9c-2076">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2076">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="b0c9c-2077">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2077">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b0c9c-2078">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2078">Data Lake Analytics</span></span>

* <span data-ttu-id="b0c9c-2079">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2079">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="b0c9c-2080">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2080">Add support for new catalog item type: package.</span></span> <span data-ttu-id="b0c9c-2081">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2081">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="b0c9c-2082">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2082">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="b0c9c-2083">テーブル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2083">Table</span></span>
  * <span data-ttu-id="b0c9c-2084">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2084">Table valued function</span></span>
  * <span data-ttu-id="b0c9c-2085">表示</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2085">View</span></span>
  * <span data-ttu-id="b0c9c-2086">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2086">Table Statistics.</span></span> <span data-ttu-id="b0c9c-2087">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2087">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b0c9c-2088">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2088">Data Lake Store</span></span>

* <span data-ttu-id="b0c9c-2089">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2089">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="b0c9c-2090">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2090">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="b0c9c-2091">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2091">missed help for access show.</span></span> <span data-ttu-id="b0c9c-2092">追加しました </span><span class="sxs-lookup"><span data-stu-id="b0c9c-2092">adding it.</span></span> <span data-ttu-id="b0c9c-2093">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2093">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="b0c9c-2094">検索</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2094">Find</span></span>

* <span data-ttu-id="b0c9c-2095">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2095">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="b0c9c-2096">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2096">KeyVault</span></span>

* <span data-ttu-id="b0c9c-2097">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2097">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="b0c9c-2098">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2098">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="b0c9c-2099">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2099">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="b0c9c-2100">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2100">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="b0c9c-2101">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2101">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="b0c9c-2102">ラボ</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2102">Lab</span></span>

* <span data-ttu-id="b0c9c-2103">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2103">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="b0c9c-2104">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2104">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="b0c9c-2105">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2105">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="b0c9c-2106">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2106">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="b0c9c-2107">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2107">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="b0c9c-2108">監視</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2108">Monitor</span></span>

* <span data-ttu-id="b0c9c-2109">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2109">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="b0c9c-2110">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2110">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="b0c9c-2111">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2111">Network</span></span>

* <span data-ttu-id="b0c9c-2112">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2112">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="b0c9c-2113">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2113">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="b0c9c-2114">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2114">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="b0c9c-2115">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2115">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="b0c9c-2116">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2116">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="b0c9c-2117">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2117">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="b0c9c-2118">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2118">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="b0c9c-2119">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2119">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="b0c9c-2120">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2120">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="b0c9c-2121">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2121">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="b0c9c-2122">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2122">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="b0c9c-2123">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2123">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="b0c9c-2124">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2124">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="b0c9c-2125">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2125">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="b0c9c-2126">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2126">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="b0c9c-2127">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2127">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="b0c9c-2128">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2128">Profile</span></span>

* <span data-ttu-id="b0c9c-2129">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2129">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="b0c9c-2130">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2130">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="b0c9c-2131">Redis</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2131">Redis</span></span>

* <span data-ttu-id="b0c9c-2132">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2132">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="b0c9c-2133">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2133">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="b0c9c-2134">リソース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2134">Resource</span></span>

* <span data-ttu-id="b0c9c-2135">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2135">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="b0c9c-2136">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2136">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="b0c9c-2137">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2137">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="b0c9c-2138">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="b0c9c-2138">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="b0c9c-2139">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2139">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="b0c9c-2140">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="b0c9c-2140">Add docs for az lock update.</span></span> <span data-ttu-id="b0c9c-2141">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2141">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="b0c9c-2142">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="b0c9c-2142">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="b0c9c-2143">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2143">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="b0c9c-2144">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2144">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="b0c9c-2145">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2145">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="b0c9c-2146">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2146">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="b0c9c-2147">Role</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2147">Role</span></span>

* <span data-ttu-id="b0c9c-2148">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2148">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="b0c9c-2149">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2149">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="b0c9c-2150">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2150">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="b0c9c-2151">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2151">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="b0c9c-2152">SQL</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2152">SQL</span></span>

* <span data-ttu-id="b0c9c-2153">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2153">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="b0c9c-2154">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2154">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="b0c9c-2155">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2155">Storage</span></span>

* <span data-ttu-id="b0c9c-2156">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2156">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="b0c9c-2157">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2157">Add support for incremental blob copy</span></span>
* <span data-ttu-id="b0c9c-2158">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2158">Add support for large block blob upload</span></span>
* <span data-ttu-id="b0c9c-2159">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2159">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-2160">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2160">VM</span></span>

* <span data-ttu-id="b0c9c-2161">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2161">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="b0c9c-2162">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2162">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="b0c9c-2163">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2163">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="b0c9c-2164">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2164">az vm/vmss disk</span></span>
  3. <span data-ttu-id="b0c9c-2165">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2165">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="b0c9c-2166">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2166">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="b0c9c-2167">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2167">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="b0c9c-2168">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2168">April 3, 2017</span></span>

<span data-ttu-id="b0c9c-2169">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2169">Version 2.0.2</span></span>

<span data-ttu-id="b0c9c-2170">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2170">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="b0c9c-2171">コア</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2171">Core</span></span>

* <span data-ttu-id="b0c9c-2172">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2172">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="b0c9c-2173">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2173">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="b0c9c-2174">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2174">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="b0c9c-2175">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2175">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="b0c9c-2176">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2176">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="b0c9c-2177">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="b0c9c-2177">Add prompting for missing template parameters.</span></span> <span data-ttu-id="b0c9c-2178">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2178">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="b0c9c-2179">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2179">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="b0c9c-2180">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2180">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="b0c9c-2181">ACS</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2181">ACS</span></span>

* <span data-ttu-id="b0c9c-2182">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2182">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="b0c9c-2183">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="b0c9c-2183">Add support for ssh key password prompting.</span></span> <span data-ttu-id="b0c9c-2184">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2184">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="b0c9c-2185">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="b0c9c-2185">Add support for windows clusters.</span></span> <span data-ttu-id="b0c9c-2186">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2186">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="b0c9c-2187">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="b0c9c-2187">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="b0c9c-2188">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2188">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="b0c9c-2189">AppService</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2189">AppService</span></span>

* <span data-ttu-id="b0c9c-2190">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2190">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="b0c9c-2191">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2191">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="b0c9c-2192">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2192">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="b0c9c-2193">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2193">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="b0c9c-2194">DataLake</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2194">DataLake</span></span>

* <span data-ttu-id="b0c9c-2195">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2195">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="b0c9c-2196">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2196">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="b0c9c-2197">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2197">DocuemntDB</span></span>

* <span data-ttu-id="b0c9c-2198">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2198">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="b0c9c-2199">VM</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2199">VM</span></span>

* <span data-ttu-id="b0c9c-2200">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2200">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="b0c9c-2201">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2201">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="b0c9c-2202">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2202">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="b0c9c-2203">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2203">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="b0c9c-2204">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2204">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="b0c9c-2205">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2205">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="b0c9c-2206">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2206">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="b0c9c-2207">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2207">February 27, 2017</span></span>

<span data-ttu-id="b0c9c-2208">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2208">Version 2.0.0</span></span>

<span data-ttu-id="b0c9c-2209">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2209">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="b0c9c-2210">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2210">Container Service (acs)</span></span>
- <span data-ttu-id="b0c9c-2211">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2211">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="b0c9c-2212">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2212">Networking</span></span>
- <span data-ttu-id="b0c9c-2213">Storage</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2213">Storage</span></span>

<span data-ttu-id="b0c9c-2214">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2214">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="b0c9c-2215">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2215">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="b0c9c-2216">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2216">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="b0c9c-2217">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2217">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="b0c9c-2218">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2218">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="b0c9c-2219">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2219">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="b0c9c-2220">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2220">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="b0c9c-2221">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2221">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="b0c9c-2222">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="b0c9c-2222">Provide feedback from the command line with the `az feedback` command</span></span>

