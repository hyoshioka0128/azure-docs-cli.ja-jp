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
ms.openlocfilehash: 761bd61474e7c72fb2daeb756828f00196b56c3a
ms.sourcegitcommit: bb649ebd7e7fce8fb5008ac1e2e2c33481a45df9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="39a2e-104">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="39a2e-104">Azure CLI 2.0 release notes</span></span>

## <a name="november-14-2017"></a><span data-ttu-id="39a2e-105">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-105">November 14, 2017</span></span>

<span data-ttu-id="39a2e-106">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="39a2e-106">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="39a2e-107">ACR</span><span class="sxs-lookup"><span data-stu-id="39a2e-107">ACR</span></span>

* <span data-ttu-id="39a2e-108">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-108">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="39a2e-109">ACS</span><span class="sxs-lookup"><span data-stu-id="39a2e-109">ACS</span></span>

* <span data-ttu-id="39a2e-110">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-110">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="39a2e-111">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-111">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="39a2e-112">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-112">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="39a2e-113">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-113">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="39a2e-114">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-114">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="39a2e-115">Appservice</span><span class="sxs-lookup"><span data-stu-id="39a2e-115">Appservice</span></span>

* <span data-ttu-id="39a2e-116">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-116">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="39a2e-117">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-117">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="39a2e-118">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-118">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="39a2e-119">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-119">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="39a2e-120">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-120">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="39a2e-121">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="39a2e-121">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="39a2e-122">Batch</span><span class="sxs-lookup"><span data-stu-id="39a2e-122">Batch</span></span>

* <span data-ttu-id="39a2e-123">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-123">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="39a2e-124">Batchai</span><span class="sxs-lookup"><span data-stu-id="39a2e-124">Batchai</span></span>

* <span data-ttu-id="39a2e-125">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-125">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="39a2e-126">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-126">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="39a2e-127">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-127">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="39a2e-128">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-128">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="39a2e-129">クラウド</span><span class="sxs-lookup"><span data-stu-id="39a2e-129">Cloud</span></span>

* <span data-ttu-id="39a2e-130">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-130">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="39a2e-131">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39a2e-131">Container</span></span>

* <span data-ttu-id="39a2e-132">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-132">Added support to open multiple ports</span></span>
* <span data-ttu-id="39a2e-133">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-133">Added container group restart policy</span></span>
* <span data-ttu-id="39a2e-134">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-134">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="39a2e-135">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-135">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="39a2e-136">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="39a2e-136">Data Lake Analytics</span></span>

* <span data-ttu-id="39a2e-137">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-137">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="39a2e-138">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="39a2e-138">Data Lake Store</span></span>

* <span data-ttu-id="39a2e-139">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-139">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="39a2e-140">内線番号</span><span class="sxs-lookup"><span data-stu-id="39a2e-140">Extension</span></span>

* <span data-ttu-id="39a2e-141">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-141">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="39a2e-142">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-142">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="39a2e-143">IoT</span><span class="sxs-lookup"><span data-stu-id="39a2e-143">IoT</span></span>

* <span data-ttu-id="39a2e-144">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-144">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="39a2e-145">監視</span><span class="sxs-lookup"><span data-stu-id="39a2e-145">Monitor</span></span>

* <span data-ttu-id="39a2e-146">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-146">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="39a2e-147">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39a2e-147">Network</span></span>

* <span data-ttu-id="39a2e-148">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-148">Added support for CAA DNS records</span></span>
* <span data-ttu-id="39a2e-149">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-149">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="39a2e-150">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-150">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="39a2e-151">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-151">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="39a2e-152">Reservations</span><span class="sxs-lookup"><span data-stu-id="39a2e-152">Reservations</span></span>

* <span data-ttu-id="39a2e-153">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="39a2e-153">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="39a2e-154">リソース</span><span class="sxs-lookup"><span data-stu-id="39a2e-154">Resource</span></span>

* <span data-ttu-id="39a2e-155">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-155">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="39a2e-156">SQL</span><span class="sxs-lookup"><span data-stu-id="39a2e-156">SQL</span></span>

* <span data-ttu-id="39a2e-157">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-157">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="39a2e-158">ストレージ</span><span class="sxs-lookup"><span data-stu-id="39a2e-158">Storage</span></span>

* <span data-ttu-id="39a2e-159">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-159">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="39a2e-160">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-160">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="39a2e-161">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-161">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="39a2e-162">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-162">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="39a2e-163">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-163">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="39a2e-164">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-164">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="39a2e-165">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-165">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="39a2e-166">VM</span><span class="sxs-lookup"><span data-stu-id="39a2e-166">VM</span></span>

* <span data-ttu-id="39a2e-167">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-167">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="39a2e-168">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-168">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="39a2e-169">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-169">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="39a2e-170">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-170">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="39a2e-171">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-171">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="39a2e-172">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-172">October 24, 2017</span></span>

<span data-ttu-id="39a2e-173">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="39a2e-173">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="39a2e-174">コア</span><span class="sxs-lookup"><span data-stu-id="39a2e-174">Core</span></span>

* <span data-ttu-id="39a2e-175">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-175">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="39a2e-176">ACR</span><span class="sxs-lookup"><span data-stu-id="39a2e-176">ACR</span></span>

* <span data-ttu-id="39a2e-177">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-177">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="39a2e-178">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-178">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="39a2e-179">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-179">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="39a2e-180">ACS</span><span class="sxs-lookup"><span data-stu-id="39a2e-180">ACS</span></span>

* <span data-ttu-id="39a2e-181">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-181">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="39a2e-182">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-182">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="39a2e-183">Appservice</span><span class="sxs-lookup"><span data-stu-id="39a2e-183">Appservice</span></span>

* <span data-ttu-id="39a2e-184">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-184">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="39a2e-185">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="39a2e-185">Component</span></span>

* <span data-ttu-id="39a2e-186">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-186">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="39a2e-187">監視</span><span class="sxs-lookup"><span data-stu-id="39a2e-187">Monitor</span></span>

* <span data-ttu-id="39a2e-188">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-188">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="39a2e-189">リソース</span><span class="sxs-lookup"><span data-stu-id="39a2e-189">Resource</span></span>

* <span data-ttu-id="39a2e-190">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-190">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="39a2e-191">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-191">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="39a2e-192">VM</span><span class="sxs-lookup"><span data-stu-id="39a2e-192">VM</span></span>

* <span data-ttu-id="39a2e-193">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-193">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="39a2e-194">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-194">October 9, 2017</span></span>

<span data-ttu-id="39a2e-195">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="39a2e-195">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="39a2e-196">コア</span><span class="sxs-lookup"><span data-stu-id="39a2e-196">Core</span></span>

* <span data-ttu-id="39a2e-197">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-197">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="39a2e-198">Appservice</span><span class="sxs-lookup"><span data-stu-id="39a2e-198">Appservice</span></span>

* <span data-ttu-id="39a2e-199">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-199">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="39a2e-200">Batch</span><span class="sxs-lookup"><span data-stu-id="39a2e-200">Batch</span></span>

* <span data-ttu-id="39a2e-201">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-201">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="39a2e-202">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-202">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="39a2e-203">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-203">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="39a2e-204">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-204">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="39a2e-205">Batchai</span><span class="sxs-lookup"><span data-stu-id="39a2e-205">Batchai</span></span>

* <span data-ttu-id="39a2e-206">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39a2e-206">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="39a2e-207">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39a2e-207">Keyvault</span></span>

* <span data-ttu-id="39a2e-208">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-208">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="39a2e-209">(#4448)</span><span class="sxs-lookup"><span data-stu-id="39a2e-209">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="39a2e-210">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39a2e-210">Network</span></span>

* <span data-ttu-id="39a2e-211">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-211">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="39a2e-212">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-212">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="39a2e-213">リソース</span><span class="sxs-lookup"><span data-stu-id="39a2e-213">Resource</span></span>

* <span data-ttu-id="39a2e-214">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-214">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="39a2e-215">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-215">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="39a2e-216">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-216">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="39a2e-217">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-217">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="39a2e-218">SQL</span><span class="sxs-lookup"><span data-stu-id="39a2e-218">Sql</span></span>

* <span data-ttu-id="39a2e-219">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-219">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="39a2e-220">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-220">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="39a2e-221">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-221">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="39a2e-222">ストレージ</span><span class="sxs-lookup"><span data-stu-id="39a2e-222">Storage</span></span>

* <span data-ttu-id="39a2e-223">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-223">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="39a2e-224">VM</span><span class="sxs-lookup"><span data-stu-id="39a2e-224">Vm</span></span>

* <span data-ttu-id="39a2e-225">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-225">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="39a2e-226">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-226">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="39a2e-227">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-227">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="39a2e-228">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-228">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="39a2e-229">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-229">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="39a2e-230">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-230">September 22, 2017</span></span>

<span data-ttu-id="39a2e-231">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="39a2e-231">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="39a2e-232">リソース</span><span class="sxs-lookup"><span data-stu-id="39a2e-232">Resource</span></span>

* <span data-ttu-id="39a2e-233">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-233">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="39a2e-234">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-234">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="39a2e-235">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-235">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="39a2e-236">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-236">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="39a2e-237">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39a2e-237">Network</span></span>

* <span data-ttu-id="39a2e-238">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-238">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="39a2e-239">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-239">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="39a2e-240">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-240">Added `asg` application security group commands</span></span>
* <span data-ttu-id="39a2e-241">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-241">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="39a2e-242">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-242">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="39a2e-243">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-243">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="39a2e-244">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-244">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="39a2e-245">ストレージ</span><span class="sxs-lookup"><span data-stu-id="39a2e-245">Storage</span></span>

* <span data-ttu-id="39a2e-246">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-246">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="39a2e-247">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="39a2e-247">Eventgrid</span></span>

* <span data-ttu-id="39a2e-248">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-248">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="39a2e-249">SQL</span><span class="sxs-lookup"><span data-stu-id="39a2e-249">SQL</span></span>

* <span data-ttu-id="39a2e-250">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-250">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="39a2e-251">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="39a2e-251">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="39a2e-252">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-252">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="39a2e-253">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39a2e-253">Keyvault</span></span>

* <span data-ttu-id="39a2e-254">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-254">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="39a2e-255">VM</span><span class="sxs-lookup"><span data-stu-id="39a2e-255">VM</span></span>

* <span data-ttu-id="39a2e-256">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-256">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="39a2e-257">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-257">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="39a2e-258">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-258">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="39a2e-259">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-259">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="39a2e-260">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-260">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="39a2e-261">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-261">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="39a2e-262">ACS</span><span class="sxs-lookup"><span data-stu-id="39a2e-262">ACS</span></span>

* <span data-ttu-id="39a2e-263">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-263">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="39a2e-264">Appservice</span><span class="sxs-lookup"><span data-stu-id="39a2e-264">Appservice</span></span>

* <span data-ttu-id="39a2e-265">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-265">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="39a2e-266">Backup</span><span class="sxs-lookup"><span data-stu-id="39a2e-266">Backup</span></span>

* <span data-ttu-id="39a2e-267">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="39a2e-267">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="39a2e-268">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-268">September 11, 2017</span></span>

<span data-ttu-id="39a2e-269">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="39a2e-269">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="39a2e-270">コア</span><span class="sxs-lookup"><span data-stu-id="39a2e-270">Core</span></span>

* <span data-ttu-id="39a2e-271">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-271">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="39a2e-272">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-272">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="39a2e-273">ACS</span><span class="sxs-lookup"><span data-stu-id="39a2e-273">Acs</span></span>

* <span data-ttu-id="39a2e-274">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-274">Added `acs list-locations` command</span></span>
* <span data-ttu-id="39a2e-275">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-275">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="39a2e-276">Appservice</span><span class="sxs-lookup"><span data-stu-id="39a2e-276">Appservice</span></span>

* <span data-ttu-id="39a2e-277">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-277">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="39a2e-278">CDN</span><span class="sxs-lookup"><span data-stu-id="39a2e-278">CDN</span></span>

* <span data-ttu-id="39a2e-279">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-279">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="39a2e-280">内線番号</span><span class="sxs-lookup"><span data-stu-id="39a2e-280">Extension</span></span>

* <span data-ttu-id="39a2e-281">最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="39a2e-281">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="39a2e-282">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39a2e-282">Keyvault</span></span>

* <span data-ttu-id="39a2e-283">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-283">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="39a2e-284">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39a2e-284">Network</span></span>

* <span data-ttu-id="39a2e-285">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-285">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="39a2e-286">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-286">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="39a2e-287">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-287">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="39a2e-288">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-288">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="39a2e-289">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-289">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="39a2e-290">リソース</span><span class="sxs-lookup"><span data-stu-id="39a2e-290">Resource</span></span>

* <span data-ttu-id="39a2e-291">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="39a2e-291">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="39a2e-292">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="39a2e-292">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="39a2e-293">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="39a2e-293">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="39a2e-294">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-294">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="39a2e-295">SQL</span><span class="sxs-lookup"><span data-stu-id="39a2e-295">SQL</span></span>

* <span data-ttu-id="39a2e-296">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-296">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="39a2e-297">VM</span><span class="sxs-lookup"><span data-stu-id="39a2e-297">VM</span></span>

* <span data-ttu-id="39a2e-298">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="39a2e-298">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="39a2e-299">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="39a2e-299">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="39a2e-300">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-300">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="39a2e-301">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="39a2e-301">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="39a2e-302">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="39a2e-302">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="39a2e-303">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-303">August 31, 2017</span></span>

<span data-ttu-id="39a2e-304">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="39a2e-304">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="39a2e-305">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39a2e-305">Keyvault</span></span>

* <span data-ttu-id="39a2e-306">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-306">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="39a2e-307">SF</span><span class="sxs-lookup"><span data-stu-id="39a2e-307">Sf</span></span>

* <span data-ttu-id="39a2e-308">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="39a2e-308">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="39a2e-309">ストレージ</span><span class="sxs-lookup"><span data-stu-id="39a2e-309">Storage</span></span>

* <span data-ttu-id="39a2e-310">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-310">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="39a2e-311">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="39a2e-311">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="39a2e-312">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-312">August 28, 2017</span></span>

<span data-ttu-id="39a2e-313">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="39a2e-313">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="39a2e-314">CLI</span><span class="sxs-lookup"><span data-stu-id="39a2e-314">CLI</span></span>

* <span data-ttu-id="39a2e-315">`--version` に法的事項を追加しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-315">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="39a2e-316">ACS</span><span class="sxs-lookup"><span data-stu-id="39a2e-316">ACS</span></span>

* <span data-ttu-id="39a2e-317">プレビュー リージョンを修正しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-317">Corrected preview regions.</span></span>
* <span data-ttu-id="39a2e-318">既定の `dns_name_prefix` を正しい形式にしました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-318">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="39a2e-319">ACS コマンド出力を最適化しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-319">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="39a2e-320">Appservice</span><span class="sxs-lookup"><span data-stu-id="39a2e-320">Appservice</span></span>

* <span data-ttu-id="39a2e-321">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-321">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="39a2e-322">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-322">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="39a2e-323">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-323">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="39a2e-324">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-324">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="39a2e-325">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="39a2e-325">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="39a2e-326">IoT</span><span class="sxs-lookup"><span data-stu-id="39a2e-326">IoT</span></span>

* <span data-ttu-id="39a2e-327">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-327">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="39a2e-328">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39a2e-328">Network</span></span>

* <span data-ttu-id="39a2e-329">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-329">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="39a2e-330">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-330">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="39a2e-331">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-331">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="39a2e-332">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-332">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="39a2e-333">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-333">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="39a2e-334">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39a2e-334">Profile</span></span>

* <span data-ttu-id="39a2e-335">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-335">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="39a2e-336">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="39a2e-336">Service Fabric</span></span>

* <span data-ttu-id="39a2e-337">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="39a2e-337">Preview release</span></span>
* <span data-ttu-id="39a2e-338">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-338">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="39a2e-339">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-339">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="39a2e-340">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-340">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="39a2e-341">ストレージ</span><span class="sxs-lookup"><span data-stu-id="39a2e-341">Storage</span></span>

* <span data-ttu-id="39a2e-342">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-342">Enabled setting blob tier</span></span>
* <span data-ttu-id="39a2e-343">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-343">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="39a2e-344">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-344">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="39a2e-345">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-345">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="39a2e-346">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-346">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="39a2e-347">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="39a2e-347">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="39a2e-348">VM</span><span class="sxs-lookup"><span data-stu-id="39a2e-348">VM</span></span>

* <span data-ttu-id="39a2e-349">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-349">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="39a2e-350">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-350">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="39a2e-351">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-351">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="39a2e-352">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-352">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="39a2e-353">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-353">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="39a2e-354">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-354">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="39a2e-355">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-355">August 15, 2017</span></span>

<span data-ttu-id="39a2e-356">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="39a2e-356">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="39a2e-357">ACS</span><span class="sxs-lookup"><span data-stu-id="39a2e-357">ACS</span></span>

* <span data-ttu-id="39a2e-358">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-358">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="39a2e-359">Appservice</span><span class="sxs-lookup"><span data-stu-id="39a2e-359">Appservice</span></span>

* <span data-ttu-id="39a2e-360">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-360">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="39a2e-361">Event Grid</span><span class="sxs-lookup"><span data-stu-id="39a2e-361">Event Grid</span></span>

* <span data-ttu-id="39a2e-362">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-362">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="39a2e-363">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-363">August 11, 2017</span></span>

<span data-ttu-id="39a2e-364">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="39a2e-364">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="39a2e-365">ACS</span><span class="sxs-lookup"><span data-stu-id="39a2e-365">ACS</span></span>

* <span data-ttu-id="39a2e-366">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-366">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="39a2e-367">Batch</span><span class="sxs-lookup"><span data-stu-id="39a2e-367">Batch</span></span>

* <span data-ttu-id="39a2e-368">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-368">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="39a2e-369">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-369">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="39a2e-370">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-370">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="39a2e-371">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-371">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="39a2e-372">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-372">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="39a2e-373">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-373">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="39a2e-374">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="39a2e-374">Component</span></span>

* <span data-ttu-id="39a2e-375">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-375">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="39a2e-376">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39a2e-376">Container</span></span>

* <span data-ttu-id="39a2e-377">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-377">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="39a2e-378">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="39a2e-378">Data Lake Store</span></span>

* <span data-ttu-id="39a2e-379">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-379">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="39a2e-380">Event Grid</span><span class="sxs-lookup"><span data-stu-id="39a2e-380">Event Grid</span></span>

* <span data-ttu-id="39a2e-381">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39a2e-381">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="39a2e-382">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39a2e-382">Network</span></span>

* <span data-ttu-id="39a2e-383">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-383">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="39a2e-384">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-384">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="39a2e-385">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-385">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="39a2e-386">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-386">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="39a2e-387">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39a2e-387">Profile</span></span>

* <span data-ttu-id="39a2e-388">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-388">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="39a2e-389">ストレージ</span><span class="sxs-lookup"><span data-stu-id="39a2e-389">Storage</span></span>

* <span data-ttu-id="39a2e-390">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="39a2e-390">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="39a2e-391">VM</span><span class="sxs-lookup"><span data-stu-id="39a2e-391">VM</span></span>

* <span data-ttu-id="39a2e-392">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-392">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="39a2e-393">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-393">Exposed `list-skus` command</span></span>
* <span data-ttu-id="39a2e-394">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-394">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="39a2e-395">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="39a2e-395">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="39a2e-396">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-396">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="39a2e-397">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-397">July 28, 2017</span></span>

<span data-ttu-id="39a2e-398">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="39a2e-398">Version 2.0.12</span></span>

* <span data-ttu-id="39a2e-399">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-399">Added container commands</span></span>
* <span data-ttu-id="39a2e-400">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-400">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="39a2e-401">コア</span><span class="sxs-lookup"><span data-stu-id="39a2e-401">Core</span></span>

* <span data-ttu-id="39a2e-402">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="39a2e-402">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="39a2e-403">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-403">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="39a2e-404">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="39a2e-404">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="39a2e-405">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="39a2e-405">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="39a2e-406">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="39a2e-406">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="39a2e-407">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="39a2e-407">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="39a2e-408">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="39a2e-408">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="39a2e-409">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="39a2e-409">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="39a2e-410">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="39a2e-410">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="39a2e-411">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="39a2e-411">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="39a2e-412">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="39a2e-412">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="39a2e-413">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="39a2e-413">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="39a2e-414">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-414">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="39a2e-415">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-415">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="39a2e-416">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-416">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="39a2e-417">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="39a2e-417">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="39a2e-418">ACR</span><span class="sxs-lookup"><span data-stu-id="39a2e-418">ACR</span></span>

* <span data-ttu-id="39a2e-419">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-419">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="39a2e-420">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-420">Support SKU update for managed registries</span></span>
* <span data-ttu-id="39a2e-421">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-421">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="39a2e-422">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-422">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="39a2e-423">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-423">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="39a2e-424">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-424">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="39a2e-425">ACS</span><span class="sxs-lookup"><span data-stu-id="39a2e-425">ACS</span></span>

* <span data-ttu-id="39a2e-426">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-426">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="39a2e-427">Appservice</span><span class="sxs-lookup"><span data-stu-id="39a2e-427">Appservice</span></span>

* <span data-ttu-id="39a2e-428">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-428">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="39a2e-429">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-429">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="39a2e-430">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="39a2e-430">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="39a2e-431">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="39a2e-431">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="39a2e-432">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="39a2e-432">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="39a2e-433">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="39a2e-433">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="39a2e-434">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="39a2e-434">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="39a2e-435">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="39a2e-435">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="39a2e-436">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-436">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="39a2e-437">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="39a2e-437">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="39a2e-438">Batch</span><span class="sxs-lookup"><span data-stu-id="39a2e-438">Batch</span></span>

* <span data-ttu-id="39a2e-439">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-439">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="39a2e-440">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-440">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="39a2e-441">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-441">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="39a2e-442">CDN</span><span class="sxs-lookup"><span data-stu-id="39a2e-442">CDN</span></span>

* <span data-ttu-id="39a2e-443">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-443">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="39a2e-444">クラウド</span><span class="sxs-lookup"><span data-stu-id="39a2e-444">Cloud</span></span>

* <span data-ttu-id="39a2e-445">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-445">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="39a2e-446">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="39a2e-446">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="39a2e-447">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-447">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="39a2e-448">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-448">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="39a2e-449">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-449">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="39a2e-450">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="39a2e-450">CosmosDB</span></span>

* <span data-ttu-id="39a2e-451">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-451">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="39a2e-452">既定のコレクション TTL のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-452">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="39a2e-453">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="39a2e-453">Data Lake Analytics</span></span>

* <span data-ttu-id="39a2e-454">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-454">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="39a2e-455">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-455">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="39a2e-456">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-456">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="39a2e-457">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="39a2e-457">Data Lake Store</span></span>

* <span data-ttu-id="39a2e-458">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-458">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="39a2e-459">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-459">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="39a2e-460">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-460">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="39a2e-461">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="39a2e-461">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="39a2e-462">対話</span><span class="sxs-lookup"><span data-stu-id="39a2e-462">Interactive</span></span>

* <span data-ttu-id="39a2e-463">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-463">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="39a2e-464">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="39a2e-464">Increased test coverage</span></span>
* <span data-ttu-id="39a2e-465">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-465">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="39a2e-466">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="39a2e-466">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="39a2e-467">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="39a2e-467">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="39a2e-468">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="39a2e-468">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="39a2e-469">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="39a2e-469">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="39a2e-470">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-470">Added `--progress` flag</span></span>
* <span data-ttu-id="39a2e-471">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-471">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="39a2e-472">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="39a2e-472">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="39a2e-473">IoT</span><span class="sxs-lookup"><span data-stu-id="39a2e-473">IoT</span></span>

* <span data-ttu-id="39a2e-474">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-474">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="39a2e-475">(#3934)</span><span class="sxs-lookup"><span data-stu-id="39a2e-475">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="39a2e-476">Key Vault</span><span class="sxs-lookup"><span data-stu-id="39a2e-476">Key vault</span></span>

* <span data-ttu-id="39a2e-477">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-477">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="39a2e-478">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="39a2e-478">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="39a2e-479">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="39a2e-479">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="39a2e-480">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="39a2e-480">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="39a2e-481">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="39a2e-481">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="39a2e-482">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="39a2e-482">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="39a2e-483">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-483">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="39a2e-484">(#3307)</span><span class="sxs-lookup"><span data-stu-id="39a2e-484">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="39a2e-485">ラボ</span><span class="sxs-lookup"><span data-stu-id="39a2e-485">Lab</span></span>

* <span data-ttu-id="39a2e-486">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-486">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="39a2e-487">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-487">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="39a2e-488">監視</span><span class="sxs-lookup"><span data-stu-id="39a2e-488">Monitor</span></span>

* <span data-ttu-id="39a2e-489">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="39a2e-489">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="39a2e-490">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-490">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="39a2e-491">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-491">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="39a2e-492">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-492">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="39a2e-493">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-493">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="39a2e-494">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-494">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="39a2e-495">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-495">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="39a2e-496">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="39a2e-496">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="39a2e-497">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-497">`location` no longer required</span></span>
  * <span data-ttu-id="39a2e-498">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="39a2e-498">Add name and ID support for target</span></span>
  * <span data-ttu-id="39a2e-499">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="39a2e-499">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="39a2e-500">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-500">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="39a2e-501">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-501">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="39a2e-502">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="39a2e-502">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="39a2e-503">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-503">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="39a2e-504">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-504">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="39a2e-505">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39a2e-505">Network</span></span>

* <span data-ttu-id="39a2e-506">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-506">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="39a2e-507">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-507">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="39a2e-508">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-508">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="39a2e-509">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-509">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="39a2e-510">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-510">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="39a2e-511">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-511">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="39a2e-512">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-512">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="39a2e-513">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-513">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="39a2e-514">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-514">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="39a2e-515">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-515">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="39a2e-516">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-516">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="39a2e-517">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-517">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="39a2e-518">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-518">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="39a2e-519">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-519">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="39a2e-520">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-520">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="39a2e-521">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-521">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="39a2e-522">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-522">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="39a2e-523">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-523">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="39a2e-524">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-524">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="39a2e-525">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-525">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="39a2e-526">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-526">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="39a2e-527">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-527">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="39a2e-528">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-528">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="39a2e-529">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="39a2e-529">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="39a2e-530">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="39a2e-530">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="39a2e-531">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="39a2e-531">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="39a2e-532">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="39a2e-532">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="39a2e-533">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39a2e-533">Profile</span></span>

* <span data-ttu-id="39a2e-534">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-534">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="39a2e-535">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-535">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="39a2e-536">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="39a2e-536">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="39a2e-537">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-537">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="39a2e-538">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-538">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="39a2e-539">RDBMS</span><span class="sxs-lookup"><span data-stu-id="39a2e-539">RDBMS</span></span>

* <span data-ttu-id="39a2e-540">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="39a2e-540">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="39a2e-541">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="39a2e-541">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="39a2e-542">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="39a2e-542">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="39a2e-543">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="39a2e-543">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="39a2e-544">リソース</span><span class="sxs-lookup"><span data-stu-id="39a2e-544">Resource</span></span>

* <span data-ttu-id="39a2e-545">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-545">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="39a2e-546">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-546">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="39a2e-547">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-547">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="39a2e-548">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-548">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="39a2e-549">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="39a2e-549">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="39a2e-550">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-550">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="39a2e-551">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="39a2e-551">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="39a2e-552">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-552">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="39a2e-553">役割</span><span class="sxs-lookup"><span data-stu-id="39a2e-553">Role</span></span>

* <span data-ttu-id="39a2e-554">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-554">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="39a2e-555">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="39a2e-555">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="39a2e-556">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="39a2e-556">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="39a2e-557">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="39a2e-557">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="39a2e-558">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-558">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="39a2e-559">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="39a2e-559">Service Fabric</span></span>
* <span data-ttu-id="39a2e-560">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="39a2e-560">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="39a2e-561">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="39a2e-561">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="39a2e-562">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="39a2e-562">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="39a2e-563">SQL</span><span class="sxs-lookup"><span data-stu-id="39a2e-563">SQL</span></span>

* <span data-ttu-id="39a2e-564">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-564">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="39a2e-565">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-565">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="39a2e-566">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-566">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="39a2e-567">ストレージ</span><span class="sxs-lookup"><span data-stu-id="39a2e-567">Storage</span></span>

* <span data-ttu-id="39a2e-568">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="39a2e-568">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="39a2e-569">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-569">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="39a2e-570">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="39a2e-570">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="39a2e-571">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="39a2e-571">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="39a2e-572">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="39a2e-572">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="39a2e-573">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="39a2e-573">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="39a2e-574">VM</span><span class="sxs-lookup"><span data-stu-id="39a2e-574">VM</span></span>

* <span data-ttu-id="39a2e-575">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-575">Support configuring nsg</span></span>
* <span data-ttu-id="39a2e-576">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-576">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="39a2e-577">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="39a2e-577">Support managed service identities</span></span>
* <span data-ttu-id="39a2e-578">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-578">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="39a2e-579">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="39a2e-579">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="39a2e-580">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-580">May 10, 2017</span></span>

<span data-ttu-id="39a2e-581">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="39a2e-581">Version 2.0.6</span></span>

* <span data-ttu-id="39a2e-582">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="39a2e-582">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="39a2e-583">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="39a2e-583">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="39a2e-584">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-584">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="39a2e-585">Cognitive Services モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-585">Include Cognitive Services module.</span></span>
* <span data-ttu-id="39a2e-586">Service Fabric モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-586">Include Service Fabric module.</span></span>
* <span data-ttu-id="39a2e-587">対話型モジュールが追加されました (az-shell の名前変更)。</span><span class="sxs-lookup"><span data-stu-id="39a2e-587">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="39a2e-588">CDN コマンドに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-588">Add support for CDN commands.</span></span>
* <span data-ttu-id="39a2e-589">コンテナー モジュールが削除されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-589">Remove Container module.</span></span>
* <span data-ttu-id="39a2e-590">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="39a2e-590">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="39a2e-591">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="39a2e-591">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="39a2e-592">コア</span><span class="sxs-lookup"><span data-stu-id="39a2e-592">Core</span></span>

* <span data-ttu-id="39a2e-593">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="39a2e-593">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="39a2e-594">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="39a2e-594">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="39a2e-595">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="39a2e-595">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="39a2e-596">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="39a2e-596">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="39a2e-597">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="39a2e-597">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="39a2e-598">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="39a2e-598">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="39a2e-599">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="39a2e-599">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="39a2e-600">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="39a2e-600">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="39a2e-601">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="39a2e-601">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="39a2e-602">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="39a2e-602">core: Improved performance</span></span>
* <span data-ttu-id="39a2e-603">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="39a2e-603">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="39a2e-604">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="39a2e-604">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="39a2e-605">ACS</span><span class="sxs-lookup"><span data-stu-id="39a2e-605">ACS</span></span>

* <span data-ttu-id="39a2e-606">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="39a2e-606">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="39a2e-607">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="39a2e-607">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="39a2e-608">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="39a2e-608">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="39a2e-609">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="39a2e-609">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="39a2e-610">AppService</span><span class="sxs-lookup"><span data-stu-id="39a2e-610">AppService</span></span>

* <span data-ttu-id="39a2e-611">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-611">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="39a2e-612">Team Services (VSTS) が継続的な配信オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="39a2e-612">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="39a2e-613">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="39a2e-613">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="39a2e-614">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="39a2e-614">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="39a2e-615">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="39a2e-615">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="39a2e-616">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="39a2e-616">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="39a2e-617">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="39a2e-617">support slot swap with preview</span></span>
* <span data-ttu-id="39a2e-618">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="39a2e-618">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="39a2e-619">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="39a2e-619">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="39a2e-620">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="39a2e-620">CosmosDB</span></span>

* <span data-ttu-id="39a2e-621">documentdb モジュールから cosmosdb に名前が変更されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-621">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="39a2e-622">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-622">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="39a2e-623">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-623">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="39a2e-624">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-624">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="39a2e-625">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="39a2e-625">Data Lake Analytics</span></span>

* <span data-ttu-id="39a2e-626">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-626">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="39a2e-627">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-627">Add support for new catalog item type: package.</span></span> <span data-ttu-id="39a2e-628">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="39a2e-628">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="39a2e-629">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="39a2e-629">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="39a2e-630">テーブル</span><span class="sxs-lookup"><span data-stu-id="39a2e-630">Table</span></span>
  * <span data-ttu-id="39a2e-631">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="39a2e-631">Table valued function</span></span>
  * <span data-ttu-id="39a2e-632">表示</span><span class="sxs-lookup"><span data-stu-id="39a2e-632">View</span></span>
  * <span data-ttu-id="39a2e-633">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="39a2e-633">Table Statistics.</span></span> <span data-ttu-id="39a2e-634">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="39a2e-634">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="39a2e-635">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="39a2e-635">Data Lake Store</span></span>

* <span data-ttu-id="39a2e-636">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-636">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="39a2e-637">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="39a2e-637">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="39a2e-638">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="39a2e-638">missed help for access show.</span></span> <span data-ttu-id="39a2e-639">追加しました </span><span class="sxs-lookup"><span data-stu-id="39a2e-639">adding it.</span></span> <span data-ttu-id="39a2e-640">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="39a2e-640">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="39a2e-641">検索</span><span class="sxs-lookup"><span data-stu-id="39a2e-641">Find</span></span>

* <span data-ttu-id="39a2e-642">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="39a2e-642">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="39a2e-643">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39a2e-643">KeyVault</span></span>

* <span data-ttu-id="39a2e-644">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="39a2e-644">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="39a2e-645">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-645">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="39a2e-646">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="39a2e-646">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="39a2e-647">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-647">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="39a2e-648">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="39a2e-648">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="39a2e-649">ラボ</span><span class="sxs-lookup"><span data-stu-id="39a2e-649">Lab</span></span>

* <span data-ttu-id="39a2e-650">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-650">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="39a2e-651">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-651">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="39a2e-652">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-652">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="39a2e-653">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-653">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="39a2e-654">ラボ内でシークレットを管理するためのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-654">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="39a2e-655">監視</span><span class="sxs-lookup"><span data-stu-id="39a2e-655">Monitor</span></span>

* <span data-ttu-id="39a2e-656">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="39a2e-656">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="39a2e-657">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="39a2e-657">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="39a2e-658">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39a2e-658">Network</span></span>

* <span data-ttu-id="39a2e-659">`network watcher test-connectivity` コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-659">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="39a2e-660">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-660">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="39a2e-661">Application Gateway 接続のドレインに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-661">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="39a2e-662">Application Gateway WAF 規則セットの構成に対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-662">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="39a2e-663">ExpressRoute ルート フィルターとルールに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-663">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="39a2e-664">TrafficManager の地理的なルーティングに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-664">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="39a2e-665">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-665">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="39a2e-666">VPN 接続 IPSec ポリシーに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-666">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="39a2e-667">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-667">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="39a2e-668">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-668">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="39a2e-669">`network vpn-connection list/show` コマンドの出力から null 値が削除されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-669">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="39a2e-670">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="39a2e-670">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="39a2e-671">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-671">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="39a2e-672">`dns zone import` でレコードが適切にインポートされないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-672">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="39a2e-673">`traffic-manager endpoint update` が動作しないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-673">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="39a2e-674">"Network Watcher" プレビューのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-674">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="39a2e-675">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39a2e-675">Profile</span></span>

* <span data-ttu-id="39a2e-676">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="39a2e-676">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="39a2e-677">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="39a2e-677">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="39a2e-678">Redis</span><span class="sxs-lookup"><span data-stu-id="39a2e-678">Redis</span></span>

* <span data-ttu-id="39a2e-679">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="39a2e-679">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="39a2e-680">"update-settings" コマンドが廃止されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-680">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="39a2e-681">リソース</span><span class="sxs-lookup"><span data-stu-id="39a2e-681">Resource</span></span>

* <span data-ttu-id="39a2e-682">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="39a2e-682">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="39a2e-683">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="39a2e-683">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="39a2e-684">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="39a2e-684">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="39a2e-685">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="39a2e-685">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="39a2e-686">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="39a2e-686">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="39a2e-687">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="39a2e-687">Add docs for az lock update.</span></span> <span data-ttu-id="39a2e-688">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="39a2e-688">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="39a2e-689">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="39a2e-689">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="39a2e-690">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="39a2e-690">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="39a2e-691">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-691">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="39a2e-692">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="39a2e-692">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="39a2e-693">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="39a2e-693">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="39a2e-694">役割</span><span class="sxs-lookup"><span data-stu-id="39a2e-694">Role</span></span>

* <span data-ttu-id="39a2e-695">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="39a2e-695">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="39a2e-696">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="39a2e-696">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="39a2e-697">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="39a2e-697">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="39a2e-698">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="39a2e-698">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="39a2e-699">SQL</span><span class="sxs-lookup"><span data-stu-id="39a2e-699">SQL</span></span>

* <span data-ttu-id="39a2e-700">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-700">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="39a2e-701">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="39a2e-701">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="39a2e-702">Storage</span><span class="sxs-lookup"><span data-stu-id="39a2e-702">Storage</span></span>

* <span data-ttu-id="39a2e-703">`storage account create` のリソース グループの場所に対する既定の場所。</span><span class="sxs-lookup"><span data-stu-id="39a2e-703">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="39a2e-704">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-704">Add support for incremental blob copy</span></span>
* <span data-ttu-id="39a2e-705">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-705">Add support for large block blob upload</span></span>
* <span data-ttu-id="39a2e-706">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="39a2e-706">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="39a2e-707">VM</span><span class="sxs-lookup"><span data-stu-id="39a2e-707">VM</span></span>

* <span data-ttu-id="39a2e-708">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="39a2e-708">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="39a2e-709">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="39a2e-709">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="39a2e-710">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="39a2e-710">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="39a2e-711">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="39a2e-711">az vm/vmss disk</span></span>
  3. <span data-ttu-id="39a2e-712">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="39a2e-712">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="39a2e-713">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="39a2e-713">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="39a2e-714">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="39a2e-714">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="39a2e-715">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-715">April 3, 2017</span></span>

<span data-ttu-id="39a2e-716">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="39a2e-716">Version 2.0.2</span></span>

<span data-ttu-id="39a2e-717">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました。</span><span class="sxs-lookup"><span data-stu-id="39a2e-717">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="39a2e-718">コア</span><span class="sxs-lookup"><span data-stu-id="39a2e-718">Core</span></span>

* <span data-ttu-id="39a2e-719">既定の一覧に acr、lab、monitor、find モジュールを追加。</span><span class="sxs-lookup"><span data-stu-id="39a2e-719">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="39a2e-720">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="39a2e-720">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="39a2e-721">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="39a2e-721">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="39a2e-722">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="39a2e-722">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="39a2e-723">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="39a2e-723">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="39a2e-724">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="39a2e-724">Add prompting for missing template parameters.</span></span> <span data-ttu-id="39a2e-725">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="39a2e-725">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="39a2e-726">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="39a2e-726">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="39a2e-727">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="39a2e-727">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="39a2e-728">ACS</span><span class="sxs-lookup"><span data-stu-id="39a2e-728">ACS</span></span>

* <span data-ttu-id="39a2e-729">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="39a2e-729">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="39a2e-730">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="39a2e-730">Add support for ssh key password prompting.</span></span> <span data-ttu-id="39a2e-731">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="39a2e-731">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="39a2e-732">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="39a2e-732">Add support for windows clusters.</span></span> <span data-ttu-id="39a2e-733">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="39a2e-733">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="39a2e-734">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="39a2e-734">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="39a2e-735">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="39a2e-735">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="39a2e-736">AppService</span><span class="sxs-lookup"><span data-stu-id="39a2e-736">AppService</span></span>

* <span data-ttu-id="39a2e-737">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="39a2e-737">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="39a2e-738">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="39a2e-738">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="39a2e-739">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="39a2e-739">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="39a2e-740">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="39a2e-740">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="39a2e-741">DataLake</span><span class="sxs-lookup"><span data-stu-id="39a2e-741">DataLake</span></span>

* <span data-ttu-id="39a2e-742">Data Lake Analytics モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="39a2e-742">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="39a2e-743">Data Lake Store モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="39a2e-743">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="39a2e-744">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="39a2e-744">DocuemntDB</span></span>

* <span data-ttu-id="39a2e-745">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="39a2e-745">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="39a2e-746">VM</span><span class="sxs-lookup"><span data-stu-id="39a2e-746">VM</span></span>

* <span data-ttu-id="39a2e-747">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="39a2e-747">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="39a2e-748">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="39a2e-748">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="39a2e-749">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="39a2e-749">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="39a2e-750">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="39a2e-750">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="39a2e-751">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート * ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="39a2e-751">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="39a2e-752">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="39a2e-752">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="39a2e-753">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="39a2e-753">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="39a2e-754">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="39a2e-754">February 27, 2017</span></span>

<span data-ttu-id="39a2e-755">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="39a2e-755">Version 2.0.0</span></span>

<span data-ttu-id="39a2e-756">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。</span><span class="sxs-lookup"><span data-stu-id="39a2e-756">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="39a2e-757">一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="39a2e-757">General availability applies to these command modules:</span></span>
- <span data-ttu-id="39a2e-758">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="39a2e-758">Container Service (acs)</span></span>
- <span data-ttu-id="39a2e-759">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="39a2e-759">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="39a2e-760">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39a2e-760">Networking</span></span>
- <span data-ttu-id="39a2e-761">Storage</span><span class="sxs-lookup"><span data-stu-id="39a2e-761">Storage</span></span>

<span data-ttu-id="39a2e-762">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="39a2e-762">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="39a2e-763">問題は、Microsoft サポートで直接開くことも、[github の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="39a2e-763">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="39a2e-764">[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="39a2e-764">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="39a2e-765">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません。</span><span class="sxs-lookup"><span data-stu-id="39a2e-765">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="39a2e-766">CLI のバージョンを確認するには、`az --version` を使用します。</span><span class="sxs-lookup"><span data-stu-id="39a2e-766">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="39a2e-767">出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="39a2e-767">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="39a2e-768">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。</span><span class="sxs-lookup"><span data-stu-id="39a2e-768">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="39a2e-769">これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です。</span><span class="sxs-lookup"><span data-stu-id="39a2e-769">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="39a2e-770">CLI のナイトリー プレビュー ビルドもあります。</span><span class="sxs-lookup"><span data-stu-id="39a2e-770">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="39a2e-771">詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39a2e-771">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="39a2e-772">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="39a2e-772">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="39a2e-773">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="39a2e-773">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="39a2e-774">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる。</span><span class="sxs-lookup"><span data-stu-id="39a2e-774">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="39a2e-775">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る。</span><span class="sxs-lookup"><span data-stu-id="39a2e-775">Provide feedback from the command line with the `az feedback` command.</span></span>

