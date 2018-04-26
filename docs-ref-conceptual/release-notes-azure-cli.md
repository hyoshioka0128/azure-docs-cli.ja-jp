---
title: Azure CLI 2.0 リリース ノート
description: Azure CLI 2.0 の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 04/10/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 1e6bd4cd8bab853fb417ed9c4dd71d56e5de7cdc
ms.sourcegitcommit: 204fd027d3668959b98b936969ccb41eada0fd29
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="8f25e-103">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="8f25e-103">Azure CLI 2.0 release notes</span></span>

## <a name="april-10-2018"></a><span data-ttu-id="8f25e-104">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-104">April 10, 2018</span></span>

<span data-ttu-id="8f25e-105">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="8f25e-105">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="8f25e-106">ACR</span><span class="sxs-lookup"><span data-stu-id="8f25e-106">ACR</span></span>

* <span data-ttu-id="8f25e-107">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-107">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-108">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-108">ACS</span></span>

* <span data-ttu-id="8f25e-109">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-109">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-110">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-110">Appservice</span></span>

* [重大な変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="8f25e-112">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-112">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="8f25e-113">BatchAI</span><span class="sxs-lookup"><span data-stu-id="8f25e-113">BatchAI</span></span>

* <span data-ttu-id="8f25e-114">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-114">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="8f25e-115">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="8f25e-115">Job level mounting</span></span>
 - <span data-ttu-id="8f25e-116">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="8f25e-116">Environment variables with secret values</span></span>
 - <span data-ttu-id="8f25e-117">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="8f25e-117">Performance counters settings</span></span>
 - <span data-ttu-id="8f25e-118">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="8f25e-118">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="8f25e-119">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="8f25e-119">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="8f25e-120">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="8f25e-120">Usage and limits reporting</span></span>
 - <span data-ttu-id="8f25e-121">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="8f25e-121">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="8f25e-122">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="8f25e-122">Support for custom images</span></span>
 - <span data-ttu-id="8f25e-123">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-123">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="8f25e-124">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-124">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="8f25e-125">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="8f25e-125">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="8f25e-126">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="8f25e-126">National clouds are supported</span></span>
* <span data-ttu-id="8f25e-127">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-127">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="8f25e-128">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-128">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="8f25e-129">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-129">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="8f25e-130">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-130">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="8f25e-131">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="8f25e-131">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="8f25e-132">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="8f25e-132">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="8f25e-133">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-133">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="8f25e-134">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-134">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="8f25e-135">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="8f25e-135">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="8f25e-136">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-136">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="8f25e-137">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-137">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="8f25e-138">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-138">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="8f25e-139">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-139">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="8f25e-140">課金</span><span class="sxs-lookup"><span data-stu-id="8f25e-140">Billing</span></span>

* <span data-ttu-id="8f25e-141">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-141">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="8f25e-142">消費</span><span class="sxs-lookup"><span data-stu-id="8f25e-142">Consumption</span></span>

* <span data-ttu-id="8f25e-143">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-143">Added `marketplace` commands</span></span>
* <span data-ttu-id="8f25e-144">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-144">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="8f25e-145">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-145">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="8f25e-146">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-146">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="8f25e-147">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-147">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="8f25e-148">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-148">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="8f25e-149">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8f25e-149">Container</span></span>

* <span data-ttu-id="8f25e-150">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-150">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="8f25e-151">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-151">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="8f25e-152">内線番号</span><span class="sxs-lookup"><span data-stu-id="8f25e-152">Extension</span></span>

* <span data-ttu-id="8f25e-153">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-153">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="8f25e-154">対話</span><span class="sxs-lookup"><span data-stu-id="8f25e-154">Interactive</span></span>

* <span data-ttu-id="8f25e-155">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-155">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="8f25e-156">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-156">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="8f25e-157">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-157">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-158">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-158">Network</span></span>

* <span data-ttu-id="8f25e-159">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-159">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="8f25e-160">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-160">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="8f25e-161">#4910</span><span class="sxs-lookup"><span data-stu-id="8f25e-161">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="8f25e-162">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-162">Added `ddos-protection` commands to create DDoS protection plans</span></span> 
* <span data-ttu-id="8f25e-163">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="8f25e-163">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="8f25e-164">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-164">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="8f25e-165">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-165">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="8f25e-166">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-166">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="8f25e-167">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8f25e-167">Profile</span></span>

* <span data-ttu-id="8f25e-168">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-168">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="8f25e-169">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-169">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="8f25e-170">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8f25e-170">RDBMS</span></span>

* <span data-ttu-id="8f25e-171">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-171">Added `georestore` command</span></span>
* <span data-ttu-id="8f25e-172">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-172">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-173">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-173">Resource</span></span>

* <span data-ttu-id="8f25e-174">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-174">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="8f25e-175">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-175">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="8f25e-176">SQL</span><span class="sxs-lookup"><span data-stu-id="8f25e-176">SQL</span></span>

* <span data-ttu-id="8f25e-177">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-177">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-178">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-178">Storage</span></span>

* <span data-ttu-id="8f25e-179">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-179">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-180">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-180">VM</span></span>

* <span data-ttu-id="8f25e-181">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-181">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="8f25e-182">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-182">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大な変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="8f25e-184">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-184">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="8f25e-185">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-185">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="8f25e-186">#5718</span><span class="sxs-lookup"><span data-stu-id="8f25e-186">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="8f25e-187">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-187">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="8f25e-188">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-188">March 27, 2018</span></span>

<span data-ttu-id="8f25e-189">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="8f25e-189">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="8f25e-190">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-190">Core</span></span>

* <span data-ttu-id="8f25e-191">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="8f25e-191">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-192">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-192">ACS</span></span>

* <span data-ttu-id="8f25e-193">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-193">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-194">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-194">Appservice</span></span>

* <span data-ttu-id="8f25e-195">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-195">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="8f25e-196">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-196">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="8f25e-197">バックアップ</span><span class="sxs-lookup"><span data-stu-id="8f25e-197">Backup</span></span>

* <span data-ttu-id="8f25e-198">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-198">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="8f25e-199">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="8f25e-199">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="8f25e-200">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-200">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="8f25e-201">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-201">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="8f25e-202">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8f25e-202">Container</span></span>

* <span data-ttu-id="8f25e-203">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-203">Added `container exec` command.</span></span> <span data-ttu-id="8f25e-204">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="8f25e-204">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="8f25e-205">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="8f25e-205">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="8f25e-206">内線番号</span><span class="sxs-lookup"><span data-stu-id="8f25e-206">Extension</span></span>

* <span data-ttu-id="8f25e-207">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-207">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="8f25e-208">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-208">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="8f25e-209">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-209">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="8f25e-210">対話</span><span class="sxs-lookup"><span data-stu-id="8f25e-210">Interactive</span></span>

* <span data-ttu-id="8f25e-211">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-211">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="8f25e-212">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-212">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="8f25e-213">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-213">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="8f25e-214">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-214">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="8f25e-215">ラボ</span><span class="sxs-lookup"><span data-stu-id="8f25e-215">Lab</span></span>

* <span data-ttu-id="8f25e-216">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-216">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="8f25e-217">監視</span><span class="sxs-lookup"><span data-stu-id="8f25e-217">Monitor</span></span>

* <span data-ttu-id="8f25e-218">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="8f25e-218">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="8f25e-219">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="8f25e-219">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="8f25e-220">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="8f25e-220">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-221">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-221">Network</span></span>

* <span data-ttu-id="8f25e-222">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-222">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="8f25e-223">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8f25e-223">Profile</span></span>

* <span data-ttu-id="8f25e-224">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-224">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="8f25e-225">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8f25e-225">RDBMS</span></span>

* <span data-ttu-id="8f25e-226">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-226">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-227">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-227">Resource</span></span>

* [重大な変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="8f25e-229">役割</span><span class="sxs-lookup"><span data-stu-id="8f25e-229">Role</span></span>

* <span data-ttu-id="8f25e-230">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-230">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="8f25e-231">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-231">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="8f25e-232">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-232">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="8f25e-233">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-233">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="8f25e-234">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-234">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-235">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-235">Storage</span></span>

* <span data-ttu-id="8f25e-236">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-236">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="8f25e-237">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-237">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-238">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-238">VM</span></span>

* <span data-ttu-id="8f25e-239">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-239">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="8f25e-240">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-240">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="8f25e-241">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-241">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="8f25e-242">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-242">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="8f25e-243">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-243">March 13, 2018</span></span>

<span data-ttu-id="8f25e-244">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="8f25e-244">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="8f25e-245">ACR</span><span class="sxs-lookup"><span data-stu-id="8f25e-245">ACR</span></span>

* <span data-ttu-id="8f25e-246">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-246">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="8f25e-247">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-247">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="8f25e-248">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-248">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-249">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-249">ACS</span></span>

* <span data-ttu-id="8f25e-250">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-250">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="8f25e-251">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-251">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="8f25e-252">Advisor</span><span class="sxs-lookup"><span data-stu-id="8f25e-252">Advisor</span></span>

* <span data-ttu-id="8f25e-253">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-253">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="8f25e-254">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-254">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="8f25e-255">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-255">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span> 
* <span data-ttu-id="8f25e-256">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-256">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="8f25e-257">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-257">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-258">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-258">Appservice</span></span>

* <span data-ttu-id="8f25e-259">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-259">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="8f25e-260">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-260">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="8f25e-261">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="8f25e-261">Eventhubs</span></span>

* <span data-ttu-id="8f25e-262">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-262">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="8f25e-263">内線番号</span><span class="sxs-lookup"><span data-stu-id="8f25e-263">Extension</span></span>

* <span data-ttu-id="8f25e-264">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-264">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="8f25e-265">対話</span><span class="sxs-lookup"><span data-stu-id="8f25e-265">Interactive</span></span>

* <span data-ttu-id="8f25e-266">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="8f25e-266">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="8f25e-267">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="8f25e-267">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="8f25e-268">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="8f25e-268">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="8f25e-269">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-269">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="8f25e-270">監視</span><span class="sxs-lookup"><span data-stu-id="8f25e-270">Monitor</span></span>

* <span data-ttu-id="8f25e-271">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-271">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="8f25e-272">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-272">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="8f25e-273">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-273">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="8f25e-274">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-274">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-275">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-275">Network</span></span>

* <span data-ttu-id="8f25e-276">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-276">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="8f25e-277">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-277">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="8f25e-278">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-278">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="8f25e-279">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-279">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="8f25e-280">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8f25e-280">Profile</span></span>

* <span data-ttu-id="8f25e-281">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-281">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="8f25e-282">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-282">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="8f25e-283">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8f25e-283">RDBMS</span></span>

* <span data-ttu-id="8f25e-284">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-284">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="8f25e-285">Service Bus</span><span class="sxs-lookup"><span data-stu-id="8f25e-285">Service Bus</span></span>

* <span data-ttu-id="8f25e-286">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-286">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-287">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-287">Storage</span></span>

* <span data-ttu-id="8f25e-288">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-288">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="8f25e-289">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-289">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-290">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-290">VM</span></span>

* <span data-ttu-id="8f25e-291">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-291">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="8f25e-292">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-292">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="8f25e-293">非推奨にしたコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-293">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="8f25e-294">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-294">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="8f25e-295">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-295">February 27, 2018</span></span>

<span data-ttu-id="8f25e-296">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="8f25e-296">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="8f25e-297">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-297">Core</span></span>

* <span data-ttu-id="8f25e-298">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="8f25e-298">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="8f25e-299">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-299">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="8f25e-300">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-300">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-301">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-301">ACS</span></span>

* <span data-ttu-id="8f25e-302">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-302">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="8f25e-303">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="8f25e-303">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="8f25e-304">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-304">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="8f25e-305">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-305">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-306">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-306">Appservice</span></span>

* <span data-ttu-id="8f25e-307">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="8f25e-307">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="8f25e-308">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="8f25e-308">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="8f25e-309">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="8f25e-309">Cognitive Services</span></span>

* <span data-ttu-id="8f25e-310">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-310">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="8f25e-311">消費</span><span class="sxs-lookup"><span data-stu-id="8f25e-311">Consumption</span></span>

* <span data-ttu-id="8f25e-312">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-312">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="8f25e-313">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-313">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="8f25e-314">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8f25e-314">Container</span></span>

* <span data-ttu-id="8f25e-315">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-315">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-316">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-316">Network</span></span>

* <span data-ttu-id="8f25e-317">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="8f25e-317">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-318">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-318">Resource</span></span>

* <span data-ttu-id="8f25e-319">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-319">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="8f25e-320">役割</span><span class="sxs-lookup"><span data-stu-id="8f25e-320">Role</span></span>

* <span data-ttu-id="8f25e-321">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-321">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="8f25e-322">SQL</span><span class="sxs-lookup"><span data-stu-id="8f25e-322">SQL</span></span>

* <span data-ttu-id="8f25e-323">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-323">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-324">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-324">Storage</span></span>

* <span data-ttu-id="8f25e-325">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-325">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-326">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-326">VM</span></span>

* <span data-ttu-id="8f25e-327">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-327">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="8f25e-328">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-328">February 13, 2018</span></span>

<span data-ttu-id="8f25e-329">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="8f25e-329">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="8f25e-330">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-330">Core</span></span>

* <span data-ttu-id="8f25e-331">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-331">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-332">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-332">ACS</span></span>

* <span data-ttu-id="8f25e-333">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-333">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="8f25e-334">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-334">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="8f25e-335">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-335">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="8f25e-336">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-336">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="8f25e-337">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-337">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="8f25e-338">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-338">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="8f25e-339">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-339">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="8f25e-340">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="8f25e-340">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-341">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-341">Appservice</span></span>

* <span data-ttu-id="8f25e-342">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-342">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="8f25e-343">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-343">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="8f25e-344">CDN</span><span class="sxs-lookup"><span data-stu-id="8f25e-344">CDN</span></span>

* <span data-ttu-id="8f25e-345">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-345">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="8f25e-346">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8f25e-346">Container</span></span>

* <span data-ttu-id="8f25e-347">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-347">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="8f25e-348">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-348">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8f25e-349">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8f25e-349">CosmosDB</span></span>

* <span data-ttu-id="8f25e-350">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-350">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="8f25e-351">内線番号</span><span class="sxs-lookup"><span data-stu-id="8f25e-351">Extension</span></span>

* <span data-ttu-id="8f25e-352">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-352">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="8f25e-353">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-353">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="8f25e-354">フィードバック</span><span class="sxs-lookup"><span data-stu-id="8f25e-354">Feedback</span></span>

* <span data-ttu-id="8f25e-355">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-355">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="8f25e-356">対話</span><span class="sxs-lookup"><span data-stu-id="8f25e-356">Interactive</span></span>

* <span data-ttu-id="8f25e-357">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-357">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="8f25e-358">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-358">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="8f25e-359">IoT</span><span class="sxs-lookup"><span data-stu-id="8f25e-359">IoT</span></span>

* <span data-ttu-id="8f25e-360">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-360">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="8f25e-361">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-361">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="8f25e-362">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-362">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="8f25e-363">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-363">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="8f25e-364">監視</span><span class="sxs-lookup"><span data-stu-id="8f25e-364">Monitor</span></span>

* <span data-ttu-id="8f25e-365">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-365">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-366">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-366">Network</span></span>

* <span data-ttu-id="8f25e-367">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-367">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="8f25e-368">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8f25e-368">Profile</span></span>

* <span data-ttu-id="8f25e-369">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-369">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-370">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-370">Resource</span></span>

* <span data-ttu-id="8f25e-371">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-371">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="8f25e-372">役割</span><span class="sxs-lookup"><span data-stu-id="8f25e-372">Role</span></span>

* <span data-ttu-id="8f25e-373">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-373">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="8f25e-374">SQL</span><span class="sxs-lookup"><span data-stu-id="8f25e-374">SQL</span></span>

* <span data-ttu-id="8f25e-375">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-375">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="8f25e-376">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-376">Added `sql db rename`</span></span>
* <span data-ttu-id="8f25e-377">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-377">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-378">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-378">Storage</span></span>

* <span data-ttu-id="8f25e-379">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-379">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-380">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-380">VM</span></span>

* <span data-ttu-id="8f25e-381">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-381">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="8f25e-382">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-382">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="8f25e-383">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="8f25e-383">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="8f25e-384">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-384">January 31, 2018</span></span>

<span data-ttu-id="8f25e-385">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="8f25e-385">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="8f25e-386">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-386">Core</span></span>

* <span data-ttu-id="8f25e-387">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-387">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="8f25e-388">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-388">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="8f25e-389">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-389">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="8f25e-390">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="8f25e-390">Use `--verbose` to see</span></span>
* <span data-ttu-id="8f25e-391">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="8f25e-391">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-392">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-392">ACS</span></span>

* <span data-ttu-id="8f25e-393">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-393">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="8f25e-394">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-394">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-395">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-395">Appservice</span></span>

* <span data-ttu-id="8f25e-396">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="8f25e-396">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="8f25e-397">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-397">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="8f25e-398">CDN</span><span class="sxs-lookup"><span data-stu-id="8f25e-398">CDN</span></span>

* <span data-ttu-id="8f25e-399">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-399">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8f25e-400">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8f25e-400">CosmosDB</span></span>

* <span data-ttu-id="8f25e-401">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-401">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="8f25e-402">対話</span><span class="sxs-lookup"><span data-stu-id="8f25e-402">Interactive</span></span>

* <span data-ttu-id="8f25e-403">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-403">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-404">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-404">Network</span></span>

* <span data-ttu-id="8f25e-405">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-405">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="8f25e-406">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-406">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="8f25e-407">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-407">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="8f25e-408">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-408">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="8f25e-409">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-409">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="8f25e-410">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-410">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="8f25e-411">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-411">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="8f25e-412">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-412">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="8f25e-413">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-413">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="8f25e-414">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-414">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="8f25e-415">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8f25e-415">Profile</span></span>

* <span data-ttu-id="8f25e-416">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-416">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-417">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-417">Resource</span></span>

* <span data-ttu-id="8f25e-418">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-418">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-419">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-419">Storage</span></span>

* <span data-ttu-id="8f25e-420">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-420">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="8f25e-421">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-421">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="8f25e-422">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-422">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="8f25e-423">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-423">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="8f25e-424">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-424">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-425">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-425">VM</span></span>

* <span data-ttu-id="8f25e-426">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-426">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="8f25e-427">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-427">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="8f25e-428">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-428">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="8f25e-429">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-429">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="8f25e-430">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-430">January 17, 2018</span></span>

<span data-ttu-id="8f25e-431">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="8f25e-431">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="8f25e-432">ACR</span><span class="sxs-lookup"><span data-stu-id="8f25e-432">ACR</span></span>

* <span data-ttu-id="8f25e-433">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-433">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="8f25e-434">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-434">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-435">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-435">ACS</span></span>

* <span data-ttu-id="8f25e-436">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-436">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="8f25e-437">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-437">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-438">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-438">Appservice</span></span>

* <span data-ttu-id="8f25e-439">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-439">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="8f25e-440">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-440">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="8f25e-441">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-441">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="8f25e-442">バックアップ</span><span class="sxs-lookup"><span data-stu-id="8f25e-442">Backup</span></span>

* <span data-ttu-id="8f25e-443">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-443">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="8f25e-444">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-444">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="8f25e-445">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-445">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="8f25e-446">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-446">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="8f25e-447">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-447">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="8f25e-448">Batch</span><span class="sxs-lookup"><span data-stu-id="8f25e-448">Batch</span></span>

* <span data-ttu-id="8f25e-449">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-449">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="8f25e-450">クラウド</span><span class="sxs-lookup"><span data-stu-id="8f25e-450">Cloud</span></span>

* <span data-ttu-id="8f25e-451">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-451">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="8f25e-452">消費</span><span class="sxs-lookup"><span data-stu-id="8f25e-452">Consumption</span></span>

* <span data-ttu-id="8f25e-453">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-453">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="8f25e-454">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8f25e-454">Event Grid</span></span>

* <span data-ttu-id="8f25e-455">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-455">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="8f25e-456">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-456">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="8f25e-457">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-457">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="8f25e-458">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8f25e-458">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="8f25e-459">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-459">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="8f25e-460">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-460">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="8f25e-461">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-461">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="8f25e-462">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-462">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="8f25e-463">対話</span><span class="sxs-lookup"><span data-stu-id="8f25e-463">Interactive</span></span>

* <span data-ttu-id="8f25e-464">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-464">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="8f25e-465">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-465">Fixed errors on startup</span></span>
* <span data-ttu-id="8f25e-466">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-466">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="8f25e-467">IoT</span><span class="sxs-lookup"><span data-stu-id="8f25e-467">IoT</span></span>

* <span data-ttu-id="8f25e-468">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-468">Added support for device provisioning service</span></span>
* <span data-ttu-id="8f25e-469">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-469">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="8f25e-470">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-470">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="8f25e-471">監視</span><span class="sxs-lookup"><span data-stu-id="8f25e-471">Monitor</span></span>

* <span data-ttu-id="8f25e-472">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-472">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="8f25e-473">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-473">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="8f25e-474">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-474">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-475">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-475">Network</span></span>

* <span data-ttu-id="8f25e-476">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-476">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="8f25e-477">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-477">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="8f25e-478">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8f25e-478">Profile</span></span>

* <span data-ttu-id="8f25e-479">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-479">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="8f25e-480">役割</span><span class="sxs-lookup"><span data-stu-id="8f25e-480">Role</span></span>

* <span data-ttu-id="8f25e-481">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-481">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8f25e-482">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8f25e-482">Service Fabric</span></span>

* <span data-ttu-id="8f25e-483">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-483">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="8f25e-484">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-484">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-485">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-485">VM</span></span>

* <span data-ttu-id="8f25e-486">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="8f25e-486">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="8f25e-487">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-487">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="8f25e-488">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-488">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="8f25e-489">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-489">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="8f25e-490">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-490">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="8f25e-491">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-491">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="8f25e-492">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-492">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="8f25e-493">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-493">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="8f25e-494">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-494">December 19, 2017</span></span>

<span data-ttu-id="8f25e-495">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="8f25e-495">Version 2.0.23</span></span>

* <span data-ttu-id="8f25e-496">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-496">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="8f25e-497">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8f25e-497">Container</span></span>

* <span data-ttu-id="8f25e-498">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-498">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-499">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-499">Network</span></span>

* <span data-ttu-id="8f25e-500">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-500">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="8f25e-501">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-501">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-502">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-502">Storage</span></span>

* <span data-ttu-id="8f25e-503">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-503">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-504">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-504">VM</span></span>

* <span data-ttu-id="8f25e-505">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-505">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="8f25e-506">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-506">December 5, 2017</span></span>

<span data-ttu-id="8f25e-507">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="8f25e-507">Version 2.0.22</span></span>

* <span data-ttu-id="8f25e-508">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-508">Removed `az component` commands.</span></span> <span data-ttu-id="8f25e-509">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8f25e-509">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="8f25e-510">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-510">Core</span></span>
* <span data-ttu-id="8f25e-511">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-511">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="8f25e-512">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-512">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-513">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-513">ACS</span></span>

* <span data-ttu-id="8f25e-514">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-514">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="8f25e-515">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-515">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="8f25e-516">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-516">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="8f25e-517">Advisor</span><span class="sxs-lookup"><span data-stu-id="8f25e-517">Advisor</span></span>

* <span data-ttu-id="8f25e-518">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-518">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-519">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-519">Appservice</span></span>

* <span data-ttu-id="8f25e-520">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-520">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="8f25e-521">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-521">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="8f25e-522">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-522">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="8f25e-523">消費</span><span class="sxs-lookup"><span data-stu-id="8f25e-523">Consumption</span></span>

* <span data-ttu-id="8f25e-524">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-524">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="8f25e-525">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8f25e-525">Container</span></span>

* <span data-ttu-id="8f25e-526">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-526">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="8f25e-527">監視</span><span class="sxs-lookup"><span data-stu-id="8f25e-527">Monitor</span></span>

* <span data-ttu-id="8f25e-528">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-528">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-529">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-529">Resource</span></span>

* <span data-ttu-id="8f25e-530">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-530">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="8f25e-531">役割</span><span class="sxs-lookup"><span data-stu-id="8f25e-531">Role</span></span>

* <span data-ttu-id="8f25e-532">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-532">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="8f25e-533">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-533">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="8f25e-534">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-534">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="8f25e-535">SQL</span><span class="sxs-lookup"><span data-stu-id="8f25e-535">SQL</span></span>

* <span data-ttu-id="8f25e-536">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-536">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="8f25e-537">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-537">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-538">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-538">VM</span></span>

* <span data-ttu-id="8f25e-539">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-539">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="8f25e-540">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-540">November 14, 2017</span></span>

<span data-ttu-id="8f25e-541">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="8f25e-541">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="8f25e-542">ACR</span><span class="sxs-lookup"><span data-stu-id="8f25e-542">ACR</span></span>

* <span data-ttu-id="8f25e-543">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-543">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="8f25e-544">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-544">ACS</span></span>

* <span data-ttu-id="8f25e-545">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-545">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="8f25e-546">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-546">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="8f25e-547">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-547">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="8f25e-548">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-548">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="8f25e-549">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-549">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-550">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-550">Appservice</span></span>

* <span data-ttu-id="8f25e-551">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-551">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="8f25e-552">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-552">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="8f25e-553">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-553">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="8f25e-554">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-554">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="8f25e-555">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-555">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="8f25e-556">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="8f25e-556">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="8f25e-557">Batch</span><span class="sxs-lookup"><span data-stu-id="8f25e-557">Batch</span></span>

* <span data-ttu-id="8f25e-558">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-558">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="8f25e-559">Batchai</span><span class="sxs-lookup"><span data-stu-id="8f25e-559">Batchai</span></span>

* <span data-ttu-id="8f25e-560">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-560">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="8f25e-561">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-561">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="8f25e-562">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-562">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="8f25e-563">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-563">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="8f25e-564">クラウド</span><span class="sxs-lookup"><span data-stu-id="8f25e-564">Cloud</span></span>

* <span data-ttu-id="8f25e-565">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-565">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="8f25e-566">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8f25e-566">Container</span></span>

* <span data-ttu-id="8f25e-567">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-567">Added support to open multiple ports</span></span>
* <span data-ttu-id="8f25e-568">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-568">Added container group restart policy</span></span>
* <span data-ttu-id="8f25e-569">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-569">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="8f25e-570">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-570">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8f25e-571">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8f25e-571">Data Lake Analytics</span></span>

* <span data-ttu-id="8f25e-572">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-572">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8f25e-573">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8f25e-573">Data Lake Store</span></span>

* <span data-ttu-id="8f25e-574">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-574">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="8f25e-575">内線番号</span><span class="sxs-lookup"><span data-stu-id="8f25e-575">Extension</span></span>

* <span data-ttu-id="8f25e-576">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-576">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="8f25e-577">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-577">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="8f25e-578">IoT</span><span class="sxs-lookup"><span data-stu-id="8f25e-578">IoT</span></span>

* <span data-ttu-id="8f25e-579">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-579">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="8f25e-580">監視</span><span class="sxs-lookup"><span data-stu-id="8f25e-580">Monitor</span></span>

* <span data-ttu-id="8f25e-581">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-581">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-582">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-582">Network</span></span>

* <span data-ttu-id="8f25e-583">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-583">Added support for CAA DNS records</span></span>
* <span data-ttu-id="8f25e-584">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-584">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="8f25e-585">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-585">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="8f25e-586">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-586">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="8f25e-587">Reservations</span><span class="sxs-lookup"><span data-stu-id="8f25e-587">Reservations</span></span>

* <span data-ttu-id="8f25e-588">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-588">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-589">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-589">Resource</span></span>

* <span data-ttu-id="8f25e-590">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-590">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="8f25e-591">SQL</span><span class="sxs-lookup"><span data-stu-id="8f25e-591">SQL</span></span>

* <span data-ttu-id="8f25e-592">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-592">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-593">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-593">Storage</span></span>

* <span data-ttu-id="8f25e-594">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-594">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="8f25e-595">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-595">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="8f25e-596">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-596">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="8f25e-597">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-597">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="8f25e-598">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-598">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="8f25e-599">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-599">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="8f25e-600">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-600">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-601">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-601">VM</span></span>

* <span data-ttu-id="8f25e-602">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-602">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="8f25e-603">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-603">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="8f25e-604">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-604">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="8f25e-605">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-605">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="8f25e-606">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-606">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="8f25e-607">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-607">October 24, 2017</span></span>

<span data-ttu-id="8f25e-608">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="8f25e-608">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="8f25e-609">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-609">Core</span></span>

* <span data-ttu-id="8f25e-610">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-610">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="8f25e-611">ACR</span><span class="sxs-lookup"><span data-stu-id="8f25e-611">ACR</span></span>

* <span data-ttu-id="8f25e-612">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-612">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="8f25e-613">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-613">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="8f25e-614">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-614">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-615">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-615">ACS</span></span>

* <span data-ttu-id="8f25e-616">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-616">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="8f25e-617">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-617">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-618">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-618">Appservice</span></span>

* <span data-ttu-id="8f25e-619">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-619">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="8f25e-620">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8f25e-620">Component</span></span>

* <span data-ttu-id="8f25e-621">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-621">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="8f25e-622">監視</span><span class="sxs-lookup"><span data-stu-id="8f25e-622">Monitor</span></span>

* <span data-ttu-id="8f25e-623">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-623">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-624">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-624">Resource</span></span>

* <span data-ttu-id="8f25e-625">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-625">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="8f25e-626">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-626">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-627">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-627">VM</span></span>

* <span data-ttu-id="8f25e-628">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-628">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="8f25e-629">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-629">October 9, 2017</span></span>

<span data-ttu-id="8f25e-630">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="8f25e-630">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="8f25e-631">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-631">Core</span></span>

* <span data-ttu-id="8f25e-632">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-632">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-633">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-633">Appservice</span></span>

* <span data-ttu-id="8f25e-634">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-634">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="8f25e-635">Batch</span><span class="sxs-lookup"><span data-stu-id="8f25e-635">Batch</span></span>

* <span data-ttu-id="8f25e-636">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-636">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="8f25e-637">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-637">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="8f25e-638">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-638">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="8f25e-639">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-639">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="8f25e-640">Batchai</span><span class="sxs-lookup"><span data-stu-id="8f25e-640">Batchai</span></span>

* <span data-ttu-id="8f25e-641">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-641">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="8f25e-642">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8f25e-642">Keyvault</span></span>

* <span data-ttu-id="8f25e-643">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-643">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="8f25e-644">(#4448)</span><span class="sxs-lookup"><span data-stu-id="8f25e-644">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="8f25e-645">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-645">Network</span></span>

* <span data-ttu-id="8f25e-646">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-646">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="8f25e-647">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-647">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-648">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-648">Resource</span></span>

* <span data-ttu-id="8f25e-649">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-649">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="8f25e-650">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-650">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="8f25e-651">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-651">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="8f25e-652">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-652">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="8f25e-653">SQL</span><span class="sxs-lookup"><span data-stu-id="8f25e-653">Sql</span></span>

* <span data-ttu-id="8f25e-654">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-654">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="8f25e-655">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-655">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="8f25e-656">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-656">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-657">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-657">Storage</span></span>

* <span data-ttu-id="8f25e-658">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-658">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-659">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-659">Vm</span></span>

* <span data-ttu-id="8f25e-660">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-660">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="8f25e-661">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-661">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="8f25e-662">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-662">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="8f25e-663">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-663">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="8f25e-664">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-664">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="8f25e-665">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-665">September 22, 2017</span></span>

<span data-ttu-id="8f25e-666">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="8f25e-666">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-667">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-667">Resource</span></span>

* <span data-ttu-id="8f25e-668">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-668">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="8f25e-669">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-669">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="8f25e-670">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-670">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="8f25e-671">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-671">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-672">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-672">Network</span></span>

* <span data-ttu-id="8f25e-673">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-673">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="8f25e-674">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-674">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="8f25e-675">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-675">Added `asg` application security group commands</span></span>
* <span data-ttu-id="8f25e-676">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-676">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="8f25e-677">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-677">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="8f25e-678">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-678">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="8f25e-679">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-679">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-680">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-680">Storage</span></span>

* <span data-ttu-id="8f25e-681">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-681">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="8f25e-682">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="8f25e-682">Eventgrid</span></span>

* <span data-ttu-id="8f25e-683">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-683">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="8f25e-684">SQL</span><span class="sxs-lookup"><span data-stu-id="8f25e-684">SQL</span></span>

* <span data-ttu-id="8f25e-685">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-685">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="8f25e-686">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="8f25e-686">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="8f25e-687">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-687">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="8f25e-688">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8f25e-688">Keyvault</span></span>

* <span data-ttu-id="8f25e-689">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-689">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-690">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-690">VM</span></span>

* <span data-ttu-id="8f25e-691">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-691">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="8f25e-692">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-692">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="8f25e-693">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-693">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="8f25e-694">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-694">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="8f25e-695">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-695">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="8f25e-696">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-696">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-697">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-697">ACS</span></span>

* <span data-ttu-id="8f25e-698">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-698">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-699">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-699">Appservice</span></span>

* <span data-ttu-id="8f25e-700">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-700">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="8f25e-701">バックアップ</span><span class="sxs-lookup"><span data-stu-id="8f25e-701">Backup</span></span>

* <span data-ttu-id="8f25e-702">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-702">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="8f25e-703">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-703">September 11, 2017</span></span>

<span data-ttu-id="8f25e-704">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="8f25e-704">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="8f25e-705">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-705">Core</span></span>

* <span data-ttu-id="8f25e-706">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-706">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="8f25e-707">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-707">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-708">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-708">Acs</span></span>

* <span data-ttu-id="8f25e-709">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-709">Added `acs list-locations` command</span></span>
* <span data-ttu-id="8f25e-710">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-710">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-711">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-711">Appservice</span></span>

* <span data-ttu-id="8f25e-712">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-712">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="8f25e-713">CDN</span><span class="sxs-lookup"><span data-stu-id="8f25e-713">CDN</span></span>

* <span data-ttu-id="8f25e-714">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-714">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="8f25e-715">内線番号</span><span class="sxs-lookup"><span data-stu-id="8f25e-715">Extension</span></span>

* <span data-ttu-id="8f25e-716">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-716">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="8f25e-717">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8f25e-717">Keyvault</span></span>

* <span data-ttu-id="8f25e-718">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-718">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-719">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-719">Network</span></span>

* <span data-ttu-id="8f25e-720">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-720">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="8f25e-721">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-721">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="8f25e-722">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-722">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="8f25e-723">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-723">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="8f25e-724">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-724">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-725">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-725">Resource</span></span>

* <span data-ttu-id="8f25e-726">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="8f25e-726">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="8f25e-727">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="8f25e-727">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="8f25e-728">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="8f25e-728">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="8f25e-729">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-729">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="8f25e-730">SQL</span><span class="sxs-lookup"><span data-stu-id="8f25e-730">SQL</span></span>

* <span data-ttu-id="8f25e-731">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-731">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-732">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-732">VM</span></span>

* <span data-ttu-id="8f25e-733">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="8f25e-733">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="8f25e-734">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="8f25e-734">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="8f25e-735">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-735">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="8f25e-736">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="8f25e-736">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="8f25e-737">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="8f25e-737">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="8f25e-738">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-738">August 31, 2017</span></span>

<span data-ttu-id="8f25e-739">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="8f25e-739">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="8f25e-740">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8f25e-740">Keyvault</span></span>

* <span data-ttu-id="8f25e-741">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-741">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="8f25e-742">SF</span><span class="sxs-lookup"><span data-stu-id="8f25e-742">Sf</span></span>

* <span data-ttu-id="8f25e-743">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="8f25e-743">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-744">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-744">Storage</span></span>

* <span data-ttu-id="8f25e-745">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-745">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="8f25e-746">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="8f25e-746">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="8f25e-747">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-747">August 28, 2017</span></span>

<span data-ttu-id="8f25e-748">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="8f25e-748">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="8f25e-749">CLI</span><span class="sxs-lookup"><span data-stu-id="8f25e-749">CLI</span></span>

* <span data-ttu-id="8f25e-750">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-750">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-751">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-751">ACS</span></span>

* <span data-ttu-id="8f25e-752">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-752">Corrected preview regions</span></span>
* <span data-ttu-id="8f25e-753">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-753">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="8f25e-754">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-754">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-755">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-755">Appservice</span></span>

* <span data-ttu-id="8f25e-756">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-756">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="8f25e-757">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-757">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="8f25e-758">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-758">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="8f25e-759">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-759">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="8f25e-760">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="8f25e-760">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="8f25e-761">IoT</span><span class="sxs-lookup"><span data-stu-id="8f25e-761">IoT</span></span>

* <span data-ttu-id="8f25e-762">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-762">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-763">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-763">Network</span></span>

* <span data-ttu-id="8f25e-764">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-764">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="8f25e-765">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-765">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="8f25e-766">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-766">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="8f25e-767">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-767">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="8f25e-768">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-768">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="8f25e-769">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8f25e-769">Profile</span></span>

* <span data-ttu-id="8f25e-770">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-770">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8f25e-771">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8f25e-771">Service Fabric</span></span>

* <span data-ttu-id="8f25e-772">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-772">Preview release</span></span>
* <span data-ttu-id="8f25e-773">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-773">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="8f25e-774">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-774">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="8f25e-775">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-775">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-776">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-776">Storage</span></span>

* <span data-ttu-id="8f25e-777">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-777">Enabled setting blob tier</span></span>
* <span data-ttu-id="8f25e-778">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-778">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="8f25e-779">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-779">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="8f25e-780">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-780">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="8f25e-781">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-781">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="8f25e-782">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="8f25e-782">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-783">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-783">VM</span></span>

* <span data-ttu-id="8f25e-784">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-784">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="8f25e-785">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-785">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="8f25e-786">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-786">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="8f25e-787">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-787">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="8f25e-788">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-788">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="8f25e-789">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-789">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="8f25e-790">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-790">August 15, 2017</span></span>

<span data-ttu-id="8f25e-791">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="8f25e-791">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-792">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-792">ACS</span></span>

* <span data-ttu-id="8f25e-793">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-793">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-794">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-794">Appservice</span></span>

* <span data-ttu-id="8f25e-795">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-795">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="8f25e-796">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8f25e-796">Event Grid</span></span>

* <span data-ttu-id="8f25e-797">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-797">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="8f25e-798">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-798">August 11, 2017</span></span>

<span data-ttu-id="8f25e-799">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="8f25e-799">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-800">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-800">ACS</span></span>

* <span data-ttu-id="8f25e-801">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-801">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="8f25e-802">Batch</span><span class="sxs-lookup"><span data-stu-id="8f25e-802">Batch</span></span>

* <span data-ttu-id="8f25e-803">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-803">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="8f25e-804">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-804">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="8f25e-805">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-805">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="8f25e-806">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-806">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="8f25e-807">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-807">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="8f25e-808">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-808">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="8f25e-809">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8f25e-809">Component</span></span>

* <span data-ttu-id="8f25e-810">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-810">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="8f25e-811">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8f25e-811">Container</span></span>

* <span data-ttu-id="8f25e-812">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-812">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="8f25e-813">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8f25e-813">Data Lake Store</span></span>

* <span data-ttu-id="8f25e-814">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-814">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="8f25e-815">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8f25e-815">Event Grid</span></span>

* <span data-ttu-id="8f25e-816">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-816">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-817">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-817">Network</span></span>

* <span data-ttu-id="8f25e-818">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-818">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="8f25e-819">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-819">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="8f25e-820">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-820">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="8f25e-821">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-821">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="8f25e-822">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8f25e-822">Profile</span></span>

* <span data-ttu-id="8f25e-823">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-823">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-824">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-824">Storage</span></span>

* <span data-ttu-id="8f25e-825">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="8f25e-825">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-826">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-826">VM</span></span>

* <span data-ttu-id="8f25e-827">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-827">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="8f25e-828">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-828">Exposed `list-skus` command</span></span>
* <span data-ttu-id="8f25e-829">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-829">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="8f25e-830">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="8f25e-830">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="8f25e-831">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-831">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="8f25e-832">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-832">July 28, 2017</span></span>

<span data-ttu-id="8f25e-833">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="8f25e-833">Version 2.0.12</span></span>

* <span data-ttu-id="8f25e-834">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-834">Added container commands</span></span>
* <span data-ttu-id="8f25e-835">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-835">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="8f25e-836">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-836">Core</span></span>

* <span data-ttu-id="8f25e-837">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="8f25e-837">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="8f25e-838">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-838">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="8f25e-839">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="8f25e-839">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="8f25e-840">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="8f25e-840">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="8f25e-841">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="8f25e-841">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="8f25e-842">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="8f25e-842">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="8f25e-843">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="8f25e-843">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="8f25e-844">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="8f25e-844">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="8f25e-845">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="8f25e-845">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="8f25e-846">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="8f25e-846">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="8f25e-847">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="8f25e-847">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="8f25e-848">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="8f25e-848">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="8f25e-849">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-849">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="8f25e-850">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-850">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="8f25e-851">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-851">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="8f25e-852">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="8f25e-852">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="8f25e-853">ACR</span><span class="sxs-lookup"><span data-stu-id="8f25e-853">ACR</span></span>

* <span data-ttu-id="8f25e-854">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-854">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="8f25e-855">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-855">Support SKU update for managed registries</span></span>
* <span data-ttu-id="8f25e-856">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-856">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="8f25e-857">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-857">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="8f25e-858">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-858">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="8f25e-859">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-859">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-860">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-860">ACS</span></span>

* <span data-ttu-id="8f25e-861">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-861">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-862">Appservice</span><span class="sxs-lookup"><span data-stu-id="8f25e-862">Appservice</span></span>

* <span data-ttu-id="8f25e-863">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-863">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="8f25e-864">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-864">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="8f25e-865">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="8f25e-865">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="8f25e-866">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="8f25e-866">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="8f25e-867">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="8f25e-867">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="8f25e-868">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="8f25e-868">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="8f25e-869">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="8f25e-869">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="8f25e-870">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="8f25e-870">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="8f25e-871">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-871">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="8f25e-872">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8f25e-872">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="8f25e-873">Batch</span><span class="sxs-lookup"><span data-stu-id="8f25e-873">Batch</span></span>

* <span data-ttu-id="8f25e-874">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-874">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="8f25e-875">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-875">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="8f25e-876">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-876">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="8f25e-877">CDN</span><span class="sxs-lookup"><span data-stu-id="8f25e-877">CDN</span></span>

* <span data-ttu-id="8f25e-878">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-878">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="8f25e-879">クラウド</span><span class="sxs-lookup"><span data-stu-id="8f25e-879">Cloud</span></span>

* <span data-ttu-id="8f25e-880">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-880">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="8f25e-881">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="8f25e-881">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="8f25e-882">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-882">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="8f25e-883">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-883">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="8f25e-884">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-884">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8f25e-885">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8f25e-885">CosmosDB</span></span>

* <span data-ttu-id="8f25e-886">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-886">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="8f25e-887">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-887">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8f25e-888">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8f25e-888">Data Lake Analytics</span></span>

* <span data-ttu-id="8f25e-889">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-889">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="8f25e-890">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-890">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="8f25e-891">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-891">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8f25e-892">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8f25e-892">Data Lake Store</span></span>

* <span data-ttu-id="8f25e-893">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-893">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="8f25e-894">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-894">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="8f25e-895">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-895">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="8f25e-896">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="8f25e-896">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="8f25e-897">対話</span><span class="sxs-lookup"><span data-stu-id="8f25e-897">Interactive</span></span>

* <span data-ttu-id="8f25e-898">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-898">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="8f25e-899">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="8f25e-899">Increased test coverage</span></span>
* <span data-ttu-id="8f25e-900">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-900">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="8f25e-901">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="8f25e-901">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="8f25e-902">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="8f25e-902">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="8f25e-903">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="8f25e-903">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="8f25e-904">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="8f25e-904">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="8f25e-905">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-905">Added `--progress` flag</span></span>
* <span data-ttu-id="8f25e-906">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-906">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="8f25e-907">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="8f25e-907">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="8f25e-908">IoT</span><span class="sxs-lookup"><span data-stu-id="8f25e-908">IoT</span></span>

* <span data-ttu-id="8f25e-909">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-909">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="8f25e-910">(#3934)</span><span class="sxs-lookup"><span data-stu-id="8f25e-910">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="8f25e-911">Key Vault</span><span class="sxs-lookup"><span data-stu-id="8f25e-911">Key vault</span></span>

* <span data-ttu-id="8f25e-912">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-912">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="8f25e-913">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8f25e-913">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="8f25e-914">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8f25e-914">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="8f25e-915">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8f25e-915">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="8f25e-916">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8f25e-916">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="8f25e-917">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="8f25e-917">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="8f25e-918">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-918">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="8f25e-919">(#3307)</span><span class="sxs-lookup"><span data-stu-id="8f25e-919">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="8f25e-920">ラボ</span><span class="sxs-lookup"><span data-stu-id="8f25e-920">Lab</span></span>

* <span data-ttu-id="8f25e-921">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-921">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="8f25e-922">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-922">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="8f25e-923">監視</span><span class="sxs-lookup"><span data-stu-id="8f25e-923">Monitor</span></span>

* <span data-ttu-id="8f25e-924">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="8f25e-924">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="8f25e-925">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-925">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="8f25e-926">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-926">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="8f25e-927">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-927">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="8f25e-928">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-928">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="8f25e-929">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-929">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="8f25e-930">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-930">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="8f25e-931">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="8f25e-931">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="8f25e-932">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-932">`location` no longer required</span></span>
  * <span data-ttu-id="8f25e-933">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="8f25e-933">Add name and ID support for target</span></span>
  * <span data-ttu-id="8f25e-934">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="8f25e-934">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="8f25e-935">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-935">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="8f25e-936">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-936">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="8f25e-937">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="8f25e-937">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="8f25e-938">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-938">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="8f25e-939">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-939">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-940">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-940">Network</span></span>

* <span data-ttu-id="8f25e-941">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-941">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="8f25e-942">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-942">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="8f25e-943">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-943">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="8f25e-944">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-944">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="8f25e-945">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-945">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="8f25e-946">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-946">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="8f25e-947">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-947">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="8f25e-948">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-948">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="8f25e-949">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-949">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="8f25e-950">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-950">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="8f25e-951">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-951">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="8f25e-952">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-952">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="8f25e-953">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-953">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="8f25e-954">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-954">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="8f25e-955">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-955">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="8f25e-956">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-956">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="8f25e-957">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-957">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="8f25e-958">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-958">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="8f25e-959">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-959">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="8f25e-960">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-960">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="8f25e-961">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-961">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="8f25e-962">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-962">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="8f25e-963">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-963">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="8f25e-964">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8f25e-964">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="8f25e-965">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8f25e-965">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="8f25e-966">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8f25e-966">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="8f25e-967">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8f25e-967">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="8f25e-968">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8f25e-968">Profile</span></span>

* <span data-ttu-id="8f25e-969">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-969">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="8f25e-970">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-970">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="8f25e-971">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="8f25e-971">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="8f25e-972">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-972">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="8f25e-973">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-973">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="8f25e-974">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8f25e-974">RDBMS</span></span>

* <span data-ttu-id="8f25e-975">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="8f25e-975">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="8f25e-976">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="8f25e-976">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="8f25e-977">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="8f25e-977">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="8f25e-978">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="8f25e-978">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-979">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-979">Resource</span></span>

* <span data-ttu-id="8f25e-980">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-980">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="8f25e-981">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-981">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="8f25e-982">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-982">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="8f25e-983">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-983">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="8f25e-984">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="8f25e-984">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="8f25e-985">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-985">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="8f25e-986">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="8f25e-986">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="8f25e-987">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-987">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="8f25e-988">役割</span><span class="sxs-lookup"><span data-stu-id="8f25e-988">Role</span></span>

* <span data-ttu-id="8f25e-989">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-989">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="8f25e-990">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="8f25e-990">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="8f25e-991">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="8f25e-991">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="8f25e-992">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="8f25e-992">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="8f25e-993">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-993">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8f25e-994">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8f25e-994">Service Fabric</span></span>
* <span data-ttu-id="8f25e-995">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="8f25e-995">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="8f25e-996">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="8f25e-996">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="8f25e-997">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="8f25e-997">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="8f25e-998">SQL</span><span class="sxs-lookup"><span data-stu-id="8f25e-998">SQL</span></span>

* <span data-ttu-id="8f25e-999">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-999">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="8f25e-1000">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1000">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="8f25e-1001">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1001">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-1002">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-1002">Storage</span></span>

* <span data-ttu-id="8f25e-1003">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="8f25e-1003">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="8f25e-1004">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1004">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="8f25e-1005">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="8f25e-1005">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="8f25e-1006">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="8f25e-1006">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="8f25e-1007">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="8f25e-1007">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="8f25e-1008">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="8f25e-1008">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-1009">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-1009">VM</span></span>

* <span data-ttu-id="8f25e-1010">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-1010">Support configuring nsg</span></span>
* <span data-ttu-id="8f25e-1011">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1011">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="8f25e-1012">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="8f25e-1012">Support managed service identities</span></span>
* <span data-ttu-id="8f25e-1013">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1013">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="8f25e-1014">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="8f25e-1014">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="8f25e-1015">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-1015">May 10, 2017</span></span>

<span data-ttu-id="8f25e-1016">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="8f25e-1016">Version 2.0.6</span></span>

* <span data-ttu-id="8f25e-1017">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1017">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="8f25e-1018">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1018">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="8f25e-1019">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1019">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="8f25e-1020">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1020">Include Cognitive Services module</span></span>
* <span data-ttu-id="8f25e-1021">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1021">Include Service Fabric module</span></span>
* <span data-ttu-id="8f25e-1022">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="8f25e-1022">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="8f25e-1023">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1023">Add support for CDN commands</span></span>
* <span data-ttu-id="8f25e-1024">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1024">Remove Container module</span></span>
* <span data-ttu-id="8f25e-1025">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1025">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="8f25e-1026">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1026">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="8f25e-1027">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-1027">Core</span></span>

* <span data-ttu-id="8f25e-1028">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="8f25e-1028">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="8f25e-1029">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1029">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="8f25e-1030">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1030">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="8f25e-1031">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1031">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="8f25e-1032">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1032">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="8f25e-1033">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1033">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="8f25e-1034">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1034">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="8f25e-1035">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1035">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="8f25e-1036">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1036">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="8f25e-1037">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="8f25e-1037">core: Improved performance</span></span>
* <span data-ttu-id="8f25e-1038">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="8f25e-1038">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="8f25e-1039">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="8f25e-1039">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-1040">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-1040">ACS</span></span>

* <span data-ttu-id="8f25e-1041">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1041">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="8f25e-1042">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1042">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="8f25e-1043">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1043">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="8f25e-1044">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1044">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-1045">AppService</span><span class="sxs-lookup"><span data-stu-id="8f25e-1045">AppService</span></span>

* <span data-ttu-id="8f25e-1046">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1046">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="8f25e-1047">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1047">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="8f25e-1048">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="8f25e-1048">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="8f25e-1049">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1049">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="8f25e-1050">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1050">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="8f25e-1051">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1051">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="8f25e-1052">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="8f25e-1052">support slot swap with preview</span></span>
* <span data-ttu-id="8f25e-1053">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1053">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="8f25e-1054">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1054">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8f25e-1055">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8f25e-1055">CosmosDB</span></span>

* <span data-ttu-id="8f25e-1056">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1056">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="8f25e-1057">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1057">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="8f25e-1058">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1058">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="8f25e-1059">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1059">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8f25e-1060">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8f25e-1060">Data Lake Analytics</span></span>

* <span data-ttu-id="8f25e-1061">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1061">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="8f25e-1062">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-1062">Add support for new catalog item type: package.</span></span> <span data-ttu-id="8f25e-1063">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="8f25e-1063">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="8f25e-1064">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="8f25e-1064">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="8f25e-1065">テーブル</span><span class="sxs-lookup"><span data-stu-id="8f25e-1065">Table</span></span>
  * <span data-ttu-id="8f25e-1066">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="8f25e-1066">Table valued function</span></span>
  * <span data-ttu-id="8f25e-1067">表示</span><span class="sxs-lookup"><span data-stu-id="8f25e-1067">View</span></span>
  * <span data-ttu-id="8f25e-1068">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="8f25e-1068">Table Statistics.</span></span> <span data-ttu-id="8f25e-1069">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="8f25e-1069">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8f25e-1070">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8f25e-1070">Data Lake Store</span></span>

* <span data-ttu-id="8f25e-1071">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1071">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="8f25e-1072">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1072">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="8f25e-1073">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="8f25e-1073">missed help for access show.</span></span> <span data-ttu-id="8f25e-1074">追加しました </span><span class="sxs-lookup"><span data-stu-id="8f25e-1074">adding it.</span></span> <span data-ttu-id="8f25e-1075">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1075">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="8f25e-1076">検索</span><span class="sxs-lookup"><span data-stu-id="8f25e-1076">Find</span></span>

* <span data-ttu-id="8f25e-1077">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1077">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="8f25e-1078">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8f25e-1078">KeyVault</span></span>

* <span data-ttu-id="8f25e-1079">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1079">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="8f25e-1080">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1080">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="8f25e-1081">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="8f25e-1081">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="8f25e-1082">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1082">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="8f25e-1083">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1083">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="8f25e-1084">ラボ</span><span class="sxs-lookup"><span data-stu-id="8f25e-1084">Lab</span></span>

* <span data-ttu-id="8f25e-1085">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1085">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="8f25e-1086">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1086">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="8f25e-1087">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1087">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="8f25e-1088">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1088">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="8f25e-1089">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1089">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="8f25e-1090">監視</span><span class="sxs-lookup"><span data-stu-id="8f25e-1090">Monitor</span></span>

* <span data-ttu-id="8f25e-1091">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1091">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="8f25e-1092">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1092">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="8f25e-1093">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-1093">Network</span></span>

* <span data-ttu-id="8f25e-1094">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1094">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="8f25e-1095">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1095">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="8f25e-1096">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1096">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="8f25e-1097">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1097">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="8f25e-1098">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1098">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="8f25e-1099">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1099">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="8f25e-1100">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1100">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="8f25e-1101">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1101">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="8f25e-1102">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1102">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="8f25e-1103">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1103">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="8f25e-1104">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1104">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="8f25e-1105">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1105">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="8f25e-1106">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1106">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="8f25e-1107">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1107">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="8f25e-1108">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1108">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="8f25e-1109">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1109">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="8f25e-1110">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8f25e-1110">Profile</span></span>

* <span data-ttu-id="8f25e-1111">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1111">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="8f25e-1112">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1112">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="8f25e-1113">Redis</span><span class="sxs-lookup"><span data-stu-id="8f25e-1113">Redis</span></span>

* <span data-ttu-id="8f25e-1114">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1114">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="8f25e-1115">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1115">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="8f25e-1116">リソース</span><span class="sxs-lookup"><span data-stu-id="8f25e-1116">Resource</span></span>

* <span data-ttu-id="8f25e-1117">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1117">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="8f25e-1118">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1118">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="8f25e-1119">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1119">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="8f25e-1120">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="8f25e-1120">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="8f25e-1121">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1121">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="8f25e-1122">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="8f25e-1122">Add docs for az lock update.</span></span> <span data-ttu-id="8f25e-1123">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1123">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="8f25e-1124">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="8f25e-1124">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="8f25e-1125">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1125">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="8f25e-1126">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="8f25e-1126">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="8f25e-1127">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1127">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="8f25e-1128">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1128">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="8f25e-1129">役割</span><span class="sxs-lookup"><span data-stu-id="8f25e-1129">Role</span></span>

* <span data-ttu-id="8f25e-1130">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1130">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="8f25e-1131">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1131">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="8f25e-1132">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1132">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="8f25e-1133">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="8f25e-1133">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="8f25e-1134">SQL</span><span class="sxs-lookup"><span data-stu-id="8f25e-1134">SQL</span></span>

* <span data-ttu-id="8f25e-1135">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1135">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="8f25e-1136">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1136">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="8f25e-1137">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-1137">Storage</span></span>

* <span data-ttu-id="8f25e-1138">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="8f25e-1138">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="8f25e-1139">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1139">Add support for incremental blob copy</span></span>
* <span data-ttu-id="8f25e-1140">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1140">Add support for large block blob upload</span></span>
* <span data-ttu-id="8f25e-1141">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="8f25e-1141">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-1142">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-1142">VM</span></span>

* <span data-ttu-id="8f25e-1143">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1143">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="8f25e-1144">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="8f25e-1144">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="8f25e-1145">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="8f25e-1145">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="8f25e-1146">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="8f25e-1146">az vm/vmss disk</span></span>
  3. <span data-ttu-id="8f25e-1147">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="8f25e-1147">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="8f25e-1148">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="8f25e-1148">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="8f25e-1149">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1149">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="8f25e-1150">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-1150">April 3, 2017</span></span>

<span data-ttu-id="8f25e-1151">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="8f25e-1151">Version 2.0.2</span></span>

<span data-ttu-id="8f25e-1152">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="8f25e-1152">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="8f25e-1153">コア</span><span class="sxs-lookup"><span data-stu-id="8f25e-1153">Core</span></span>

* <span data-ttu-id="8f25e-1154">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="8f25e-1154">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="8f25e-1155">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1155">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="8f25e-1156">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1156">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="8f25e-1157">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1157">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="8f25e-1158">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1158">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="8f25e-1159">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="8f25e-1159">Add prompting for missing template parameters.</span></span> <span data-ttu-id="8f25e-1160">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1160">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="8f25e-1161">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="8f25e-1161">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="8f25e-1162">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="8f25e-1162">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="8f25e-1163">ACS</span><span class="sxs-lookup"><span data-stu-id="8f25e-1163">ACS</span></span>

* <span data-ttu-id="8f25e-1164">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1164">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="8f25e-1165">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="8f25e-1165">Add support for ssh key password prompting.</span></span> <span data-ttu-id="8f25e-1166">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1166">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="8f25e-1167">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="8f25e-1167">Add support for windows clusters.</span></span> <span data-ttu-id="8f25e-1168">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1168">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="8f25e-1169">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="8f25e-1169">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="8f25e-1170">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1170">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="8f25e-1171">AppService</span><span class="sxs-lookup"><span data-stu-id="8f25e-1171">AppService</span></span>

* <span data-ttu-id="8f25e-1172">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1172">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="8f25e-1173">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1173">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="8f25e-1174">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1174">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="8f25e-1175">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1175">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="8f25e-1176">DataLake</span><span class="sxs-lookup"><span data-stu-id="8f25e-1176">DataLake</span></span>

* <span data-ttu-id="8f25e-1177">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-1177">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="8f25e-1178">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8f25e-1178">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="8f25e-1179">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="8f25e-1179">DocuemntDB</span></span>

* <span data-ttu-id="8f25e-1180">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1180">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="8f25e-1181">VM</span><span class="sxs-lookup"><span data-stu-id="8f25e-1181">VM</span></span>

* <span data-ttu-id="8f25e-1182">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1182">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="8f25e-1183">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1183">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="8f25e-1184">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1184">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="8f25e-1185">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1185">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="8f25e-1186">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1186">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="8f25e-1187">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1187">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="8f25e-1188">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="8f25e-1188">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="8f25e-1189">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="8f25e-1189">February 27, 2017</span></span>

<span data-ttu-id="8f25e-1190">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="8f25e-1190">Version 2.0.0</span></span>

<span data-ttu-id="8f25e-1191">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="8f25e-1191">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="8f25e-1192">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="8f25e-1192">Container Service (acs)</span></span>
- <span data-ttu-id="8f25e-1193">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="8f25e-1193">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="8f25e-1194">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8f25e-1194">Networking</span></span>
- <span data-ttu-id="8f25e-1195">Storage</span><span class="sxs-lookup"><span data-stu-id="8f25e-1195">Storage</span></span>

<span data-ttu-id="8f25e-1196">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="8f25e-1196">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="8f25e-1197">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="8f25e-1197">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="8f25e-1198">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="8f25e-1198">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="8f25e-1199">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="8f25e-1199">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="8f25e-1200">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="8f25e-1200">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="8f25e-1201">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="8f25e-1201">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="8f25e-1202">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="8f25e-1202">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="8f25e-1203">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="8f25e-1203">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="8f25e-1204">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="8f25e-1204">Provide feedback from the command line with the `az feedback` command</span></span>

