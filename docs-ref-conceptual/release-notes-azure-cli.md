---
title: Azure CLI 2.0 リリース ノート
description: Azure CLI 2.0 の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 04/10/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 254c7b306440d921cef6b611268839150fdf3196
ms.sourcegitcommit: 15d6dfaee2075d0abceb2aa2423f0b6ef7b2ac9b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="82a60-103">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="82a60-103">Azure CLI 2.0 release notes</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="82a60-104">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="82a60-104">May 7, 2018</span></span>

<span data-ttu-id="82a60-105">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="82a60-105">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="82a60-106">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-106">Core</span></span>

* <span data-ttu-id="82a60-107">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-107">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="82a60-108">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-108">Added limited support for positional arguments</span></span>
* <span data-ttu-id="82a60-109">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-109">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="82a60-110">#5591</span><span class="sxs-lookup"><span data-stu-id="82a60-110">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="82a60-111">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-111">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="82a60-112">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="82a60-112">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="82a60-113">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-113">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="82a60-114">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-114">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="82a60-115">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-115">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="82a60-116">ACR</span><span class="sxs-lookup"><span data-stu-id="82a60-116">ACR</span></span>

* <span data-ttu-id="82a60-117">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-117">Added ACR Build commands</span></span>
* <span data-ttu-id="82a60-118">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-118">Improved resource not found error messages</span></span>
* <span data-ttu-id="82a60-119">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-119">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="82a60-120">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-120">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="82a60-121">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-121">Improved repository commands error messages</span></span>
* <span data-ttu-id="82a60-122">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-122">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-123">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-123">ACS</span></span>

* <span data-ttu-id="82a60-124">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-124">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="82a60-125">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-125">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="82a60-126">AMS</span><span class="sxs-lookup"><span data-stu-id="82a60-126">AMS</span></span>

* <span data-ttu-id="82a60-127">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="82a60-127">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-128">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-128">Appservice</span></span>

* <span data-ttu-id="82a60-129">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-129">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="82a60-130">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-130">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="82a60-131">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-131">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="82a60-132">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-132">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="82a60-133">Batch AI</span><span class="sxs-lookup"><span data-stu-id="82a60-133">Batch AI</span></span>

* <span data-ttu-id="82a60-134">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-134">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="82a60-135">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="82a60-135">Cognitive Services</span></span>

* <span data-ttu-id="82a60-136">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-136">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="82a60-137">消費</span><span class="sxs-lookup"><span data-stu-id="82a60-137">Consumption</span></span>

* <span data-ttu-id="82a60-138">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-138">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="82a60-139">コンテナー</span><span class="sxs-lookup"><span data-stu-id="82a60-139">Container</span></span>

* <span data-ttu-id="82a60-140">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-140">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="82a60-141">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="82a60-141">Cosmos DB</span></span>

* <span data-ttu-id="82a60-142">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="82a60-142">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="82a60-143">DMS</span><span class="sxs-lookup"><span data-stu-id="82a60-143">DMS</span></span>

* <span data-ttu-id="82a60-144">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-144">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="82a60-145">内線番号</span><span class="sxs-lookup"><span data-stu-id="82a60-145">Extension</span></span>

* <span data-ttu-id="82a60-146">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-146">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="82a60-147">対話</span><span class="sxs-lookup"><span data-stu-id="82a60-147">Interactive</span></span>

* <span data-ttu-id="82a60-148">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-148">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="82a60-149">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="82a60-149">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="82a60-150">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-150">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="82a60-151">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-151">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="82a60-152">ラボ</span><span class="sxs-lookup"><span data-stu-id="82a60-152">Lab</span></span>

* <span data-ttu-id="82a60-153">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-153">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="82a60-154">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-154">Network</span></span>

* <span data-ttu-id="82a60-155">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-155">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span> 
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="82a60-156">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-156">Profile</span></span>

* <span data-ttu-id="82a60-157">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-157">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="82a60-158">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-158">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="82a60-159">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-159">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="82a60-160">Redis</span><span class="sxs-lookup"><span data-stu-id="82a60-160">Redis</span></span>

* <span data-ttu-id="82a60-161">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-161">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="82a60-162">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="82a60-162">Deprecated `redis list-all`.</span></span> <span data-ttu-id="82a60-163">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="82a60-163">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="82a60-164">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-164">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="82a60-165">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-165">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="82a60-166">役割</span><span class="sxs-lookup"><span data-stu-id="82a60-166">Role</span></span>

* <span data-ttu-id="82a60-167">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-167">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-168">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-168">Storage</span></span>

* <span data-ttu-id="82a60-169">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="82a60-169">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="82a60-170">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="82a60-170">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="82a60-171">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="82a60-171">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="82a60-172">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="82a60-172">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="82a60-173">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-173">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-174">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-174">VM</span></span>

* <span data-ttu-id="82a60-175">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-175">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="82a60-176">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-176">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="82a60-177">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="82a60-177">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="82a60-178">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-178">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="82a60-179">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-179">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="82a60-180">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-180">Added write accelerator support</span></span> 
* <span data-ttu-id="82a60-181">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-181">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="82a60-182">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-182">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="82a60-183">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-183">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="82a60-184">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="82a60-184">April 10, 2018</span></span>

<span data-ttu-id="82a60-185">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="82a60-185">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="82a60-186">ACR</span><span class="sxs-lookup"><span data-stu-id="82a60-186">ACR</span></span>

* <span data-ttu-id="82a60-187">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-187">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-188">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-188">ACS</span></span>

* <span data-ttu-id="82a60-189">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-189">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-190">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-190">Appservice</span></span>

* [重大な変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="82a60-192">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-192">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="82a60-193">BatchAI</span><span class="sxs-lookup"><span data-stu-id="82a60-193">BatchAI</span></span>

* <span data-ttu-id="82a60-194">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-194">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="82a60-195">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="82a60-195">Job level mounting</span></span>
 - <span data-ttu-id="82a60-196">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="82a60-196">Environment variables with secret values</span></span>
 - <span data-ttu-id="82a60-197">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="82a60-197">Performance counters settings</span></span>
 - <span data-ttu-id="82a60-198">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="82a60-198">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="82a60-199">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="82a60-199">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="82a60-200">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="82a60-200">Usage and limits reporting</span></span>
 - <span data-ttu-id="82a60-201">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="82a60-201">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="82a60-202">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="82a60-202">Support for custom images</span></span>
 - <span data-ttu-id="82a60-203">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-203">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="82a60-204">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-204">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="82a60-205">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="82a60-205">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="82a60-206">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="82a60-206">National clouds are supported</span></span>
* <span data-ttu-id="82a60-207">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-207">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="82a60-208">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-208">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="82a60-209">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-209">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="82a60-210">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-210">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="82a60-211">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="82a60-211">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="82a60-212">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="82a60-212">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="82a60-213">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-213">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="82a60-214">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-214">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="82a60-215">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="82a60-215">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="82a60-216">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-216">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="82a60-217">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="82a60-217">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="82a60-218">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="82a60-218">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="82a60-219">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-219">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="82a60-220">課金</span><span class="sxs-lookup"><span data-stu-id="82a60-220">Billing</span></span>

* <span data-ttu-id="82a60-221">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-221">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="82a60-222">消費</span><span class="sxs-lookup"><span data-stu-id="82a60-222">Consumption</span></span>

* <span data-ttu-id="82a60-223">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-223">Added `marketplace` commands</span></span>
* <span data-ttu-id="82a60-224">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-224">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="82a60-225">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-225">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="82a60-226">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-226">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="82a60-227">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-227">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="82a60-228">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-228">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="82a60-229">コンテナー</span><span class="sxs-lookup"><span data-stu-id="82a60-229">Container</span></span>

* <span data-ttu-id="82a60-230">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-230">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="82a60-231">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-231">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="82a60-232">内線番号</span><span class="sxs-lookup"><span data-stu-id="82a60-232">Extension</span></span>

* <span data-ttu-id="82a60-233">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-233">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="82a60-234">対話</span><span class="sxs-lookup"><span data-stu-id="82a60-234">Interactive</span></span>

* <span data-ttu-id="82a60-235">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-235">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="82a60-236">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-236">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="82a60-237">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-237">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="82a60-238">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-238">Network</span></span>

* <span data-ttu-id="82a60-239">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-239">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="82a60-240">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-240">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="82a60-241">#4910</span><span class="sxs-lookup"><span data-stu-id="82a60-241">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="82a60-242">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-242">Added `ddos-protection` commands to create DDoS protection plans</span></span> 
* <span data-ttu-id="82a60-243">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="82a60-243">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="82a60-244">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-244">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="82a60-245">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-245">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="82a60-246">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-246">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="82a60-247">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-247">Profile</span></span>

* <span data-ttu-id="82a60-248">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-248">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="82a60-249">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-249">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="82a60-250">RDBMS</span><span class="sxs-lookup"><span data-stu-id="82a60-250">RDBMS</span></span>

* <span data-ttu-id="82a60-251">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-251">Added `georestore` command</span></span>
* <span data-ttu-id="82a60-252">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-252">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-253">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-253">Resource</span></span>

* <span data-ttu-id="82a60-254">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-254">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="82a60-255">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-255">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="82a60-256">SQL</span><span class="sxs-lookup"><span data-stu-id="82a60-256">SQL</span></span>

* <span data-ttu-id="82a60-257">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-257">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-258">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-258">Storage</span></span>

* <span data-ttu-id="82a60-259">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-259">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-260">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-260">VM</span></span>

* <span data-ttu-id="82a60-261">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-261">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="82a60-262">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-262">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大な変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="82a60-264">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-264">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="82a60-265">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-265">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="82a60-266">#5718</span><span class="sxs-lookup"><span data-stu-id="82a60-266">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="82a60-267">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-267">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="82a60-268">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="82a60-268">March 27, 2018</span></span>

<span data-ttu-id="82a60-269">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="82a60-269">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="82a60-270">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-270">Core</span></span>

* <span data-ttu-id="82a60-271">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="82a60-271">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-272">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-272">ACS</span></span>

* <span data-ttu-id="82a60-273">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-273">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-274">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-274">Appservice</span></span>

* <span data-ttu-id="82a60-275">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-275">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="82a60-276">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-276">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="82a60-277">Backup</span><span class="sxs-lookup"><span data-stu-id="82a60-277">Backup</span></span>

* <span data-ttu-id="82a60-278">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-278">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="82a60-279">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="82a60-279">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="82a60-280">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-280">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="82a60-281">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-281">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="82a60-282">コンテナー</span><span class="sxs-lookup"><span data-stu-id="82a60-282">Container</span></span>

* <span data-ttu-id="82a60-283">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-283">Added `container exec` command.</span></span> <span data-ttu-id="82a60-284">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="82a60-284">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="82a60-285">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="82a60-285">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="82a60-286">内線番号</span><span class="sxs-lookup"><span data-stu-id="82a60-286">Extension</span></span>

* <span data-ttu-id="82a60-287">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-287">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="82a60-288">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-288">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="82a60-289">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-289">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="82a60-290">対話</span><span class="sxs-lookup"><span data-stu-id="82a60-290">Interactive</span></span>

* <span data-ttu-id="82a60-291">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-291">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="82a60-292">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-292">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="82a60-293">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="82a60-293">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="82a60-294">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="82a60-294">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="82a60-295">ラボ</span><span class="sxs-lookup"><span data-stu-id="82a60-295">Lab</span></span>

* <span data-ttu-id="82a60-296">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-296">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="82a60-297">監視</span><span class="sxs-lookup"><span data-stu-id="82a60-297">Monitor</span></span>

* <span data-ttu-id="82a60-298">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="82a60-298">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="82a60-299">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="82a60-299">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="82a60-300">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="82a60-300">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="82a60-301">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-301">Network</span></span>

* <span data-ttu-id="82a60-302">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-302">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="82a60-303">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-303">Profile</span></span>

* <span data-ttu-id="82a60-304">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-304">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="82a60-305">RDBMS</span><span class="sxs-lookup"><span data-stu-id="82a60-305">RDBMS</span></span>

* <span data-ttu-id="82a60-306">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-306">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-307">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-307">Resource</span></span>

* [重大な変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="82a60-309">役割</span><span class="sxs-lookup"><span data-stu-id="82a60-309">Role</span></span>

* <span data-ttu-id="82a60-310">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-310">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="82a60-311">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-311">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="82a60-312">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-312">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="82a60-313">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-313">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="82a60-314">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-314">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-315">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-315">Storage</span></span>

* <span data-ttu-id="82a60-316">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-316">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="82a60-317">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-317">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-318">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-318">VM</span></span>

* <span data-ttu-id="82a60-319">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-319">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="82a60-320">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-320">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="82a60-321">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-321">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="82a60-322">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-322">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="82a60-323">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="82a60-323">March 13, 2018</span></span>

<span data-ttu-id="82a60-324">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="82a60-324">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="82a60-325">ACR</span><span class="sxs-lookup"><span data-stu-id="82a60-325">ACR</span></span>

* <span data-ttu-id="82a60-326">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-326">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="82a60-327">コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました`repository delete`</span><span class="sxs-lookup"><span data-stu-id="82a60-327">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="82a60-328">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-328">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-329">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-329">ACS</span></span>

* <span data-ttu-id="82a60-330">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-330">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="82a60-331">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-331">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="82a60-332">Advisor</span><span class="sxs-lookup"><span data-stu-id="82a60-332">Advisor</span></span>

* <span data-ttu-id="82a60-333">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-333">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="82a60-334">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-334">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="82a60-335">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-335">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span> 
* <span data-ttu-id="82a60-336">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-336">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="82a60-337">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-337">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-338">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-338">Appservice</span></span>

* <span data-ttu-id="82a60-339">を非推奨にしました `[webapp|functionapp] assign-identity`</span><span class="sxs-lookup"><span data-stu-id="82a60-339">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="82a60-340">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-340">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="82a60-341">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="82a60-341">Eventhubs</span></span>

* <span data-ttu-id="82a60-342">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="82a60-342">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="82a60-343">内線番号</span><span class="sxs-lookup"><span data-stu-id="82a60-343">Extension</span></span>

* <span data-ttu-id="82a60-344">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-344">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="82a60-345">対話</span><span class="sxs-lookup"><span data-stu-id="82a60-345">Interactive</span></span>

* <span data-ttu-id="82a60-346">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="82a60-346">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="82a60-347">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="82a60-347">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="82a60-348">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="82a60-348">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="82a60-349">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-349">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="82a60-350">監視</span><span class="sxs-lookup"><span data-stu-id="82a60-350">Monitor</span></span>

* <span data-ttu-id="82a60-351">コマンドを非推奨にしました `monitor autoscale-settings`</span><span class="sxs-lookup"><span data-stu-id="82a60-351">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="82a60-352">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-352">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="82a60-353">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-353">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="82a60-354">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-354">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="82a60-355">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-355">Network</span></span>

* <span data-ttu-id="82a60-356">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-356">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="82a60-357">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-357">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="82a60-358">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-358">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="82a60-359">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-359">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="82a60-360">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-360">Profile</span></span>

* <span data-ttu-id="82a60-361">の `--msi` パラメーターを非推奨にしました `az login`</span><span class="sxs-lookup"><span data-stu-id="82a60-361">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="82a60-362">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-362">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="82a60-363">RDBMS</span><span class="sxs-lookup"><span data-stu-id="82a60-363">RDBMS</span></span>

* <span data-ttu-id="82a60-364">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-364">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="82a60-365">Service Bus</span><span class="sxs-lookup"><span data-stu-id="82a60-365">Service Bus</span></span>

* <span data-ttu-id="82a60-366">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="82a60-366">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-367">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-367">Storage</span></span>

* <span data-ttu-id="82a60-368">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-368">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="82a60-369">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="82a60-369">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-370">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-370">VM</span></span>

* <span data-ttu-id="82a60-371">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-371">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="82a60-372">および `[vm|vmss] assign-identity` を非推奨にしました `[vm|vmss] remove-identity`</span><span class="sxs-lookup"><span data-stu-id="82a60-372">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="82a60-373">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-373">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="82a60-374">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-374">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="82a60-375">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="82a60-375">February 27, 2018</span></span>

<span data-ttu-id="82a60-376">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="82a60-376">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="82a60-377">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-377">Core</span></span>

* <span data-ttu-id="82a60-378">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="82a60-378">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="82a60-379">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-379">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="82a60-380">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-380">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-381">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-381">ACS</span></span>

* <span data-ttu-id="82a60-382">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-382">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="82a60-383">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="82a60-383">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="82a60-384">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-384">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="82a60-385">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-385">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-386">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-386">Appservice</span></span>

* <span data-ttu-id="82a60-387">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="82a60-387">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="82a60-388">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="82a60-388">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="82a60-389">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="82a60-389">Cognitive Services</span></span>

* <span data-ttu-id="82a60-390">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-390">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="82a60-391">消費</span><span class="sxs-lookup"><span data-stu-id="82a60-391">Consumption</span></span>

* <span data-ttu-id="82a60-392">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-392">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="82a60-393">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-393">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="82a60-394">コンテナー</span><span class="sxs-lookup"><span data-stu-id="82a60-394">Container</span></span>

* <span data-ttu-id="82a60-395">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-395">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="82a60-396">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-396">Network</span></span>

* <span data-ttu-id="82a60-397">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="82a60-397">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-398">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-398">Resource</span></span>

* <span data-ttu-id="82a60-399">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-399">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="82a60-400">役割</span><span class="sxs-lookup"><span data-stu-id="82a60-400">Role</span></span>

* <span data-ttu-id="82a60-401">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-401">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="82a60-402">SQL</span><span class="sxs-lookup"><span data-stu-id="82a60-402">SQL</span></span>

* <span data-ttu-id="82a60-403">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-403">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-404">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-404">Storage</span></span>

* <span data-ttu-id="82a60-405">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-405">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-406">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-406">VM</span></span>

* <span data-ttu-id="82a60-407">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-407">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="82a60-408">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="82a60-408">February 13, 2018</span></span>

<span data-ttu-id="82a60-409">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="82a60-409">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="82a60-410">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-410">Core</span></span>

* <span data-ttu-id="82a60-411">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-411">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-412">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-412">ACS</span></span>

* <span data-ttu-id="82a60-413">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-413">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="82a60-414">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-414">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="82a60-415">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-415">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="82a60-416">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-416">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="82a60-417">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-417">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="82a60-418">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="82a60-418">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="82a60-419">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-419">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="82a60-420">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="82a60-420">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-421">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-421">Appservice</span></span>

* <span data-ttu-id="82a60-422">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-422">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="82a60-423">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-423">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="82a60-424">CDN</span><span class="sxs-lookup"><span data-stu-id="82a60-424">CDN</span></span>

* <span data-ttu-id="82a60-425">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-425">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="82a60-426">コンテナー</span><span class="sxs-lookup"><span data-stu-id="82a60-426">Container</span></span>

* <span data-ttu-id="82a60-427">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-427">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="82a60-428">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-428">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="82a60-429">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="82a60-429">CosmosDB</span></span>

* <span data-ttu-id="82a60-430">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-430">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="82a60-431">内線番号</span><span class="sxs-lookup"><span data-stu-id="82a60-431">Extension</span></span>

* <span data-ttu-id="82a60-432">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-432">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="82a60-433">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-433">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="82a60-434">フィードバック</span><span class="sxs-lookup"><span data-stu-id="82a60-434">Feedback</span></span>

* <span data-ttu-id="82a60-435">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-435">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="82a60-436">対話</span><span class="sxs-lookup"><span data-stu-id="82a60-436">Interactive</span></span>

* <span data-ttu-id="82a60-437">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-437">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="82a60-438">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-438">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="82a60-439">IoT</span><span class="sxs-lookup"><span data-stu-id="82a60-439">IoT</span></span>

* <span data-ttu-id="82a60-440">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-440">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="82a60-441">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-441">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="82a60-442">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-442">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="82a60-443">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-443">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="82a60-444">監視</span><span class="sxs-lookup"><span data-stu-id="82a60-444">Monitor</span></span>

* <span data-ttu-id="82a60-445">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-445">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="82a60-446">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-446">Network</span></span>

* <span data-ttu-id="82a60-447">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-447">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="82a60-448">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-448">Profile</span></span>

* <span data-ttu-id="82a60-449">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-449">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-450">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-450">Resource</span></span>

* <span data-ttu-id="82a60-451">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-451">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="82a60-452">役割</span><span class="sxs-lookup"><span data-stu-id="82a60-452">Role</span></span>

* <span data-ttu-id="82a60-453">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-453">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="82a60-454">SQL</span><span class="sxs-lookup"><span data-stu-id="82a60-454">SQL</span></span>

* <span data-ttu-id="82a60-455">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-455">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="82a60-456">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-456">Added `sql db rename`</span></span>
* <span data-ttu-id="82a60-457">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-457">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-458">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-458">Storage</span></span>

* <span data-ttu-id="82a60-459">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-459">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-460">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-460">VM</span></span>

* <span data-ttu-id="82a60-461">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-461">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="82a60-462">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-462">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="82a60-463">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="82a60-463">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="82a60-464">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="82a60-464">January 31, 2018</span></span>

<span data-ttu-id="82a60-465">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="82a60-465">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="82a60-466">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-466">Core</span></span>

* <span data-ttu-id="82a60-467">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-467">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="82a60-468">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-468">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="82a60-469">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-469">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="82a60-470">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="82a60-470">Use `--verbose` to see</span></span>
* <span data-ttu-id="82a60-471">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="82a60-471">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-472">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-472">ACS</span></span>

* <span data-ttu-id="82a60-473">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="82a60-473">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="82a60-474">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="82a60-474">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-475">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-475">Appservice</span></span>

* <span data-ttu-id="82a60-476">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="82a60-476">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="82a60-477">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-477">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="82a60-478">CDN</span><span class="sxs-lookup"><span data-stu-id="82a60-478">CDN</span></span>

* <span data-ttu-id="82a60-479">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-479">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="82a60-480">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="82a60-480">CosmosDB</span></span>

* <span data-ttu-id="82a60-481">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-481">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="82a60-482">対話</span><span class="sxs-lookup"><span data-stu-id="82a60-482">Interactive</span></span>

* <span data-ttu-id="82a60-483">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-483">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="82a60-484">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-484">Network</span></span>

* <span data-ttu-id="82a60-485">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-485">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="82a60-486">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-486">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="82a60-487">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-487">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="82a60-488">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-488">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="82a60-489">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-489">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="82a60-490">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-490">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="82a60-491">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-491">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="82a60-492">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-492">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="82a60-493">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-493">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="82a60-494">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="82a60-494">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="82a60-495">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-495">Profile</span></span>

* <span data-ttu-id="82a60-496">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-496">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-497">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-497">Resource</span></span>

* <span data-ttu-id="82a60-498">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-498">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-499">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-499">Storage</span></span>

* <span data-ttu-id="82a60-500">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-500">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="82a60-501">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-501">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="82a60-502">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-502">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="82a60-503">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-503">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="82a60-504">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-504">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-505">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-505">VM</span></span>

* <span data-ttu-id="82a60-506">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-506">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="82a60-507">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-507">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="82a60-508">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-508">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="82a60-509">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-509">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="82a60-510">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="82a60-510">January 17, 2018</span></span>

<span data-ttu-id="82a60-511">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="82a60-511">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="82a60-512">ACR</span><span class="sxs-lookup"><span data-stu-id="82a60-512">ACR</span></span>

* <span data-ttu-id="82a60-513">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-513">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="82a60-514">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-514">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-515">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-515">ACS</span></span>

* <span data-ttu-id="82a60-516">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-516">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="82a60-517">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-517">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-518">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-518">Appservice</span></span>

* <span data-ttu-id="82a60-519">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-519">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="82a60-520">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-520">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="82a60-521">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-521">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="82a60-522">Backup</span><span class="sxs-lookup"><span data-stu-id="82a60-522">Backup</span></span>

* <span data-ttu-id="82a60-523">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-523">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="82a60-524">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-524">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="82a60-525">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-525">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="82a60-526">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-526">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="82a60-527">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-527">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="82a60-528">Batch</span><span class="sxs-lookup"><span data-stu-id="82a60-528">Batch</span></span>

* <span data-ttu-id="82a60-529">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-529">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="82a60-530">クラウド</span><span class="sxs-lookup"><span data-stu-id="82a60-530">Cloud</span></span>

* <span data-ttu-id="82a60-531">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-531">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="82a60-532">消費</span><span class="sxs-lookup"><span data-stu-id="82a60-532">Consumption</span></span>

* <span data-ttu-id="82a60-533">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-533">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="82a60-534">Event Grid</span><span class="sxs-lookup"><span data-stu-id="82a60-534">Event Grid</span></span>

* <span data-ttu-id="82a60-535">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="82a60-535">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="82a60-536">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="82a60-536">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="82a60-537">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-537">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="82a60-538">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="82a60-538">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="82a60-539">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-539">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="82a60-540">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-540">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="82a60-541">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-541">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="82a60-542">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-542">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="82a60-543">対話</span><span class="sxs-lookup"><span data-stu-id="82a60-543">Interactive</span></span>

* <span data-ttu-id="82a60-544">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="82a60-544">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="82a60-545">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-545">Fixed errors on startup</span></span>
* <span data-ttu-id="82a60-546">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-546">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="82a60-547">IoT</span><span class="sxs-lookup"><span data-stu-id="82a60-547">IoT</span></span>

* <span data-ttu-id="82a60-548">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-548">Added support for device provisioning service</span></span>
* <span data-ttu-id="82a60-549">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-549">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="82a60-550">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-550">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="82a60-551">監視</span><span class="sxs-lookup"><span data-stu-id="82a60-551">Monitor</span></span>

* <span data-ttu-id="82a60-552">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-552">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="82a60-553">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="82a60-553">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="82a60-554">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-554">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="82a60-555">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-555">Network</span></span>

* <span data-ttu-id="82a60-556">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-556">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="82a60-557">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-557">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="82a60-558">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-558">Profile</span></span>

* <span data-ttu-id="82a60-559">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-559">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="82a60-560">役割</span><span class="sxs-lookup"><span data-stu-id="82a60-560">Role</span></span>

* <span data-ttu-id="82a60-561">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-561">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="82a60-562">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="82a60-562">Service Fabric</span></span>

* <span data-ttu-id="82a60-563">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-563">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="82a60-564">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-564">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-565">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-565">VM</span></span>

* <span data-ttu-id="82a60-566">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="82a60-566">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="82a60-567">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-567">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="82a60-568">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-568">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="82a60-569">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-569">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="82a60-570">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-570">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="82a60-571">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-571">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="82a60-572">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-572">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="82a60-573">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-573">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="82a60-574">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="82a60-574">December 19, 2017</span></span>

<span data-ttu-id="82a60-575">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="82a60-575">Version 2.0.23</span></span>

* <span data-ttu-id="82a60-576">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-576">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="82a60-577">コンテナー</span><span class="sxs-lookup"><span data-stu-id="82a60-577">Container</span></span>

* <span data-ttu-id="82a60-578">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-578">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="82a60-579">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-579">Network</span></span>

* <span data-ttu-id="82a60-580">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-580">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="82a60-581">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-581">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-582">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-582">Storage</span></span>

* <span data-ttu-id="82a60-583">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-583">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-584">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-584">VM</span></span>

* <span data-ttu-id="82a60-585">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-585">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="82a60-586">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="82a60-586">December 5, 2017</span></span>

<span data-ttu-id="82a60-587">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="82a60-587">Version 2.0.22</span></span>

* <span data-ttu-id="82a60-588">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-588">Removed `az component` commands.</span></span> <span data-ttu-id="82a60-589">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="82a60-589">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="82a60-590">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-590">Core</span></span>
* <span data-ttu-id="82a60-591">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-591">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="82a60-592">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-592">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-593">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-593">ACS</span></span>

* <span data-ttu-id="82a60-594">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-594">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="82a60-595">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-595">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="82a60-596">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-596">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="82a60-597">Advisor</span><span class="sxs-lookup"><span data-stu-id="82a60-597">Advisor</span></span>

* <span data-ttu-id="82a60-598">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="82a60-598">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-599">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-599">Appservice</span></span>

* <span data-ttu-id="82a60-600">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-600">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="82a60-601">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-601">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="82a60-602">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-602">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="82a60-603">消費</span><span class="sxs-lookup"><span data-stu-id="82a60-603">Consumption</span></span>

* <span data-ttu-id="82a60-604">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-604">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="82a60-605">コンテナー</span><span class="sxs-lookup"><span data-stu-id="82a60-605">Container</span></span>

* <span data-ttu-id="82a60-606">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-606">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="82a60-607">監視</span><span class="sxs-lookup"><span data-stu-id="82a60-607">Monitor</span></span>

* <span data-ttu-id="82a60-608">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-608">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-609">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-609">Resource</span></span>

* <span data-ttu-id="82a60-610">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-610">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="82a60-611">役割</span><span class="sxs-lookup"><span data-stu-id="82a60-611">Role</span></span>

* <span data-ttu-id="82a60-612">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-612">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="82a60-613">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="82a60-613">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="82a60-614">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-614">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="82a60-615">SQL</span><span class="sxs-lookup"><span data-stu-id="82a60-615">SQL</span></span>

* <span data-ttu-id="82a60-616">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-616">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="82a60-617">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-617">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-618">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-618">VM</span></span>

* <span data-ttu-id="82a60-619">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-619">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="82a60-620">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="82a60-620">November 14, 2017</span></span>

<span data-ttu-id="82a60-621">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="82a60-621">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="82a60-622">ACR</span><span class="sxs-lookup"><span data-stu-id="82a60-622">ACR</span></span>

* <span data-ttu-id="82a60-623">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-623">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="82a60-624">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-624">ACS</span></span>

* <span data-ttu-id="82a60-625">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-625">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="82a60-626">の `--orchestrator-release` オプションを非推奨にしました `acs create`</span><span class="sxs-lookup"><span data-stu-id="82a60-626">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="82a60-627">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-627">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="82a60-628">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-628">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="82a60-629">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-629">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-630">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-630">Appservice</span></span>

* <span data-ttu-id="82a60-631">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-631">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="82a60-632">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-632">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="82a60-633">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-633">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="82a60-634">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-634">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="82a60-635">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-635">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="82a60-636">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="82a60-636">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="82a60-637">Batch</span><span class="sxs-lookup"><span data-stu-id="82a60-637">Batch</span></span>

* <span data-ttu-id="82a60-638">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-638">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="82a60-639">Batchai</span><span class="sxs-lookup"><span data-stu-id="82a60-639">Batchai</span></span>

* <span data-ttu-id="82a60-640">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-640">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="82a60-641">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-641">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="82a60-642">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-642">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="82a60-643">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-643">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="82a60-644">クラウド</span><span class="sxs-lookup"><span data-stu-id="82a60-644">Cloud</span></span>

* <span data-ttu-id="82a60-645">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-645">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="82a60-646">コンテナー</span><span class="sxs-lookup"><span data-stu-id="82a60-646">Container</span></span>

* <span data-ttu-id="82a60-647">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-647">Added support to open multiple ports</span></span>
* <span data-ttu-id="82a60-648">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-648">Added container group restart policy</span></span>
* <span data-ttu-id="82a60-649">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-649">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="82a60-650">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-650">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="82a60-651">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="82a60-651">Data Lake Analytics</span></span>

* <span data-ttu-id="82a60-652">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-652">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="82a60-653">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="82a60-653">Data Lake Store</span></span>

* <span data-ttu-id="82a60-654">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-654">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="82a60-655">内線番号</span><span class="sxs-lookup"><span data-stu-id="82a60-655">Extension</span></span>

* <span data-ttu-id="82a60-656">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-656">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="82a60-657">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-657">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="82a60-658">IoT</span><span class="sxs-lookup"><span data-stu-id="82a60-658">IoT</span></span>

* <span data-ttu-id="82a60-659">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-659">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="82a60-660">監視</span><span class="sxs-lookup"><span data-stu-id="82a60-660">Monitor</span></span>

* <span data-ttu-id="82a60-661">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-661">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="82a60-662">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-662">Network</span></span>

* <span data-ttu-id="82a60-663">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-663">Added support for CAA DNS records</span></span>
* <span data-ttu-id="82a60-664">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-664">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="82a60-665">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-665">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="82a60-666">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-666">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="82a60-667">Reservations</span><span class="sxs-lookup"><span data-stu-id="82a60-667">Reservations</span></span>

* <span data-ttu-id="82a60-668">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="82a60-668">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-669">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-669">Resource</span></span>

* <span data-ttu-id="82a60-670">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-670">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="82a60-671">SQL</span><span class="sxs-lookup"><span data-stu-id="82a60-671">SQL</span></span>

* <span data-ttu-id="82a60-672">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-672">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-673">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-673">Storage</span></span>

* <span data-ttu-id="82a60-674">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-674">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="82a60-675">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-675">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="82a60-676">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-676">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="82a60-677">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-677">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="82a60-678">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-678">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="82a60-679">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-679">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="82a60-680">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-680">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-681">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-681">VM</span></span>

* <span data-ttu-id="82a60-682">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-682">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="82a60-683">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-683">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="82a60-684">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-684">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="82a60-685">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-685">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="82a60-686">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-686">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="82a60-687">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="82a60-687">October 24, 2017</span></span>

<span data-ttu-id="82a60-688">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="82a60-688">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="82a60-689">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-689">Core</span></span>

* <span data-ttu-id="82a60-690">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-690">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="82a60-691">ACR</span><span class="sxs-lookup"><span data-stu-id="82a60-691">ACR</span></span>

* <span data-ttu-id="82a60-692">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-692">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="82a60-693">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-693">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="82a60-694">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-694">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-695">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-695">ACS</span></span>

* <span data-ttu-id="82a60-696">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-696">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="82a60-697">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-697">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-698">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-698">Appservice</span></span>

* <span data-ttu-id="82a60-699">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-699">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="82a60-700">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="82a60-700">Component</span></span>

* <span data-ttu-id="82a60-701">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-701">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="82a60-702">監視</span><span class="sxs-lookup"><span data-stu-id="82a60-702">Monitor</span></span>

* <span data-ttu-id="82a60-703">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-703">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-704">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-704">Resource</span></span>

* <span data-ttu-id="82a60-705">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-705">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="82a60-706">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-706">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-707">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-707">VM</span></span>

* <span data-ttu-id="82a60-708">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-708">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="82a60-709">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="82a60-709">October 9, 2017</span></span>

<span data-ttu-id="82a60-710">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="82a60-710">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="82a60-711">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-711">Core</span></span>

* <span data-ttu-id="82a60-712">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-712">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-713">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-713">Appservice</span></span>

* <span data-ttu-id="82a60-714">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-714">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="82a60-715">Batch</span><span class="sxs-lookup"><span data-stu-id="82a60-715">Batch</span></span>

* <span data-ttu-id="82a60-716">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-716">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="82a60-717">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-717">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="82a60-718">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-718">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="82a60-719">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-719">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="82a60-720">Batchai</span><span class="sxs-lookup"><span data-stu-id="82a60-720">Batchai</span></span>

* <span data-ttu-id="82a60-721">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="82a60-721">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="82a60-722">KeyVault</span><span class="sxs-lookup"><span data-stu-id="82a60-722">Keyvault</span></span>

* <span data-ttu-id="82a60-723">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-723">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="82a60-724">(#4448)</span><span class="sxs-lookup"><span data-stu-id="82a60-724">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="82a60-725">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-725">Network</span></span>

* <span data-ttu-id="82a60-726">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-726">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="82a60-727">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-727">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-728">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-728">Resource</span></span>

* <span data-ttu-id="82a60-729">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-729">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="82a60-730">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-730">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="82a60-731">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-731">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="82a60-732">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-732">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="82a60-733">SQL</span><span class="sxs-lookup"><span data-stu-id="82a60-733">Sql</span></span>

* <span data-ttu-id="82a60-734">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-734">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="82a60-735">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="82a60-735">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="82a60-736">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="82a60-736">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-737">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-737">Storage</span></span>

* <span data-ttu-id="82a60-738">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-738">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-739">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-739">Vm</span></span>

* <span data-ttu-id="82a60-740">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-740">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="82a60-741">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-741">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="82a60-742">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-742">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="82a60-743">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-743">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="82a60-744">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-744">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="82a60-745">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="82a60-745">September 22, 2017</span></span>

<span data-ttu-id="82a60-746">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="82a60-746">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-747">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-747">Resource</span></span>

* <span data-ttu-id="82a60-748">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-748">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="82a60-749">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-749">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="82a60-750">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-750">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="82a60-751">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-751">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="82a60-752">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-752">Network</span></span>

* <span data-ttu-id="82a60-753">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-753">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="82a60-754">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-754">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="82a60-755">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-755">Added `asg` application security group commands</span></span>
* <span data-ttu-id="82a60-756">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-756">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="82a60-757">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-757">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="82a60-758">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-758">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="82a60-759">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-759">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-760">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-760">Storage</span></span>

* <span data-ttu-id="82a60-761">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-761">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="82a60-762">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="82a60-762">Eventgrid</span></span>

* <span data-ttu-id="82a60-763">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-763">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="82a60-764">SQL</span><span class="sxs-lookup"><span data-stu-id="82a60-764">SQL</span></span>

* <span data-ttu-id="82a60-765">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-765">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="82a60-766">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="82a60-766">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="82a60-767">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-767">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="82a60-768">KeyVault</span><span class="sxs-lookup"><span data-stu-id="82a60-768">Keyvault</span></span>

* <span data-ttu-id="82a60-769">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-769">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-770">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-770">VM</span></span>

* <span data-ttu-id="82a60-771">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-771">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="82a60-772">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-772">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="82a60-773">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-773">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="82a60-774">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-774">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="82a60-775">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-775">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="82a60-776">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-776">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-777">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-777">ACS</span></span>

* <span data-ttu-id="82a60-778">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-778">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-779">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-779">Appservice</span></span>

* <span data-ttu-id="82a60-780">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-780">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="82a60-781">Backup</span><span class="sxs-lookup"><span data-stu-id="82a60-781">Backup</span></span>

* <span data-ttu-id="82a60-782">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="82a60-782">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="82a60-783">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="82a60-783">September 11, 2017</span></span>

<span data-ttu-id="82a60-784">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="82a60-784">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="82a60-785">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-785">Core</span></span>

* <span data-ttu-id="82a60-786">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-786">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="82a60-787">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-787">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-788">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-788">Acs</span></span>

* <span data-ttu-id="82a60-789">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-789">Added `acs list-locations` command</span></span>
* <span data-ttu-id="82a60-790">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="82a60-790">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-791">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-791">Appservice</span></span>

* <span data-ttu-id="82a60-792">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-792">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="82a60-793">CDN</span><span class="sxs-lookup"><span data-stu-id="82a60-793">CDN</span></span>

* <span data-ttu-id="82a60-794">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-794">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="82a60-795">内線番号</span><span class="sxs-lookup"><span data-stu-id="82a60-795">Extension</span></span>

* <span data-ttu-id="82a60-796">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="82a60-796">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="82a60-797">KeyVault</span><span class="sxs-lookup"><span data-stu-id="82a60-797">Keyvault</span></span>

* <span data-ttu-id="82a60-798">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-798">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="82a60-799">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-799">Network</span></span>

* <span data-ttu-id="82a60-800">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-800">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="82a60-801">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-801">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="82a60-802">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-802">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="82a60-803">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-803">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="82a60-804">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-804">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-805">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-805">Resource</span></span>

* <span data-ttu-id="82a60-806">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="82a60-806">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="82a60-807">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="82a60-807">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="82a60-808">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="82a60-808">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="82a60-809">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="82a60-809">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="82a60-810">SQL</span><span class="sxs-lookup"><span data-stu-id="82a60-810">SQL</span></span>

* <span data-ttu-id="82a60-811">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-811">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-812">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-812">VM</span></span>

* <span data-ttu-id="82a60-813">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="82a60-813">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="82a60-814">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="82a60-814">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="82a60-815">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-815">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="82a60-816">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="82a60-816">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="82a60-817">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="82a60-817">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="82a60-818">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="82a60-818">August 31, 2017</span></span>

<span data-ttu-id="82a60-819">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="82a60-819">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="82a60-820">KeyVault</span><span class="sxs-lookup"><span data-stu-id="82a60-820">Keyvault</span></span>

* <span data-ttu-id="82a60-821">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-821">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="82a60-822">SF</span><span class="sxs-lookup"><span data-stu-id="82a60-822">Sf</span></span>

* <span data-ttu-id="82a60-823">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="82a60-823">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-824">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-824">Storage</span></span>

* <span data-ttu-id="82a60-825">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-825">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="82a60-826">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="82a60-826">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="82a60-827">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="82a60-827">August 28, 2017</span></span>

<span data-ttu-id="82a60-828">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="82a60-828">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="82a60-829">CLI</span><span class="sxs-lookup"><span data-stu-id="82a60-829">CLI</span></span>

* <span data-ttu-id="82a60-830">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-830">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-831">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-831">ACS</span></span>

* <span data-ttu-id="82a60-832">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-832">Corrected preview regions</span></span>
* <span data-ttu-id="82a60-833">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-833">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="82a60-834">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="82a60-834">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-835">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-835">Appservice</span></span>

* <span data-ttu-id="82a60-836">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-836">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="82a60-837">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-837">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="82a60-838">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="82a60-838">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="82a60-839">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="82a60-839">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="82a60-840">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="82a60-840">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="82a60-841">IoT</span><span class="sxs-lookup"><span data-stu-id="82a60-841">IoT</span></span>

* <span data-ttu-id="82a60-842">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="82a60-842">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="82a60-843">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-843">Network</span></span>

* <span data-ttu-id="82a60-844">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-844">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="82a60-845">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-845">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="82a60-846">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-846">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="82a60-847">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-847">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="82a60-848">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-848">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="82a60-849">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-849">Profile</span></span>

* <span data-ttu-id="82a60-850">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="82a60-850">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="82a60-851">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="82a60-851">Service Fabric</span></span>

* <span data-ttu-id="82a60-852">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="82a60-852">Preview release</span></span>
* <span data-ttu-id="82a60-853">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="82a60-853">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="82a60-854">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-854">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="82a60-855">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-855">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-856">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-856">Storage</span></span>

* <span data-ttu-id="82a60-857">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-857">Enabled setting blob tier</span></span>
* <span data-ttu-id="82a60-858">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-858">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="82a60-859">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-859">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="82a60-860">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-860">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="82a60-861">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-861">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="82a60-862">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="82a60-862">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-863">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-863">VM</span></span>

* <span data-ttu-id="82a60-864">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-864">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="82a60-865">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-865">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="82a60-866">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-866">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="82a60-867">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-867">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="82a60-868">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-868">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="82a60-869">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-869">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="82a60-870">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="82a60-870">August 15, 2017</span></span>

<span data-ttu-id="82a60-871">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="82a60-871">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-872">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-872">ACS</span></span>

* <span data-ttu-id="82a60-873">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-873">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-874">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-874">Appservice</span></span>

* <span data-ttu-id="82a60-875">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-875">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="82a60-876">Event Grid</span><span class="sxs-lookup"><span data-stu-id="82a60-876">Event Grid</span></span>

* <span data-ttu-id="82a60-877">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-877">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="82a60-878">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="82a60-878">August 11, 2017</span></span>

<span data-ttu-id="82a60-879">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="82a60-879">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-880">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-880">ACS</span></span>

* <span data-ttu-id="82a60-881">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-881">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="82a60-882">Batch</span><span class="sxs-lookup"><span data-stu-id="82a60-882">Batch</span></span>

* <span data-ttu-id="82a60-883">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="82a60-883">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="82a60-884">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-884">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="82a60-885">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-885">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="82a60-886">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-886">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="82a60-887">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-887">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="82a60-888">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-888">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="82a60-889">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="82a60-889">Component</span></span>

* <span data-ttu-id="82a60-890">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-890">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="82a60-891">コンテナー</span><span class="sxs-lookup"><span data-stu-id="82a60-891">Container</span></span>

* <span data-ttu-id="82a60-892">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-892">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="82a60-893">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="82a60-893">Data Lake Store</span></span>

* <span data-ttu-id="82a60-894">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-894">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="82a60-895">Event Grid</span><span class="sxs-lookup"><span data-stu-id="82a60-895">Event Grid</span></span>

* <span data-ttu-id="82a60-896">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="82a60-896">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="82a60-897">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-897">Network</span></span>

* <span data-ttu-id="82a60-898">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-898">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="82a60-899">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-899">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="82a60-900">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-900">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="82a60-901">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-901">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="82a60-902">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-902">Profile</span></span>

* <span data-ttu-id="82a60-903">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-903">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-904">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-904">Storage</span></span>

* <span data-ttu-id="82a60-905">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="82a60-905">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-906">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-906">VM</span></span>

* <span data-ttu-id="82a60-907">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="82a60-907">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="82a60-908">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="82a60-908">Exposed `list-skus` command</span></span>
* <span data-ttu-id="82a60-909">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-909">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="82a60-910">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="82a60-910">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="82a60-911">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-911">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="82a60-912">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="82a60-912">July 28, 2017</span></span>

<span data-ttu-id="82a60-913">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="82a60-913">Version 2.0.12</span></span>

* <span data-ttu-id="82a60-914">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-914">Added container commands</span></span>
* <span data-ttu-id="82a60-915">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-915">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="82a60-916">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-916">Core</span></span>

* <span data-ttu-id="82a60-917">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="82a60-917">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="82a60-918">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-918">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="82a60-919">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="82a60-919">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="82a60-920">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="82a60-920">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="82a60-921">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="82a60-921">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="82a60-922">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="82a60-922">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="82a60-923">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="82a60-923">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="82a60-924">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="82a60-924">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="82a60-925">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="82a60-925">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="82a60-926">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="82a60-926">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="82a60-927">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="82a60-927">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="82a60-928">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="82a60-928">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="82a60-929">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="82a60-929">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="82a60-930">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="82a60-930">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="82a60-931">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-931">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="82a60-932">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="82a60-932">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="82a60-933">ACR</span><span class="sxs-lookup"><span data-stu-id="82a60-933">ACR</span></span>

* <span data-ttu-id="82a60-934">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-934">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="82a60-935">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-935">Support SKU update for managed registries</span></span>
* <span data-ttu-id="82a60-936">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-936">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="82a60-937">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-937">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="82a60-938">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-938">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="82a60-939">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-939">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-940">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-940">ACS</span></span>

* <span data-ttu-id="82a60-941">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-941">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-942">Appservice</span><span class="sxs-lookup"><span data-stu-id="82a60-942">Appservice</span></span>

* <span data-ttu-id="82a60-943">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-943">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="82a60-944">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-944">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="82a60-945">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="82a60-945">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="82a60-946">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="82a60-946">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="82a60-947">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="82a60-947">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="82a60-948">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="82a60-948">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="82a60-949">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="82a60-949">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="82a60-950">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="82a60-950">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="82a60-951">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-951">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="82a60-952">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="82a60-952">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="82a60-953">Batch</span><span class="sxs-lookup"><span data-stu-id="82a60-953">Batch</span></span>

* <span data-ttu-id="82a60-954">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="82a60-954">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="82a60-955">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-955">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="82a60-956">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-956">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="82a60-957">CDN</span><span class="sxs-lookup"><span data-stu-id="82a60-957">CDN</span></span>

* <span data-ttu-id="82a60-958">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-958">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="82a60-959">クラウド</span><span class="sxs-lookup"><span data-stu-id="82a60-959">Cloud</span></span>

* <span data-ttu-id="82a60-960">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-960">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="82a60-961">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="82a60-961">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="82a60-962">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-962">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="82a60-963">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="82a60-963">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="82a60-964">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="82a60-964">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="82a60-965">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="82a60-965">CosmosDB</span></span>

* <span data-ttu-id="82a60-966">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-966">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="82a60-967">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-967">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="82a60-968">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="82a60-968">Data Lake Analytics</span></span>

* <span data-ttu-id="82a60-969">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-969">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="82a60-970">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-970">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="82a60-971">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-971">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="82a60-972">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="82a60-972">Data Lake Store</span></span>

* <span data-ttu-id="82a60-973">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-973">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="82a60-974">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="82a60-974">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="82a60-975">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-975">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="82a60-976">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="82a60-976">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="82a60-977">対話</span><span class="sxs-lookup"><span data-stu-id="82a60-977">Interactive</span></span>

* <span data-ttu-id="82a60-978">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="82a60-978">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="82a60-979">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="82a60-979">Increased test coverage</span></span>
* <span data-ttu-id="82a60-980">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="82a60-980">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="82a60-981">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="82a60-981">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="82a60-982">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="82a60-982">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="82a60-983">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="82a60-983">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="82a60-984">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="82a60-984">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="82a60-985">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-985">Added `--progress` flag</span></span>
* <span data-ttu-id="82a60-986">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-986">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="82a60-987">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="82a60-987">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="82a60-988">IoT</span><span class="sxs-lookup"><span data-stu-id="82a60-988">IoT</span></span>

* <span data-ttu-id="82a60-989">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-989">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="82a60-990">(#3934)</span><span class="sxs-lookup"><span data-stu-id="82a60-990">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="82a60-991">Key Vault</span><span class="sxs-lookup"><span data-stu-id="82a60-991">Key vault</span></span>

* <span data-ttu-id="82a60-992">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-992">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="82a60-993">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="82a60-993">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="82a60-994">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="82a60-994">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="82a60-995">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="82a60-995">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="82a60-996">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="82a60-996">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="82a60-997">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="82a60-997">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="82a60-998">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-998">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="82a60-999">(#3307)</span><span class="sxs-lookup"><span data-stu-id="82a60-999">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="82a60-1000">ラボ</span><span class="sxs-lookup"><span data-stu-id="82a60-1000">Lab</span></span>

* <span data-ttu-id="82a60-1001">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1001">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="82a60-1002">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1002">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="82a60-1003">監視</span><span class="sxs-lookup"><span data-stu-id="82a60-1003">Monitor</span></span>

* <span data-ttu-id="82a60-1004">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="82a60-1004">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="82a60-1005">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1005">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="82a60-1006">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1006">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="82a60-1007">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1007">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="82a60-1008">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1008">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="82a60-1009">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="82a60-1009">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="82a60-1010">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1010">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="82a60-1011">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="82a60-1011">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="82a60-1012">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1012">`location` no longer required</span></span>
  * <span data-ttu-id="82a60-1013">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="82a60-1013">Add name and ID support for target</span></span>
  * <span data-ttu-id="82a60-1014">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="82a60-1014">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="82a60-1015">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-1015">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="82a60-1016">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1016">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="82a60-1017">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="82a60-1017">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="82a60-1018">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-1018">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="82a60-1019">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1019">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="82a60-1020">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-1020">Network</span></span>

* <span data-ttu-id="82a60-1021">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1021">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="82a60-1022">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1022">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="82a60-1023">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1023">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="82a60-1024">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1024">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="82a60-1025">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1025">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="82a60-1026">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1026">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="82a60-1027">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1027">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="82a60-1028">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1028">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="82a60-1029">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1029">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="82a60-1030">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1030">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="82a60-1031">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1031">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="82a60-1032">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1032">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="82a60-1033">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1033">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="82a60-1034">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1034">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="82a60-1035">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1035">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="82a60-1036">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1036">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="82a60-1037">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1037">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="82a60-1038">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1038">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="82a60-1039">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1039">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="82a60-1040">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1040">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="82a60-1041">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1041">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="82a60-1042">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1042">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="82a60-1043">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1043">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="82a60-1044">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="82a60-1044">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="82a60-1045">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="82a60-1045">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="82a60-1046">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="82a60-1046">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="82a60-1047">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="82a60-1047">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="82a60-1048">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-1048">Profile</span></span>

* <span data-ttu-id="82a60-1049">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-1049">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="82a60-1050">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-1050">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="82a60-1051">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="82a60-1051">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="82a60-1052">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1052">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="82a60-1053">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-1053">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="82a60-1054">RDBMS</span><span class="sxs-lookup"><span data-stu-id="82a60-1054">RDBMS</span></span>

* <span data-ttu-id="82a60-1055">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="82a60-1055">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="82a60-1056">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="82a60-1056">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="82a60-1057">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="82a60-1057">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="82a60-1058">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="82a60-1058">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-1059">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-1059">Resource</span></span>

* <span data-ttu-id="82a60-1060">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1060">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="82a60-1061">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1061">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="82a60-1062">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1062">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="82a60-1063">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-1063">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="82a60-1064">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="82a60-1064">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="82a60-1065">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1065">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="82a60-1066">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="82a60-1066">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="82a60-1067">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1067">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="82a60-1068">役割</span><span class="sxs-lookup"><span data-stu-id="82a60-1068">Role</span></span>

* <span data-ttu-id="82a60-1069">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-1069">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="82a60-1070">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="82a60-1070">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="82a60-1071">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="82a60-1071">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="82a60-1072">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="82a60-1072">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="82a60-1073">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1073">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="82a60-1074">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="82a60-1074">Service Fabric</span></span>
* <span data-ttu-id="82a60-1075">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="82a60-1075">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="82a60-1076">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="82a60-1076">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="82a60-1077">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="82a60-1077">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="82a60-1078">SQL</span><span class="sxs-lookup"><span data-stu-id="82a60-1078">SQL</span></span>

* <span data-ttu-id="82a60-1079">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1079">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="82a60-1080">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1080">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="82a60-1081">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1081">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-1082">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-1082">Storage</span></span>

* <span data-ttu-id="82a60-1083">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="82a60-1083">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="82a60-1084">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-1084">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="82a60-1085">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="82a60-1085">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="82a60-1086">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="82a60-1086">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="82a60-1087">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="82a60-1087">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="82a60-1088">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="82a60-1088">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-1089">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-1089">VM</span></span>

* <span data-ttu-id="82a60-1090">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-1090">Support configuring nsg</span></span>
* <span data-ttu-id="82a60-1091">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1091">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="82a60-1092">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="82a60-1092">Support managed service identities</span></span>
* <span data-ttu-id="82a60-1093">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1093">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="82a60-1094">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="82a60-1094">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="82a60-1095">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="82a60-1095">May 10, 2017</span></span>

<span data-ttu-id="82a60-1096">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="82a60-1096">Version 2.0.6</span></span>

* <span data-ttu-id="82a60-1097">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1097">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="82a60-1098">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1098">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="82a60-1099">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1099">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="82a60-1100">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1100">Include Cognitive Services module</span></span>
* <span data-ttu-id="82a60-1101">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1101">Include Service Fabric module</span></span>
* <span data-ttu-id="82a60-1102">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="82a60-1102">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="82a60-1103">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1103">Add support for CDN commands</span></span>
* <span data-ttu-id="82a60-1104">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1104">Remove Container module</span></span>
* <span data-ttu-id="82a60-1105">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="82a60-1105">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="82a60-1106">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="82a60-1106">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="82a60-1107">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-1107">Core</span></span>

* <span data-ttu-id="82a60-1108">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="82a60-1108">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="82a60-1109">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="82a60-1109">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="82a60-1110">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="82a60-1110">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="82a60-1111">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="82a60-1111">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="82a60-1112">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="82a60-1112">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="82a60-1113">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="82a60-1113">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="82a60-1114">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="82a60-1114">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="82a60-1115">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="82a60-1115">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="82a60-1116">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="82a60-1116">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="82a60-1117">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="82a60-1117">core: Improved performance</span></span>
* <span data-ttu-id="82a60-1118">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="82a60-1118">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="82a60-1119">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="82a60-1119">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-1120">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-1120">ACS</span></span>

* <span data-ttu-id="82a60-1121">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1121">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="82a60-1122">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1122">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="82a60-1123">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1123">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="82a60-1124">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="82a60-1124">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-1125">AppService</span><span class="sxs-lookup"><span data-stu-id="82a60-1125">AppService</span></span>

* <span data-ttu-id="82a60-1126">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1126">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="82a60-1127">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1127">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="82a60-1128">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="82a60-1128">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="82a60-1129">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1129">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="82a60-1130">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1130">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="82a60-1131">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="82a60-1131">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="82a60-1132">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="82a60-1132">support slot swap with preview</span></span>
* <span data-ttu-id="82a60-1133">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="82a60-1133">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="82a60-1134">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="82a60-1134">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="82a60-1135">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="82a60-1135">CosmosDB</span></span>

* <span data-ttu-id="82a60-1136">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1136">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="82a60-1137">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1137">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="82a60-1138">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1138">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="82a60-1139">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1139">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="82a60-1140">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="82a60-1140">Data Lake Analytics</span></span>

* <span data-ttu-id="82a60-1141">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1141">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="82a60-1142">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="82a60-1142">Add support for new catalog item type: package.</span></span> <span data-ttu-id="82a60-1143">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="82a60-1143">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="82a60-1144">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="82a60-1144">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="82a60-1145">テーブル</span><span class="sxs-lookup"><span data-stu-id="82a60-1145">Table</span></span>
  * <span data-ttu-id="82a60-1146">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="82a60-1146">Table valued function</span></span>
  * <span data-ttu-id="82a60-1147">表示</span><span class="sxs-lookup"><span data-stu-id="82a60-1147">View</span></span>
  * <span data-ttu-id="82a60-1148">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="82a60-1148">Table Statistics.</span></span> <span data-ttu-id="82a60-1149">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="82a60-1149">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="82a60-1150">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="82a60-1150">Data Lake Store</span></span>

* <span data-ttu-id="82a60-1151">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1151">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="82a60-1152">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="82a60-1152">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="82a60-1153">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="82a60-1153">missed help for access show.</span></span> <span data-ttu-id="82a60-1154">追加しました </span><span class="sxs-lookup"><span data-stu-id="82a60-1154">adding it.</span></span> <span data-ttu-id="82a60-1155">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="82a60-1155">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="82a60-1156">検索</span><span class="sxs-lookup"><span data-stu-id="82a60-1156">Find</span></span>

* <span data-ttu-id="82a60-1157">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="82a60-1157">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="82a60-1158">KeyVault</span><span class="sxs-lookup"><span data-stu-id="82a60-1158">KeyVault</span></span>

* <span data-ttu-id="82a60-1159">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1159">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="82a60-1160">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1160">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="82a60-1161">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="82a60-1161">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="82a60-1162">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1162">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="82a60-1163">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="82a60-1163">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="82a60-1164">ラボ</span><span class="sxs-lookup"><span data-stu-id="82a60-1164">Lab</span></span>

* <span data-ttu-id="82a60-1165">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1165">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="82a60-1166">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1166">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="82a60-1167">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1167">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="82a60-1168">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1168">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="82a60-1169">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1169">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="82a60-1170">監視</span><span class="sxs-lookup"><span data-stu-id="82a60-1170">Monitor</span></span>

* <span data-ttu-id="82a60-1171">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="82a60-1171">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="82a60-1172">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="82a60-1172">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="82a60-1173">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-1173">Network</span></span>

* <span data-ttu-id="82a60-1174">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1174">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="82a60-1175">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1175">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="82a60-1176">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1176">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="82a60-1177">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1177">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="82a60-1178">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1178">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="82a60-1179">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1179">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="82a60-1180">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1180">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="82a60-1181">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1181">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="82a60-1182">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1182">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="82a60-1183">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1183">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="82a60-1184">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1184">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="82a60-1185">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1185">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="82a60-1186">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1186">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="82a60-1187">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1187">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="82a60-1188">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="82a60-1188">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="82a60-1189">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1189">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="82a60-1190">プロファイル</span><span class="sxs-lookup"><span data-stu-id="82a60-1190">Profile</span></span>

* <span data-ttu-id="82a60-1191">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="82a60-1191">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="82a60-1192">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="82a60-1192">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="82a60-1193">Redis</span><span class="sxs-lookup"><span data-stu-id="82a60-1193">Redis</span></span>

* <span data-ttu-id="82a60-1194">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1194">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="82a60-1195">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1195">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="82a60-1196">リソース</span><span class="sxs-lookup"><span data-stu-id="82a60-1196">Resource</span></span>

* <span data-ttu-id="82a60-1197">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="82a60-1197">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="82a60-1198">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="82a60-1198">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="82a60-1199">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="82a60-1199">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="82a60-1200">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="82a60-1200">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="82a60-1201">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="82a60-1201">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="82a60-1202">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="82a60-1202">Add docs for az lock update.</span></span> <span data-ttu-id="82a60-1203">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="82a60-1203">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="82a60-1204">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="82a60-1204">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="82a60-1205">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="82a60-1205">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="82a60-1206">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="82a60-1206">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="82a60-1207">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="82a60-1207">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="82a60-1208">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="82a60-1208">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="82a60-1209">役割</span><span class="sxs-lookup"><span data-stu-id="82a60-1209">Role</span></span>

* <span data-ttu-id="82a60-1210">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="82a60-1210">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="82a60-1211">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="82a60-1211">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="82a60-1212">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="82a60-1212">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="82a60-1213">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="82a60-1213">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="82a60-1214">SQL</span><span class="sxs-lookup"><span data-stu-id="82a60-1214">SQL</span></span>

* <span data-ttu-id="82a60-1215">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="82a60-1215">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="82a60-1216">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="82a60-1216">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="82a60-1217">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-1217">Storage</span></span>

* <span data-ttu-id="82a60-1218">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="82a60-1218">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="82a60-1219">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1219">Add support for incremental blob copy</span></span>
* <span data-ttu-id="82a60-1220">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1220">Add support for large block blob upload</span></span>
* <span data-ttu-id="82a60-1221">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="82a60-1221">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-1222">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-1222">VM</span></span>

* <span data-ttu-id="82a60-1223">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="82a60-1223">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="82a60-1224">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="82a60-1224">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="82a60-1225">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="82a60-1225">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="82a60-1226">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="82a60-1226">az vm/vmss disk</span></span>
  3. <span data-ttu-id="82a60-1227">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="82a60-1227">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="82a60-1228">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="82a60-1228">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="82a60-1229">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="82a60-1229">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="82a60-1230">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="82a60-1230">April 3, 2017</span></span>

<span data-ttu-id="82a60-1231">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="82a60-1231">Version 2.0.2</span></span>

<span data-ttu-id="82a60-1232">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="82a60-1232">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="82a60-1233">コア</span><span class="sxs-lookup"><span data-stu-id="82a60-1233">Core</span></span>

* <span data-ttu-id="82a60-1234">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="82a60-1234">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="82a60-1235">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="82a60-1235">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="82a60-1236">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="82a60-1236">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="82a60-1237">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="82a60-1237">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="82a60-1238">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="82a60-1238">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="82a60-1239">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="82a60-1239">Add prompting for missing template parameters.</span></span> <span data-ttu-id="82a60-1240">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="82a60-1240">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="82a60-1241">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="82a60-1241">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="82a60-1242">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="82a60-1242">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="82a60-1243">ACS</span><span class="sxs-lookup"><span data-stu-id="82a60-1243">ACS</span></span>

* <span data-ttu-id="82a60-1244">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="82a60-1244">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="82a60-1245">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="82a60-1245">Add support for ssh key password prompting.</span></span> <span data-ttu-id="82a60-1246">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="82a60-1246">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="82a60-1247">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="82a60-1247">Add support for windows clusters.</span></span> <span data-ttu-id="82a60-1248">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="82a60-1248">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="82a60-1249">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="82a60-1249">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="82a60-1250">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="82a60-1250">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="82a60-1251">AppService</span><span class="sxs-lookup"><span data-stu-id="82a60-1251">AppService</span></span>

* <span data-ttu-id="82a60-1252">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="82a60-1252">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="82a60-1253">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="82a60-1253">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="82a60-1254">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="82a60-1254">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="82a60-1255">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="82a60-1255">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="82a60-1256">DataLake</span><span class="sxs-lookup"><span data-stu-id="82a60-1256">DataLake</span></span>

* <span data-ttu-id="82a60-1257">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="82a60-1257">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="82a60-1258">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="82a60-1258">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="82a60-1259">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="82a60-1259">DocuemntDB</span></span>

* <span data-ttu-id="82a60-1260">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="82a60-1260">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="82a60-1261">VM</span><span class="sxs-lookup"><span data-stu-id="82a60-1261">VM</span></span>

* <span data-ttu-id="82a60-1262">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="82a60-1262">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="82a60-1263">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="82a60-1263">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="82a60-1264">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="82a60-1264">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="82a60-1265">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="82a60-1265">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="82a60-1266">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="82a60-1266">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="82a60-1267">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="82a60-1267">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="82a60-1268">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="82a60-1268">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="82a60-1269">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="82a60-1269">February 27, 2017</span></span>

<span data-ttu-id="82a60-1270">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="82a60-1270">Version 2.0.0</span></span>

<span data-ttu-id="82a60-1271">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="82a60-1271">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="82a60-1272">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="82a60-1272">Container Service (acs)</span></span>
- <span data-ttu-id="82a60-1273">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="82a60-1273">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="82a60-1274">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="82a60-1274">Networking</span></span>
- <span data-ttu-id="82a60-1275">Storage</span><span class="sxs-lookup"><span data-stu-id="82a60-1275">Storage</span></span>

<span data-ttu-id="82a60-1276">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="82a60-1276">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="82a60-1277">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="82a60-1277">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="82a60-1278">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="82a60-1278">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="82a60-1279">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="82a60-1279">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="82a60-1280">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="82a60-1280">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="82a60-1281">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="82a60-1281">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="82a60-1282">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="82a60-1282">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="82a60-1283">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="82a60-1283">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="82a60-1284">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="82a60-1284">Provide feedback from the command line with the `az feedback` command</span></span>

