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
ms.openlocfilehash: e02b84891f4bf60cde12591b8e85987f4b3c9e79
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/09/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="67161-104">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="67161-104">Azure CLI 2.0 release notes</span></span>

## <a name="december-5-2017"></a><span data-ttu-id="67161-105">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="67161-105">December 5, 2017</span></span>

<span data-ttu-id="67161-106">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="67161-106">Version 2.0.22</span></span>

* <span data-ttu-id="67161-107">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="67161-107">Removed `az component` commands.</span></span> <span data-ttu-id="67161-108">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="67161-108">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="67161-109">コア</span><span class="sxs-lookup"><span data-stu-id="67161-109">Core</span></span>
* <span data-ttu-id="67161-110">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-110">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="67161-111">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-111">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="67161-112">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-112">ACS</span></span>

* <span data-ttu-id="67161-113">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-113">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="67161-114">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="67161-114">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="67161-115">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-115">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="67161-116">Advisor</span><span class="sxs-lookup"><span data-stu-id="67161-116">Advisor</span></span>

* <span data-ttu-id="67161-117">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="67161-117">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-118">Appservice</span><span class="sxs-lookup"><span data-stu-id="67161-118">Appservice</span></span>

* <span data-ttu-id="67161-119">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-119">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="67161-120">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-120">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="67161-121">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-121">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="67161-122">使用量</span><span class="sxs-lookup"><span data-stu-id="67161-122">Consumption</span></span>

* <span data-ttu-id="67161-123">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-123">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="67161-124">コンテナー</span><span class="sxs-lookup"><span data-stu-id="67161-124">Container</span></span>

* <span data-ttu-id="67161-125">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-125">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="67161-126">監視</span><span class="sxs-lookup"><span data-stu-id="67161-126">Monitor</span></span>

* <span data-ttu-id="67161-127">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-127">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="67161-128">リソース</span><span class="sxs-lookup"><span data-stu-id="67161-128">Resource</span></span>

* <span data-ttu-id="67161-129">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-129">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="67161-130">役割</span><span class="sxs-lookup"><span data-stu-id="67161-130">Role</span></span>

* <span data-ttu-id="67161-131">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-131">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="67161-132">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="67161-132">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="67161-133">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="67161-133">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="67161-134">SQL</span><span class="sxs-lookup"><span data-stu-id="67161-134">SQL</span></span>

* <span data-ttu-id="67161-135">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-135">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="67161-136">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-136">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="67161-137">VM</span><span class="sxs-lookup"><span data-stu-id="67161-137">VM</span></span>

* <span data-ttu-id="67161-138">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-138">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="67161-139">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="67161-139">November 14, 2017</span></span>

<span data-ttu-id="67161-140">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="67161-140">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="67161-141">ACR</span><span class="sxs-lookup"><span data-stu-id="67161-141">ACR</span></span>

* <span data-ttu-id="67161-142">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-142">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="67161-143">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-143">ACS</span></span>

* <span data-ttu-id="67161-144">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-144">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="67161-145">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="67161-145">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="67161-146">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-146">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="67161-147">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-147">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="67161-148">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-148">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-149">Appservice</span><span class="sxs-lookup"><span data-stu-id="67161-149">Appservice</span></span>

* <span data-ttu-id="67161-150">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-150">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="67161-151">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-151">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="67161-152">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="67161-152">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="67161-153">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="67161-153">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="67161-154">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-154">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="67161-155">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="67161-155">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="67161-156">Batch</span><span class="sxs-lookup"><span data-stu-id="67161-156">Batch</span></span>

* <span data-ttu-id="67161-157">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-157">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="67161-158">Batchai</span><span class="sxs-lookup"><span data-stu-id="67161-158">Batchai</span></span>

* <span data-ttu-id="67161-159">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-159">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="67161-160">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-160">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="67161-161">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-161">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="67161-162">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-162">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="67161-163">クラウド</span><span class="sxs-lookup"><span data-stu-id="67161-163">Cloud</span></span>

* <span data-ttu-id="67161-164">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-164">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="67161-165">コンテナー</span><span class="sxs-lookup"><span data-stu-id="67161-165">Container</span></span>

* <span data-ttu-id="67161-166">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-166">Added support to open multiple ports</span></span>
* <span data-ttu-id="67161-167">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-167">Added container group restart policy</span></span>
* <span data-ttu-id="67161-168">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-168">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="67161-169">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="67161-169">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="67161-170">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="67161-170">Data Lake Analytics</span></span>

* <span data-ttu-id="67161-171">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-171">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="67161-172">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="67161-172">Data Lake Store</span></span>

* <span data-ttu-id="67161-173">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-173">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="67161-174">内線番号</span><span class="sxs-lookup"><span data-stu-id="67161-174">Extension</span></span>

* <span data-ttu-id="67161-175">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-175">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="67161-176">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-176">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="67161-177">IoT</span><span class="sxs-lookup"><span data-stu-id="67161-177">IoT</span></span>

* <span data-ttu-id="67161-178">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-178">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="67161-179">監視</span><span class="sxs-lookup"><span data-stu-id="67161-179">Monitor</span></span>

* <span data-ttu-id="67161-180">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-180">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="67161-181">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="67161-181">Network</span></span>

* <span data-ttu-id="67161-182">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-182">Added support for CAA DNS records</span></span>
* <span data-ttu-id="67161-183">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-183">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="67161-184">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-184">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="67161-185">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-185">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="67161-186">Reservations</span><span class="sxs-lookup"><span data-stu-id="67161-186">Reservations</span></span>

* <span data-ttu-id="67161-187">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="67161-187">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="67161-188">リソース</span><span class="sxs-lookup"><span data-stu-id="67161-188">Resource</span></span>

* <span data-ttu-id="67161-189">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-189">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="67161-190">SQL</span><span class="sxs-lookup"><span data-stu-id="67161-190">SQL</span></span>

* <span data-ttu-id="67161-191">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-191">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="67161-192">ストレージ</span><span class="sxs-lookup"><span data-stu-id="67161-192">Storage</span></span>

* <span data-ttu-id="67161-193">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-193">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="67161-194">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-194">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="67161-195">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-195">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="67161-196">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-196">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="67161-197">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-197">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="67161-198">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-198">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="67161-199">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-199">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="67161-200">VM</span><span class="sxs-lookup"><span data-stu-id="67161-200">VM</span></span>

* <span data-ttu-id="67161-201">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-201">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="67161-202">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-202">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="67161-203">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-203">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="67161-204">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-204">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="67161-205">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-205">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="67161-206">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="67161-206">October 24, 2017</span></span>

<span data-ttu-id="67161-207">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="67161-207">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="67161-208">コア</span><span class="sxs-lookup"><span data-stu-id="67161-208">Core</span></span>

* <span data-ttu-id="67161-209">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="67161-209">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="67161-210">ACR</span><span class="sxs-lookup"><span data-stu-id="67161-210">ACR</span></span>

* <span data-ttu-id="67161-211">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="67161-211">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="67161-212">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-212">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="67161-213">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-213">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="67161-214">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-214">ACS</span></span>

* <span data-ttu-id="67161-215">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-215">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="67161-216">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-216">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-217">Appservice</span><span class="sxs-lookup"><span data-stu-id="67161-217">Appservice</span></span>

* <span data-ttu-id="67161-218">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-218">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="67161-219">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="67161-219">Component</span></span>

* <span data-ttu-id="67161-220">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-220">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="67161-221">監視</span><span class="sxs-lookup"><span data-stu-id="67161-221">Monitor</span></span>

* <span data-ttu-id="67161-222">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-222">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="67161-223">リソース</span><span class="sxs-lookup"><span data-stu-id="67161-223">Resource</span></span>

* <span data-ttu-id="67161-224">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-224">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="67161-225">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-225">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="67161-226">VM</span><span class="sxs-lookup"><span data-stu-id="67161-226">VM</span></span>

* <span data-ttu-id="67161-227">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-227">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="67161-228">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="67161-228">October 9, 2017</span></span>

<span data-ttu-id="67161-229">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="67161-229">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="67161-230">コア</span><span class="sxs-lookup"><span data-stu-id="67161-230">Core</span></span>

* <span data-ttu-id="67161-231">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-231">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-232">Appservice</span><span class="sxs-lookup"><span data-stu-id="67161-232">Appservice</span></span>

* <span data-ttu-id="67161-233">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-233">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="67161-234">Batch</span><span class="sxs-lookup"><span data-stu-id="67161-234">Batch</span></span>

* <span data-ttu-id="67161-235">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="67161-235">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="67161-236">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="67161-236">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="67161-237">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-237">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="67161-238">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="67161-238">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="67161-239">Batchai</span><span class="sxs-lookup"><span data-stu-id="67161-239">Batchai</span></span>

* <span data-ttu-id="67161-240">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="67161-240">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="67161-241">KeyVault</span><span class="sxs-lookup"><span data-stu-id="67161-241">Keyvault</span></span>

* <span data-ttu-id="67161-242">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="67161-242">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="67161-243">(#4448)</span><span class="sxs-lookup"><span data-stu-id="67161-243">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="67161-244">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="67161-244">Network</span></span>

* <span data-ttu-id="67161-245">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-245">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="67161-246">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="67161-246">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="67161-247">リソース</span><span class="sxs-lookup"><span data-stu-id="67161-247">Resource</span></span>

* <span data-ttu-id="67161-248">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-248">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="67161-249">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-249">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="67161-250">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-250">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="67161-251">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-251">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="67161-252">SQL</span><span class="sxs-lookup"><span data-stu-id="67161-252">Sql</span></span>

* <span data-ttu-id="67161-253">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-253">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="67161-254">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="67161-254">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="67161-255">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="67161-255">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="67161-256">ストレージ</span><span class="sxs-lookup"><span data-stu-id="67161-256">Storage</span></span>

* <span data-ttu-id="67161-257">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-257">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="67161-258">VM</span><span class="sxs-lookup"><span data-stu-id="67161-258">Vm</span></span>

* <span data-ttu-id="67161-259">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-259">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="67161-260">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-260">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="67161-261">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-261">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="67161-262">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-262">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="67161-263">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-263">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="67161-264">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="67161-264">September 22, 2017</span></span>

<span data-ttu-id="67161-265">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="67161-265">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="67161-266">リソース</span><span class="sxs-lookup"><span data-stu-id="67161-266">Resource</span></span>

* <span data-ttu-id="67161-267">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-267">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="67161-268">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-268">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="67161-269">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-269">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="67161-270">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-270">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="67161-271">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="67161-271">Network</span></span>

* <span data-ttu-id="67161-272">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-272">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="67161-273">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-273">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="67161-274">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-274">Added `asg` application security group commands</span></span>
* <span data-ttu-id="67161-275">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-275">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="67161-276">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-276">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="67161-277">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-277">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="67161-278">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-278">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="67161-279">ストレージ</span><span class="sxs-lookup"><span data-stu-id="67161-279">Storage</span></span>

* <span data-ttu-id="67161-280">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-280">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="67161-281">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="67161-281">Eventgrid</span></span>

* <span data-ttu-id="67161-282">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="67161-282">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="67161-283">SQL</span><span class="sxs-lookup"><span data-stu-id="67161-283">SQL</span></span>

* <span data-ttu-id="67161-284">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="67161-284">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="67161-285">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="67161-285">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="67161-286">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-286">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="67161-287">KeyVault</span><span class="sxs-lookup"><span data-stu-id="67161-287">Keyvault</span></span>

* <span data-ttu-id="67161-288">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-288">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="67161-289">VM</span><span class="sxs-lookup"><span data-stu-id="67161-289">VM</span></span>

* <span data-ttu-id="67161-290">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-290">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="67161-291">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-291">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="67161-292">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-292">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="67161-293">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-293">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="67161-294">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-294">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="67161-295">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-295">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="67161-296">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-296">ACS</span></span>

* <span data-ttu-id="67161-297">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-297">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-298">Appservice</span><span class="sxs-lookup"><span data-stu-id="67161-298">Appservice</span></span>

* <span data-ttu-id="67161-299">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-299">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="67161-300">Backup</span><span class="sxs-lookup"><span data-stu-id="67161-300">Backup</span></span>

* <span data-ttu-id="67161-301">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="67161-301">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="67161-302">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="67161-302">September 11, 2017</span></span>

<span data-ttu-id="67161-303">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="67161-303">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="67161-304">コア</span><span class="sxs-lookup"><span data-stu-id="67161-304">Core</span></span>

* <span data-ttu-id="67161-305">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="67161-305">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="67161-306">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-306">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="67161-307">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-307">Acs</span></span>

* <span data-ttu-id="67161-308">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-308">Added `acs list-locations` command</span></span>
* <span data-ttu-id="67161-309">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="67161-309">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-310">Appservice</span><span class="sxs-lookup"><span data-stu-id="67161-310">Appservice</span></span>

* <span data-ttu-id="67161-311">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-311">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="67161-312">CDN</span><span class="sxs-lookup"><span data-stu-id="67161-312">CDN</span></span>

* <span data-ttu-id="67161-313">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="67161-313">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="67161-314">内線番号</span><span class="sxs-lookup"><span data-stu-id="67161-314">Extension</span></span>

* <span data-ttu-id="67161-315">最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="67161-315">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="67161-316">KeyVault</span><span class="sxs-lookup"><span data-stu-id="67161-316">Keyvault</span></span>

* <span data-ttu-id="67161-317">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="67161-317">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="67161-318">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="67161-318">Network</span></span>

* <span data-ttu-id="67161-319">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-319">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="67161-320">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-320">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="67161-321">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-321">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="67161-322">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-322">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="67161-323">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-323">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="67161-324">リソース</span><span class="sxs-lookup"><span data-stu-id="67161-324">Resource</span></span>

* <span data-ttu-id="67161-325">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="67161-325">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="67161-326">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="67161-326">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="67161-327">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="67161-327">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="67161-328">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="67161-328">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="67161-329">SQL</span><span class="sxs-lookup"><span data-stu-id="67161-329">SQL</span></span>

* <span data-ttu-id="67161-330">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-330">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="67161-331">VM</span><span class="sxs-lookup"><span data-stu-id="67161-331">VM</span></span>

* <span data-ttu-id="67161-332">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="67161-332">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="67161-333">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="67161-333">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="67161-334">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="67161-334">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="67161-335">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="67161-335">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="67161-336">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="67161-336">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="67161-337">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="67161-337">August 31, 2017</span></span>

<span data-ttu-id="67161-338">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="67161-338">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="67161-339">KeyVault</span><span class="sxs-lookup"><span data-stu-id="67161-339">Keyvault</span></span>

* <span data-ttu-id="67161-340">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-340">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="67161-341">SF</span><span class="sxs-lookup"><span data-stu-id="67161-341">Sf</span></span>

* <span data-ttu-id="67161-342">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="67161-342">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="67161-343">ストレージ</span><span class="sxs-lookup"><span data-stu-id="67161-343">Storage</span></span>

* <span data-ttu-id="67161-344">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-344">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="67161-345">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="67161-345">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="67161-346">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="67161-346">August 28, 2017</span></span>

<span data-ttu-id="67161-347">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="67161-347">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="67161-348">CLI</span><span class="sxs-lookup"><span data-stu-id="67161-348">CLI</span></span>

* <span data-ttu-id="67161-349">`--version` に法的事項を追加しました。</span><span class="sxs-lookup"><span data-stu-id="67161-349">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="67161-350">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-350">ACS</span></span>

* <span data-ttu-id="67161-351">プレビュー リージョンを修正しました。</span><span class="sxs-lookup"><span data-stu-id="67161-351">Corrected preview regions.</span></span>
* <span data-ttu-id="67161-352">既定の `dns_name_prefix` を正しい形式にしました。</span><span class="sxs-lookup"><span data-stu-id="67161-352">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="67161-353">ACS コマンド出力を最適化しました。</span><span class="sxs-lookup"><span data-stu-id="67161-353">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-354">Appservice</span><span class="sxs-lookup"><span data-stu-id="67161-354">Appservice</span></span>

* <span data-ttu-id="67161-355">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-355">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="67161-356">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-356">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="67161-357">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="67161-357">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="67161-358">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="67161-358">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="67161-359">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="67161-359">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="67161-360">IoT</span><span class="sxs-lookup"><span data-stu-id="67161-360">IoT</span></span>

* <span data-ttu-id="67161-361">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="67161-361">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="67161-362">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="67161-362">Network</span></span>

* <span data-ttu-id="67161-363">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-363">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="67161-364">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-364">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="67161-365">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-365">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="67161-366">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-366">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="67161-367">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-367">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="67161-368">プロファイル</span><span class="sxs-lookup"><span data-stu-id="67161-368">Profile</span></span>

* <span data-ttu-id="67161-369">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="67161-369">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="67161-370">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="67161-370">Service Fabric</span></span>

* <span data-ttu-id="67161-371">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="67161-371">Preview release</span></span>
* <span data-ttu-id="67161-372">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="67161-372">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="67161-373">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-373">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="67161-374">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-374">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="67161-375">ストレージ</span><span class="sxs-lookup"><span data-stu-id="67161-375">Storage</span></span>

* <span data-ttu-id="67161-376">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="67161-376">Enabled setting blob tier</span></span>
* <span data-ttu-id="67161-377">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-377">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="67161-378">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-378">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="67161-379">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="67161-379">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="67161-380">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-380">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="67161-381">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="67161-381">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="67161-382">VM</span><span class="sxs-lookup"><span data-stu-id="67161-382">VM</span></span>

* <span data-ttu-id="67161-383">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-383">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="67161-384">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="67161-384">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="67161-385">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="67161-385">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="67161-386">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-386">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="67161-387">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-387">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="67161-388">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-388">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="67161-389">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="67161-389">August 15, 2017</span></span>

<span data-ttu-id="67161-390">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="67161-390">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="67161-391">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-391">ACS</span></span>

* <span data-ttu-id="67161-392">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-392">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-393">Appservice</span><span class="sxs-lookup"><span data-stu-id="67161-393">Appservice</span></span>

* <span data-ttu-id="67161-394">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-394">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="67161-395">Event Grid</span><span class="sxs-lookup"><span data-stu-id="67161-395">Event Grid</span></span>

* <span data-ttu-id="67161-396">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-396">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="67161-397">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="67161-397">August 11, 2017</span></span>

<span data-ttu-id="67161-398">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="67161-398">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="67161-399">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-399">ACS</span></span>

* <span data-ttu-id="67161-400">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-400">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="67161-401">Batch</span><span class="sxs-lookup"><span data-stu-id="67161-401">Batch</span></span>

* <span data-ttu-id="67161-402">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="67161-402">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="67161-403">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-403">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="67161-404">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-404">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="67161-405">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="67161-405">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="67161-406">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-406">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="67161-407">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-407">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="67161-408">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="67161-408">Component</span></span>

* <span data-ttu-id="67161-409">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-409">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="67161-410">コンテナー</span><span class="sxs-lookup"><span data-stu-id="67161-410">Container</span></span>

* <span data-ttu-id="67161-411">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-411">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="67161-412">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="67161-412">Data Lake Store</span></span>

* <span data-ttu-id="67161-413">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="67161-413">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="67161-414">Event Grid</span><span class="sxs-lookup"><span data-stu-id="67161-414">Event Grid</span></span>

* <span data-ttu-id="67161-415">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="67161-415">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="67161-416">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="67161-416">Network</span></span>

* <span data-ttu-id="67161-417">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-417">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="67161-418">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-418">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="67161-419">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-419">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="67161-420">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-420">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="67161-421">プロファイル</span><span class="sxs-lookup"><span data-stu-id="67161-421">Profile</span></span>

* <span data-ttu-id="67161-422">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-422">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="67161-423">ストレージ</span><span class="sxs-lookup"><span data-stu-id="67161-423">Storage</span></span>

* <span data-ttu-id="67161-424">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="67161-424">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="67161-425">VM</span><span class="sxs-lookup"><span data-stu-id="67161-425">VM</span></span>

* <span data-ttu-id="67161-426">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="67161-426">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="67161-427">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="67161-427">Exposed `list-skus` command</span></span>
* <span data-ttu-id="67161-428">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-428">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="67161-429">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="67161-429">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="67161-430">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="67161-430">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="67161-431">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="67161-431">July 28, 2017</span></span>

<span data-ttu-id="67161-432">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="67161-432">Version 2.0.12</span></span>

* <span data-ttu-id="67161-433">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-433">Added container commands</span></span>
* <span data-ttu-id="67161-434">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-434">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="67161-435">コア</span><span class="sxs-lookup"><span data-stu-id="67161-435">Core</span></span>

* <span data-ttu-id="67161-436">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="67161-436">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="67161-437">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-437">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="67161-438">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="67161-438">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="67161-439">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="67161-439">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="67161-440">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="67161-440">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="67161-441">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="67161-441">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="67161-442">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="67161-442">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="67161-443">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="67161-443">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="67161-444">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="67161-444">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="67161-445">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="67161-445">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="67161-446">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="67161-446">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="67161-447">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="67161-447">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="67161-448">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="67161-448">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="67161-449">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="67161-449">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="67161-450">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-450">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="67161-451">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="67161-451">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="67161-452">ACR</span><span class="sxs-lookup"><span data-stu-id="67161-452">ACR</span></span>

* <span data-ttu-id="67161-453">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-453">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="67161-454">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-454">Support SKU update for managed registries</span></span>
* <span data-ttu-id="67161-455">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-455">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="67161-456">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-456">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="67161-457">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-457">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="67161-458">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-458">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="67161-459">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-459">ACS</span></span>

* <span data-ttu-id="67161-460">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-460">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-461">Appservice</span><span class="sxs-lookup"><span data-stu-id="67161-461">Appservice</span></span>

* <span data-ttu-id="67161-462">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-462">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="67161-463">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-463">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="67161-464">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="67161-464">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="67161-465">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="67161-465">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="67161-466">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="67161-466">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="67161-467">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="67161-467">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="67161-468">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="67161-468">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="67161-469">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="67161-469">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="67161-470">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="67161-470">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="67161-471">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="67161-471">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="67161-472">Batch</span><span class="sxs-lookup"><span data-stu-id="67161-472">Batch</span></span>

* <span data-ttu-id="67161-473">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="67161-473">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="67161-474">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-474">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="67161-475">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-475">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="67161-476">CDN</span><span class="sxs-lookup"><span data-stu-id="67161-476">CDN</span></span>

* <span data-ttu-id="67161-477">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました。</span><span class="sxs-lookup"><span data-stu-id="67161-477">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="67161-478">クラウド</span><span class="sxs-lookup"><span data-stu-id="67161-478">Cloud</span></span>

* <span data-ttu-id="67161-479">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-479">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="67161-480">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="67161-480">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="67161-481">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-481">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="67161-482">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="67161-482">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="67161-483">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="67161-483">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="67161-484">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="67161-484">CosmosDB</span></span>

* <span data-ttu-id="67161-485">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-485">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="67161-486">既定のコレクション TTL のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="67161-486">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="67161-487">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="67161-487">Data Lake Analytics</span></span>

* <span data-ttu-id="67161-488">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-488">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="67161-489">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-489">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="67161-490">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-490">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="67161-491">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="67161-491">Data Lake Store</span></span>

* <span data-ttu-id="67161-492">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-492">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="67161-493">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="67161-493">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="67161-494">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="67161-494">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="67161-495">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="67161-495">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="67161-496">対話</span><span class="sxs-lookup"><span data-stu-id="67161-496">Interactive</span></span>

* <span data-ttu-id="67161-497">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="67161-497">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="67161-498">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="67161-498">Increased test coverage</span></span>
* <span data-ttu-id="67161-499">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="67161-499">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="67161-500">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="67161-500">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="67161-501">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="67161-501">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="67161-502">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="67161-502">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="67161-503">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="67161-503">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="67161-504">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-504">Added `--progress` flag</span></span>
* <span data-ttu-id="67161-505">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="67161-505">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="67161-506">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="67161-506">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="67161-507">IoT</span><span class="sxs-lookup"><span data-stu-id="67161-507">IoT</span></span>

* <span data-ttu-id="67161-508">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="67161-508">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="67161-509">(#3934)</span><span class="sxs-lookup"><span data-stu-id="67161-509">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="67161-510">Key Vault</span><span class="sxs-lookup"><span data-stu-id="67161-510">Key vault</span></span>

* <span data-ttu-id="67161-511">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="67161-511">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="67161-512">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="67161-512">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="67161-513">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="67161-513">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="67161-514">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="67161-514">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="67161-515">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="67161-515">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="67161-516">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="67161-516">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="67161-517">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="67161-517">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="67161-518">(#3307)</span><span class="sxs-lookup"><span data-stu-id="67161-518">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="67161-519">ラボ</span><span class="sxs-lookup"><span data-stu-id="67161-519">Lab</span></span>

* <span data-ttu-id="67161-520">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-520">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="67161-521">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-521">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="67161-522">監視</span><span class="sxs-lookup"><span data-stu-id="67161-522">Monitor</span></span>

* <span data-ttu-id="67161-523">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="67161-523">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="67161-524">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-524">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="67161-525">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-525">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="67161-526">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-526">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="67161-527">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="67161-527">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="67161-528">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="67161-528">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="67161-529">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="67161-529">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="67161-530">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="67161-530">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="67161-531">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="67161-531">`location` no longer required</span></span>
  * <span data-ttu-id="67161-532">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="67161-532">Add name and ID support for target</span></span>
  * <span data-ttu-id="67161-533">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="67161-533">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="67161-534">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="67161-534">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="67161-535">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="67161-535">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="67161-536">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="67161-536">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="67161-537">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-537">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="67161-538">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-538">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="67161-539">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="67161-539">Network</span></span>

* <span data-ttu-id="67161-540">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-540">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="67161-541">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-541">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="67161-542">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-542">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="67161-543">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-543">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="67161-544">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-544">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="67161-545">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-545">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="67161-546">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-546">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="67161-547">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-547">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="67161-548">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-548">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="67161-549">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-549">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="67161-550">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-550">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="67161-551">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-551">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="67161-552">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-552">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="67161-553">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-553">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="67161-554">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-554">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="67161-555">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="67161-555">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="67161-556">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-556">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="67161-557">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-557">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="67161-558">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-558">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="67161-559">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-559">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="67161-560">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-560">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="67161-561">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-561">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="67161-562">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="67161-562">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="67161-563">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="67161-563">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="67161-564">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="67161-564">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="67161-565">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="67161-565">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="67161-566">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="67161-566">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="67161-567">プロファイル</span><span class="sxs-lookup"><span data-stu-id="67161-567">Profile</span></span>

* <span data-ttu-id="67161-568">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-568">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="67161-569">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-569">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="67161-570">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="67161-570">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="67161-571">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-571">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="67161-572">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-572">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="67161-573">RDBMS</span><span class="sxs-lookup"><span data-stu-id="67161-573">RDBMS</span></span>

* <span data-ttu-id="67161-574">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="67161-574">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="67161-575">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="67161-575">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="67161-576">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="67161-576">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="67161-577">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="67161-577">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="67161-578">リソース</span><span class="sxs-lookup"><span data-stu-id="67161-578">Resource</span></span>

* <span data-ttu-id="67161-579">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="67161-579">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="67161-580">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="67161-580">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="67161-581">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-581">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="67161-582">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-582">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="67161-583">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="67161-583">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="67161-584">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-584">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="67161-585">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="67161-585">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="67161-586">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-586">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="67161-587">役割</span><span class="sxs-lookup"><span data-stu-id="67161-587">Role</span></span>

* <span data-ttu-id="67161-588">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-588">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="67161-589">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="67161-589">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="67161-590">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="67161-590">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="67161-591">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="67161-591">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="67161-592">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-592">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="67161-593">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="67161-593">Service Fabric</span></span>
* <span data-ttu-id="67161-594">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="67161-594">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="67161-595">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="67161-595">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="67161-596">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="67161-596">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="67161-597">SQL</span><span class="sxs-lookup"><span data-stu-id="67161-597">SQL</span></span>

* <span data-ttu-id="67161-598">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="67161-598">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="67161-599">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="67161-599">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="67161-600">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="67161-600">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="67161-601">ストレージ</span><span class="sxs-lookup"><span data-stu-id="67161-601">Storage</span></span>

* <span data-ttu-id="67161-602">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="67161-602">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="67161-603">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="67161-603">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="67161-604">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="67161-604">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="67161-605">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="67161-605">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="67161-606">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="67161-606">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="67161-607">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="67161-607">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="67161-608">VM</span><span class="sxs-lookup"><span data-stu-id="67161-608">VM</span></span>

* <span data-ttu-id="67161-609">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-609">Support configuring nsg</span></span>
* <span data-ttu-id="67161-610">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="67161-610">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="67161-611">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="67161-611">Support managed service identities</span></span>
* <span data-ttu-id="67161-612">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="67161-612">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="67161-613">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="67161-613">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="67161-614">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="67161-614">May 10, 2017</span></span>

<span data-ttu-id="67161-615">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="67161-615">Version 2.0.6</span></span>

* <span data-ttu-id="67161-616">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="67161-616">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="67161-617">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="67161-617">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="67161-618">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-618">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="67161-619">Cognitive Services モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-619">Include Cognitive Services module.</span></span>
* <span data-ttu-id="67161-620">Service Fabric モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-620">Include Service Fabric module.</span></span>
* <span data-ttu-id="67161-621">対話型モジュールが追加されました (az-shell の名前変更)。</span><span class="sxs-lookup"><span data-stu-id="67161-621">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="67161-622">CDN コマンドに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="67161-622">Add support for CDN commands.</span></span>
* <span data-ttu-id="67161-623">コンテナー モジュールが削除されました。</span><span class="sxs-lookup"><span data-stu-id="67161-623">Remove Container module.</span></span>
* <span data-ttu-id="67161-624">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="67161-624">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="67161-625">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="67161-625">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="67161-626">コア</span><span class="sxs-lookup"><span data-stu-id="67161-626">Core</span></span>

* <span data-ttu-id="67161-627">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="67161-627">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="67161-628">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="67161-628">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="67161-629">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="67161-629">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="67161-630">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="67161-630">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="67161-631">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="67161-631">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="67161-632">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="67161-632">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="67161-633">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="67161-633">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="67161-634">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="67161-634">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="67161-635">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="67161-635">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="67161-636">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="67161-636">core: Improved performance</span></span>
* <span data-ttu-id="67161-637">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="67161-637">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="67161-638">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="67161-638">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="67161-639">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-639">ACS</span></span>

* <span data-ttu-id="67161-640">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="67161-640">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="67161-641">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="67161-641">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="67161-642">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="67161-642">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="67161-643">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="67161-643">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-644">AppService</span><span class="sxs-lookup"><span data-stu-id="67161-644">AppService</span></span>

* <span data-ttu-id="67161-645">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="67161-645">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="67161-646">Team Services (VSTS) が継続的な配信オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="67161-646">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="67161-647">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="67161-647">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="67161-648">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="67161-648">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="67161-649">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="67161-649">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="67161-650">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="67161-650">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="67161-651">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="67161-651">support slot swap with preview</span></span>
* <span data-ttu-id="67161-652">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="67161-652">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="67161-653">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="67161-653">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="67161-654">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="67161-654">CosmosDB</span></span>

* <span data-ttu-id="67161-655">documentdb モジュールから cosmosdb に名前が変更されました。</span><span class="sxs-lookup"><span data-stu-id="67161-655">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="67161-656">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="67161-656">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="67161-657">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="67161-657">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="67161-658">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="67161-658">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="67161-659">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="67161-659">Data Lake Analytics</span></span>

* <span data-ttu-id="67161-660">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="67161-660">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="67161-661">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="67161-661">Add support for new catalog item type: package.</span></span> <span data-ttu-id="67161-662">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="67161-662">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="67161-663">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="67161-663">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="67161-664">テーブル</span><span class="sxs-lookup"><span data-stu-id="67161-664">Table</span></span>
  * <span data-ttu-id="67161-665">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="67161-665">Table valued function</span></span>
  * <span data-ttu-id="67161-666">表示</span><span class="sxs-lookup"><span data-stu-id="67161-666">View</span></span>
  * <span data-ttu-id="67161-667">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="67161-667">Table Statistics.</span></span> <span data-ttu-id="67161-668">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="67161-668">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="67161-669">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="67161-669">Data Lake Store</span></span>

* <span data-ttu-id="67161-670">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました。</span><span class="sxs-lookup"><span data-stu-id="67161-670">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="67161-671">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="67161-671">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="67161-672">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="67161-672">missed help for access show.</span></span> <span data-ttu-id="67161-673">追加しました </span><span class="sxs-lookup"><span data-stu-id="67161-673">adding it.</span></span> <span data-ttu-id="67161-674">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="67161-674">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="67161-675">検索</span><span class="sxs-lookup"><span data-stu-id="67161-675">Find</span></span>

* <span data-ttu-id="67161-676">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="67161-676">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="67161-677">KeyVault</span><span class="sxs-lookup"><span data-stu-id="67161-677">KeyVault</span></span>

* <span data-ttu-id="67161-678">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="67161-678">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="67161-679">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました。</span><span class="sxs-lookup"><span data-stu-id="67161-679">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="67161-680">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="67161-680">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="67161-681">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="67161-681">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="67161-682">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="67161-682">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="67161-683">ラボ</span><span class="sxs-lookup"><span data-stu-id="67161-683">Lab</span></span>

* <span data-ttu-id="67161-684">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-684">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="67161-685">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-685">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="67161-686">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-686">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="67161-687">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-687">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="67161-688">ラボ内でシークレットを管理するためのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-688">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="67161-689">監視</span><span class="sxs-lookup"><span data-stu-id="67161-689">Monitor</span></span>

* <span data-ttu-id="67161-690">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="67161-690">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="67161-691">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="67161-691">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="67161-692">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="67161-692">Network</span></span>

* <span data-ttu-id="67161-693">`network watcher test-connectivity` コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-693">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="67161-694">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="67161-694">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="67161-695">Application Gateway 接続のドレインに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="67161-695">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="67161-696">Application Gateway WAF 規則セットの構成に対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="67161-696">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="67161-697">ExpressRoute ルート フィルターとルールに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="67161-697">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="67161-698">TrafficManager の地理的なルーティングに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="67161-698">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="67161-699">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="67161-699">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="67161-700">VPN 接続 IPSec ポリシーに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="67161-700">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="67161-701">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="67161-701">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="67161-702">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="67161-702">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="67161-703">`network vpn-connection list/show` コマンドの出力から null 値が削除されました。</span><span class="sxs-lookup"><span data-stu-id="67161-703">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="67161-704">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="67161-704">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="67161-705">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="67161-705">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="67161-706">`dns zone import` でレコードが適切にインポートされないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="67161-706">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="67161-707">`traffic-manager endpoint update` が動作しないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="67161-707">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="67161-708">"Network Watcher" プレビューのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-708">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="67161-709">プロファイル</span><span class="sxs-lookup"><span data-stu-id="67161-709">Profile</span></span>

* <span data-ttu-id="67161-710">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="67161-710">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="67161-711">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="67161-711">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="67161-712">Redis</span><span class="sxs-lookup"><span data-stu-id="67161-712">Redis</span></span>

* <span data-ttu-id="67161-713">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="67161-713">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="67161-714">"update-settings" コマンドが廃止されました。</span><span class="sxs-lookup"><span data-stu-id="67161-714">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="67161-715">リソース</span><span class="sxs-lookup"><span data-stu-id="67161-715">Resource</span></span>

* <span data-ttu-id="67161-716">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="67161-716">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="67161-717">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="67161-717">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="67161-718">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="67161-718">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="67161-719">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="67161-719">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="67161-720">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="67161-720">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="67161-721">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="67161-721">Add docs for az lock update.</span></span> <span data-ttu-id="67161-722">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="67161-722">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="67161-723">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="67161-723">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="67161-724">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="67161-724">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="67161-725">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="67161-725">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="67161-726">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="67161-726">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="67161-727">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="67161-727">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="67161-728">役割</span><span class="sxs-lookup"><span data-stu-id="67161-728">Role</span></span>

* <span data-ttu-id="67161-729">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="67161-729">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="67161-730">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="67161-730">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="67161-731">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="67161-731">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="67161-732">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="67161-732">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="67161-733">SQL</span><span class="sxs-lookup"><span data-stu-id="67161-733">SQL</span></span>

* <span data-ttu-id="67161-734">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="67161-734">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="67161-735">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="67161-735">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="67161-736">Storage</span><span class="sxs-lookup"><span data-stu-id="67161-736">Storage</span></span>

* <span data-ttu-id="67161-737">`storage account create` のリソース グループの場所に対する既定の場所。</span><span class="sxs-lookup"><span data-stu-id="67161-737">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="67161-738">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="67161-738">Add support for incremental blob copy</span></span>
* <span data-ttu-id="67161-739">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="67161-739">Add support for large block blob upload</span></span>
* <span data-ttu-id="67161-740">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="67161-740">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="67161-741">VM</span><span class="sxs-lookup"><span data-stu-id="67161-741">VM</span></span>

* <span data-ttu-id="67161-742">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="67161-742">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="67161-743">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="67161-743">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="67161-744">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="67161-744">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="67161-745">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="67161-745">az vm/vmss disk</span></span>
  3. <span data-ttu-id="67161-746">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="67161-746">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="67161-747">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="67161-747">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="67161-748">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="67161-748">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="67161-749">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="67161-749">April 3, 2017</span></span>

<span data-ttu-id="67161-750">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="67161-750">Version 2.0.2</span></span>

<span data-ttu-id="67161-751">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました。</span><span class="sxs-lookup"><span data-stu-id="67161-751">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="67161-752">コア</span><span class="sxs-lookup"><span data-stu-id="67161-752">Core</span></span>

* <span data-ttu-id="67161-753">既定の一覧に acr、lab、monitor、find モジュールを追加。</span><span class="sxs-lookup"><span data-stu-id="67161-753">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="67161-754">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="67161-754">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="67161-755">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="67161-755">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="67161-756">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="67161-756">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="67161-757">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="67161-757">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="67161-758">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="67161-758">Add prompting for missing template parameters.</span></span> <span data-ttu-id="67161-759">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="67161-759">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="67161-760">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="67161-760">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="67161-761">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="67161-761">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="67161-762">ACS</span><span class="sxs-lookup"><span data-stu-id="67161-762">ACS</span></span>

* <span data-ttu-id="67161-763">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="67161-763">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="67161-764">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="67161-764">Add support for ssh key password prompting.</span></span> <span data-ttu-id="67161-765">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="67161-765">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="67161-766">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="67161-766">Add support for windows clusters.</span></span> <span data-ttu-id="67161-767">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="67161-767">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="67161-768">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="67161-768">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="67161-769">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="67161-769">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="67161-770">AppService</span><span class="sxs-lookup"><span data-stu-id="67161-770">AppService</span></span>

* <span data-ttu-id="67161-771">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="67161-771">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="67161-772">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="67161-772">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="67161-773">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="67161-773">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="67161-774">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="67161-774">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="67161-775">DataLake</span><span class="sxs-lookup"><span data-stu-id="67161-775">DataLake</span></span>

* <span data-ttu-id="67161-776">Data Lake Analytics モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="67161-776">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="67161-777">Data Lake Store モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="67161-777">Initial release of Data Lake Store module.</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="67161-778">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="67161-778">DocuemntDB</span></span>

* <span data-ttu-id="67161-779">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="67161-779">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="67161-780">VM</span><span class="sxs-lookup"><span data-stu-id="67161-780">VM</span></span>

* <span data-ttu-id="67161-781">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="67161-781">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="67161-782">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="67161-782">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="67161-783">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="67161-783">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="67161-784">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="67161-784">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="67161-785">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート * ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="67161-785">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="67161-786">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="67161-786">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="67161-787">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="67161-787">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="67161-788">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="67161-788">February 27, 2017</span></span>

<span data-ttu-id="67161-789">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="67161-789">Version 2.0.0</span></span>

<span data-ttu-id="67161-790">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。</span><span class="sxs-lookup"><span data-stu-id="67161-790">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="67161-791">一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="67161-791">General availability applies to these command modules:</span></span>
- <span data-ttu-id="67161-792">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="67161-792">Container Service (acs)</span></span>
- <span data-ttu-id="67161-793">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="67161-793">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="67161-794">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="67161-794">Networking</span></span>
- <span data-ttu-id="67161-795">Storage</span><span class="sxs-lookup"><span data-stu-id="67161-795">Storage</span></span>

<span data-ttu-id="67161-796">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="67161-796">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="67161-797">問題は、Microsoft サポートで直接開くことも、[github の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="67161-797">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="67161-798">[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="67161-798">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="67161-799">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません。</span><span class="sxs-lookup"><span data-stu-id="67161-799">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="67161-800">CLI のバージョンを確認するには、`az --version` を使用します。</span><span class="sxs-lookup"><span data-stu-id="67161-800">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="67161-801">出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="67161-801">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="67161-802">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。</span><span class="sxs-lookup"><span data-stu-id="67161-802">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="67161-803">これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です。</span><span class="sxs-lookup"><span data-stu-id="67161-803">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="67161-804">CLI のナイトリー プレビュー ビルドもあります。</span><span class="sxs-lookup"><span data-stu-id="67161-804">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="67161-805">詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67161-805">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="67161-806">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="67161-806">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="67161-807">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="67161-807">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="67161-808">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる。</span><span class="sxs-lookup"><span data-stu-id="67161-808">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="67161-809">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る。</span><span class="sxs-lookup"><span data-stu-id="67161-809">Provide feedback from the command line with the `az feedback` command.</span></span>

