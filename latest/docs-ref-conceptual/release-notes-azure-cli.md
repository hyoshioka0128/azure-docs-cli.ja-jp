---
title: "Azure CLI 2.0 リリース ノート"
description: "Azure CLI 2.0 の最新情報について説明します"
keywords: "Azure CLI 2.0, リリース ノート"
author: sptramer
ms.author: sttramer
manager: douge
ms.date: 04/03/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ce0428f7-0a59-4e72-9237-d907b171af51
ms.openlocfilehash: 72630c52b5e6afd69809ff19145717c0d65e0252
ms.sourcegitcommit: 3a490ae3a2a1b2e63a062806f9b720fa4c6be01e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="e335d-104">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="e335d-104">Azure CLI 2.0 release notes</span></span>

## <a name="september-22-2017"></a><span data-ttu-id="e335d-105">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="e335d-105">September 22, 2017</span></span>

<span data-ttu-id="e335d-106">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="e335d-106">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="e335d-107">リソース</span><span class="sxs-lookup"><span data-stu-id="e335d-107">Resource</span></span>

* <span data-ttu-id="e335d-108">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-108">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="e335d-109">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-109">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="e335d-110">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-110">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="e335d-111">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-111">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="e335d-112">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="e335d-112">Network</span></span>

* <span data-ttu-id="e335d-113">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-113">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="e335d-114">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-114">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="e335d-115">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-115">Added `asg` application security group commands</span></span>
* <span data-ttu-id="e335d-116">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-116">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="e335d-117">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-117">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="e335d-118">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-118">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="e335d-119">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-119">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="e335d-120">Storage</span><span class="sxs-lookup"><span data-stu-id="e335d-120">Storage</span></span>

* <span data-ttu-id="e335d-121">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-121">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="e335d-122">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="e335d-122">Eventgrid</span></span>

* <span data-ttu-id="e335d-123">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="e335d-123">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="e335d-124">SQL</span><span class="sxs-lookup"><span data-stu-id="e335d-124">SQL</span></span>

* <span data-ttu-id="e335d-125">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-125">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="e335d-126">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="e335d-126">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="e335d-127">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-127">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="e335d-128">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e335d-128">Keyvault</span></span>

* <span data-ttu-id="e335d-129">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-129">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="e335d-130">VM</span><span class="sxs-lookup"><span data-stu-id="e335d-130">VM</span></span>

* <span data-ttu-id="e335d-131">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-131">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="e335d-132">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-132">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="e335d-133">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-133">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="e335d-134">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-134">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="e335d-135">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-135">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="e335d-136">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-136">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="e335d-137">ACS</span><span class="sxs-lookup"><span data-stu-id="e335d-137">ACS</span></span>

* <span data-ttu-id="e335d-138">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-138">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="e335d-139">Appservice</span><span class="sxs-lookup"><span data-stu-id="e335d-139">Appservice</span></span>

* <span data-ttu-id="e335d-140">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-140">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="e335d-141">バックアップ</span><span class="sxs-lookup"><span data-stu-id="e335d-141">Backup</span></span>

* <span data-ttu-id="e335d-142">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="e335d-142">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="e335d-143">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="e335d-143">September 11, 2017</span></span>

<span data-ttu-id="e335d-144">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="e335d-144">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="e335d-145">コア</span><span class="sxs-lookup"><span data-stu-id="e335d-145">Core</span></span>

* <span data-ttu-id="e335d-146">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="e335d-146">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="e335d-147">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-147">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="e335d-148">ACS</span><span class="sxs-lookup"><span data-stu-id="e335d-148">Acs</span></span>

* <span data-ttu-id="e335d-149">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-149">Added `acs list-locations` command</span></span>
* <span data-ttu-id="e335d-150">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="e335d-150">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="e335d-151">Appservice</span><span class="sxs-lookup"><span data-stu-id="e335d-151">Appservice</span></span>

* <span data-ttu-id="e335d-152">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-152">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="e335d-153">CDN</span><span class="sxs-lookup"><span data-stu-id="e335d-153">CDN</span></span>

* <span data-ttu-id="e335d-154">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-154">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="e335d-155">内線番号</span><span class="sxs-lookup"><span data-stu-id="e335d-155">Extension</span></span>

* <span data-ttu-id="e335d-156">最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="e335d-156">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="e335d-157">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e335d-157">Keyvault</span></span>

* <span data-ttu-id="e335d-158">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-158">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="e335d-159">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="e335d-159">Network</span></span>

* <span data-ttu-id="e335d-160">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-160">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="e335d-161">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-161">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="e335d-162">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-162">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="e335d-163">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-163">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="e335d-164">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-164">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="e335d-165">リソース</span><span class="sxs-lookup"><span data-stu-id="e335d-165">Resource</span></span>

* <span data-ttu-id="e335d-166">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="e335d-166">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="e335d-167">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="e335d-167">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="e335d-168">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="e335d-168">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="e335d-169">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="e335d-169">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="e335d-170">SQL</span><span class="sxs-lookup"><span data-stu-id="e335d-170">SQL</span></span>

* <span data-ttu-id="e335d-171">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-171">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="e335d-172">VM</span><span class="sxs-lookup"><span data-stu-id="e335d-172">VM</span></span>

* <span data-ttu-id="e335d-173">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="e335d-173">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="e335d-174">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="e335d-174">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="e335d-175">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="e335d-175">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="e335d-176">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="e335d-176">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="e335d-177">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="e335d-177">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="e335d-178">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="e335d-178">August 31, 2017</span></span>

<span data-ttu-id="e335d-179">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="e335d-179">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="e335d-180">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e335d-180">Keyvault</span></span>

* <span data-ttu-id="e335d-181">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-181">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="e335d-182">SF</span><span class="sxs-lookup"><span data-stu-id="e335d-182">Sf</span></span>

* <span data-ttu-id="e335d-183">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="e335d-183">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="e335d-184">Storage</span><span class="sxs-lookup"><span data-stu-id="e335d-184">Storage</span></span>

* <span data-ttu-id="e335d-185">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-185">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="e335d-186">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="e335d-186">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="e335d-187">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="e335d-187">August 28, 2017</span></span>

<span data-ttu-id="e335d-188">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="e335d-188">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="e335d-189">CLI</span><span class="sxs-lookup"><span data-stu-id="e335d-189">CLI</span></span>

* <span data-ttu-id="e335d-190">`--version` に法的事項を追加しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-190">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="e335d-191">ACS</span><span class="sxs-lookup"><span data-stu-id="e335d-191">ACS</span></span>

* <span data-ttu-id="e335d-192">プレビュー リージョンを修正しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-192">Corrected preview regions.</span></span>
* <span data-ttu-id="e335d-193">既定の `dns_name_prefix` を正しい形式にしました。</span><span class="sxs-lookup"><span data-stu-id="e335d-193">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="e335d-194">ACS コマンド出力を最適化しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-194">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="e335d-195">Appservice</span><span class="sxs-lookup"><span data-stu-id="e335d-195">Appservice</span></span>

* <span data-ttu-id="e335d-196">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-196">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="e335d-197">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-197">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="e335d-198">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="e335d-198">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="e335d-199">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="e335d-199">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="e335d-200">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="e335d-200">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="e335d-201">IoT</span><span class="sxs-lookup"><span data-stu-id="e335d-201">IoT</span></span>

* <span data-ttu-id="e335d-202">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="e335d-202">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="e335d-203">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="e335d-203">Network</span></span>

* <span data-ttu-id="e335d-204">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-204">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="e335d-205">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-205">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="e335d-206">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-206">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="e335d-207">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-207">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="e335d-208">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-208">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="e335d-209">プロファイル</span><span class="sxs-lookup"><span data-stu-id="e335d-209">Profile</span></span>

* <span data-ttu-id="e335d-210">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="e335d-210">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="e335d-211">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e335d-211">Service Fabric</span></span>

* <span data-ttu-id="e335d-212">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="e335d-212">Preview release</span></span>
* <span data-ttu-id="e335d-213">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="e335d-213">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="e335d-214">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-214">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="e335d-215">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-215">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="e335d-216">Storage</span><span class="sxs-lookup"><span data-stu-id="e335d-216">Storage</span></span>

* <span data-ttu-id="e335d-217">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="e335d-217">Enabled setting blob tier</span></span>
* <span data-ttu-id="e335d-218">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-218">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="e335d-219">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-219">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="e335d-220">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="e335d-220">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="e335d-221">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-221">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="e335d-222">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="e335d-222">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="e335d-223">VM</span><span class="sxs-lookup"><span data-stu-id="e335d-223">VM</span></span>

* <span data-ttu-id="e335d-224">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-224">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="e335d-225">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-225">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="e335d-226">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="e335d-226">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="e335d-227">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-227">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="e335d-228">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-228">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="e335d-229">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-229">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="e335d-230">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="e335d-230">August 15, 2017</span></span>

<span data-ttu-id="e335d-231">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="e335d-231">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="e335d-232">ACS</span><span class="sxs-lookup"><span data-stu-id="e335d-232">ACS</span></span>

* <span data-ttu-id="e335d-233">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-233">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="e335d-234">Appservice</span><span class="sxs-lookup"><span data-stu-id="e335d-234">Appservice</span></span>

* <span data-ttu-id="e335d-235">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-235">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="e335d-236">Event Grid</span><span class="sxs-lookup"><span data-stu-id="e335d-236">Event Grid</span></span>

* <span data-ttu-id="e335d-237">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-237">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="e335d-238">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="e335d-238">August 11, 2017</span></span>

<span data-ttu-id="e335d-239">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="e335d-239">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="e335d-240">ACS</span><span class="sxs-lookup"><span data-stu-id="e335d-240">ACS</span></span>

* <span data-ttu-id="e335d-241">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-241">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="e335d-242">Batch
</span><span class="sxs-lookup"><span data-stu-id="e335d-242">Batch</span></span>

* <span data-ttu-id="e335d-243">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="e335d-243">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="e335d-244">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-244">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="e335d-245">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-245">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="e335d-246">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="e335d-246">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="e335d-247">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-247">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="e335d-248">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-248">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="e335d-249">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="e335d-249">Component</span></span>

* <span data-ttu-id="e335d-250">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-250">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="e335d-251">コンテナー</span><span class="sxs-lookup"><span data-stu-id="e335d-251">Container</span></span>

* <span data-ttu-id="e335d-252">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-252">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="e335d-253">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e335d-253">Data Lake Store</span></span>

* <span data-ttu-id="e335d-254">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="e335d-254">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="e335d-255">Event Grid</span><span class="sxs-lookup"><span data-stu-id="e335d-255">Event Grid</span></span>

* <span data-ttu-id="e335d-256">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="e335d-256">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="e335d-257">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="e335d-257">Network</span></span>

* <span data-ttu-id="e335d-258">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-258">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="e335d-259">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-259">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="e335d-260">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-260">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="e335d-261">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-261">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="e335d-262">プロファイル</span><span class="sxs-lookup"><span data-stu-id="e335d-262">Profile</span></span>

* <span data-ttu-id="e335d-263">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-263">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="e335d-264">Storage</span><span class="sxs-lookup"><span data-stu-id="e335d-264">Storage</span></span>

* <span data-ttu-id="e335d-265">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="e335d-265">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="e335d-266">VM</span><span class="sxs-lookup"><span data-stu-id="e335d-266">VM</span></span>

* <span data-ttu-id="e335d-267">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="e335d-267">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="e335d-268">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="e335d-268">Exposed `list-skus` command</span></span>
* <span data-ttu-id="e335d-269">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-269">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="e335d-270">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="e335d-270">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="e335d-271">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="e335d-271">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="e335d-272">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="e335d-272">July 28, 2017</span></span>

<span data-ttu-id="e335d-273">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="e335d-273">Version 2.0.12</span></span>

* <span data-ttu-id="e335d-274">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-274">Added container commands</span></span>
* <span data-ttu-id="e335d-275">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-275">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="e335d-276">コア</span><span class="sxs-lookup"><span data-stu-id="e335d-276">Core</span></span>

* <span data-ttu-id="e335d-277">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="e335d-277">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="e335d-278">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-278">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="e335d-279">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="e335d-279">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="e335d-280">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="e335d-280">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="e335d-281">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="e335d-281">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="e335d-282">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="e335d-282">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="e335d-283">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="e335d-283">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="e335d-284">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="e335d-284">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="e335d-285">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="e335d-285">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="e335d-286">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="e335d-286">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="e335d-287">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="e335d-287">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="e335d-288">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="e335d-288">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="e335d-289">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="e335d-289">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="e335d-290">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="e335d-290">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="e335d-291">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-291">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="e335d-292">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="e335d-292">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="e335d-293">ACR</span><span class="sxs-lookup"><span data-stu-id="e335d-293">ACR</span></span>

* <span data-ttu-id="e335d-294">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-294">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="e335d-295">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-295">Support SKU update for managed registries</span></span>
* <span data-ttu-id="e335d-296">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-296">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="e335d-297">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-297">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="e335d-298">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-298">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="e335d-299">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-299">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="e335d-300">ACS</span><span class="sxs-lookup"><span data-stu-id="e335d-300">ACS</span></span>

* <span data-ttu-id="e335d-301">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-301">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="e335d-302">Appservice</span><span class="sxs-lookup"><span data-stu-id="e335d-302">Appservice</span></span>

* <span data-ttu-id="e335d-303">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-303">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="e335d-304">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-304">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="e335d-305">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="e335d-305">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="e335d-306">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="e335d-306">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="e335d-307">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="e335d-307">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="e335d-308">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="e335d-308">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="e335d-309">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="e335d-309">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="e335d-310">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="e335d-310">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="e335d-311">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-311">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="e335d-312">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="e335d-312">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="e335d-313">Batch
</span><span class="sxs-lookup"><span data-stu-id="e335d-313">Batch</span></span>

* <span data-ttu-id="e335d-314">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="e335d-314">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="e335d-315">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-315">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="e335d-316">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-316">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="e335d-317">CDN</span><span class="sxs-lookup"><span data-stu-id="e335d-317">CDN</span></span>

* <span data-ttu-id="e335d-318">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-318">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="e335d-319">クラウド</span><span class="sxs-lookup"><span data-stu-id="e335d-319">Cloud</span></span>

* <span data-ttu-id="e335d-320">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-320">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="e335d-321">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="e335d-321">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="e335d-322">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-322">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="e335d-323">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="e335d-323">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="e335d-324">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="e335d-324">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="e335d-325">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="e335d-325">CosmosDB</span></span>

* <span data-ttu-id="e335d-326">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-326">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="e335d-327">既定のコレクション TTL のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-327">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="e335d-328">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="e335d-328">Data Lake Analytics</span></span>

* <span data-ttu-id="e335d-329">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-329">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="e335d-330">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-330">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="e335d-331">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-331">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="e335d-332">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e335d-332">Data Lake Store</span></span>

* <span data-ttu-id="e335d-333">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-333">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="e335d-334">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="e335d-334">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="e335d-335">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-335">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="e335d-336">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="e335d-336">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="e335d-337">対話</span><span class="sxs-lookup"><span data-stu-id="e335d-337">Interactive</span></span>

* <span data-ttu-id="e335d-338">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="e335d-338">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="e335d-339">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="e335d-339">Increased test coverage</span></span>
* <span data-ttu-id="e335d-340">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="e335d-340">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="e335d-341">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="e335d-341">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="e335d-342">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="e335d-342">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="e335d-343">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="e335d-343">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="e335d-344">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="e335d-344">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="e335d-345">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-345">Added `--progress` flag</span></span>
* <span data-ttu-id="e335d-346">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="e335d-346">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="e335d-347">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="e335d-347">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="e335d-348">IoT</span><span class="sxs-lookup"><span data-stu-id="e335d-348">IoT</span></span>

* <span data-ttu-id="e335d-349">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-349">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="e335d-350">(#3934)</span><span class="sxs-lookup"><span data-stu-id="e335d-350">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="e335d-351">Key Vault</span><span class="sxs-lookup"><span data-stu-id="e335d-351">Key vault</span></span>

* <span data-ttu-id="e335d-352">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-352">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="e335d-353">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="e335d-353">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="e335d-354">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="e335d-354">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="e335d-355">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="e335d-355">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="e335d-356">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="e335d-356">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="e335d-357">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="e335d-357">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="e335d-358">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-358">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="e335d-359">(#3307)</span><span class="sxs-lookup"><span data-stu-id="e335d-359">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="e335d-360">ラボ</span><span class="sxs-lookup"><span data-stu-id="e335d-360">Lab</span></span>

* <span data-ttu-id="e335d-361">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-361">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="e335d-362">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-362">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="e335d-363">監視</span><span class="sxs-lookup"><span data-stu-id="e335d-363">Monitor</span></span>

* <span data-ttu-id="e335d-364">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="e335d-364">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="e335d-365">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-365">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="e335d-366">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-366">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="e335d-367">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-367">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="e335d-368">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="e335d-368">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="e335d-369">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-369">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="e335d-370">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="e335d-370">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="e335d-371">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="e335d-371">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="e335d-372">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="e335d-372">`location` no longer required</span></span>
  * <span data-ttu-id="e335d-373">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="e335d-373">Add name and ID support for target</span></span>
  * <span data-ttu-id="e335d-374">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="e335d-374">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="e335d-375">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="e335d-375">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="e335d-376">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="e335d-376">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="e335d-377">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="e335d-377">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="e335d-378">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-378">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="e335d-379">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-379">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="e335d-380">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="e335d-380">Network</span></span>

* <span data-ttu-id="e335d-381">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-381">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="e335d-382">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-382">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="e335d-383">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-383">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="e335d-384">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-384">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="e335d-385">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-385">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="e335d-386">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-386">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="e335d-387">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-387">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="e335d-388">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-388">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="e335d-389">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-389">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="e335d-390">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-390">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="e335d-391">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-391">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="e335d-392">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-392">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="e335d-393">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-393">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="e335d-394">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-394">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="e335d-395">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-395">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="e335d-396">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="e335d-396">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="e335d-397">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-397">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="e335d-398">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-398">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="e335d-399">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-399">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="e335d-400">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-400">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="e335d-401">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-401">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="e335d-402">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-402">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="e335d-403">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="e335d-403">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="e335d-404">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="e335d-404">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="e335d-405">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="e335d-405">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="e335d-406">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="e335d-406">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="e335d-407">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="e335d-407">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="e335d-408">プロファイル</span><span class="sxs-lookup"><span data-stu-id="e335d-408">Profile</span></span>

* <span data-ttu-id="e335d-409">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-409">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="e335d-410">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-410">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="e335d-411">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="e335d-411">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="e335d-412">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-412">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="e335d-413">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-413">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="e335d-414">RDBMS</span><span class="sxs-lookup"><span data-stu-id="e335d-414">RDBMS</span></span>

* <span data-ttu-id="e335d-415">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="e335d-415">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="e335d-416">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="e335d-416">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="e335d-417">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="e335d-417">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="e335d-418">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="e335d-418">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="e335d-419">リソース</span><span class="sxs-lookup"><span data-stu-id="e335d-419">Resource</span></span>

* <span data-ttu-id="e335d-420">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="e335d-420">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="e335d-421">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="e335d-421">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="e335d-422">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-422">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="e335d-423">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-423">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="e335d-424">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="e335d-424">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="e335d-425">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-425">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="e335d-426">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="e335d-426">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="e335d-427">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-427">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="e335d-428">役割</span><span class="sxs-lookup"><span data-stu-id="e335d-428">Role</span></span>

* <span data-ttu-id="e335d-429">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-429">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="e335d-430">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="e335d-430">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="e335d-431">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="e335d-431">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="e335d-432">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="e335d-432">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="e335d-433">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-433">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="e335d-434">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e335d-434">Service Fabric</span></span>
* <span data-ttu-id="e335d-435">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="e335d-435">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="e335d-436">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="e335d-436">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="e335d-437">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="e335d-437">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="e335d-438">SQL</span><span class="sxs-lookup"><span data-stu-id="e335d-438">SQL</span></span>

* <span data-ttu-id="e335d-439">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="e335d-439">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="e335d-440">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="e335d-440">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="e335d-441">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="e335d-441">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="e335d-442">Storage</span><span class="sxs-lookup"><span data-stu-id="e335d-442">Storage</span></span>

* <span data-ttu-id="e335d-443">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="e335d-443">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="e335d-444">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="e335d-444">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="e335d-445">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="e335d-445">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="e335d-446">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="e335d-446">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="e335d-447">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="e335d-447">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="e335d-448">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="e335d-448">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="e335d-449">VM</span><span class="sxs-lookup"><span data-stu-id="e335d-449">VM</span></span>

* <span data-ttu-id="e335d-450">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-450">Support configuring nsg</span></span>
* <span data-ttu-id="e335d-451">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="e335d-451">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="e335d-452">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="e335d-452">Support managed service identities</span></span>
* <span data-ttu-id="e335d-453">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-453">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="e335d-454">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="e335d-454">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="e335d-455">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="e335d-455">May 10, 2017</span></span>

<span data-ttu-id="e335d-456">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="e335d-456">Version 2.0.6</span></span>

* <span data-ttu-id="e335d-457">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="e335d-457">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="e335d-458">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="e335d-458">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="e335d-459">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-459">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="e335d-460">Cognitive Services モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-460">Include Cognitive Services module.</span></span>
* <span data-ttu-id="e335d-461">Service Fabric モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-461">Include Service Fabric module.</span></span>
* <span data-ttu-id="e335d-462">対話型モジュールが追加されました (az-shell の名前変更)。</span><span class="sxs-lookup"><span data-stu-id="e335d-462">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="e335d-463">CDN コマンドに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e335d-463">Add support for CDN commands.</span></span>
* <span data-ttu-id="e335d-464">コンテナー モジュールが削除されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-464">Remove Container module.</span></span>
* <span data-ttu-id="e335d-465">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="e335d-465">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="e335d-466">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="e335d-466">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="e335d-467">コア</span><span class="sxs-lookup"><span data-stu-id="e335d-467">Core</span></span>

* <span data-ttu-id="e335d-468">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="e335d-468">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="e335d-469">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="e335d-469">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="e335d-470">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="e335d-470">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="e335d-471">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="e335d-471">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="e335d-472">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="e335d-472">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="e335d-473">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="e335d-473">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="e335d-474">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="e335d-474">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="e335d-475">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="e335d-475">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="e335d-476">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="e335d-476">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="e335d-477">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="e335d-477">core: Improved performance</span></span>
* <span data-ttu-id="e335d-478">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="e335d-478">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="e335d-479">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="e335d-479">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="e335d-480">ACS</span><span class="sxs-lookup"><span data-stu-id="e335d-480">ACS</span></span>

* <span data-ttu-id="e335d-481">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="e335d-481">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="e335d-482">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="e335d-482">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="e335d-483">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="e335d-483">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="e335d-484">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="e335d-484">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="e335d-485">AppService</span><span class="sxs-lookup"><span data-stu-id="e335d-485">AppService</span></span>

* <span data-ttu-id="e335d-486">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="e335d-486">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="e335d-487">Team Services (VSTS) が継続的な配信オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="e335d-487">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="e335d-488">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="e335d-488">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="e335d-489">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="e335d-489">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="e335d-490">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="e335d-490">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="e335d-491">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="e335d-491">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="e335d-492">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="e335d-492">support slot swap with preview</span></span>
* <span data-ttu-id="e335d-493">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="e335d-493">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="e335d-494">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="e335d-494">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="e335d-495">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e335d-495">CosmosDB</span></span>

* <span data-ttu-id="e335d-496">documentdb モジュールから cosmosdb に名前が変更されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-496">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="e335d-497">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="e335d-497">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="e335d-498">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="e335d-498">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="e335d-499">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="e335d-499">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="e335d-500">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="e335d-500">Data Lake Analytics</span></span>

* <span data-ttu-id="e335d-501">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-501">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="e335d-502">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e335d-502">Add support for new catalog item type: package.</span></span> <span data-ttu-id="e335d-503">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="e335d-503">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="e335d-504">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="e335d-504">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="e335d-505">テーブル</span><span class="sxs-lookup"><span data-stu-id="e335d-505">Table</span></span>
  * <span data-ttu-id="e335d-506">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="e335d-506">Table valued function</span></span>
  * <span data-ttu-id="e335d-507">表示</span><span class="sxs-lookup"><span data-stu-id="e335d-507">View</span></span>
  * <span data-ttu-id="e335d-508">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="e335d-508">Table Statistics.</span></span> <span data-ttu-id="e335d-509">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e335d-509">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="e335d-510">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e335d-510">Data Lake Store</span></span>

* <span data-ttu-id="e335d-511">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-511">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="e335d-512">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="e335d-512">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="e335d-513">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="e335d-513">missed help for access show.</span></span> <span data-ttu-id="e335d-514">追加しました </span><span class="sxs-lookup"><span data-stu-id="e335d-514">adding it.</span></span> <span data-ttu-id="e335d-515">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="e335d-515">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="e335d-516">検索</span><span class="sxs-lookup"><span data-stu-id="e335d-516">Find</span></span>

* <span data-ttu-id="e335d-517">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="e335d-517">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="e335d-518">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e335d-518">KeyVault</span></span>

* <span data-ttu-id="e335d-519">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="e335d-519">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="e335d-520">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-520">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="e335d-521">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="e335d-521">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="e335d-522">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-522">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="e335d-523">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="e335d-523">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="e335d-524">ラボ</span><span class="sxs-lookup"><span data-stu-id="e335d-524">Lab</span></span>

* <span data-ttu-id="e335d-525">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-525">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="e335d-526">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-526">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="e335d-527">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-527">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="e335d-528">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-528">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="e335d-529">ラボ内でシークレットを管理するためのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-529">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="e335d-530">監視</span><span class="sxs-lookup"><span data-stu-id="e335d-530">Monitor</span></span>

* <span data-ttu-id="e335d-531">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="e335d-531">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="e335d-532">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="e335d-532">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="e335d-533">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="e335d-533">Network</span></span>

* <span data-ttu-id="e335d-534">`network watcher test-connectivity` コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-534">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="e335d-535">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e335d-535">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="e335d-536">Application Gateway 接続のドレインに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e335d-536">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="e335d-537">Application Gateway WAF 規則セットの構成に対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e335d-537">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="e335d-538">ExpressRoute ルート フィルターとルールに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e335d-538">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="e335d-539">TrafficManager の地理的なルーティングに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e335d-539">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="e335d-540">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e335d-540">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="e335d-541">VPN 接続 IPSec ポリシーに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e335d-541">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="e335d-542">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-542">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="e335d-543">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="e335d-543">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="e335d-544">`network vpn-connection list/show` コマンドの出力から null 値が削除されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-544">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="e335d-545">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="e335d-545">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="e335d-546">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-546">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="e335d-547">`dns zone import` でレコードが適切にインポートされないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-547">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="e335d-548">`traffic-manager endpoint update` が動作しないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="e335d-548">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="e335d-549">"Network Watcher" プレビューのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-549">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="e335d-550">プロファイル</span><span class="sxs-lookup"><span data-stu-id="e335d-550">Profile</span></span>

* <span data-ttu-id="e335d-551">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="e335d-551">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="e335d-552">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="e335d-552">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="e335d-553">Redis</span><span class="sxs-lookup"><span data-stu-id="e335d-553">Redis</span></span>

* <span data-ttu-id="e335d-554">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="e335d-554">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="e335d-555">"update-settings" コマンドが廃止されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-555">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="e335d-556">リソース</span><span class="sxs-lookup"><span data-stu-id="e335d-556">Resource</span></span>

* <span data-ttu-id="e335d-557">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="e335d-557">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="e335d-558">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="e335d-558">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="e335d-559">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="e335d-559">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="e335d-560">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="e335d-560">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="e335d-561">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="e335d-561">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="e335d-562">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="e335d-562">Add docs for az lock update.</span></span> <span data-ttu-id="e335d-563">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="e335d-563">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="e335d-564">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="e335d-564">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="e335d-565">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="e335d-565">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="e335d-566">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-566">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="e335d-567">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="e335d-567">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="e335d-568">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="e335d-568">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="e335d-569">役割</span><span class="sxs-lookup"><span data-stu-id="e335d-569">Role</span></span>

* <span data-ttu-id="e335d-570">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="e335d-570">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="e335d-571">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="e335d-571">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="e335d-572">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="e335d-572">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="e335d-573">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="e335d-573">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="e335d-574">SQL</span><span class="sxs-lookup"><span data-stu-id="e335d-574">SQL</span></span>

* <span data-ttu-id="e335d-575">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e335d-575">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="e335d-576">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="e335d-576">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="e335d-577">Storage</span><span class="sxs-lookup"><span data-stu-id="e335d-577">Storage</span></span>

* <span data-ttu-id="e335d-578">`storage account create` のリソース グループの場所に対する既定の場所。</span><span class="sxs-lookup"><span data-stu-id="e335d-578">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="e335d-579">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="e335d-579">Add support for incremental blob copy</span></span>
* <span data-ttu-id="e335d-580">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="e335d-580">Add support for large block blob upload</span></span>
* <span data-ttu-id="e335d-581">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="e335d-581">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="e335d-582">VM</span><span class="sxs-lookup"><span data-stu-id="e335d-582">VM</span></span>

* <span data-ttu-id="e335d-583">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="e335d-583">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="e335d-584">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="e335d-584">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="e335d-585">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="e335d-585">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="e335d-586">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="e335d-586">az vm/vmss disk</span></span>
  3. <span data-ttu-id="e335d-587">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="e335d-587">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="e335d-588">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="e335d-588">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="e335d-589">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="e335d-589">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="e335d-590">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="e335d-590">April 3, 2017</span></span>

<span data-ttu-id="e335d-591">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="e335d-591">Version 2.0.2</span></span>

<span data-ttu-id="e335d-592">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました。</span><span class="sxs-lookup"><span data-stu-id="e335d-592">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="e335d-593">コア</span><span class="sxs-lookup"><span data-stu-id="e335d-593">Core</span></span>

* <span data-ttu-id="e335d-594">既定の一覧に acr、lab、monitor、find モジュールを追加。</span><span class="sxs-lookup"><span data-stu-id="e335d-594">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="e335d-595">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="e335d-595">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="e335d-596">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="e335d-596">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="e335d-597">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="e335d-597">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="e335d-598">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="e335d-598">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="e335d-599">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="e335d-599">Add prompting for missing template parameters.</span></span> <span data-ttu-id="e335d-600">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="e335d-600">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="e335d-601">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="e335d-601">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="e335d-602">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="e335d-602">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="e335d-603">ACS</span><span class="sxs-lookup"><span data-stu-id="e335d-603">ACS</span></span>

* <span data-ttu-id="e335d-604">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="e335d-604">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="e335d-605">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="e335d-605">Add support for ssh key password prompting.</span></span> <span data-ttu-id="e335d-606">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="e335d-606">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="e335d-607">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="e335d-607">Add support for windows clusters.</span></span> <span data-ttu-id="e335d-608">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="e335d-608">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="e335d-609">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="e335d-609">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="e335d-610">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="e335d-610">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="e335d-611">AppService</span><span class="sxs-lookup"><span data-stu-id="e335d-611">AppService</span></span>

* <span data-ttu-id="e335d-612">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="e335d-612">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="e335d-613">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="e335d-613">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="e335d-614">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="e335d-614">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="e335d-615">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="e335d-615">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="e335d-616">DataLake</span><span class="sxs-lookup"><span data-stu-id="e335d-616">DataLake</span></span>

* <span data-ttu-id="e335d-617">Data Lake Analytics モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="e335d-617">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="e335d-618">Data Lake Store モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="e335d-618">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="e335d-619">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="e335d-619">DocuemntDB</span></span>

* <span data-ttu-id="e335d-620">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="e335d-620">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="e335d-621">VM</span><span class="sxs-lookup"><span data-stu-id="e335d-621">VM</span></span>

* <span data-ttu-id="e335d-622">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="e335d-622">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="e335d-623">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="e335d-623">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="e335d-624">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="e335d-624">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="e335d-625">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="e335d-625">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="e335d-626">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート * ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="e335d-626">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="e335d-627">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="e335d-627">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="e335d-628">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="e335d-628">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="e335d-629">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="e335d-629">February 27, 2017</span></span>

<span data-ttu-id="e335d-630">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="e335d-630">Version 2.0.0</span></span>

<span data-ttu-id="e335d-631">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。</span><span class="sxs-lookup"><span data-stu-id="e335d-631">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="e335d-632">一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="e335d-632">General availability applies to these command modules:</span></span>
- <span data-ttu-id="e335d-633">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="e335d-633">Container Service (acs)</span></span>
- <span data-ttu-id="e335d-634">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="e335d-634">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="e335d-635">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="e335d-635">Networking</span></span>
- <span data-ttu-id="e335d-636">Storage</span><span class="sxs-lookup"><span data-stu-id="e335d-636">Storage</span></span>

<span data-ttu-id="e335d-637">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e335d-637">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="e335d-638">問題は、Microsoft サポートで直接開くことも、[github の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="e335d-638">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="e335d-639">[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="e335d-639">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="e335d-640">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません。</span><span class="sxs-lookup"><span data-stu-id="e335d-640">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="e335d-641">CLI のバージョンを確認するには、`az --version` を使用します。</span><span class="sxs-lookup"><span data-stu-id="e335d-641">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="e335d-642">出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="e335d-642">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="e335d-643">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。</span><span class="sxs-lookup"><span data-stu-id="e335d-643">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="e335d-644">これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です。</span><span class="sxs-lookup"><span data-stu-id="e335d-644">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="e335d-645">CLI のナイトリー プレビュー ビルドもあります。</span><span class="sxs-lookup"><span data-stu-id="e335d-645">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="e335d-646">詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e335d-646">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="e335d-647">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="e335d-647">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="e335d-648">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="e335d-648">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="e335d-649">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる。</span><span class="sxs-lookup"><span data-stu-id="e335d-649">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="e335d-650">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る。</span><span class="sxs-lookup"><span data-stu-id="e335d-650">Provide feedback from the command line with the `az feedback` command.</span></span>

