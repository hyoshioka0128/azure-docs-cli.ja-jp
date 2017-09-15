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
ms.openlocfilehash: ad30efeb7efafcc5816160ee130665d37adb62c6
ms.sourcegitcommit: e866977985ba0286fa05f41729dd7e7d9ce86f8e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="c831a-104">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="c831a-104">Azure CLI 2.0 release notes</span></span>

## <a name="september-11-2017"></a><span data-ttu-id="c831a-105">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="c831a-105">September 11, 2017</span></span>

<span data-ttu-id="c831a-106">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="c831a-106">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="c831a-107">コア</span><span class="sxs-lookup"><span data-stu-id="c831a-107">Core</span></span>

* <span data-ttu-id="c831a-108">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="c831a-108">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="c831a-109">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-109">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="c831a-110">ACS</span><span class="sxs-lookup"><span data-stu-id="c831a-110">Acs</span></span>

* <span data-ttu-id="c831a-111">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-111">Added `acs list-locations` command</span></span>
* <span data-ttu-id="c831a-112">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="c831a-112">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="c831a-113">Appservice</span><span class="sxs-lookup"><span data-stu-id="c831a-113">Appservice</span></span>

* <span data-ttu-id="c831a-114">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-114">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="c831a-115">CDN</span><span class="sxs-lookup"><span data-stu-id="c831a-115">CDN</span></span>

* <span data-ttu-id="c831a-116">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-116">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="c831a-117">内線番号</span><span class="sxs-lookup"><span data-stu-id="c831a-117">Extension</span></span>

* <span data-ttu-id="c831a-118">最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="c831a-118">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="c831a-119">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c831a-119">Keyvault</span></span>

* <span data-ttu-id="c831a-120">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-120">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="c831a-121">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c831a-121">Network</span></span>

* <span data-ttu-id="c831a-122">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-122">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="c831a-123">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-123">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="c831a-124">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-124">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="c831a-125">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-125">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="c831a-126">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-126">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="c831a-127">リソース</span><span class="sxs-lookup"><span data-stu-id="c831a-127">Resource</span></span>

* <span data-ttu-id="c831a-128">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="c831a-128">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="c831a-129">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="c831a-129">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="c831a-130">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="c831a-130">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="c831a-131">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="c831a-131">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="c831a-132">SQL</span><span class="sxs-lookup"><span data-stu-id="c831a-132">SQL</span></span>

* <span data-ttu-id="c831a-133">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-133">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="c831a-134">VM</span><span class="sxs-lookup"><span data-stu-id="c831a-134">VM</span></span>

* <span data-ttu-id="c831a-135">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="c831a-135">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="c831a-136">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="c831a-136">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="c831a-137">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c831a-137">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="c831a-138">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="c831a-138">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="c831a-139">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="c831a-139">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="c831a-140">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c831a-140">August 31, 2017</span></span>

<span data-ttu-id="c831a-141">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="c831a-141">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="c831a-142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c831a-142">Keyvault</span></span>

* <span data-ttu-id="c831a-143">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-143">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="c831a-144">SF</span><span class="sxs-lookup"><span data-stu-id="c831a-144">Sf</span></span>

* <span data-ttu-id="c831a-145">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="c831a-145">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="c831a-146">Storage</span><span class="sxs-lookup"><span data-stu-id="c831a-146">Storage</span></span>

* <span data-ttu-id="c831a-147">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-147">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="c831a-148">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="c831a-148">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="c831a-149">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="c831a-149">August 28, 2017</span></span>

<span data-ttu-id="c831a-150">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="c831a-150">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="c831a-151">CLI</span><span class="sxs-lookup"><span data-stu-id="c831a-151">CLI</span></span>

* <span data-ttu-id="c831a-152">`--version` に法的事項を追加しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-152">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="c831a-153">ACS</span><span class="sxs-lookup"><span data-stu-id="c831a-153">ACS</span></span>

* <span data-ttu-id="c831a-154">プレビュー リージョンを修正しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-154">Corrected preview regions.</span></span>
* <span data-ttu-id="c831a-155">既定の `dns_name_prefix` を正しい形式にしました。</span><span class="sxs-lookup"><span data-stu-id="c831a-155">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="c831a-156">ACS コマンド出力を最適化しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-156">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="c831a-157">Appservice</span><span class="sxs-lookup"><span data-stu-id="c831a-157">Appservice</span></span>

* <span data-ttu-id="c831a-158">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-158">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="c831a-159">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-159">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="c831a-160">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="c831a-160">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="c831a-161">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="c831a-161">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="c831a-162">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="c831a-162">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="c831a-163">IoT</span><span class="sxs-lookup"><span data-stu-id="c831a-163">IoT</span></span>

* <span data-ttu-id="c831a-164">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="c831a-164">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="c831a-165">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c831a-165">Network</span></span>

* <span data-ttu-id="c831a-166">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-166">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="c831a-167">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-167">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="c831a-168">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-168">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="c831a-169">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-169">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="c831a-170">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-170">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="c831a-171">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c831a-171">Profile</span></span>

* <span data-ttu-id="c831a-172">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="c831a-172">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="c831a-173">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c831a-173">Service Fabric</span></span>

* <span data-ttu-id="c831a-174">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="c831a-174">Preview release</span></span>
* <span data-ttu-id="c831a-175">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="c831a-175">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="c831a-176">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-176">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="c831a-177">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-177">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="c831a-178">Storage</span><span class="sxs-lookup"><span data-stu-id="c831a-178">Storage</span></span>

* <span data-ttu-id="c831a-179">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="c831a-179">Enabled setting blob tier</span></span>
* <span data-ttu-id="c831a-180">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-180">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="c831a-181">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-181">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="c831a-182">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="c831a-182">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="c831a-183">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-183">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="c831a-184">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="c831a-184">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="c831a-185">VM</span><span class="sxs-lookup"><span data-stu-id="c831a-185">VM</span></span>

* <span data-ttu-id="c831a-186">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-186">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="c831a-187">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-187">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="c831a-188">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="c831a-188">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="c831a-189">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-189">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="c831a-190">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-190">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="c831a-191">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-191">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="c831a-192">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="c831a-192">August 15, 2017</span></span>

<span data-ttu-id="c831a-193">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="c831a-193">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="c831a-194">ACS</span><span class="sxs-lookup"><span data-stu-id="c831a-194">ACS</span></span>

* <span data-ttu-id="c831a-195">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-195">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="c831a-196">Appservice</span><span class="sxs-lookup"><span data-stu-id="c831a-196">Appservice</span></span>

* <span data-ttu-id="c831a-197">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-197">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="c831a-198">Event Grid</span><span class="sxs-lookup"><span data-stu-id="c831a-198">Event Grid</span></span>

* <span data-ttu-id="c831a-199">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-199">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="c831a-200">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="c831a-200">August 11, 2017</span></span>

<span data-ttu-id="c831a-201">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="c831a-201">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="c831a-202">ACS</span><span class="sxs-lookup"><span data-stu-id="c831a-202">ACS</span></span>

* <span data-ttu-id="c831a-203">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-203">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="c831a-204">Batch
</span><span class="sxs-lookup"><span data-stu-id="c831a-204">Batch</span></span>

* <span data-ttu-id="c831a-205">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="c831a-205">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="c831a-206">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-206">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="c831a-207">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-207">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="c831a-208">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="c831a-208">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="c831a-209">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-209">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="c831a-210">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-210">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="c831a-211">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="c831a-211">Component</span></span>

* <span data-ttu-id="c831a-212">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-212">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="c831a-213">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c831a-213">Container</span></span>

* <span data-ttu-id="c831a-214">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-214">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="c831a-215">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c831a-215">Data Lake Store</span></span>

* <span data-ttu-id="c831a-216">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="c831a-216">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="c831a-217">Event Grid</span><span class="sxs-lookup"><span data-stu-id="c831a-217">Event Grid</span></span>

* <span data-ttu-id="c831a-218">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c831a-218">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="c831a-219">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c831a-219">Network</span></span>

* <span data-ttu-id="c831a-220">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-220">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="c831a-221">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-221">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="c831a-222">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-222">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="c831a-223">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-223">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="c831a-224">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c831a-224">Profile</span></span>

* <span data-ttu-id="c831a-225">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-225">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="c831a-226">Storage</span><span class="sxs-lookup"><span data-stu-id="c831a-226">Storage</span></span>

* <span data-ttu-id="c831a-227">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="c831a-227">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="c831a-228">VM</span><span class="sxs-lookup"><span data-stu-id="c831a-228">VM</span></span>

* <span data-ttu-id="c831a-229">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="c831a-229">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="c831a-230">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="c831a-230">Exposed `list-skus` command</span></span>
* <span data-ttu-id="c831a-231">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-231">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="c831a-232">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="c831a-232">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="c831a-233">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="c831a-233">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="c831a-234">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="c831a-234">July 28, 2017</span></span>

<span data-ttu-id="c831a-235">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="c831a-235">Version 2.0.12</span></span>

* <span data-ttu-id="c831a-236">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-236">Added container commands</span></span>
* <span data-ttu-id="c831a-237">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-237">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="c831a-238">コア</span><span class="sxs-lookup"><span data-stu-id="c831a-238">Core</span></span>

* <span data-ttu-id="c831a-239">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="c831a-239">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="c831a-240">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-240">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="c831a-241">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="c831a-241">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="c831a-242">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="c831a-242">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="c831a-243">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="c831a-243">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="c831a-244">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="c831a-244">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="c831a-245">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="c831a-245">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="c831a-246">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="c831a-246">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="c831a-247">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="c831a-247">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="c831a-248">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="c831a-248">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="c831a-249">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="c831a-249">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="c831a-250">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="c831a-250">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="c831a-251">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="c831a-251">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="c831a-252">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="c831a-252">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="c831a-253">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-253">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="c831a-254">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="c831a-254">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="c831a-255">ACR</span><span class="sxs-lookup"><span data-stu-id="c831a-255">ACR</span></span>

* <span data-ttu-id="c831a-256">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-256">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="c831a-257">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-257">Support SKU update for managed registries</span></span>
* <span data-ttu-id="c831a-258">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-258">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="c831a-259">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-259">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="c831a-260">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-260">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="c831a-261">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-261">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="c831a-262">ACS</span><span class="sxs-lookup"><span data-stu-id="c831a-262">ACS</span></span>

* <span data-ttu-id="c831a-263">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-263">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="c831a-264">Appservice</span><span class="sxs-lookup"><span data-stu-id="c831a-264">Appservice</span></span>

* <span data-ttu-id="c831a-265">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-265">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="c831a-266">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-266">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="c831a-267">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="c831a-267">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="c831a-268">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="c831a-268">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="c831a-269">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="c831a-269">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="c831a-270">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="c831a-270">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="c831a-271">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="c831a-271">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="c831a-272">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="c831a-272">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="c831a-273">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-273">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="c831a-274">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="c831a-274">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="c831a-275">Batch
</span><span class="sxs-lookup"><span data-stu-id="c831a-275">Batch</span></span>

* <span data-ttu-id="c831a-276">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="c831a-276">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="c831a-277">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-277">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="c831a-278">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-278">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="c831a-279">CDN</span><span class="sxs-lookup"><span data-stu-id="c831a-279">CDN</span></span>

* <span data-ttu-id="c831a-280">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-280">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="c831a-281">クラウド</span><span class="sxs-lookup"><span data-stu-id="c831a-281">Cloud</span></span>

* <span data-ttu-id="c831a-282">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-282">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="c831a-283">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="c831a-283">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="c831a-284">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-284">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="c831a-285">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="c831a-285">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="c831a-286">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="c831a-286">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c831a-287">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c831a-287">CosmosDB</span></span>

* <span data-ttu-id="c831a-288">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-288">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="c831a-289">既定のコレクション TTL のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-289">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="c831a-290">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="c831a-290">Data Lake Analytics</span></span>

* <span data-ttu-id="c831a-291">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-291">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="c831a-292">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-292">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="c831a-293">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-293">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="c831a-294">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c831a-294">Data Lake Store</span></span>

* <span data-ttu-id="c831a-295">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-295">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="c831a-296">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="c831a-296">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="c831a-297">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-297">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="c831a-298">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="c831a-298">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="c831a-299">対話</span><span class="sxs-lookup"><span data-stu-id="c831a-299">Interactive</span></span>

* <span data-ttu-id="c831a-300">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="c831a-300">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="c831a-301">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="c831a-301">Increased test coverage</span></span>
* <span data-ttu-id="c831a-302">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="c831a-302">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="c831a-303">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="c831a-303">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="c831a-304">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="c831a-304">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="c831a-305">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="c831a-305">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="c831a-306">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="c831a-306">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="c831a-307">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-307">Added `--progress` flag</span></span>
* <span data-ttu-id="c831a-308">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c831a-308">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="c831a-309">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="c831a-309">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="c831a-310">IoT</span><span class="sxs-lookup"><span data-stu-id="c831a-310">IoT</span></span>

* <span data-ttu-id="c831a-311">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-311">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="c831a-312">(#3934)</span><span class="sxs-lookup"><span data-stu-id="c831a-312">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="c831a-313">Key Vault</span><span class="sxs-lookup"><span data-stu-id="c831a-313">Key vault</span></span>

* <span data-ttu-id="c831a-314">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-314">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="c831a-315">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c831a-315">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="c831a-316">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c831a-316">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="c831a-317">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c831a-317">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="c831a-318">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c831a-318">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="c831a-319">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="c831a-319">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="c831a-320">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-320">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="c831a-321">(#3307)</span><span class="sxs-lookup"><span data-stu-id="c831a-321">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="c831a-322">ラボ</span><span class="sxs-lookup"><span data-stu-id="c831a-322">Lab</span></span>

* <span data-ttu-id="c831a-323">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-323">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="c831a-324">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-324">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="c831a-325">監視</span><span class="sxs-lookup"><span data-stu-id="c831a-325">Monitor</span></span>

* <span data-ttu-id="c831a-326">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="c831a-326">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="c831a-327">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-327">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="c831a-328">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-328">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="c831a-329">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-329">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="c831a-330">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c831a-330">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="c831a-331">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-331">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="c831a-332">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="c831a-332">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="c831a-333">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="c831a-333">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="c831a-334">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="c831a-334">`location` no longer required</span></span>
  * <span data-ttu-id="c831a-335">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="c831a-335">Add name and ID support for target</span></span>
  * <span data-ttu-id="c831a-336">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="c831a-336">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="c831a-337">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="c831a-337">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="c831a-338">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="c831a-338">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="c831a-339">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="c831a-339">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="c831a-340">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-340">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="c831a-341">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-341">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="c831a-342">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c831a-342">Network</span></span>

* <span data-ttu-id="c831a-343">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-343">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="c831a-344">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-344">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="c831a-345">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-345">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="c831a-346">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-346">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="c831a-347">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-347">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="c831a-348">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-348">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="c831a-349">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-349">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="c831a-350">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-350">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="c831a-351">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-351">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="c831a-352">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-352">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="c831a-353">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-353">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="c831a-354">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-354">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="c831a-355">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-355">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="c831a-356">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-356">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="c831a-357">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-357">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="c831a-358">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="c831a-358">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="c831a-359">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-359">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="c831a-360">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-360">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="c831a-361">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-361">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="c831a-362">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-362">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="c831a-363">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-363">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="c831a-364">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-364">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="c831a-365">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="c831a-365">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="c831a-366">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="c831a-366">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="c831a-367">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="c831a-367">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="c831a-368">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="c831a-368">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="c831a-369">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="c831a-369">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="c831a-370">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c831a-370">Profile</span></span>

* <span data-ttu-id="c831a-371">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-371">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="c831a-372">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-372">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="c831a-373">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="c831a-373">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="c831a-374">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-374">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="c831a-375">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-375">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="c831a-376">RDBMS</span><span class="sxs-lookup"><span data-stu-id="c831a-376">RDBMS</span></span>

* <span data-ttu-id="c831a-377">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="c831a-377">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="c831a-378">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="c831a-378">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="c831a-379">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="c831a-379">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="c831a-380">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="c831a-380">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="c831a-381">リソース</span><span class="sxs-lookup"><span data-stu-id="c831a-381">Resource</span></span>

* <span data-ttu-id="c831a-382">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="c831a-382">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="c831a-383">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="c831a-383">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="c831a-384">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-384">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="c831a-385">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-385">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="c831a-386">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="c831a-386">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="c831a-387">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-387">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="c831a-388">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="c831a-388">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="c831a-389">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-389">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="c831a-390">役割</span><span class="sxs-lookup"><span data-stu-id="c831a-390">Role</span></span>

* <span data-ttu-id="c831a-391">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-391">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="c831a-392">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="c831a-392">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="c831a-393">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="c831a-393">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="c831a-394">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="c831a-394">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="c831a-395">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-395">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="c831a-396">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c831a-396">Service Fabric</span></span>
* <span data-ttu-id="c831a-397">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="c831a-397">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="c831a-398">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="c831a-398">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="c831a-399">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="c831a-399">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="c831a-400">SQL</span><span class="sxs-lookup"><span data-stu-id="c831a-400">SQL</span></span>

* <span data-ttu-id="c831a-401">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="c831a-401">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="c831a-402">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="c831a-402">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="c831a-403">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c831a-403">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="c831a-404">Storage</span><span class="sxs-lookup"><span data-stu-id="c831a-404">Storage</span></span>

* <span data-ttu-id="c831a-405">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="c831a-405">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="c831a-406">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="c831a-406">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="c831a-407">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="c831a-407">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="c831a-408">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="c831a-408">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="c831a-409">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="c831a-409">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="c831a-410">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="c831a-410">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="c831a-411">VM</span><span class="sxs-lookup"><span data-stu-id="c831a-411">VM</span></span>

* <span data-ttu-id="c831a-412">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-412">Support configuring nsg</span></span>
* <span data-ttu-id="c831a-413">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c831a-413">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="c831a-414">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="c831a-414">Support managed service identities</span></span>
* <span data-ttu-id="c831a-415">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-415">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="c831a-416">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="c831a-416">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="c831a-417">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="c831a-417">May 10, 2017</span></span>

<span data-ttu-id="c831a-418">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="c831a-418">Version 2.0.6</span></span>

* <span data-ttu-id="c831a-419">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="c831a-419">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="c831a-420">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="c831a-420">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="c831a-421">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-421">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="c831a-422">Cognitive Services モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-422">Include Cognitive Services module.</span></span>
* <span data-ttu-id="c831a-423">Service Fabric モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-423">Include Service Fabric module.</span></span>
* <span data-ttu-id="c831a-424">対話型モジュールが追加されました (az-shell の名前変更)。</span><span class="sxs-lookup"><span data-stu-id="c831a-424">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="c831a-425">CDN コマンドに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="c831a-425">Add support for CDN commands.</span></span>
* <span data-ttu-id="c831a-426">コンテナー モジュールが削除されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-426">Remove Container module.</span></span>
* <span data-ttu-id="c831a-427">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="c831a-427">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="c831a-428">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="c831a-428">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="c831a-429">コア</span><span class="sxs-lookup"><span data-stu-id="c831a-429">Core</span></span>

* <span data-ttu-id="c831a-430">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="c831a-430">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="c831a-431">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="c831a-431">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="c831a-432">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="c831a-432">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="c831a-433">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="c831a-433">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="c831a-434">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="c831a-434">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="c831a-435">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="c831a-435">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="c831a-436">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="c831a-436">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="c831a-437">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="c831a-437">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="c831a-438">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="c831a-438">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="c831a-439">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="c831a-439">core: Improved performance</span></span>
* <span data-ttu-id="c831a-440">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="c831a-440">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="c831a-441">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="c831a-441">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="c831a-442">ACS</span><span class="sxs-lookup"><span data-stu-id="c831a-442">ACS</span></span>

* <span data-ttu-id="c831a-443">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="c831a-443">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="c831a-444">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="c831a-444">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="c831a-445">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="c831a-445">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="c831a-446">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="c831a-446">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="c831a-447">AppService</span><span class="sxs-lookup"><span data-stu-id="c831a-447">AppService</span></span>

* <span data-ttu-id="c831a-448">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c831a-448">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="c831a-449">Team Services (VSTS) が継続的な配信オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="c831a-449">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="c831a-450">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="c831a-450">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="c831a-451">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="c831a-451">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="c831a-452">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="c831a-452">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="c831a-453">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="c831a-453">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="c831a-454">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="c831a-454">support slot swap with preview</span></span>
* <span data-ttu-id="c831a-455">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="c831a-455">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="c831a-456">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="c831a-456">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c831a-457">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c831a-457">CosmosDB</span></span>

* <span data-ttu-id="c831a-458">documentdb モジュールから cosmosdb に名前が変更されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-458">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="c831a-459">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c831a-459">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="c831a-460">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c831a-460">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="c831a-461">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c831a-461">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="c831a-462">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="c831a-462">Data Lake Analytics</span></span>

* <span data-ttu-id="c831a-463">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-463">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="c831a-464">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="c831a-464">Add support for new catalog item type: package.</span></span> <span data-ttu-id="c831a-465">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="c831a-465">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="c831a-466">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="c831a-466">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="c831a-467">テーブル</span><span class="sxs-lookup"><span data-stu-id="c831a-467">Table</span></span>
  * <span data-ttu-id="c831a-468">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="c831a-468">Table valued function</span></span>
  * <span data-ttu-id="c831a-469">表示</span><span class="sxs-lookup"><span data-stu-id="c831a-469">View</span></span>
  * <span data-ttu-id="c831a-470">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="c831a-470">Table Statistics.</span></span> <span data-ttu-id="c831a-471">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c831a-471">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="c831a-472">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c831a-472">Data Lake Store</span></span>

* <span data-ttu-id="c831a-473">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-473">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="c831a-474">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="c831a-474">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="c831a-475">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="c831a-475">missed help for access show.</span></span> <span data-ttu-id="c831a-476">追加しました </span><span class="sxs-lookup"><span data-stu-id="c831a-476">adding it.</span></span> <span data-ttu-id="c831a-477">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="c831a-477">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="c831a-478">検索</span><span class="sxs-lookup"><span data-stu-id="c831a-478">Find</span></span>

* <span data-ttu-id="c831a-479">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="c831a-479">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="c831a-480">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c831a-480">KeyVault</span></span>

* <span data-ttu-id="c831a-481">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="c831a-481">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="c831a-482">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-482">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="c831a-483">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="c831a-483">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="c831a-484">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-484">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="c831a-485">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="c831a-485">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="c831a-486">ラボ</span><span class="sxs-lookup"><span data-stu-id="c831a-486">Lab</span></span>

* <span data-ttu-id="c831a-487">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-487">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="c831a-488">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-488">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="c831a-489">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-489">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="c831a-490">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-490">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="c831a-491">ラボ内でシークレットを管理するためのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-491">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="c831a-492">監視</span><span class="sxs-lookup"><span data-stu-id="c831a-492">Monitor</span></span>

* <span data-ttu-id="c831a-493">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="c831a-493">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="c831a-494">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="c831a-494">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="c831a-495">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c831a-495">Network</span></span>

* <span data-ttu-id="c831a-496">`network watcher test-connectivity` コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-496">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="c831a-497">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="c831a-497">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="c831a-498">Application Gateway 接続のドレインに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="c831a-498">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="c831a-499">Application Gateway WAF 規則セットの構成に対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="c831a-499">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="c831a-500">ExpressRoute ルート フィルターとルールに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="c831a-500">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="c831a-501">TrafficManager の地理的なルーティングに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="c831a-501">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="c831a-502">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="c831a-502">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="c831a-503">VPN 接続 IPSec ポリシーに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="c831a-503">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="c831a-504">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-504">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="c831a-505">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c831a-505">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="c831a-506">`network vpn-connection list/show` コマンドの出力から null 値が削除されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-506">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="c831a-507">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="c831a-507">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="c831a-508">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-508">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="c831a-509">`dns zone import` でレコードが適切にインポートされないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-509">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="c831a-510">`traffic-manager endpoint update` が動作しないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="c831a-510">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="c831a-511">"Network Watcher" プレビューのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-511">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="c831a-512">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c831a-512">Profile</span></span>

* <span data-ttu-id="c831a-513">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="c831a-513">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="c831a-514">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="c831a-514">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="c831a-515">Redis</span><span class="sxs-lookup"><span data-stu-id="c831a-515">Redis</span></span>

* <span data-ttu-id="c831a-516">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="c831a-516">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="c831a-517">"update-settings" コマンドが廃止されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-517">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="c831a-518">リソース</span><span class="sxs-lookup"><span data-stu-id="c831a-518">Resource</span></span>

* <span data-ttu-id="c831a-519">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="c831a-519">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="c831a-520">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="c831a-520">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="c831a-521">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="c831a-521">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="c831a-522">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="c831a-522">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="c831a-523">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="c831a-523">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="c831a-524">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="c831a-524">Add docs for az lock update.</span></span> <span data-ttu-id="c831a-525">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="c831a-525">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="c831a-526">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="c831a-526">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="c831a-527">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="c831a-527">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="c831a-528">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-528">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="c831a-529">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="c831a-529">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="c831a-530">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="c831a-530">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="c831a-531">役割</span><span class="sxs-lookup"><span data-stu-id="c831a-531">Role</span></span>

* <span data-ttu-id="c831a-532">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="c831a-532">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="c831a-533">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="c831a-533">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="c831a-534">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="c831a-534">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="c831a-535">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="c831a-535">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="c831a-536">SQL</span><span class="sxs-lookup"><span data-stu-id="c831a-536">SQL</span></span>

* <span data-ttu-id="c831a-537">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c831a-537">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="c831a-538">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="c831a-538">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="c831a-539">Storage</span><span class="sxs-lookup"><span data-stu-id="c831a-539">Storage</span></span>

* <span data-ttu-id="c831a-540">`storage account create` のリソース グループの場所に対する既定の場所。</span><span class="sxs-lookup"><span data-stu-id="c831a-540">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="c831a-541">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c831a-541">Add support for incremental blob copy</span></span>
* <span data-ttu-id="c831a-542">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c831a-542">Add support for large block blob upload</span></span>
* <span data-ttu-id="c831a-543">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="c831a-543">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="c831a-544">VM</span><span class="sxs-lookup"><span data-stu-id="c831a-544">VM</span></span>

* <span data-ttu-id="c831a-545">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="c831a-545">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="c831a-546">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="c831a-546">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="c831a-547">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="c831a-547">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="c831a-548">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="c831a-548">az vm/vmss disk</span></span>
  3. <span data-ttu-id="c831a-549">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="c831a-549">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="c831a-550">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="c831a-550">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="c831a-551">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="c831a-551">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="c831a-552">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="c831a-552">April 3, 2017</span></span>

<span data-ttu-id="c831a-553">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="c831a-553">Version 2.0.2</span></span>

<span data-ttu-id="c831a-554">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました。</span><span class="sxs-lookup"><span data-stu-id="c831a-554">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="c831a-555">コア</span><span class="sxs-lookup"><span data-stu-id="c831a-555">Core</span></span>

* <span data-ttu-id="c831a-556">既定の一覧に acr、lab、monitor、find モジュールを追加。</span><span class="sxs-lookup"><span data-stu-id="c831a-556">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="c831a-557">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="c831a-557">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="c831a-558">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="c831a-558">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="c831a-559">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="c831a-559">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="c831a-560">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="c831a-560">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="c831a-561">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="c831a-561">Add prompting for missing template parameters.</span></span> <span data-ttu-id="c831a-562">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="c831a-562">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="c831a-563">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="c831a-563">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="c831a-564">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="c831a-564">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="c831a-565">ACS</span><span class="sxs-lookup"><span data-stu-id="c831a-565">ACS</span></span>

* <span data-ttu-id="c831a-566">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="c831a-566">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="c831a-567">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="c831a-567">Add support for ssh key password prompting.</span></span> <span data-ttu-id="c831a-568">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="c831a-568">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="c831a-569">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="c831a-569">Add support for windows clusters.</span></span> <span data-ttu-id="c831a-570">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="c831a-570">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="c831a-571">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="c831a-571">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="c831a-572">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="c831a-572">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="c831a-573">AppService</span><span class="sxs-lookup"><span data-stu-id="c831a-573">AppService</span></span>

* <span data-ttu-id="c831a-574">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="c831a-574">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="c831a-575">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="c831a-575">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="c831a-576">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="c831a-576">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="c831a-577">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="c831a-577">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="c831a-578">DataLake</span><span class="sxs-lookup"><span data-stu-id="c831a-578">DataLake</span></span>

* <span data-ttu-id="c831a-579">Data Lake Analytics モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="c831a-579">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="c831a-580">Data Lake Store モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="c831a-580">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="c831a-581">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="c831a-581">DocuemntDB</span></span>

* <span data-ttu-id="c831a-582">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="c831a-582">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="c831a-583">VM</span><span class="sxs-lookup"><span data-stu-id="c831a-583">VM</span></span>

* <span data-ttu-id="c831a-584">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="c831a-584">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="c831a-585">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="c831a-585">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="c831a-586">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="c831a-586">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="c831a-587">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="c831a-587">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="c831a-588">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート * ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="c831a-588">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="c831a-589">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="c831a-589">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="c831a-590">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="c831a-590">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="c831a-591">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="c831a-591">February 27, 2017</span></span>

<span data-ttu-id="c831a-592">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="c831a-592">Version 2.0.0</span></span>

<span data-ttu-id="c831a-593">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。</span><span class="sxs-lookup"><span data-stu-id="c831a-593">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="c831a-594">一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="c831a-594">General availability applies to these command modules:</span></span>
- <span data-ttu-id="c831a-595">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="c831a-595">Container Service (acs)</span></span>
- <span data-ttu-id="c831a-596">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="c831a-596">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="c831a-597">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c831a-597">Networking</span></span>
- <span data-ttu-id="c831a-598">Storage</span><span class="sxs-lookup"><span data-stu-id="c831a-598">Storage</span></span>

<span data-ttu-id="c831a-599">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c831a-599">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="c831a-600">問題は、Microsoft サポートで直接開くことも、[github の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="c831a-600">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="c831a-601">[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="c831a-601">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="c831a-602">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません。</span><span class="sxs-lookup"><span data-stu-id="c831a-602">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="c831a-603">CLI のバージョンを確認するには、`az --version` を使用します。</span><span class="sxs-lookup"><span data-stu-id="c831a-603">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="c831a-604">出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="c831a-604">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="c831a-605">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。</span><span class="sxs-lookup"><span data-stu-id="c831a-605">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="c831a-606">これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です。</span><span class="sxs-lookup"><span data-stu-id="c831a-606">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="c831a-607">CLI のナイトリー プレビュー ビルドもあります。</span><span class="sxs-lookup"><span data-stu-id="c831a-607">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="c831a-608">詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c831a-608">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="c831a-609">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="c831a-609">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="c831a-610">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="c831a-610">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="c831a-611">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる。</span><span class="sxs-lookup"><span data-stu-id="c831a-611">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="c831a-612">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る。</span><span class="sxs-lookup"><span data-stu-id="c831a-612">Provide feedback from the command line with the `az feedback` command.</span></span>

