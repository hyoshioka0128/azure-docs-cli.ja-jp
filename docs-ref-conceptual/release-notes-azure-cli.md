---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 02/04/2020
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: eafd18344ac4c1c0124ff53864a45510070b6fe7
ms.sourcegitcommit: d0b2763cc856eef44a6ecb78f6b8c64291625750
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "77013286"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="68059-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="68059-103">Azure CLI release notes</span></span>

## <a name="february-04-2020"></a><span data-ttu-id="68059-104">2020 年 2 月 4 日</span><span class="sxs-lookup"><span data-stu-id="68059-104">February 04, 2020</span></span>

<span data-ttu-id="68059-105">バージョン 2.0.81</span><span class="sxs-lookup"><span data-stu-id="68059-105">Version 2.0.81</span></span>

### <a name="acs"></a><span data-ttu-id="68059-106">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-106">ACS</span></span>

* <span data-ttu-id="68059-107">Standard Load Balancer でアウトバウンド割当てポートとアイドル タイムアウトを設定するためのサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-107">Add support to set outbound allocated ports and idle timeouts on standard load balancer</span></span>
* <span data-ttu-id="68059-108">API バージョン 2019-11-01 への更新を行います</span><span class="sxs-lookup"><span data-stu-id="68059-108">Update to API Version 2019-11-01</span></span>

### <a name="acr"></a><span data-ttu-id="68059-109">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-109">ACR</span></span>

* <span data-ttu-id="68059-110">[破壊的変更] `az acr delete` でプロンプトが表示されます</span><span class="sxs-lookup"><span data-stu-id="68059-110">[BREAKING CHANGE] `az acr delete` will prompt</span></span>
* <span data-ttu-id="68059-111">[重大な変更] 'az acr task delete' でプロンプトが表示されます</span><span class="sxs-lookup"><span data-stu-id="68059-111">[BREAKING CHANGE] 'az acr task delete' will prompt</span></span>
* <span data-ttu-id="68059-112">taskrun 管理用の新しいコマンド グループ 'az acr taskrun show/list/delete' を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-112">Add a new command group 'az acr taskrun show/list/delete' for taskrun management</span></span>

### <a name="aks"></a><span data-ttu-id="68059-113">AKS</span><span class="sxs-lookup"><span data-stu-id="68059-113">AKS</span></span>

* <span data-ttu-id="68059-114">各クラスターは、分離を向上させるために、個別のサービス プリンシパルを取得します</span><span class="sxs-lookup"><span data-stu-id="68059-114">Each cluster gets a separate service principal to improve isolation</span></span>

### <a name="appconfig"></a><span data-ttu-id="68059-115">AppConfig</span><span class="sxs-lookup"><span data-stu-id="68059-115">AppConfig</span></span>

* <span data-ttu-id="68059-116">appservice との間での keyvault 参照のインポート/エクスポートをサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-116">Support import/export of keyvault references from/to appservice</span></span>
* <span data-ttu-id="68059-117">appconfig から appconfig へのすべてのラベルのインポート/エクスポートをサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-117">Support import/export of all labels from appconfig to appconfig</span></span>
* <span data-ttu-id="68059-118">設定とインポートの前にキーと機能の名前を検証します</span><span class="sxs-lookup"><span data-stu-id="68059-118">Validate key and feature names before setting and importing</span></span>
* <span data-ttu-id="68059-119">構成ストアの SKU 変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="68059-119">Expose sku modification for configuration store.</span></span>
* <span data-ttu-id="68059-120">マネージド ID のコマンド グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="68059-120">Add command group for managed identity.</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-121">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-121">AppService</span></span>

* <span data-ttu-id="68059-122">Azure Stack: 2019-03-01-hybrid のプロファイルの下の surface コマンド</span><span class="sxs-lookup"><span data-stu-id="68059-122">Azure Stack: surface commands under the profile of 2019-03-01-hybrid</span></span>
* <span data-ttu-id="68059-123">functionapp:Linux で Java 関数アプリを作成する機能を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-123">functionapp: Add ability to create Java function apps in Linux</span></span>

### <a name="arm"></a><span data-ttu-id="68059-124">ARM</span><span class="sxs-lookup"><span data-stu-id="68059-124">ARM</span></span>

* <span data-ttu-id="68059-125">問題 #10246 を修正: 渡されたパラメーター `--ids` がリソース グループ ID の場合、`az resource tag` がクラッシュします</span><span class="sxs-lookup"><span data-stu-id="68059-125">Fix issue #10246: `az resource tag` crashes when the parameter `--ids` passed in is resource group ID</span></span>
* <span data-ttu-id="68059-126">問題 #11658 を修正: `az group export` コマンド が `--query` と `--output` パラメーターをサポートしません</span><span class="sxs-lookup"><span data-stu-id="68059-126">Fix issue #11658: `az group export` command does not support `--query` and `--output` parameters</span></span>
* <span data-ttu-id="68059-127">問題 #10279 を修正:検証が失敗した場合、`az group deployment validate` の終了コードは 0 になります</span><span class="sxs-lookup"><span data-stu-id="68059-127">Fix issue #10279: The exit code of `az group deployment validate` is 0 when the verification fails</span></span>
* <span data-ttu-id="68059-128">問題 #9916 を修正:`az resource list` コマンドのタグとその他のフィルター条件間の競合に関するエラー メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="68059-128">Fix issue #9916: Improve the error message of the conflict between tag and other filter conditions for `az resource list` command</span></span>
* <span data-ttu-id="68059-129">コマンド `az group create` の managedBy 情報の追加をサポートする新しいパラメーター `--managed-by` を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-129">Add new parameter `--managed-by` to support adding managedBy information for command `az group create`</span></span>

### <a name="azure-red-hat-openshift"></a><span data-ttu-id="68059-130">Azure Red Hat OpenShift</span><span class="sxs-lookup"><span data-stu-id="68059-130">Azure Red Hat OpenShift</span></span>

* <span data-ttu-id="68059-131">Azure Red Hat OpensShift クラスターで Log Analytics 監視を管理するための `monitor` サブグループを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-131">Add `monitor` subgroup to manage Log Analytics monitoring in Azure Red Hat OpensShift cluster</span></span>

### <a name="botservice"></a><span data-ttu-id="68059-132">BotService</span><span class="sxs-lookup"><span data-stu-id="68059-132">BotService</span></span>

* <span data-ttu-id="68059-133">問題 #11697 を修正: `az bot create` がべき等ではありません</span><span class="sxs-lookup"><span data-stu-id="68059-133">Fix issue #11697: `az bot create` is not idempotent</span></span>
* <span data-ttu-id="68059-134">名前修正テストをライブ モードでのみ実行するように変更します</span><span class="sxs-lookup"><span data-stu-id="68059-134">Change name-correcting tests to run in Live-mode only</span></span>

### <a name="cdn"></a><span data-ttu-id="68059-135">CDN</span><span class="sxs-lookup"><span data-stu-id="68059-135">CDN</span></span>

* <span data-ttu-id="68059-136">rulesEngine 機能のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-136">Add support for rulesEngine feature</span></span>
* <span data-ttu-id="68059-137">規則を管理するための新しいコマンド グループ 'cdn endpoint rule' を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-137">Add new commands group 'cdn endpoint rule' to manage rules</span></span>
* <span data-ttu-id="68059-138">API バージョン 2019-04-15 を使用するように azure-mgmt-cdn バージョンを 4.0.0 に更新します</span><span class="sxs-lookup"><span data-stu-id="68059-138">Update azure-mgmt-cdn version to 4.0.0 to use api version 2019-04-15</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="68059-139">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="68059-139">Deployment Manager</span></span>

* <span data-ttu-id="68059-140">すべてのリソースのリスト操作を追加します。</span><span class="sxs-lookup"><span data-stu-id="68059-140">Add list operation for all resources.</span></span>
* <span data-ttu-id="68059-141">新しい手順の種類に対する手順リソースを強化します。</span><span class="sxs-lookup"><span data-stu-id="68059-141">Enhance step resource for new step type.</span></span>
* <span data-ttu-id="68059-142">バージョン 0.2.0 を使用するように azure-mgmt-deploymentmanager パッケージを更新します。</span><span class="sxs-lookup"><span data-stu-id="68059-142">Update azure-mgmt-deploymentmanager package to use version 0.2.0.</span></span>

### <a name="iot"></a><span data-ttu-id="68059-143">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-143">IoT</span></span>

* <span data-ttu-id="68059-144">'IoT hub Job' コマンドを廃止します。</span><span class="sxs-lookup"><span data-stu-id="68059-144">Deprecate 'IoT hub Job' commands.</span></span>

### <a name="iot-central"></a><span data-ttu-id="68059-145">IoT Central</span><span class="sxs-lookup"><span data-stu-id="68059-145">IoT Central</span></span>

* <span data-ttu-id="68059-146">新しい SKU 名 ST0、ST1、ST2 でのアプリの作成/更新をサポートします。</span><span class="sxs-lookup"><span data-stu-id="68059-146">Support app creation/update with the new sku name ST0, ST1, ST2.</span></span>

### <a name="key-vault"></a><span data-ttu-id="68059-147">Key Vault</span><span class="sxs-lookup"><span data-stu-id="68059-147">Key Vault</span></span>

* <span data-ttu-id="68059-148">キーをダウンロードするための新しいコマンド `az keyvault key download` を追加します。</span><span class="sxs-lookup"><span data-stu-id="68059-148">Add a new command `az keyvault key download` for downloading keys.</span></span>

### <a name="misc"></a><span data-ttu-id="68059-149">その他</span><span class="sxs-lookup"><span data-stu-id="68059-149">Misc</span></span>

* <span data-ttu-id="68059-150">#6371 を修正:Bash でのファイル名と環境変数の補完をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-150">Fix #6371: Support filename and environment variable completion in Bash</span></span>

### <a name="network"></a><span data-ttu-id="68059-151">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-151">Network</span></span>

* <span data-ttu-id="68059-152">#2092 を修正: az network dns record-add/remove: レコード セットが見つからない場合に警告を追加します。</span><span class="sxs-lookup"><span data-stu-id="68059-152">Fix #2092: az network dns record-set add/remove: add warning when record-set is not found.</span></span> <span data-ttu-id="68059-153">今後、この自動作成を確認するための追加の引数がサポートされる予定です。</span><span class="sxs-lookup"><span data-stu-id="68059-153">In the future, an extra argument will be supported to confirm this auto creation.</span></span>

### <a name="policy"></a><span data-ttu-id="68059-154">ポリシー</span><span class="sxs-lookup"><span data-stu-id="68059-154">Policy</span></span>

* <span data-ttu-id="68059-155">豊富なポリシー メタデータ リソースを取得するための新しいコマンド `az policy metadata` を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-155">Add new command `az policy metadata` to retrieve rich policy metadata resources</span></span>
* <span data-ttu-id="68059-156">`az policy remediation create`:`--resource-discovery-mode` パラメーターを使用して、修復前にコンプライアンスを再評価する必要があるかどうかを指定します</span><span class="sxs-lookup"><span data-stu-id="68059-156">`az policy remediation create`: Specify whether compliance should be re-evaluated prior to remediation with the `--resource-discovery-mode` parameter</span></span>

### <a name="profile"></a><span data-ttu-id="68059-157">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-157">Profile</span></span>

* <span data-ttu-id="68059-158">`az account get-access-token`:サブスクリプションを指定することなく、テナントのトークンを直接取得するための `--tenant` パラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-158">`az account get-access-token`: Add `--tenant` parameter to acquire token for the tenant directly, needless to specify a subscription</span></span>

### <a name="rbac"></a><span data-ttu-id="68059-159">RBAC</span><span class="sxs-lookup"><span data-stu-id="68059-159">RBAC</span></span>

* <span data-ttu-id="68059-160">[重大な変更] #11883 を修正: `az role assignment create`: 空のスコープの場合にエラーが表示されます</span><span class="sxs-lookup"><span data-stu-id="68059-160">[BREAKING CHANGE] Fix #11883: `az role assignment create`: empty scope will prompt error</span></span>

### <a name="security"></a><span data-ttu-id="68059-161">Security</span><span class="sxs-lookup"><span data-stu-id="68059-161">Security</span></span>

* <span data-ttu-id="68059-162">ストレージ アカウントの高度な脅威保護設定を表示および管理するための新しいコマンド `az atp show` と `az atp update` を追加します。</span><span class="sxs-lookup"><span data-stu-id="68059-162">Add new commands `az atp show` and `az atp update` to view and manage advanced threat protection settings for storage accounts.</span></span>

### <a name="sql"></a><span data-ttu-id="68059-163">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-163">SQL</span></span>

* <span data-ttu-id="68059-164">`sql dw create`: `--zone-redundant` と `--read-replica-count` パラメーターを廃止します。</span><span class="sxs-lookup"><span data-stu-id="68059-164">`sql dw create`: deprecate `--zone-redundant` and `--read-replica-count` parameters.</span></span> <span data-ttu-id="68059-165">これらのパラメーターは、DataWarehouse には適用されません。</span><span class="sxs-lookup"><span data-stu-id="68059-165">These parameters do not apply to DataWarehouse.</span></span>
* <span data-ttu-id="68059-166">[破壊的変更] `az sql db create`:"az sql db create --sample-name" に対して使用可能な値としてドキュメントに記載されている "WideWorldImportersStd" と "WideWorldImportersFull" を削除します。</span><span class="sxs-lookup"><span data-stu-id="68059-166">[BREAKING CHANGE] `az sql db create`: Remove "WideWorldImportersStd" and "WideWorldImportersFull" as documented allowed values for "az sql db create --sample-name".</span></span> <span data-ttu-id="68059-167">これらのサンプル データベースを使用すると、常に作成が失敗します。</span><span class="sxs-lookup"><span data-stu-id="68059-167">These sample databases would always cause creation to fail.</span></span>
* <span data-ttu-id="68059-168">SQL データベースの機密性分類を管理するための新しいコマンド `sql db classification show/list/update/delete` と `sql db classification recommendation list/enable/disable` を追加します。</span><span class="sxs-lookup"><span data-stu-id="68059-168">Add New commands `sql db classification show/list/update/delete` and `sql db classification recommendation list/enable/disable` to manage sensitivity classifications for SQL databases.</span></span>
* <span data-ttu-id="68059-169">`az sql db audit-policy`:空の監査アクションとグループの修正</span><span class="sxs-lookup"><span data-stu-id="68059-169">`az sql db audit-policy`: Fix for empty audit actions and groups</span></span>

### <a name="storage"></a><span data-ttu-id="68059-170">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-170">Storage</span></span>

* <span data-ttu-id="68059-171">Azure ファイル共有の管理操作に Microsoft.Storage リソース プロバイダーを使用するための新しいコマンド グループ `az storage share-rm` を追加します。</span><span class="sxs-lookup"><span data-stu-id="68059-171">Add a new command group `az storage share-rm` to use the Microsoft.Storage resource provider for Azure file share management operations.</span></span>
* <span data-ttu-id="68059-172">問題 #11415 を修正: `az storage blob update` のアクセス許可エラー</span><span class="sxs-lookup"><span data-stu-id="68059-172">Fix issue #11415: permission error for `az storage blob update`</span></span>
* <span data-ttu-id="68059-173">Azcopy 10.3.3 を統合し、Win32 をサポートします。</span><span class="sxs-lookup"><span data-stu-id="68059-173">Integrate Azcopy 10.3.3 and support Win32.</span></span>
* <span data-ttu-id="68059-174">`az storage copy`:`--include-path`、`--include-pattern`、`--exclude-path`、および `--exclude-pattern` パラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-174">`az storage copy`: Add `--include-path`, `--include-pattern`, `--exclude-path` and`--exclude-pattern` parameters</span></span>
* <span data-ttu-id="68059-175">`az storage remove`:`--inlcude` および `--exclude` パラメーターを `--include-path`、`--include-pattern`、`--exclude-path`、および `--exclude-pattern` パラメーターに変更します</span><span class="sxs-lookup"><span data-stu-id="68059-175">`az storage remove`: Change `--inlcude` and `--exclude` parameters to `--include-path`, `--include-pattern`, `--exclude-path` and`--exclude-pattern` parameters</span></span>
* <span data-ttu-id="68059-176">`az storage sync`:`--include-pattern`、`--exclude-path`、および `--exclude-pattern` パラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-176">`az storage sync`: Add `--include-pattern`, `--exclude-path` and`--exclude-pattern` parameters</span></span>

### <a name="servicefabric"></a><span data-ttu-id="68059-177">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68059-177">ServiceFabric</span></span>

* <span data-ttu-id="68059-178">アプリケーションとサービスを管理するための新しいコマンドを追加します。</span><span class="sxs-lookup"><span data-stu-id="68059-178">Add new commands to manage appliaction and services.</span></span>

## <a name="january-13-2020"></a><span data-ttu-id="68059-179">2020 年 1 月 13 日</span><span class="sxs-lookup"><span data-stu-id="68059-179">January 13, 2020</span></span>

<span data-ttu-id="68059-180">バージョン 2.0.80</span><span class="sxs-lookup"><span data-stu-id="68059-180">Version 2.0.80</span></span>

### <a name="compute"></a><span data-ttu-id="68059-181">Compute</span><span class="sxs-lookup"><span data-stu-id="68059-181">Compute</span></span>

* <span data-ttu-id="68059-182">disk update:--disk-encryption-set と --encryption-type を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-182">disk update: Add --disk-encryption-set and --encryption-type</span></span>
* <span data-ttu-id="68059-183">snapshot create/update:--disk-encryption-set と --encryption-type を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-183">snapshot create/update: Add --disk-encryption-set and --encryption-type</span></span>

### <a name="storage"></a><span data-ttu-id="68059-184">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-184">Storage</span></span>

* <span data-ttu-id="68059-185">azure-mgmt-storage のバージョンを 7.1.0 にアップグレードします</span><span class="sxs-lookup"><span data-stu-id="68059-185">Upgrade azure-mgmt-storage version to 7.1.0</span></span>
* <span data-ttu-id="68059-186">`az storage account create`:テーブルとキューの暗号化サービスをサポートするための `--encryption-key-type-for-table` と `--encryption-key-type-for-queue` を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-186">`az storage account create`: Add `--encryption-key-type-for-table` and `--encryption-key-type-for-queue` to support Table and Queue Encryption Service</span></span>

## <a name="january-07-2020"></a><span data-ttu-id="68059-187">2020 年 1 月 7 日</span><span class="sxs-lookup"><span data-stu-id="68059-187">January 07, 2020</span></span>

<span data-ttu-id="68059-188">バージョン 2.0.79</span><span class="sxs-lookup"><span data-stu-id="68059-188">Version 2.0.79</span></span>

### <a name="acr"></a><span data-ttu-id="68059-189">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-189">ACR</span></span>

* <span data-ttu-id="68059-190">[重大な変更] 'acr build'、'acr task create/update'、'acr run'、および 'acr pack' の '--os' パラメーターを削除します。</span><span class="sxs-lookup"><span data-stu-id="68059-190">[BREAKING CHANGE] Remove '--os' parameter for 'acr build', 'acr task create/update', 'acr run', and 'acr pack'.</span></span> <span data-ttu-id="68059-191">代わりに、'--platform' を使用してください。</span><span class="sxs-lookup"><span data-stu-id="68059-191">Use '--platform' instead.</span></span>

### <a name="appconfig"></a><span data-ttu-id="68059-192">AppConfig</span><span class="sxs-lookup"><span data-stu-id="68059-192">AppConfig</span></span>

* <span data-ttu-id="68059-193">機能フラグのインポート/エクスポートのサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-193">Add support for importing/exporting feature flags</span></span>
* <span data-ttu-id="68059-194">keyvault 参照を作成するための新しいコマンド 'az appconfig kv set-keyvault' を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-194">Add new command 'az appconfig kv set-keyvault' for creating keyvault reference</span></span>
* <span data-ttu-id="68059-195">機能フラグをファイルにエクスポートするときに、さまざまな名前付け規則をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-195">Support various naming conventions when exporting feature flags to file</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-196">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-196">AppService</span></span>

* <span data-ttu-id="68059-197">問題 #7154 を修正:単一引用符ではなく、アクサン グラーブを使用するように、コマンド < > のドキュメントを更新しています</span><span class="sxs-lookup"><span data-stu-id="68059-197">Fix issue #7154: Updating documentation for command <> to use back ticks instead of single quotes</span></span>
* <span data-ttu-id="68059-198">問題 #11287 を修正: webapp up:既定で、up を使用して作成されたアプリを 'SSL 有効' にする必要がある</span><span class="sxs-lookup"><span data-stu-id="68059-198">Fix issue #11287: webapp up: By default make the app created using up 'should be 'SSL enabled'</span></span>
* <span data-ttu-id="68059-199">問題 #11592 を修正:HTML 静的サイトに az webapp up フラグを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-199">Fix issue #11592: Add az webapp up flag for html static sites</span></span>

### <a name="arm"></a><span data-ttu-id="68059-200">ARM</span><span class="sxs-lookup"><span data-stu-id="68059-200">ARM</span></span>

* <span data-ttu-id="68059-201">`az resource tag` を修正:Recovery Services コンテナー タグを更新できない</span><span class="sxs-lookup"><span data-stu-id="68059-201">Fix `az resource tag`: Recovery Services Vault tags cannot be updated</span></span>

### <a name="backup"></a><span data-ttu-id="68059-202">バックアップ</span><span class="sxs-lookup"><span data-stu-id="68059-202">Backup</span></span>

* <span data-ttu-id="68059-203">IaasVM ワークロードの論理的な削除機能を有効にするための新しいコマンド 'backup protection undelete' を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-203">Added new command 'backup protection undelete' to enable soft-delete feature for IaasVM workload</span></span>
* <span data-ttu-id="68059-204">backup-properties コマンドを設定するための新しいパラメーター '--soft-delete-feature-state' を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-204">Added new parameter '--soft-delete-feature-state' to set backup-properties command</span></span>
* <span data-ttu-id="68059-205">IaasVM ワークロードのディスク除外のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-205">Added disk exclusion support for IaasVM workload</span></span>

### <a name="compute"></a><span data-ttu-id="68059-206">Compute</span><span class="sxs-lookup"><span data-stu-id="68059-206">Compute</span></span>

* <span data-ttu-id="68059-207">Azure Stack プロファイルの `vm create` エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="68059-207">Fix `vm create` failure in Azure Stack profile.</span></span>
* <span data-ttu-id="68059-208">vm monitor metrics tail/list-definitions: VM のクエリ メトリックとリスト定義をサポートします。</span><span class="sxs-lookup"><span data-stu-id="68059-208">vm monitor metrics tail/list-definitions: support query metric and list definitions for a vm.</span></span>
* <span data-ttu-id="68059-209">az vm の新しい再適用コマンド アクションを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-209">Add new reapply command action for az vm</span></span>

### <a name="hdinsight"></a><span data-ttu-id="68059-210">HDInsight</span><span class="sxs-lookup"><span data-stu-id="68059-210">HDInsight</span></span>

* <span data-ttu-id="68059-211">Kafka REST プロキシを使用する Kafka クラスターの作成のサポート</span><span class="sxs-lookup"><span data-stu-id="68059-211">Support for creating a Kafka cluster with Kafka Rest Proxy</span></span>
* <span data-ttu-id="68059-212">azure-mgmt-hdinsight を 1.3.0 にアップグレード</span><span class="sxs-lookup"><span data-stu-id="68059-212">Upgrade azure-mgmt-hdinsight to 1.3.0</span></span>

### <a name="misc"></a><span data-ttu-id="68059-213">その他</span><span class="sxs-lookup"><span data-stu-id="68059-213">Misc.</span></span>

* <span data-ttu-id="68059-214">既定の JSON 形式 または --output によって構成された形式で Azure CLI モジュールと拡張機能のバージョンを表示するプレビュー コマンド `az version show` を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-214">Add preview command `az version show` to show the versions of Azure CLI modules and extensions in JSON format by default or format configured by --output</span></span>

### <a name="event-hubs"></a><span data-ttu-id="68059-215">Event Hubs</span><span class="sxs-lookup"><span data-stu-id="68059-215">Event Hubs</span></span>

* <span data-ttu-id="68059-216">[重大な変更] コマンド 'az eventhubs eventhub update' と 'az eventhubs eventhub create' から 'ReceiveDisabled' status オプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="68059-216">[BREAKING CHANGE] Remove 'ReceiveDisabled' status option from command 'az eventhubs eventhub update' and 'az eventhubs eventhub create'.</span></span> <span data-ttu-id="68059-217">このオプションは、イベント ハブ エンティティに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="68059-217">This option is not valid for Event Hub entities.</span></span>

### <a name="service-bus"></a><span data-ttu-id="68059-218">Service Bus</span><span class="sxs-lookup"><span data-stu-id="68059-218">Service Bus</span></span>

* <span data-ttu-id="68059-219">[重大な変更] コマンド 'az servicebus topic create'、'az servicebus topic update'、'az servicebus queue create'、および 'az servicebus queue update' から 'ReceiveDisabled' status オプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="68059-219">[BREAKING CHANGE] Remove 'ReceiveDisabled' status option from command 'az servicebus topic create', 'az servicebus topic update', 'az servicebus queue create', and 'az servicebus queue update'.</span></span> <span data-ttu-id="68059-220">このオプションは、Service Bus のトピックとキューに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="68059-220">This option is not valid for Service Bus topics and queues.</span></span>

### <a name="rbac"></a><span data-ttu-id="68059-221">RBAC</span><span class="sxs-lookup"><span data-stu-id="68059-221">RBAC</span></span>

* <span data-ttu-id="68059-222">#11712 を修正: アプリケーションまたはサービス プリンシパルが存在しない場合に `az ad app/sp show` で終了コード 3 が返されない</span><span class="sxs-lookup"><span data-stu-id="68059-222">Fix #11712: `az ad app/sp show` does not return exit code 3 when the application or service principal does not exist</span></span>

### <a name="storage"></a><span data-ttu-id="68059-223">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-223">Storage</span></span>

* <span data-ttu-id="68059-224">`az storage account create`:--enable-hierarchical-namespace パラメーターのプレビュー フラグを削除します</span><span class="sxs-lookup"><span data-stu-id="68059-224">`az storage account create`: Remove preview flag for --enable-hierarchical-namespace parameter</span></span>
* <span data-ttu-id="68059-225">API バージョン 2019-06-01 を使用するために azure-mgmt-storage バージョンを 7.0.0 に更新します</span><span class="sxs-lookup"><span data-stu-id="68059-225">Update azure-mgmt-storage version to 7.0.0 to use api version 2019-06-01</span></span>
* <span data-ttu-id="68059-226">ストレージ アカウント blob-service-properties の削除の保持ポリシーの管理をサポートするために、新しいパラメーター `--enable-delete-retention` と `--delete-retention-days` を追加します。</span><span class="sxs-lookup"><span data-stu-id="68059-226">Add new parameters `--enable-delete-retention` and `--delete-retention-days` to support managing delete retention policy for storage account blob-service-properties.</span></span>

## <a name="december-17-2019"></a><span data-ttu-id="68059-227">2019 年 12 月 17 日</span><span class="sxs-lookup"><span data-stu-id="68059-227">December 17, 2019</span></span>

<span data-ttu-id="68059-228">2.0.78</span><span class="sxs-lookup"><span data-stu-id="68059-228">2.0.78</span></span>

### <a name="acr"></a><span data-ttu-id="68059-229">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-229">ACR</span></span>

* <span data-ttu-id="68059-230">acr task run でのローカル コンテキストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-230">Added support Local context in acr task run</span></span>

### <a name="acs"></a><span data-ttu-id="68059-231">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-231">ACS</span></span>

* <span data-ttu-id="68059-232">[重大な変更] az openshift create: `--workspace-resource-id` の名前を `--workspace-id` に変更します。</span><span class="sxs-lookup"><span data-stu-id="68059-232">[BREAKING CHANGE]az openshift create: rename `--workspace-resource-id` to `--workspace-id`.</span></span>

### <a name="ams"></a><span data-ttu-id="68059-233">AMS</span><span class="sxs-lookup"><span data-stu-id="68059-233">AMS</span></span>

* <span data-ttu-id="68059-234">リソースが見つからない場合に 3 を返すように表示コマンドを更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-234">Updated show commands to return 3 when resource not found</span></span>

### <a name="appconfig"></a><span data-ttu-id="68059-235">AppConfig</span><span class="sxs-lookup"><span data-stu-id="68059-235">AppConfig</span></span>

* <span data-ttu-id="68059-236">要求 URL に api-version を追加するときのバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-236">Fixed bug when appending api-version to request url.</span></span> <span data-ttu-id="68059-237">既存のソリューションは、改ページ位置の自動修正で機能しません。</span><span class="sxs-lookup"><span data-stu-id="68059-237">The existing solution doesn't work with pagination.</span></span>
* <span data-ttu-id="68059-238">英語以外の言語を表示するためのサポートを追加しました。これは、Microsoft のバックエンド サービスがグローバリゼーション向けに unicode をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="68059-238">Added support for showing languages besides English as our backend service support unicode for globalization.</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-239">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-239">AppService</span></span>

* <span data-ttu-id="68059-240">問題 #11217 を修正: webapp: az webapp config ssl upload はスロット パラメーターをサポートする必要がある</span><span class="sxs-lookup"><span data-stu-id="68059-240">Fixed issue #11217: webapp: az webapp config ssl upload should support slot parameter</span></span>
* <span data-ttu-id="68059-241">問題 #10965 を修正:エラー:名前を空にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="68059-241">Fixed issue #10965: Error: Name cannot be empty.</span></span> <span data-ttu-id="68059-242">ip_address とサブネットによる削除を許可します</span><span class="sxs-lookup"><span data-stu-id="68059-242">Allow remove by ip_address and subnet</span></span>
* <span data-ttu-id="68059-243">Key Vault `az webapp config ssl import` からの証明書のインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-243">Added support for importing certificates from Key Vault `az webapp config ssl import`</span></span>

### <a name="arm"></a><span data-ttu-id="68059-244">ARM</span><span class="sxs-lookup"><span data-stu-id="68059-244">ARM</span></span>

* <span data-ttu-id="68059-245">6\.0.0 を使用するように azure-mgmt-resource パッケージを更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-245">Updated azure-mgmt-resource package to use 6.0.0</span></span>
* <span data-ttu-id="68059-246">新しいパラメーター `--aux-subs` の追加による `az group deployment create` コマンドのクロス テナントのサポート</span><span class="sxs-lookup"><span data-stu-id="68059-246">Cross Tenant Support for `az group deployment create` command by adding new parameter `--aux-subs`</span></span>
* <span data-ttu-id="68059-247">ポリシー セット定義へのメタデータ情報の追加をサポートするために、新しいパラメーター `--metadata` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-247">Added new parameter `--metadata` to support adding metadata information for policy set definitions.</span></span>

### <a name="backup"></a><span data-ttu-id="68059-248">バックアップ</span><span class="sxs-lookup"><span data-stu-id="68059-248">Backup</span></span>

* <span data-ttu-id="68059-249">SQL および SAP Hana ワークロードのバックアップ サポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-249">Added Backup support for SQL and SAP Hana workload.</span></span>

### <a name="botservice"></a><span data-ttu-id="68059-250">BotService</span><span class="sxs-lookup"><span data-stu-id="68059-250">BotService</span></span>

* <span data-ttu-id="68059-251">[重大な変更] プレビューコマンド 'az bot create' から '--version' フラグを削除します。</span><span class="sxs-lookup"><span data-stu-id="68059-251">[Breaking change] Remove '--version' flag from preview command 'az bot create'.</span></span> <span data-ttu-id="68059-252">v4 SDK ボットのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="68059-252">Only v4 SDK bots are supported.</span></span>
* <span data-ttu-id="68059-253">名前を使用できるかどうかのチェックを 'sz bot create' に追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-253">Added name availability check for 'az bot create'.</span></span>
* <span data-ttu-id="68059-254">'az bot update' を使用してボットのアイコン URL を更新するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-254">Added support for updating the icon URL for a bot via 'az bot update'.</span></span>
* <span data-ttu-id="68059-255">'az bot directline update' を使用して Direct Line チャネルを更新するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-255">Added support for updating a Direct Line channel via 'az bot directline update'.</span></span>
* <span data-ttu-id="68059-256">'az bot directline create' に '--enable-enhanced-auth' フラグのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-256">Added '--enable-enhanced-auth' flag support to 'az bot directline create'.</span></span>
* <span data-ttu-id="68059-257">コマンド グループ 'az bot authsetting' は、プレビュー段階ではなく、GA です。</span><span class="sxs-lookup"><span data-stu-id="68059-257">The following command groups are GA and not in preview: 'az bot authsetting'.</span></span>
* <span data-ttu-id="68059-258">'az bot' の次のコマンドは、プレビュー段階ではなく、GA です: 'create'、'prepare-deploy'、'show'、'delete'、'update'。</span><span class="sxs-lookup"><span data-stu-id="68059-258">The following commands in 'az bot' are GA and not in preview: 'create', 'prepare-deploy', 'show', 'delete', 'update'.</span></span>
* <span data-ttu-id="68059-259">'az bot prepare-deploy' が修正され、 '--proj-file-path' 値が小文字に変更されます (例:"Test.csproj" が "test.csproj" に)。</span><span class="sxs-lookup"><span data-stu-id="68059-259">Fixed 'az bot prepare-deploy' changing '--proj-file-path' value to lower case (e.g. "Test.csproj" to "test.csproj").</span></span>

### <a name="compute"></a><span data-ttu-id="68059-260">Compute</span><span class="sxs-lookup"><span data-stu-id="68059-260">Compute</span></span>

* <span data-ttu-id="68059-261">vmss create/update:--scale-in-policy を追加しました。これは、VMSS がスケールインされるときに削除対象として選択される仮想マシンを決定します。</span><span class="sxs-lookup"><span data-stu-id="68059-261">vmss create/update: Added --scale-in-policy, which decides which virtual machines are chosen for removal when a VMSS is scaled-in.</span></span>
* <span data-ttu-id="68059-262">vm/vmss update:--priority を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-262">vm/vmss update: Added --priority.</span></span>
* <span data-ttu-id="68059-263">vm/vmss update:--max-price を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-263">vm/vmss update: Added --max-price.</span></span>
* <span data-ttu-id="68059-264">disk-encryption-set コマンド グループ (create、show、update、delete、list) を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-264">Added disk-encryption-set command group (create, show, update, delete, list).</span></span>
* <span data-ttu-id="68059-265">disk create:--encryption-type と --disk-encryption-set を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-265">disk create: Added --encryption-type and --disk-encryption-set.</span></span>
* <span data-ttu-id="68059-266">vm/vmss create: --os-disk-encryption-set と --data-disk-encryption-sets を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-266">vm/vmss create: Added --os-disk-encryption-set and --data-disk-encryption-sets.</span></span>

### <a name="core"></a><span data-ttu-id="68059-267">コア</span><span class="sxs-lookup"><span data-stu-id="68059-267">Core</span></span>

* <span data-ttu-id="68059-268">Python 3.4 のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-268">Removed support for Python 3.4</span></span>
* <span data-ttu-id="68059-269">複数のコマンドでの HaTS 調査のプラグイン</span><span class="sxs-lookup"><span data-stu-id="68059-269">Plug in HaTS survey in multiple commands</span></span>

### <a name="dls"></a><span data-ttu-id="68059-270">DLS</span><span class="sxs-lookup"><span data-stu-id="68059-270">DLS</span></span>

* <span data-ttu-id="68059-271">ADLS SDK バージョンを更新しました (0.0.48)。</span><span class="sxs-lookup"><span data-stu-id="68059-271">Updated ADLS sdk version (0.0.48).</span></span>

### <a name="install"></a><span data-ttu-id="68059-272">インストール</span><span class="sxs-lookup"><span data-stu-id="68059-272">Install</span></span>

* <span data-ttu-id="68059-273">インストール スクリプトで python 3.8 がサポートされます</span><span class="sxs-lookup"><span data-stu-id="68059-273">Install script support python 3.8</span></span>

### <a name="iot"></a><span data-ttu-id="68059-274">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-274">IOT</span></span>

* <span data-ttu-id="68059-275">[重大な変更] manual-failover から --failover-region パラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-275">[BREAKING CHANGE] Removed --failover-region parameter from manual-failover.</span></span> <span data-ttu-id="68059-276">これで、割り当てられた geo ペアのセカンダリ リージョンにフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="68059-276">Now it will failover to assigned geo-paired secondary region.</span></span>

### <a name="key-vault"></a><span data-ttu-id="68059-277">Key Vault</span><span class="sxs-lookup"><span data-stu-id="68059-277">Key Vault</span></span>

* <span data-ttu-id="68059-278">#8095 を修正: `az keyvault storage remove`: ヘルプ メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="68059-278">Fixed #8095: `az keyvault storage remove`: improve the help message</span></span>
* <span data-ttu-id="68059-279">#8921 を修正: `az keyvault key/secret/certificate list/list-deleted/list-versions`: パラメーター `--maxresults` の検証のバグを修正します</span><span class="sxs-lookup"><span data-stu-id="68059-279">Fixed #8921: `az keyvault key/secret/certificate list/list-deleted/list-versions`: fix the validation bug on parameter `--maxresults`</span></span>
* <span data-ttu-id="68059-280">#10512 を修正: `az keyvault set-policy`: `--object-id`、`--spn`、`--upn` のいずれも指定されていない場合のエラー メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="68059-280">Fixed #10512: `az keyvault set-policy`: improve the error message when none of `--object-id`, `--spn` or `--upn` is specified</span></span>
* <span data-ttu-id="68059-281">#10846 を修正: `az keyvault secret show-deleted`: `--id` を指定した場合、`--name/-n` は必要ありません</span><span class="sxs-lookup"><span data-stu-id="68059-281">Fixed #10846: `az keyvault secret show-deleted`: when `--id` is specified, `--name/-n` is not required</span></span>
* <span data-ttu-id="68059-282">#11084 を修正: `az keyvault secret download`: パラメーター `--encoding` のヘルプ メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="68059-282">Fixed #11084: `az keyvault secret download`: improve the help message of parameter `--encoding`</span></span>

### <a name="network"></a><span data-ttu-id="68059-283">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-283">Network</span></span>

* <span data-ttu-id="68059-284">az network application-gateway probe:作成および更新時にバックエンド サーバーをプローブするためのポートを指定する --port オプションのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-284">az network application-gateway probe: Added support --port option to specify a port for probing backend servers when create and update</span></span>
* <span data-ttu-id="68059-285">az network application-gateway url-path-map create/update: `--waf-policy` のバグ修正</span><span class="sxs-lookup"><span data-stu-id="68059-285">az network application-gateway url-path-map create/update: bug fix for `--waf-policy`</span></span>
* <span data-ttu-id="68059-286">az network application-gateway:`--rewrite-rule-set` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-286">az network application-gateway: Added support `--rewrite-rule-set`</span></span>
* <span data-ttu-id="68059-287">az network list-service-aliases:サービス エンドポイント ポリシーに使用できるサービス別名を一覧表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-287">az network list-service-aliases: Added support list service aliases which can be used for Service Endpoint Policies</span></span>
* <span data-ttu-id="68059-288">az network dns zone import:レコード名での .@ のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-288">az network dns zone import: Added support .@ in record name</span></span>

### <a name="packaging"></a><span data-ttu-id="68059-289">梱包</span><span class="sxs-lookup"><span data-stu-id="68059-289">Packaging</span></span>

* <span data-ttu-id="68059-290">pip インストール用のバック エッジ ビルドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-290">Added back edge builds for pip install</span></span>
* <span data-ttu-id="68059-291">Ubuntu eoan パッケージを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-291">Added Ubuntu eoan package</span></span>

### <a name="policy"></a><span data-ttu-id="68059-292">ポリシー</span><span class="sxs-lookup"><span data-stu-id="68059-292">Policy</span></span>

* <span data-ttu-id="68059-293">ポリシー API バージョン 2019-09-01 のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-293">Added support for Policy API version 2019-09-01.</span></span>
* <span data-ttu-id="68059-294">az policy set-definition:`--definition-groups` パラメーターを使用したポリシー セット定義内のグループ化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-294">az policy set-definition: Added support grouping within policy set definitions with `--definition-groups` parameter</span></span>

### <a name="redis"></a><span data-ttu-id="68059-295">Redis</span><span class="sxs-lookup"><span data-stu-id="68059-295">Redis</span></span>

* <span data-ttu-id="68059-296">`az redis create` コマンドにプレビュー パラメーター `--replicas-per-master` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-296">Added preview param `--replicas-per-master` to `az redis create` command</span></span>
* <span data-ttu-id="68059-297">azure-mgmt-redis を 6.0.0 から 7.0.0rc1 に更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-297">Updated azure-mgmt-redis from 6.0.0 to 7.0.0rc1</span></span>

### <a name="servicefabric"></a><span data-ttu-id="68059-298">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68059-298">ServiceFabric</span></span>

* <span data-ttu-id="68059-299">#10963 を含む node-type 追加ロジックを修正:持続性レベル Gold で新しいノード タイプを追加すると、常に CLI エラーがスローされる</span><span class="sxs-lookup"><span data-stu-id="68059-299">Fixed in node-type add logic including #10963: Adding new node type with durability level Gold will always throw CLI error</span></span>
* <span data-ttu-id="68059-300">作成テンプレートの ServiceFabricNodeVmExt バージョンを 1.1 に更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-300">Updated ServiceFabricNodeVmExt version to 1.1 in creation template</span></span>

### <a name="sql"></a><span data-ttu-id="68059-301">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-301">SQL</span></span>

* <span data-ttu-id="68059-302">読み取りスケール管理をサポートするために、sql db create および update コマンドに "--read-scale" と "--read-replicas" パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-302">Added "--read-scale" and "--read-replicas" parameters to sql db create and update commands, to support read scale management.</span></span>

### <a name="storage"></a><span data-ttu-id="68059-303">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-303">Storage</span></span>

* <span data-ttu-id="68059-304">GA リリースでの storage account create および update コマンド用の大きいファイルの共有プロパティ</span><span class="sxs-lookup"><span data-stu-id="68059-304">GA Release Large File Shares property for storage account create and update command</span></span>
* <span data-ttu-id="68059-305">GA リリースでのユーザー委任 SAS トークンのサポート</span><span class="sxs-lookup"><span data-stu-id="68059-305">GA Release User Delegation SAS token Support</span></span>
* <span data-ttu-id="68059-306">ストレージ アカウントの Blob service のプロパティを管理するための新しいコマンド `az storage account blob-service-properties show` と `az storage account blob-service-properties update --enable-change-feed` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="68059-306">Added new commands `az storage account blob-service-properties show` and `az storage account blob-service-properties update --enable-change-feed` to manage blob service properties for storage account.</span></span>
* <span data-ttu-id="68059-307">[今後の破壊的変更] `az storage copy`: `*` 文字は URL 内のワイルドカードとしてサポートされなくなりましたが、新しいパラメーターの --include-pattern と --exclude-pattern が `*` ワイルドカードをサポートして追加されます。</span><span class="sxs-lookup"><span data-stu-id="68059-307">[COMING BREAKING CHANGE] `az storage copy`: `*` character is no longer supported as a wildcard in URL, but new parameters --include-pattern and --exclude-pattern will be added with `*` wildcard support.</span></span>
* <span data-ttu-id="68059-308">問題 #11043 を修正:`az storage remove` コマンドでコンテナー/共有全体を削除するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-308">Fixed issue #11043: Added support to remove whole container/share in `az storage remove` command</span></span>

## <a name="november-26-2019"></a><span data-ttu-id="68059-309">2019 年 11 月 26 日</span><span class="sxs-lookup"><span data-stu-id="68059-309">November 26, 2019</span></span>

<span data-ttu-id="68059-310">バージョン 2.0.77</span><span class="sxs-lookup"><span data-stu-id="68059-310">Version 2.0.77</span></span>

### <a name="acr"></a><span data-ttu-id="68059-311">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-311">ACR</span></span>

* <span data-ttu-id="68059-312">acr task create/update からパラメーター `--branch` が非推奨になりました</span><span class="sxs-lookup"><span data-stu-id="68059-312">Deprecated parameter `--branch` from acr task create/update</span></span>

### <a name="azure-red-hat-openshift"></a><span data-ttu-id="68059-313">Azure Red Hat OpenShift</span><span class="sxs-lookup"><span data-stu-id="68059-313">Azure Red Hat OpenShift</span></span>

* <span data-ttu-id="68059-314">監視を使用して Azure Red Hat Openshift クラスターを作成できるように、`--workspace-resource-id` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-314">Added `--workspace-resource-id` flag to allow creation of Azure Red Hat Openshift cluster with monitoring</span></span>
* <span data-ttu-id="68059-315">監視を使用して Azure Red Hat OpenShift クラスターを作成するために `monitor_profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-315">Added `monitor_profile` to create Azure Red Hat OpenShift cluster with monitoring</span></span>

### <a name="aks"></a><span data-ttu-id="68059-316">AKS</span><span class="sxs-lookup"><span data-stu-id="68059-316">AKS</span></span>

* <span data-ttu-id="68059-317">"az aks rotate-certs" を使用したクラスター証明書ローテーション操作のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-317">Added support cluster certificate rotation operation using "az aks rotate-certs".</span></span>

### <a name="appconfig"></a><span data-ttu-id="68059-318">AppConfig</span><span class="sxs-lookup"><span data-stu-id="68059-318">AppConfig</span></span>

* <span data-ttu-id="68059-319">`as az appconfig kv import` の区切り文字に ":" を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-319">Added support for using ":" for `as az appconfig kv import` separator</span></span>
* <span data-ttu-id="68059-320">null ラベルを含む複数のラベルを持つキー値の一覧表示に関する問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-320">Fixed issue for listing key values with multiple labels including null label.</span></span> 
* <span data-ttu-id="68059-321">管理プレーン SKD である azure-mgmt-appconfiguration を バージョン 0.3.0 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="68059-321">Updated management plane sdk, azure-mgmt-appconfiguration, to version 0.3.0.</span></span> 

### <a name="appservice"></a><span data-ttu-id="68059-322">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-322">AppService</span></span>

* <span data-ttu-id="68059-323">問題 #11100 を修正:サービス プランの作成時の az webapp up の AttributeError</span><span class="sxs-lookup"><span data-stu-id="68059-323">Fixed issue #11100: AttributeError for az webapp up when create service plan</span></span>
* <span data-ttu-id="68059-324">az webapp up:サポートされている言語のサイトに作成またはデプロイを強制します。既定値は使用されません。</span><span class="sxs-lookup"><span data-stu-id="68059-324">az webapp up: Forcing the creation or deployment to a site for supported languages, no defaults used.</span></span>
* <span data-ttu-id="68059-325">App Service Environment のサポートを追加しました: az appservice ase show | list | list-addresses | list-plans | create | update | delete</span><span class="sxs-lookup"><span data-stu-id="68059-325">Added support for App Service Environment: az appservice ase show | list | list-addresses | list-plans | create | update | delete</span></span>

### <a name="backup"></a><span data-ttu-id="68059-326">バックアップ</span><span class="sxs-lookup"><span data-stu-id="68059-326">Backup</span></span>

* <span data-ttu-id="68059-327">az backup policy list-associated-items の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-327">Fixed issue in az backup policy list-associated-items.</span></span> <span data-ttu-id="68059-328">省略可能な BackupManagementType パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-328">Added optional BackupManagementType parameter.</span></span>

### <a name="compute"></a><span data-ttu-id="68059-329">Compute</span><span class="sxs-lookup"><span data-stu-id="68059-329">Compute</span></span>

* <span data-ttu-id="68059-330">コンピューティング、ディスク、スナップショットの API バージョンを 2019-07-01 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="68059-330">Upgraded API version of compute, disks, snapshots to 2019-07-01</span></span>
* <span data-ttu-id="68059-331">vmss create: --orchestration-mode の改善</span><span class="sxs-lookup"><span data-stu-id="68059-331">vmss create: Improvement for --orchestration-mode</span></span>
* <span data-ttu-id="68059-332">sig image-definition create: --os-state を追加して、このイメージの下に作成された仮想マシンを "一般化" するか、または "特殊化" するかを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="68059-332">sig image-definition create: Added --os-state to allow specifying whether the virtual machines created under this image are 'Generalized' or 'Specialized'</span></span>
* <span data-ttu-id="68059-333">sig image-definition create: --hyper-v-generation を追加して、ハイパーバイザーの生成を指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="68059-333">sig image-definition create: Added --hyper-v-generation to allow specifying the hypervisor generation</span></span>
* <span data-ttu-id="68059-334">sig image-version create: --os-snapshot と --data-snapshots のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-334">sig image-version create: Added support --os-snapshot and --data-snapshots</span></span>
* <span data-ttu-id="68059-335">image create: --data-disk-caching を追加して、データ ディスクのキャッシュ設定を指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="68059-335">image create: Added --data-disk-caching to allow specifying caching setting of data disks</span></span>
* <span data-ttu-id="68059-336">Python Compute SDK を 10.0.0 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="68059-336">Upgraded Python Compute SDK to 10.0.0</span></span>
* <span data-ttu-id="68059-337">vm/vmss create: 'Priority' 列挙型プロパティに 'Spot' を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-337">vm/vmss create: Added 'Spot' to 'Priority' enum property</span></span>
* <span data-ttu-id="68059-338">[重大な変更] Swagger と Powershell のコマンドレットとの一貫性を維持するために、VM と VMSS の両方で '--max-billing' パラメーターを '--max-price' に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-338">[Breaking change] Renamed '--max-billing' parameter to '--max-price', for both VM and VMSS, to be consistent with Swagger and Powershell cmdlets</span></span>
* <span data-ttu-id="68059-339">vm monitor log show: リンクされた Log Analytics ワークスペースに対してログのクエリを実行するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-339">vm monitor log show: Added support for querying log over linked log analytics workspace.</span></span>

### <a name="iot"></a><span data-ttu-id="68059-340">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-340">IOT</span></span>

* <span data-ttu-id="68059-341">#2531 の修正: ハブの更新に便利な引数を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-341">Fix #2531: Added convenience arguments for hub update.</span></span>
* <span data-ttu-id="68059-342">#8323 の修正: ストレージ カスタム エンドポイントを作成するために不足しているパラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-342">Fix #8323: Added missing parameters to create storage custom endpoint.</span></span>
* <span data-ttu-id="68059-343">回帰バグの修正: 既定のストレージ エンドポイントをオーバーライドする変更を元に戻しました。</span><span class="sxs-lookup"><span data-stu-id="68059-343">Fix regression bug: Reverted the changes which overrides the default storage endpoint.</span></span>

### <a name="key-vault"></a><span data-ttu-id="68059-344">Key Vault</span><span class="sxs-lookup"><span data-stu-id="68059-344">Key Vault</span></span>

* <span data-ttu-id="68059-345">#11121 を修正しました: `az keyvault certificate list` を使用する場合、`--include-pending` を渡すときに `true` または `false` の値が必須ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="68059-345">Fixed #11121: When using `az keyvault certificate list`, passing `--include-pending` now doesn't require a value of `true` or `false`</span></span>

### <a name="netappfiles"></a><span data-ttu-id="68059-346">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="68059-346">NetAppFiles</span></span>

* <span data-ttu-id="68059-347">azure-mgmt-netapp を 0.7.0 にアップグレードしました。これには、今後のレプリケーション操作に関連した追加のボリューム プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="68059-347">Upgraded azure-mgmt-netapp to 0.7.0 which includes some additional volume properties associated with upcoming replication operations</span></span>

### <a name="network"></a><span data-ttu-id="68059-348">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-348">Network</span></span>

* <span data-ttu-id="68059-349">application-gateway waf-config: 非推奨になりました</span><span class="sxs-lookup"><span data-stu-id="68059-349">application-gateway waf-config: deprecated</span></span>
* <span data-ttu-id="68059-350">application-gateway waf-policy: 管理されているルール セットと除外ルールを管理するために、サブグループ managed-rules を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-350">application-gateway waf-policy: Added subgroup managed-rules to manage managed rule sets and exclusion rules</span></span>
* <span data-ttu-id="68059-351">application-gateway waf-policy: waf-policy のグローバル構成を管理するために、サブグループ policy-setting を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-351">application-gateway waf-policy: Added subgroup policy-setting to manage global configuration of a waf-policy</span></span>
* <span data-ttu-id="68059-352">[重大な変更] application-gateway waf-policy: subgroup rule を custom-rule に名前変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-352">[BREAKING CHANGE] application-gateway waf-policy: Renamed subgroup rule to custom-rule</span></span>
* <span data-ttu-id="68059-353">application-gateway http-listener: 作成時の --firewall-policy を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-353">application-gateway http-listener: Added --firewall-policy when create</span></span>
* <span data-ttu-id="68059-354">application-gateway url-path-map rule: 作成時の --firewall-policy を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-354">application-gateway url-path-map rule: Added --firewall-policy when create</span></span>

### <a name="packaging"></a><span data-ttu-id="68059-355">梱包</span><span class="sxs-lookup"><span data-stu-id="68059-355">Packaging</span></span>

* <span data-ttu-id="68059-356">az ラッパーを Python で書き直しました</span><span class="sxs-lookup"><span data-stu-id="68059-356">Rewrote the az wrapper in Python</span></span>
* <span data-ttu-id="68059-357">Python 3.8 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-357">Added support for Python 3.8</span></span>
* <span data-ttu-id="68059-358">RPM パッケージで Python 3 に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-358">Changed to Python 3 for RPM package</span></span>

### <a name="profile"></a><span data-ttu-id="68059-359">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-359">Profile</span></span>

* <span data-ttu-id="68059-360">Microsoft アカウントで `az login -u {} -p {}` を実行するときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-360">Polished error when running `az login -u {} -p {}` with Microsoft account</span></span>
* <span data-ttu-id="68059-361">自己署名ルート証明書使用してプロキシの背後で `az login` を実行するときの `SSLError` を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-361">Polished `SSLError` when running `az login` behind a proxy with self-signed root certificate</span></span>
* <span data-ttu-id="68059-362">#10578 を修正: Windows または WSL で同時に複数のインスタンスを起動すると `az login` がハングする</span><span class="sxs-lookup"><span data-stu-id="68059-362">Fixed #10578: `az login` hangs when more than one instances are launched at the same time on Windows or WSL</span></span>
* <span data-ttu-id="68059-363">#11059 を修正: テナントにサブスクリプションがあると `az login --allow-no-subscriptions` が失敗する</span><span class="sxs-lookup"><span data-stu-id="68059-363">Fixed #11059: `az login --allow-no-subscriptions` fails if there are subscriptions in the tenant</span></span>
* <span data-ttu-id="68059-364">#11238 を修正: サブスクリプションの名前を変更した後、MSI を使用してログインすると、同じサブスクリプションが 2 回表示される</span><span class="sxs-lookup"><span data-stu-id="68059-364">Fixed #11238: After renaming a subscription, logging in with MSI will result in the same subscription appearing twice</span></span>

### <a name="rbac"></a><span data-ttu-id="68059-365">RBAC</span><span class="sxs-lookup"><span data-stu-id="68059-365">RBAC</span></span>

* <span data-ttu-id="68059-366">#10996 を修正: `--password` が指定されていないときの `az ad user update` での `--force-change-password-next-login` のエラーを改善</span><span class="sxs-lookup"><span data-stu-id="68059-366">Fixed #10996: Polish error for `--force-change-password-next-login` in `az ad user update` when `--password` is not specified</span></span>

### <a name="redis"></a><span data-ttu-id="68059-367">Redis</span><span class="sxs-lookup"><span data-stu-id="68059-367">Redis</span></span>

* <span data-ttu-id="68059-368">#2902 を修正: Basic SKU キャッシュの更新中、メモリ構成を設定しない</span><span class="sxs-lookup"><span data-stu-id="68059-368">Fixed #2902: Avoid setting memory configs while updating Basic SKU cache</span></span>

### <a name="reservations"></a><span data-ttu-id="68059-369">Reservations</span><span class="sxs-lookup"><span data-stu-id="68059-369">Reservations</span></span>

* <span data-ttu-id="68059-370">SDK バージョンを 0.6.0 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="68059-370">Upgraded SDK Version to 0.6.0</span></span>
* <span data-ttu-id="68059-371">Gat-Gatalogs を呼び出した後の billingplan の詳細情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-371">Added billingplan details info after calling Get-Gatalogs</span></span>
* <span data-ttu-id="68059-372">予約の価格を計算するための新しいコマンド `az reservations reservation-order calculate` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-372">Added new command `az reservations reservation-order calculate` to calculate the price for a reservation</span></span>
* <span data-ttu-id="68059-373">新しい予約を購入するための新しいコマンド `az reservations reservation-order purchase` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-373">Added new command `az reservations reservation-order purchase` to purchase a new reservation</span></span>

### <a name="rest"></a><span data-ttu-id="68059-374">REST</span><span class="sxs-lookup"><span data-stu-id="68059-374">Rest</span></span>
* <span data-ttu-id="68059-375">`az rest` を GA に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-375">Changed `az rest` to GA</span></span>

### <a name="sql"></a><span data-ttu-id="68059-376">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-376">SQL</span></span>

* <span data-ttu-id="68059-377">azure-mgmt-sql をバージョン 0.15.0 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="68059-377">Updated azure-mgmt-sql to version 0.15.0.</span></span>

### <a name="storage"></a><span data-ttu-id="68059-378">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-378">Storage</span></span>

* <span data-ttu-id="68059-379">storage account create: Blob service でのファイルシステムのセマンティクスをサポートするために、--enable-hierarchical-namespace を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-379">storage account create: Added --enable-hierarchical-namespace to support filesystem semantics in blob service.</span></span>
* <span data-ttu-id="68059-380">エラー メッセージから関連性のない例外を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-380">Removed unrelated exception from error message</span></span>
* <span data-ttu-id="68059-381">"この操作を実行するのに必要なアクセス許可がありません" という誤ったエラー メッセージが</span><span class="sxs-lookup"><span data-stu-id="68059-381">Fixed issues with incorrect error message "You do not have the required permissions needed to perform this operation."</span></span> <span data-ttu-id="68059-382">ネットワーク ルールまたは AuthenticationFailed によってブロックされた場合に表示される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-382">when blocked by network rules or AuthenticationFailed.</span></span>

## <a name="november-4-2019"></a><span data-ttu-id="68059-383">2019 年 11 月 4 日</span><span class="sxs-lookup"><span data-stu-id="68059-383">November 4, 2019</span></span>

<span data-ttu-id="68059-384">バージョン 2.0.76</span><span class="sxs-lookup"><span data-stu-id="68059-384">Version 2.0.76</span></span>

### <a name="acr"></a><span data-ttu-id="68059-385">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-385">ACR</span></span>

* <span data-ttu-id="68059-386">コマンド `az acr pack build` にプレビュー パラメーター `--pack-image-tag` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-386">Added a preview parameter `--pack-image-tag` to command `az acr pack build`.</span></span>
* <span data-ttu-id="68059-387">レジストリ作成時の監査を有効にするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-387">Added support for enabling auditing on creating a registry</span></span>
* <span data-ttu-id="68059-388">レジストリ スコープが設定された RBAC のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-388">Added support for Repository-scoped RBAC</span></span>

### <a name="aks"></a><span data-ttu-id="68059-389">AKS</span><span class="sxs-lookup"><span data-stu-id="68059-389">AKS</span></span>

* <span data-ttu-id="68059-390">`az aks create` コマンドに `--enable-cluster-autoscaler`、`--min-count`、および `--max-count` を追加しました。これにより、ノード プールのクラスター オートスケーラーが有効になります。</span><span class="sxs-lookup"><span data-stu-id="68059-390">Added `--enable-cluster-autoscaler`, `--min-count` and `--max-count` to the `az aks create` command, which enables cluster autoscaler for the node pool.</span></span>
* <span data-ttu-id="68059-391">上記のフラグに加えて、`--update-cluster-autoscaler` および `--disable-cluster-autoscaler` を `az aks update` コマンドに追加し、クラスター オートスケーラーを更新できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="68059-391">Added the above flags as well as `--update-cluster-autoscaler` and `--disable-cluster-autoscaler` to the `az aks update` command, allowing updates to cluster autoscaler.</span></span>

### <a name="appconfig"></a><span data-ttu-id="68059-392">AppConfig</span><span class="sxs-lookup"><span data-stu-id="68059-392">AppConfig</span></span>

* <span data-ttu-id="68059-393">App Configuration に格納される機能フラグを管理するために、appconfig feature コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-393">Added appconfig feature command group to manage feature flags stored in an App Configuration.</span></span>
* <span data-ttu-id="68059-394">ファイルに対する appconfig kv export コマンドの軽微なバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-394">Fixed minor bug for appconfig kv export to file command.</span></span> <span data-ttu-id="68059-395">エクスポート中に宛先ファイルの内容を読み取らないようにしました。</span><span class="sxs-lookup"><span data-stu-id="68059-395">Stop reading dest file contents during export.</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-396">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-396">AppService</span></span>

* <span data-ttu-id="68059-397">`az appservice plan create`:appservice plan create に "persitescaling" を設定するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-397">`az appservice plan create`: Added support to set 'persitescaling' on appservice plan create.</span></span>
* <span data-ttu-id="68059-398">webapp config ssl bind 操作がリソースから既存のタグを削除する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-398">Fixed an issue where webapp config ssl bind operation was removing existing tags from the resource</span></span>
* <span data-ttu-id="68059-399">関数アプリのデプロイ時にリモート ビルド アクションをサポートするために、`az functionapp deployment source config-zip` に `--build-remote` フラグを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-399">Added `--build-remote` flag for `az functionapp deployment source config-zip` to support remote build action during function app deployment.</span></span>
* <span data-ttu-id="68059-400">Windows 向けの関数アプリの既定のノードバージョンを 10 に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-400">Changed default node version on function apps to ~10 for Windows</span></span>
* <span data-ttu-id="68059-401">`az functionapp create` に `--runtime-version` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-401">Added `--runtime-version` property to `az functionapp create`</span></span>

### <a name="arm"></a><span data-ttu-id="68059-402">ARM</span><span class="sxs-lookup"><span data-stu-id="68059-402">ARM</span></span>

* <span data-ttu-id="68059-403">`az deployment/group deployment validate`:デプロイ時に、json テンプレートで複数行とコメントをサポートするために `--handle-extended-json-format` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-403">`az deployment/group deployment validate`: Added `--handle-extended-json-format` parameter to support multiline and comments in json template when deployment.</span></span>
* <span data-ttu-id="68059-404">azure-mgmt-resource を 2019-07-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="68059-404">Bumped azure-mgmt-resource to 2019-07-01</span></span>

### <a name="backup"></a><span data-ttu-id="68059-405">バックアップ</span><span class="sxs-lookup"><span data-stu-id="68059-405">Backup</span></span>

* <span data-ttu-id="68059-406">AzureFiles のバックアップ サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-406">Added AzureFiles backup support</span></span>

### <a name="compute"></a><span data-ttu-id="68059-407">Compute</span><span class="sxs-lookup"><span data-stu-id="68059-407">Compute</span></span>

* <span data-ttu-id="68059-408">`az vm create`:高速ネットワークと既存の NIC を一緒に指定した場合の警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-408">`az vm create`: Added warning when specifying accelerated networking and an existing NIC together.</span></span>
* <span data-ttu-id="68059-409">`az vm create`:仮想マシンを割り当てる必要がある既存の仮想マシン スケール セットを指定するための `--vmss` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-409">`az vm create`: Added `--vmss` to specify an existing virtual machine scale set that the virtual machine should be assigned to.</span></span>
* <span data-ttu-id="68059-410">`az vm/vmss create`:イメージ エイリアス ファイルのローカル コピーを追加し、制限付きネットワーク環境でそれにアクセスできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="68059-410">`az vm/vmss create`: Added a local copy of image alias file so that it can be accessed in a restricted network environment.</span></span>
* <span data-ttu-id="68059-411">`az vmss create`:スケール セットによる仮想マシンの管理方法を指定するための `--orchestration-mode` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-411">`az vmss create`: Added `--orchestration-mode` to specify how virtual machines are managed by the scale set.</span></span>
* <span data-ttu-id="68059-412">`az vm/vmss update`:Ultra SSD 設定を更新できるように `--ultra-ssd-enabled` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-412">`az vm/vmss update`: Added `--ultra-ssd-enabled` to allow updating ultra SSD setting.</span></span>
* <span data-ttu-id="68059-413">[破壊的変更] `az vm extension set`:ユーザーが `--ids` を使用して、VM に拡張機能を設定できないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-413">[BREAKING CHANGE] `az vm extension set`: Fixed bug where users could not set an extension on a VM with `--ids`.</span></span>
* <span data-ttu-id="68059-414">Azure Marketplace イメージの使用条件を管理するための新しいコマンド `az vm image terms accept/cancel/show` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-414">Added new commands `az vm image terms accept/cancel/show` to manage Azure Marketplace image terms.</span></span>
* <span data-ttu-id="68059-415">VMAccessForLinux をバージョン 1.5 に更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-415">Updated VMAccessForLinux to version 1.5</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-416">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-416">CosmosDB</span></span>

* <span data-ttu-id="68059-417">[破壊的変更] `az sql container create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-417">[BREAKING CHANGE] `az sql container create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="68059-418">[破壊的変更] `az gremlin graph create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-418">[BREAKING CHANGE] `az gremlin graph create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="68059-419">`az sql container create`:`--unique-key-policy` および `--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-419">`az sql container create`: Added `--unique-key-policy` and `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="68059-420">`az sql container create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-420">`az sql container create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="68059-421">`gremlin graph create`:`--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-421">`gremlin graph create`: Added `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="68059-422">`gremlin graph create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-422">`gremlin graph create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="68059-423">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-423">Fixed typo in help message</span></span>
* <span data-ttu-id="68059-424">データベース:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-424">database: Added deprecation infomation</span></span>
* <span data-ttu-id="68059-425">コレクション:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-425">collection: Added deprecation infomation</span></span>

### <a name="iot"></a><span data-ttu-id="68059-426">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-426">IoT</span></span>

* <span data-ttu-id="68059-427">新しいルーティング ソースの種類を追加しました: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="68059-427">Added new routing source type: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="68059-428">`az iot hub create` の不十分な機能を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-428">Fixed missing features in `az iot hub create`</span></span>

### <a name="key-vault"></a><span data-ttu-id="68059-429">Key Vault</span><span class="sxs-lookup"><span data-stu-id="68059-429">Key Vault</span></span>

* <span data-ttu-id="68059-430">証明書ファイルが存在しない場合の予期しないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-430">Fixed an unexpected error when certificate file does not exist</span></span>
* <span data-ttu-id="68059-431">`az keyvault recover/purge` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-431">Fixed `az keyvault recover/purge` not working</span></span>

### <a name="netappfiles"></a><span data-ttu-id="68059-432">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="68059-432">NetAppFiles</span></span>

* <span data-ttu-id="68059-433">API バージョン 2019-07-01 を使用するために azure-mgmt-netapp を 0.6.0 にアップグレードしました。</span><span class="sxs-lookup"><span data-stu-id="68059-433">Upgraded azure-mgmt-netapp to 0.6.0 to use API version 2019-07-01.</span></span> <span data-ttu-id="68059-434">この新しい API バージョンには以下の変更内容が含まれます。</span><span class="sxs-lookup"><span data-stu-id="68059-434">This new API version includes:</span></span>

    - <span data-ttu-id="68059-435">ボリューム作成の `--protocol-types` が "NFSv4" ではなく "NFSv 4.1" を受け入れるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-435">Volume creation `--protocol-types` accepts now "NFSv4.1" not "NFSv4"</span></span>
    - <span data-ttu-id="68059-436">ボリューム エクスポート ポリシー プロパティの名前が "nfsv4" ではなく "nfsv41" に変更されました</span><span class="sxs-lookup"><span data-stu-id="68059-436">Volume export policy property now named 'nfsv41' not 'nfsv4'</span></span>
    - <span data-ttu-id="68059-437">ボリュームの `--creation-token` の名前が `--file-path` に変更されました</span><span class="sxs-lookup"><span data-stu-id="68059-437">Volume `--creation-token` renamed to `--file-path`</span></span>
    - <span data-ttu-id="68059-438">スナップショット作成日の名前が単に "created" に変更されました</span><span class="sxs-lookup"><span data-stu-id="68059-438">Snapshot creation date now named just 'created'</span></span>

### <a name="network"></a><span data-ttu-id="68059-439">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-439">Network</span></span>

* <span data-ttu-id="68059-440">`az network private-dns link vnet create/update`:テナント間の仮想ネットワーク リンクがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="68059-440">`az network private-dns link vnet create/update`: Support cross-tenant virtual network linking.</span></span>
* <span data-ttu-id="68059-441">[破壊的変更] `az network vnet subnet list`:`--resource-group` と `--vnet-name` を必須に変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-441">[BREAKING CHANGE] `az network vnet subnet list`: Changed `--resource-group` and `--vnet-name` to be required now.</span></span>
* <span data-ttu-id="68059-442">`az network public-ip prefix create`:作成時に IP アドレスのバージョン (IPv4、IPv6) を指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-442">`az network public-ip prefix create`: Added support to specify IP address version (IPv4, IPv6) when creation</span></span>
* <span data-ttu-id="68059-443">azure-mgmt-network を 7.0.0 に、api-version を 2019-09-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="68059-443">Bumped azure-mgmt-network to 7.0.0 and api-version to 2019-09-01</span></span>
* <span data-ttu-id="68059-444">`az network vrouter`:新しいサービスの仮想ルーターと仮想ルーター ピアリングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-444">`az network vrouter`: Added support for new service virtual router and virtual router peering</span></span>
* <span data-ttu-id="68059-445">`az network express-route gateway connection`:`--internet-security` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-445">`az network express-route gateway connection`: Added support for `--internet-security`</span></span>

### <a name="profile"></a><span data-ttu-id="68059-446">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-446">Profile</span></span>

* <span data-ttu-id="68059-447">`az account get-access-token --resource-type ms-graph` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-447">Fixed `az account get-access-token --resource-type ms-graph` not working</span></span>
* <span data-ttu-id="68059-448">`az login` からの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-448">Removed warning from `az login`</span></span>

### <a name="rbac"></a><span data-ttu-id="68059-449">RBAC</span><span class="sxs-lookup"><span data-stu-id="68059-449">RBAC</span></span>

* <span data-ttu-id="68059-450">`az ad app update --id {} --display-name {}` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-450">Fixed `az ad app update --id {} --display-name {}` doesn't work</span></span>

### <a name="servicefabric"></a><span data-ttu-id="68059-451">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68059-451">ServiceFabric</span></span>

* <span data-ttu-id="68059-452">`az sf cluster create`:Service Fabric の Linux と Windows の template.json コンピューティング vmss を標準からマネージド ディスクに変更することによって問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-452">`az sf cluster create`: Fixed an issue by modifying service fabric linux and windows template.json compute vmss from standard to managed disks</span></span>

### <a name="sql"></a><span data-ttu-id="68059-453">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-453">SQL</span></span>

* <span data-ttu-id="68059-454">次の新しい SQL Database オファリングの CRUD 操作をサポートするために、`--compute-model`、`--auto-pause-delay`、および `--min-capacity` パラメーターを追加しました:サーバーレス コンピューティング モデル。</span><span class="sxs-lookup"><span data-stu-id="68059-454">Added `--compute-model`, `--auto-pause-delay`, and `--min-capacity` parameters to support CRUD operations for new SQL Database offering: Serverless compute model.</span></span>

### <a name="storage"></a><span data-ttu-id="68059-455">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-455">Storage</span></span>

* <span data-ttu-id="68059-456">`az storage account create/update`:Azure Files Active Directory Domain Services 認証をサポートするために、--enable-files-adds パラメーターと Azure Active Directory プロパティ引数グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-456">`az storage account create/update`: Added --enable-files-adds parameter and Azure Active Directory Properties Argument group to support Azure Files Active Directory Domain Service Authentication</span></span>
* <span data-ttu-id="68059-457">ストレージ アカウントの Kerberos キーの一覧表示または再生成をサポートするために、`az storage account keys list/renew` を拡張しました。</span><span class="sxs-lookup"><span data-stu-id="68059-457">Expanded `az storage account keys list/renew` to support listing or regenerating Kerberos keys of storage account.</span></span>

## <a name="october-15-2019"></a><span data-ttu-id="68059-458">2019 年 10 月 15 日</span><span class="sxs-lookup"><span data-stu-id="68059-458">October 15, 2019</span></span>

<span data-ttu-id="68059-459">バージョン 2.0.75</span><span class="sxs-lookup"><span data-stu-id="68059-459">Version 2.0.75</span></span>

### <a name="aks"></a><span data-ttu-id="68059-460">AKS</span><span class="sxs-lookup"><span data-stu-id="68059-460">AKS</span></span>

* <span data-ttu-id="68059-461">Kubernetes のバージョンでサポートされている場合、`--load-balancer-sku` の既定値を `standard` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-461">Changed `--load-balancer-sku` default value to `standard` if supported by the kubernetes version</span></span>
* <span data-ttu-id="68059-462">Kubernetes のバージョンでサポートされている場合、`--vm-set-type` の既定値を `virtualmachinescalesets` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-462">Changed `--vm-set-type` default value to `virtualmachinescalesets` if supported by the kubernetes version</span></span>

### <a name="ams"></a><span data-ttu-id="68059-463">AMS</span><span class="sxs-lookup"><span data-stu-id="68059-463">AMS</span></span>

* <span data-ttu-id="68059-464">[重大な変更]`job start` の名前を `job create` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-464">[BREAKING CHANGE] Changed the name of `job start` to `job create`</span></span>
* <span data-ttu-id="68059-465">[重大な変更]`content-key-policy create` の `--ask` パラメーターが UTF8 ではなく 32 文字の 16 進文字列を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-465">[BREAKING CHANGE] Changed the `--ask` parameter of `content-key-policy create` to use a 32-character hex string instead of UTF8</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-466">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-466">AppService</span></span>

* <span data-ttu-id="68059-467">コマンド `webapp config access-restriction show|set|add|remove` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-467">Added commands `webapp config access-restriction show|set|add|remove`</span></span>
* <span data-ttu-id="68059-468">より優れたエラー処理を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-468">Added better error handling to `webapp up`</span></span>
* <span data-ttu-id="68059-469">`Isolated` SKU のサポートを `appservice plan update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-469">Added support for `Isolated` SKU to `appservice plan update`</span></span>

### <a name="arm"></a><span data-ttu-id="68059-470">ARM</span><span class="sxs-lookup"><span data-stu-id="68059-470">ARM</span></span>

* <span data-ttu-id="68059-471">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `deployment create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-471">Added `--handle-extended-json-format` parameter `deployment create` to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="68059-472">Compute</span><span class="sxs-lookup"><span data-stu-id="68059-472">Compute</span></span>

* <span data-ttu-id="68059-473">`--enable-agent` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-473">Added `--enable-agent` parameter to `vm create`</span></span>
* <span data-ttu-id="68059-474">ゾーンを使用するときに標準のパブリック IP SKU を自動的に使用するように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-474">Changed `vm create` to use standard public IP SKU automatically when using zones</span></span>
* <span data-ttu-id="68059-475">VM の有効なコンピューター名が指定されていない場合に自動的に作成されるように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-475">Changed `vm create` to automatically create a valid computer name for a VM if none is provided</span></span>
* <span data-ttu-id="68059-476">VMSS 内の仮想マシンのカスタム コンピューター名プレフィックスをサポートするために `--computer-name-prefix` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-476">Added `--computer-name-prefix` parameter to `vmss create` to support custom computer name prefix of virtual machines in the VMSS</span></span>
* <span data-ttu-id="68059-477">ログ分析ワークスペースを自動的に有効にする `--workspace` パラメーターを `vm create` に追加します</span><span class="sxs-lookup"><span data-stu-id="68059-477">Add `--workspace` parameter to `vm create` to enable log analytics workspace automatically</span></span>
* <span data-ttu-id="68059-478">ギャラリーの API バージョンが 2019-07-01 に更新されました</span><span class="sxs-lookup"><span data-stu-id="68059-478">Updated galleries API version to 2019-07-01</span></span>

### <a name="core"></a><span data-ttu-id="68059-479">コア</span><span class="sxs-lookup"><span data-stu-id="68059-479">Core</span></span>

* <span data-ttu-id="68059-480">汎用の update コマンドで `--set` パラメーターの構文チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-480">Added syntax check for `--set` parameter in generic update command</span></span>

### <a name="iot"></a><span data-ttu-id="68059-481">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-481">IoT</span></span>

* <span data-ttu-id="68059-482">`iot hub show` で "リソースが見つかりません" のエラーが誤って発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-482">Fixed an issue where `iot hub show` would incorrectly error with "resource not found"</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-483">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-483">Monitor</span></span>

* <span data-ttu-id="68059-484">CRUD のサポートを `monitor log-analytics workspace` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-484">Added support for CRUD to `monitor log-analytics workspace`</span></span>

### <a name="network"></a><span data-ttu-id="68059-485">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-485">Network</span></span>

* <span data-ttu-id="68059-486">クロステナントの仮想リンクのサポートを `network private-dns link vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-486">Added support for cross-tenant virtual linking to `network private-dns link vnet [create|update]`</span></span>
* <span data-ttu-id="68059-487">[重大な変更]`network vnet subnet list` で `--resource-group` および `--vnet-name` パラメーターが必須に変更になりました</span><span class="sxs-lookup"><span data-stu-id="68059-487">[BREAKING CHANGE] Changed `network vnet subnet list` to require `--resource-group` and `--vnet-name` parameters</span></span>

### <a name="sql"></a><span data-ttu-id="68059-488">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-488">SQL</span></span>

* <span data-ttu-id="68059-489">マネージ インスタンスの AAD 管理者の設定をサポートするコマンドを `sql mi ad-admin` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-489">Added commands to `sql mi ad-admin` that support setting an AAD administrator on managed instances</span></span>

### <a name="storage"></a><span data-ttu-id="68059-490">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-490">Storage</span></span>

* <span data-ttu-id="68059-491">サービス間のコピー中にアクセス層を保持する `--preserve-s2s-access-tier` パラメーターを `storage copy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-491">Added `--preserve-s2s-access-tier` parameter `storage copy` to preserve access tier during service to service copy</span></span>
* <span data-ttu-id="68059-492">ストレージ アカウントで大容量ファイルの共有をサポートするために `--enable-large-file-share` パラメーターを `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-492">Added `--enable-large-file-share` parameter to `storage account [create|update]` to support large file shares for storage account</span></span>

## <a name="september-24-2019"></a><span data-ttu-id="68059-493">2019 年 9 月 24 日</span><span class="sxs-lookup"><span data-stu-id="68059-493">September 24, 2019</span></span>

<span data-ttu-id="68059-494">バージョン 2.0.74</span><span class="sxs-lookup"><span data-stu-id="68059-494">Version 2.0.74</span></span>

### <a name="acr"></a><span data-ttu-id="68059-495">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-495">ACR</span></span>

* <span data-ttu-id="68059-496">必須の `--type` パラメーターを `acr config retention update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-496">Added a required `--type` parameter to `acr config retention update`</span></span>
* <span data-ttu-id="68059-497">[破壊的変更] `acr config` コマンド グループでパラメーター `--name -n` の名前が `--registry -r ` に変更されました</span><span class="sxs-lookup"><span data-stu-id="68059-497">[BREAKING CHNAGE] Renamed parameter `--name -n` changed to `--registry -r ` for `acr config` command group</span></span>

### <a name="aks"></a><span data-ttu-id="68059-498">AKS</span><span class="sxs-lookup"><span data-stu-id="68059-498">AKS</span></span>

* <span data-ttu-id="68059-499">`--load-balancer-sku` パラメーターを `aks create` コマンドに追加しました。これにより、SLB を使用する AKS クラスターを作成できます</span><span class="sxs-lookup"><span data-stu-id="68059-499">Added `--load-balancer-sku` parameter to `aks create` command, which allows for creating AKS cluster with SLB</span></span>
* <span data-ttu-id="68059-500">`--load-balancer-managed-outbound-ip-count`、`--load-balancer-outbound-ips`、`--load-balancer-outbound-ip-prefixes` パラメーターを `aks [create|update]` コマンドに追加しました。これにより、SLB を使用する AKS クラスターのロード バランサー プロファイルを更新できます</span><span class="sxs-lookup"><span data-stu-id="68059-500">Added `--load-balancer-managed-outbound-ip-count`, `--load-balancer-outbound-ips` and `--load-balancer-outbound-ip-prefixes` parameters to `aks [create|update]` commands, which allow for updating load balancer profile of an AKS cluster with SLB</span></span>
* <span data-ttu-id="68059-501">`--vm-set-type` パラメーターを `aks create` コマンドに追加しました。これにより、AKS クラスターの VM の種類 (vmas または vmss) を指定できます</span><span class="sxs-lookup"><span data-stu-id="68059-501">Added `--vm-set-type` parameter to `aks create` command, which allows to specify vm types of an AKS Cluster (vmas or vmss)</span></span>

### <a name="arm"></a><span data-ttu-id="68059-502">ARM</span><span class="sxs-lookup"><span data-stu-id="68059-502">ARM</span></span>

* <span data-ttu-id="68059-503">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `group deployment create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-503">Added `--handle-extended-json-format` parameter to `group deployment create` command to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="68059-504">Compute</span><span class="sxs-lookup"><span data-stu-id="68059-504">Compute</span></span>

* <span data-ttu-id="68059-505">終了のスケジュール化されたイベントを構成しやすくするために `--terminate-notification-time` パラメーターを `vmss [create|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-505">Added `--terminate-notification-time` parameter to `vmss [create|update]` commands to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="68059-506">終了のスケジュール化されたイベントを構成しやすくするために `--enable-terminate-notification` パラメーターを `vmss update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-506">Added `--enable-terminate-notification` parameter to `vmss update` command to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="68059-507">`--priority,` `--eviction-policy,` `--max-billing` パラメーターを `[vm|vmss] create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-507">Added `--priority,` `--eviction-policy,` `--max-billing` parameters to `[vm|vmss] create` commands</span></span>
* <span data-ttu-id="68059-508">`disk create` を変更し、ディスク アップロードの正確なサイズを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="68059-508">Changed `disk create` to allow specifying the exact size of the disk upload</span></span>
* <span data-ttu-id="68059-509">マネージド ディスクの増分スナップショットのサポートを `snapshot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-509">Added support for incremental snapshots for managed disks to `snapshot create`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="68059-510">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-510">Cosmos DB</span></span>

* <span data-ttu-id="68059-511">キー、読み取り専用キー、または接続文字列を表示する `--type <key-type>` パラメーターを `cosmosdb keys list` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-511">Added `--type <key-type>` parameter to `cosmosdb keys list` command to show key, read only keys or connection strings</span></span>
* <span data-ttu-id="68059-512">`cosmosdb keys regenerate` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-512">Added `cosmosdb keys regenerate` command</span></span>
* <span data-ttu-id="68059-513">[非推奨]`cosmosdb list-connection-strings`、`cosmosdb regenerate-key`、`cosmosdb list-read-only-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-513">[DEPRECATED] Deprecated `cosmosdb list-connection-strings`, `cosmosdb regenerate-key` and `cosmosdb list-read-only-keys` commands</span></span>

### <a name="eventgrid"></a><span data-ttu-id="68059-514">EventGrid</span><span class="sxs-lookup"><span data-stu-id="68059-514">EventGrid</span></span>

* <span data-ttu-id="68059-515">正しいパラメーターを参照するようにエンドポイントのヘルプ テキストを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-515">Fixed the endpoint help text to refer to the right parameter</span></span>

### <a name="key-vault"></a><span data-ttu-id="68059-516">Key Vault</span><span class="sxs-lookup"><span data-stu-id="68059-516">Key Vault</span></span>

* <span data-ttu-id="68059-517">テナントを使用してログインすると (`login -t`)、`keyvault create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-517">Fixed issue where logging in with a tenant (`login -t`) could cause `keyvault create` to fail</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-518">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-518">Monitor</span></span>

* <span data-ttu-id="68059-519">`monitor metrics alert create` の `--condition` 引数で `:` 文字を使用できないという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-519">Fixed issue where `:` character was not allowed in `--condition` argument to `monitor metrics alert create`</span></span>

### <a name="policy"></a><span data-ttu-id="68059-520">ポリシー</span><span class="sxs-lookup"><span data-stu-id="68059-520">Policy</span></span>

* <span data-ttu-id="68059-521">Policy API バージョン 2019-06-01 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-521">Added support for Policy API version 2019-06-01</span></span>
* <span data-ttu-id="68059-522">`policy assignment create` コマンドに `--enforcement-mode` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-522">Added `--enforcement-mode` parameter to `policy assignment create` command</span></span>

### <a name="storage"></a><span data-ttu-id="68059-523">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-523">Storage</span></span>

* <span data-ttu-id="68059-524">`az storage copy` コマンドに `--blob-type` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-524">Added `--blob-type` parameter to `az storage copy` command</span></span>

## <a name="september-10-2019"></a><span data-ttu-id="68059-525">2019 年 9 月 10 日</span><span class="sxs-lookup"><span data-stu-id="68059-525">September 10, 2019</span></span>

### <a name="acr"></a><span data-ttu-id="68059-526">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-526">ACR</span></span>

* <span data-ttu-id="68059-527">アイテム保持ポリシーを構成するためのコマンド グループ `acr config retention` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-527">Added command group `acr config retention` to configure retention policy</span></span>

### <a name="aks"></a><span data-ttu-id="68059-528">AKS</span><span class="sxs-lookup"><span data-stu-id="68059-528">AKS</span></span>

* <span data-ttu-id="68059-529">次のコマンドを使用した ACR 統合のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="68059-529">Added support for ACR integration with the following commands:</span></span>
  * <span data-ttu-id="68059-530">AKS クラスターに ACR をアタッチするための `--attach-acr` パラメーターを `aks [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-530">Added `--attach-acr` parameter to `aks [create|update]` to attach an ACR to an AKS cluster</span></span>
  * <span data-ttu-id="68059-531">AKS クラスターから ACR をデタッチするための `--detach-acr` パラメーターを `aks update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-531">Added `--detach-acr` parameter to `aks update` to detach the ACR from an AKS cluster</span></span>

### <a name="arm"></a><span data-ttu-id="68059-532">ARM</span><span class="sxs-lookup"><span data-stu-id="68059-532">ARM</span></span>

* <span data-ttu-id="68059-533">API バージョン 2019-05-10 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-533">Updated to use API version 2019-05-10</span></span>

### <a name="batch"></a><span data-ttu-id="68059-534">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-534">Batch</span></span>

* <span data-ttu-id="68059-535">`batch pool create` の `--json-file` に新しい JSON 構成設定を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-535">Added new JSON configuration settings to `--json-file` for `batch pool create`:</span></span>
  * <span data-ttu-id="68059-536">ファイル システム マウント用の `MountConfigurations` を追加しました (詳細については https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="68059-536">Added `MountConfigurations` for file system mounts (see https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body for details)</span></span>
  * <span data-ttu-id="68059-537">プール上のパブリック IP 用に、`NetworkConfiguration` にオプションのプロパティ `publicIPs` を追加しました (詳細については https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="68059-537">Added optional property `publicIPs` on `NetworkConfiguration` for public IPs on pools (see https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body for details)</span></span>
* <span data-ttu-id="68059-538">共有イメージ ギャラリーのサポートを `--image` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-538">Added support for shared image galleries to `--image`</span></span>
* <span data-ttu-id="68059-539">[重大な変更]`batch pool create` の `--start-task-wait-for-success` の既定値を `true` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-539">[BREAKING CHANGE] Changed default value of `--start-task-wait-for-success` on `batch pool create` to be `true`</span></span>
* <span data-ttu-id="68059-540">[重大な変更]`AutoUserSpecification` の `Scope` の既定値が常に Pool になるように変更しました (以前は Windows ノードでは `Task`、Linux ノードでは `Pool` でした)</span><span class="sxs-lookup"><span data-stu-id="68059-540">[BREAKING CHANGE] Changed default value for `Scope` on `AutoUserSpecification` to always be Pool (was `Task` on Windows nodes, `Pool` on Linux nodes)</span></span>
  * <span data-ttu-id="68059-541">この引数は、`--json-file` を使用して JSON 構成からのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="68059-541">This argument can only be set from a JSON configuration with `--json-file`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="68059-542">HDInsight</span><span class="sxs-lookup"><span data-stu-id="68059-542">HDInsight</span></span>

* <span data-ttu-id="68059-543">GA リリース</span><span class="sxs-lookup"><span data-stu-id="68059-543">GA release</span></span>
* <span data-ttu-id="68059-544">[重大な変更]`az hdinsight resize` のパラメーター `--workernode-count/-c` が必須に変更されました。</span><span class="sxs-lookup"><span data-stu-id="68059-544">[BREAKING CHANGE] Changed parameter `--workernode-count/-c` of `az hdinsight resize` to be required.</span></span>

### <a name="key-vault"></a><span data-ttu-id="68059-545">Key Vault</span><span class="sxs-lookup"><span data-stu-id="68059-545">Key Vault</span></span>

* <span data-ttu-id="68059-546">ネットワーク ルールからサブネットを削除できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-546">Fixed issue where subnets couldn't be deleted from network rules</span></span>
* <span data-ttu-id="68059-547">重複したサブネットと IP アドレスをネットワーク ルールに追加できる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-547">Fixed issue where duplicated subnets and IP addresses could be added to network rules</span></span>

### <a name="network"></a><span data-ttu-id="68059-548">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-548">Network</span></span>

* <span data-ttu-id="68059-549">トラフィック分析間隔の値を設定する `--interval` パラメーターを `network watcher flow-log` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-549">Added `--interval` parameter to `network watcher flow-log` to set traffic analysis interval value</span></span>
* <span data-ttu-id="68059-550">ゲートウェイ ID を管理するための `network application-gateway identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-550">Added `network application-gateway identity` to manage gateway identity</span></span>
* <span data-ttu-id="68059-551">Key Vault ID を設定するためのサポートを `network application-gateway ssl-cert` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-551">Added support for setting Key Vault ID to `network application-gateway ssl-cert`</span></span>
* <span data-ttu-id="68059-552">`network express-route peering peer-connection [show|list]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-552">Added `network express-route peering peer-connection [show|list]`</span></span>

### <a name="policy"></a><span data-ttu-id="68059-553">ポリシー</span><span class="sxs-lookup"><span data-stu-id="68059-553">Policy</span></span>

* <span data-ttu-id="68059-554">API バージョン 2019-01-01 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-554">Updated to use API version 2019-01-01</span></span>

## <a name="august-27-2019"></a><span data-ttu-id="68059-555">2019 年 8 月 27 日</span><span class="sxs-lookup"><span data-stu-id="68059-555">August 27, 2019</span></span>

<span data-ttu-id="68059-556">バージョン 2.0.72</span><span class="sxs-lookup"><span data-stu-id="68059-556">Version 2.0.72</span></span>

### <a name="acr"></a><span data-ttu-id="68059-557">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-557">ACR</span></span>

* <span data-ttu-id="68059-558">[重大な変更]`classic` SKU のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-558">[BREAKING CHANGE] Removed support for the `classic` SKU</span></span>

### <a name="api-management"></a><span data-ttu-id="68059-559">API Management</span><span class="sxs-lookup"><span data-stu-id="68059-559">API Management</span></span>

* <span data-ttu-id="68059-560">[プレビュー] `apim` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-560">[PREVIEW] Added `apim` command group</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-561">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-561">AppService</span></span>

* <span data-ttu-id="68059-562">スロットを指定したときの `webapp webjob continuous start` コマンドに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-562">Fixed issue with `webapp webjob continuous start` command when specifying a slot</span></span>
* <span data-ttu-id="68059-563">`env` フォルダーを検出してデプロイに使用されているファイルから削除するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-563">Changed `webapp up` to detect `env` folder and remove it from the file used for deployment</span></span>

### <a name="keyvault"></a><span data-ttu-id="68059-564">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68059-564">Keyvault</span></span>

* <span data-ttu-id="68059-565">`--expires` 引数を無視する `keyvault secret set` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-565">Fixed a bug in `keyvault secret set` that igored the `--expires` argument</span></span>

### <a name="network"></a><span data-ttu-id="68059-566">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-566">Network</span></span>

* <span data-ttu-id="68059-567">`--private-ip-address-version` 引数に IPv6 アドレスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-567">Added support for IPv6 addresses to `--private-ip-address-version` arguments</span></span>
* <span data-ttu-id="68059-568">プライベート エンドポイントの管理用に新しいコマンド `network private-endpoint [create|update|list-types]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-568">Added new commands `network private-endpoint [create|update|list-types]` for private endpoint management</span></span>
* <span data-ttu-id="68059-569">コマンド グループ `network private-link-service` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-569">Added command group `network private-link-service`</span></span>
* <span data-ttu-id="68059-570">`--private-endpoint-network-policies` 引数と `--private-link-service-network-policies` 引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-570">Added `--private-endpoint-network-policies` and `--private-link-service-network-policies` arguments to `network vnet subnet update`</span></span>

### <a name="rbac"></a><span data-ttu-id="68059-571">RBAC</span><span class="sxs-lookup"><span data-stu-id="68059-571">RBAC</span></span>

* <span data-ttu-id="68059-572">ホームページが更新されない `ad app update --homepage` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-572">Fixed issue with `ad app update --homepage` where homepage would not be updated</span></span>

### <a name="servicefabric"></a><span data-ttu-id="68059-573">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68059-573">ServiceFabric</span></span>

* <span data-ttu-id="68059-574">キー コンテナーの大文字と小文字が混在する名前のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-574">Added support for mixed-case Key Vault names</span></span>
* <span data-ttu-id="68059-575">Key Vault で証明書を使用したときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-575">Fixed issue when using certificates in Key Vault</span></span>
* <span data-ttu-id="68059-576">PFX 証明書ファイルの使用に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-576">Fixed issue with using PFX certificate files</span></span>
* <span data-ttu-id="68059-577">Key Vault リソースグループが指定されていなかったときの `sf cluster certificate add` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-577">Fixed issue with `sf cluster certificate add` when Key Vault resource group wasn't specified</span></span>
* <span data-ttu-id="68059-578">`sf cluster set` が動作しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-578">Fixed issue with `sf cluster set` not working</span></span>

### <a name="signalr"></a><span data-ttu-id="68059-579">SignalR</span><span class="sxs-lookup"><span data-stu-id="68059-579">SignalR</span></span>

* <span data-ttu-id="68059-580">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-580">Added new commands:</span></span>
  * <span data-ttu-id="68059-581">`signalr cors`:SignalR CORS の管理</span><span class="sxs-lookup"><span data-stu-id="68059-581">`signalr cors`: Manage SignalR CORS</span></span>
  * <span data-ttu-id="68059-582">`signalr restart`:SignalR Service の再起動</span><span class="sxs-lookup"><span data-stu-id="68059-582">`signalr restart`: Restart a SignalR service</span></span>
  * <span data-ttu-id="68059-583">`signalr update`:SignalR Service の更新</span><span class="sxs-lookup"><span data-stu-id="68059-583">`signalr update`: Update a SignalR service</span></span>
* <span data-ttu-id="68059-584">`--service-mode` 引数を `signalr create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-584">Added `--service-mode` argument to `signalr create`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-585">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-585">Storage</span></span>

* <span data-ttu-id="68059-586">`storage account revoke-delegation-keys` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-586">Added `storage account revoke-delegation-keys` command</span></span>

## <a name="august-13-2019"></a><span data-ttu-id="68059-587">2019 年 8 月 13 日</span><span class="sxs-lookup"><span data-stu-id="68059-587">August 13, 2019</span></span>

<span data-ttu-id="68059-588">バージョン 2.0.71</span><span class="sxs-lookup"><span data-stu-id="68059-588">Version 2.0.71</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-589">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-589">AppService</span></span>

* <span data-ttu-id="68059-590">`webapp webjob continuous` コマンドがスロットで失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-590">Fixed issue where `webapp webjob continuous` commands were failing for slots</span></span>

### <a name="botservice"></a><span data-ttu-id="68059-591">BotService</span><span class="sxs-lookup"><span data-stu-id="68059-591">BotService</span></span>

* <span data-ttu-id="68059-592">[重大な変更] v3 SDK ボットの作成のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-592">[BREAKING CHANGE] Removed support for creating v3 SDK bots</span></span>

### <a name="cognitiveservices"></a><span data-ttu-id="68059-593">CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="68059-593">CognitiveServices</span></span>

* <span data-ttu-id="68059-594">`cognitiveservices account network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-594">Added `cognitiveservices account network-rule` commands</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="68059-595">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-595">Cosmos DB</span></span>

* <span data-ttu-id="68059-596">複数の書き込み場所を更新するときの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-596">Removed warning when updating multiple write locations</span></span>
* <span data-ttu-id="68059-597">CosmosDB SQL、MongoDB、Cassandra、Gremlin、およびテーブル リソースとリソースのスループットのための CRUD コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-597">Added CRUD commands for CosmosDB SQL, MongoDB, Cassandra, Gremlin and Table resources and resource's throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="68059-598">HDInsight</span><span class="sxs-lookup"><span data-stu-id="68059-598">HDInsight</span></span>

<span data-ttu-id="68059-599">このリリースには、多数の破壊的変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="68059-599">This release contains a large number of breaking changes.</span></span>

* <span data-ttu-id="68059-600">[重大な変更]`hdinsight create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-600">[BREAKING CHANGE] Renamed parameters for `hdinsight create`:</span></span>
  * <span data-ttu-id="68059-601">`--storage-default-container` から `--storage-container` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-601">Renamed `--storage-default-container` to `--storage-container`</span></span>
  * <span data-ttu-id="68059-602">`--storage-default-filesystem` から `--storage-filesystem` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-602">Renamed `--storage-default-filesystem` to `--storage-filesystem`</span></span>
* <span data-ttu-id="68059-603">[重大な変更]`application create` の `--name` 引数が、クラスター名の代わりにアプリケーション名を表すように変更されました</span><span class="sxs-lookup"><span data-stu-id="68059-603">[BREAKING CHANGE] Changed the `--name` argument of `application create` to represent the application name instead of the cluster name</span></span>
* <span data-ttu-id="68059-604">`--cluster-name` 引数が `application create` に追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="68059-604">Added `--cluster-name` argument to `application create` to replace old `--name` functionality</span></span>
* <span data-ttu-id="68059-605">[重大な変更]`application create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-605">[BREAKING CHANGE] Renamed parameters for `application create`:</span></span>
  * <span data-ttu-id="68059-606">`--application-type` から `--type` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-606">Renamed `--application-type` to `--type`</span></span>
  * <span data-ttu-id="68059-607">`--marketplace-identifier` から `--marketplace-id` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-607">Renamed `--marketplace-identifier` to `--marketplace-id`</span></span>
  * <span data-ttu-id="68059-608">`--https-endpoint-access-mode` から `--access-mode` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-608">Renamed `--https-endpoint-access-mode` to `--access-mode`</span></span>
  * <span data-ttu-id="68059-609">`--https-endpoint-destination-port` の名前を `--destination-port` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-609">Renamed  `--https-endpoint-destination-port` to `--destination-port`</span></span>
* <span data-ttu-id="68059-610">[重大な変更]`application create` のパラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-610">[BREAKING CHANGE] Removed parameters for `application create`:</span></span>
  * `--https-endpoint-location`
  * `--https-endpoint-public-port`
  * `--ssh-endpoint-destination-port`
  * `--ssh-endpoint-location`
  * `--ssh-endpoint-public-port`
* <span data-ttu-id="68059-611">[破壊的変更] `hdinsight resize`の `--target-instance-count` の名前を `--workernode-count` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-611">[BREAKING CHNAGE] Renamed `--target-instance-count` to `--workernode-count` for `hdinsight resize`</span></span>
* <span data-ttu-id="68059-612">[重大な変更]`hdinsight script-action` グループのすべてのコマンドが、スクリプト アクションの名前として `--name` パラメーターを使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="68059-612">[BREAKING CHANGE] Changed all commands in the `hdinsight script-action` group to use the `--name` parameter as the name of the script action.</span></span>
* <span data-ttu-id="68059-613">`--cluster-name` 引数がすべての `hdinsight script-action` コマンドに追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="68059-613">Added `--cluster-name` argument to all `hdinsight script-action` commands to replace old `--name` functionality</span></span>
* <span data-ttu-id="68059-614">[重大な変更] すべての `hdinsight script-action` コマンドで `--script-execution-id` の名前を `--execution-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-614">[BREAKING CHANGE] Renamed `--script-execution-id` to `--execution-id` for all `hdinsight script-action` commands</span></span>
* <span data-ttu-id="68059-615">[重大な変更] 名前を `hdinsight script-action show` から `hdinsight script-action show-execution-details` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-615">[BREAKING CHANGE] Renamed `hdinsight script-action show` to `hdinsight script-action show-execution-details`</span></span>
* <span data-ttu-id="68059-616">[破壊的変更] `hdinsight script-action execute --roles` に対するパラメーターを、コンマ区切りではなくスペース区切りにしました</span><span class="sxs-lookup"><span data-stu-id="68059-616">[BREAKING CHNAGE] Changed parameters to `hdinsight script-action execute --roles` to be space-separated instead of comma-separated</span></span>
* <span data-ttu-id="68059-617">[重大な変更]`hdinsight script-action list`の `--persisted` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-617">[BREAKING CHANGE] Removed the `--persisted` parameter of `hdinsight script-action list`</span></span>
* <span data-ttu-id="68059-618">ローカル JSON ファイルへのパスまたは JSON 文字列を受け入れるように `hdinsight create --cluster-configurations` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-618">Changed the `hdinsight create --cluster-configurations` parameter to accept a path to a local JSON file or a JSON string</span></span>
* <span data-ttu-id="68059-619">`hdinsight script-action list-execution-history` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-619">Added command `hdinsight script-action list-execution-history`</span></span>
* <span data-ttu-id="68059-620">Log Analytics ワークスペース ID またはワークスペース名を受け入れるように `hdinsight monitor enable --workspace` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-620">Changed `hdinsight monitor enable --workspace` to accept a Log Analytics workspace ID or workspace name</span></span>
* <span data-ttu-id="68059-621">`hdinsight monitor enable --primary-key` 引数を追加しました。これは、ワークスペース ID がパラメーターとして指定されている場合に必要です</span><span class="sxs-lookup"><span data-stu-id="68059-621">Added the `hdinsight monitor enable --primary-key` argument, which is needed if a workspace ID is provided as the parameter</span></span>
* <span data-ttu-id="68059-622">例をさらに追加し、ヘルプ メッセージの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-622">Added more examples and updated descriptions for help messages</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-623">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-623">Interactive</span></span>

* <span data-ttu-id="68059-624">読み込みエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-624">Fixed a loading error</span></span>

### <a name="kubernetes"></a><span data-ttu-id="68059-625">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="68059-625">Kubernetes</span></span>

* <span data-ttu-id="68059-626">ダッシュボードのコンテナー ポートで `https` が使用されている場合に `https` を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-626">Changed to use `https` if dashboard container port is using `https`</span></span>

### <a name="network"></a><span data-ttu-id="68059-627">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-627">Network</span></span>

* <span data-ttu-id="68059-628">`--yes` 引数を `network dns record-set cname delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-628">Added `--yes` argument `network dns record-set cname delete`</span></span>

### <a name="profile"></a><span data-ttu-id="68059-629">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-629">Profile</span></span>

* <span data-ttu-id="68059-630">リソースのアクセス トークンを取得するための `account get-access-token` に `--resource-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-630">Added `--resource-type` argument to `account get-access-token` to get resource access tokens</span></span>

### <a name="servicefabric"></a><span data-ttu-id="68059-631">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68059-631">ServiceFabric</span></span>

* <span data-ttu-id="68059-632">sf cluster create でサポートされているすべての OS バージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-632">Added all supported os version for sf cluster create</span></span>
* <span data-ttu-id="68059-633">プライマリ証明書の検証のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-633">Fixed primary certificate validation bug</span></span>

### <a name="storage"></a><span data-ttu-id="68059-634">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-634">Storage</span></span>

* <span data-ttu-id="68059-635">`storage copy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-635">Added command `storage copy`</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="68059-636">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="68059-636">July 30, 2019</span></span>

<span data-ttu-id="68059-637">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="68059-637">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="68059-638">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-638">ACR</span></span>

* <span data-ttu-id="68059-639">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-639">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="68059-640">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-640">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-641">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-641">Appservice</span></span>

* <span data-ttu-id="68059-642">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-642">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="68059-643">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-643">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="68059-644">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-644">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="68059-645">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-645">Network</span></span>

* <span data-ttu-id="68059-646">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="68059-646">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="68059-647">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-647">Fixes #9604.</span></span> <span data-ttu-id="68059-648">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-648">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="68059-649">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="68059-649">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="68059-650">RBAC</span><span class="sxs-lookup"><span data-stu-id="68059-650">RBAC</span></span>

* <span data-ttu-id="68059-651">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-651">Added `user update` command</span></span>
* <span data-ttu-id="68059-652">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-652">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="68059-653">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="68059-653">Use replacement argument `--id`</span></span>
* <span data-ttu-id="68059-654">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-654">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="68059-655">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-655">SQL</span></span>

* <span data-ttu-id="68059-656">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-656">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="68059-657">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-657">Storage</span></span>

* <span data-ttu-id="68059-658">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-658">Added `storage remove` command</span></span>
* <span data-ttu-id="68059-659">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-659">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="68059-660">VM</span><span class="sxs-lookup"><span data-stu-id="68059-660">VM</span></span>

* <span data-ttu-id="68059-661">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-661">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="68059-662">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-662">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="68059-663">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-663">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="68059-664">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-664">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="68059-665">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-665">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="68059-666">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="68059-666">July 16, 2019</span></span>

<span data-ttu-id="68059-667">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="68059-667">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-668">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-668">Appservice</span></span>

* <span data-ttu-id="68059-669">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="68059-669">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="68059-670">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-670">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="68059-671">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-671">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="68059-672">コア</span><span class="sxs-lookup"><span data-stu-id="68059-672">Core</span></span>

* <span data-ttu-id="68059-673">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-673">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="68059-674">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-674">Batch</span></span>

* <span data-ttu-id="68059-675">[重大な変更]`batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="68059-675">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="68059-676">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-676">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="68059-677">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-677">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="68059-678">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-678">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="68059-679">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="68059-679">Eventhubs</span></span>

* <span data-ttu-id="68059-680">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-680">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-681">RDBMS</span><span class="sxs-lookup"><span data-stu-id="68059-681">RDBMS</span></span>

* <span data-ttu-id="68059-682">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-682">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="68059-683">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-683">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="68059-684">リレー</span><span class="sxs-lookup"><span data-stu-id="68059-684">Relay</span></span>

* <span data-ttu-id="68059-685">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="68059-685">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="68059-686">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-686">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="68059-687">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="68059-687">Servicebus</span></span>

* <span data-ttu-id="68059-688">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-688">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="68059-689">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-689">Storage</span></span>

* <span data-ttu-id="68059-690">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="68059-690">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="68059-691">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="68059-691">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="68059-692">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="68059-692">July 2, 2019</span></span>

<span data-ttu-id="68059-693">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="68059-693">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="68059-694">コア</span><span class="sxs-lookup"><span data-stu-id="68059-694">Core</span></span>

* <span data-ttu-id="68059-695">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="68059-695">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="68059-696">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="68059-696">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="68059-697">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="68059-697">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="68059-698">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-698">ACR</span></span>

* <span data-ttu-id="68059-699">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-699">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-700">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-700">Appservice</span></span>

* <span data-ttu-id="68059-701">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-701">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="68059-702">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-702">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="68059-703">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="68059-703">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="68059-704">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-704">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="68059-705">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-705">Cosmos DB</span></span>

* <span data-ttu-id="68059-706">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-706">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="68059-707">DLS</span><span class="sxs-lookup"><span data-stu-id="68059-707">DLS</span></span>

* <span data-ttu-id="68059-708">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="68059-708">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="68059-709">フィードバック</span><span class="sxs-lookup"><span data-stu-id="68059-709">Feedback</span></span>

* <span data-ttu-id="68059-710">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-710">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="68059-711">HDInsight</span><span class="sxs-lookup"><span data-stu-id="68059-711">HDInsight</span></span>

* <span data-ttu-id="68059-712">[重大な変更]`oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-712">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="68059-713">[重大な変更]`--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="68059-713">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="68059-714">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-714">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="68059-715">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-715">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="68059-716">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-716">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="68059-717">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-717">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="68059-718">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-718">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="68059-719">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="68059-719">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="68059-720">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-720">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="68059-721">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="68059-721">Managed Services</span></span>

* <span data-ttu-id="68059-722">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="68059-722">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="68059-723">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-723">Profile</span></span>
* <span data-ttu-id="68059-724">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="68059-724">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="68059-725">RBAC</span><span class="sxs-lookup"><span data-stu-id="68059-725">RBAC</span></span>

* <span data-ttu-id="68059-726">[重大な変更]`create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-726">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="68059-727">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-727">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="68059-728">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-728">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="68059-729">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-729">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-730">RDBMS</span><span class="sxs-lookup"><span data-stu-id="68059-730">RDBMS</span></span>

* <span data-ttu-id="68059-731">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-731">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="68059-732">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-732">SQL</span></span>

* <span data-ttu-id="68059-733">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="68059-733">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-734">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-734">Storage</span></span>

* <span data-ttu-id="68059-735">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-735">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="68059-736">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-736">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="68059-737">VM</span><span class="sxs-lookup"><span data-stu-id="68059-737">VM</span></span>

* <span data-ttu-id="68059-738">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-738">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="68059-739">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-739">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="68059-740">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="68059-740">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="68059-741">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-741">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="68059-742">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="68059-742">June 18, 2019</span></span>

<span data-ttu-id="68059-743">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="68059-743">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="68059-744">コア</span><span class="sxs-lookup"><span data-stu-id="68059-744">Core</span></span>

<span data-ttu-id="68059-745">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="68059-745">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="68059-746">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="68059-746">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="68059-747">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="68059-747">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="68059-748">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="68059-748">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="68059-749">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="68059-749">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="68059-750">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="68059-750">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="68059-751">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="68059-751">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="68059-752">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-752">ACR</span></span>
* <span data-ttu-id="68059-753">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-753">Added 'acr check-health' command</span></span>
* <span data-ttu-id="68059-754">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-754">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="68059-755">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-755">ACS</span></span>
* <span data-ttu-id="68059-756">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="68059-756">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="68059-757">AMS</span><span class="sxs-lookup"><span data-stu-id="68059-757">AMS</span></span>
* <span data-ttu-id="68059-758">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-758">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-759">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-759">AppService</span></span>
* <span data-ttu-id="68059-760">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-760">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="68059-761">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-761">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="68059-762">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-762">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="68059-763">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-763">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="68059-764">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-764">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="68059-765">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-765">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="68059-766">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-766">Batch</span></span>
* <span data-ttu-id="68059-767">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-767">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="68059-768">BatchAI</span><span class="sxs-lookup"><span data-stu-id="68059-768">BatchAI</span></span>
* <span data-ttu-id="68059-769">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="68059-769">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="68059-770">BotService</span><span class="sxs-lookup"><span data-stu-id="68059-770">BotService</span></span>
* <span data-ttu-id="68059-771">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-771">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-772">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-772">CosmosDB</span></span>
* <span data-ttu-id="68059-773">[非推奨]`cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-773">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="68059-774">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="68059-774">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="68059-775">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-775">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="68059-776">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-776">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="68059-777">EventGrid</span><span class="sxs-lookup"><span data-stu-id="68059-777">EventGrid</span></span>
* <span data-ttu-id="68059-778">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-778">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="68059-779">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-779">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="68059-780">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-780">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="68059-781">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-781">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="68059-782">[重大な変更]`eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-782">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="68059-783">HDInsight</span><span class="sxs-lookup"><span data-stu-id="68059-783">HDInsight</span></span>
* <span data-ttu-id="68059-784">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-784">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="68059-785">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-785">IoT</span></span>
* <span data-ttu-id="68059-786">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-786">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="68059-787">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-787">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="68059-788">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-788">Network</span></span>
* <span data-ttu-id="68059-789">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-789">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="68059-790">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-790">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="68059-791">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-791">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="68059-792">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-792">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="68059-793">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-793">Resource</span></span>
* <span data-ttu-id="68059-794">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-794">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="68059-795">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-795">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="68059-796">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="68059-796">ServiceBus</span></span>
* <span data-ttu-id="68059-797">`servicebus topic create --max-size` での問題 [#9319](https://github.com/azure/azure-cli/issues/9319) を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-797">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="68059-798">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-798">SQL</span></span>
* <span data-ttu-id="68059-799">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="68059-799">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="68059-800">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-800">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="68059-801">SQLVm</span><span class="sxs-lookup"><span data-stu-id="68059-801">SQLVm</span></span>
* <span data-ttu-id="68059-802">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-802">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="68059-803">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-803">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="68059-804">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-804">Storage</span></span>
* <span data-ttu-id="68059-805">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-805">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="68059-806">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-806">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="68059-807">VM</span><span class="sxs-lookup"><span data-stu-id="68059-807">VM</span></span>
* <span data-ttu-id="68059-808">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-808">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="68059-809">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="68059-809">June 4, 2019</span></span>

<span data-ttu-id="68059-810">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="68059-810">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="68059-811">コア</span><span class="sxs-lookup"><span data-stu-id="68059-811">Core</span></span>
* <span data-ttu-id="68059-812">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-812">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="68059-813">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-813">ACR</span></span>
* <span data-ttu-id="68059-814">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-814">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="68059-815">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-815">ACS</span></span>
* <span data-ttu-id="68059-816">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-816">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="68059-817">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="68059-817">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="68059-818">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-818">Batch</span></span>
* <span data-ttu-id="68059-819">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-819">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="68059-820">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-820">IoT</span></span>
* <span data-ttu-id="68059-821">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-821">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="68059-822">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-822">Network</span></span>
* <span data-ttu-id="68059-823">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-823">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="68059-824">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-824">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="68059-825">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-825">Resource</span></span>
* <span data-ttu-id="68059-826">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-826">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="68059-827">Role</span><span class="sxs-lookup"><span data-stu-id="68059-827">Role</span></span>
* <span data-ttu-id="68059-828">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="68059-828">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="68059-829">Compute</span><span class="sxs-lookup"><span data-stu-id="68059-829">Compute</span></span>
* <span data-ttu-id="68059-830">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-830">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="68059-831">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="68059-831">May 21, 2019</span></span>

<span data-ttu-id="68059-832">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="68059-832">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="68059-833">コア</span><span class="sxs-lookup"><span data-stu-id="68059-833">Core</span></span>
* <span data-ttu-id="68059-834">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-834">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="68059-835">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-835">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="68059-836">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-836">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="68059-837">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-837">ACR</span></span>
* <span data-ttu-id="68059-838">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-838">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="68059-839">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-839">ACS</span></span>
* <span data-ttu-id="68059-840">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-840">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-841">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-841">AppService</span></span>
* <span data-ttu-id="68059-842">[非推奨]`functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="68059-842">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="68059-843">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-843">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="68059-844">[重大な変更]`--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="68059-844">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="68059-845">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-845">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="68059-846">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-846">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="68059-847">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-847">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="68059-848">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-848">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="68059-849">BotService</span><span class="sxs-lookup"><span data-stu-id="68059-849">BotService</span></span>
* <span data-ttu-id="68059-850">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-850">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="68059-851">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-851">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="68059-852">従量課金</span><span class="sxs-lookup"><span data-stu-id="68059-852">Consumption</span></span>
* <span data-ttu-id="68059-853">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-853">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="68059-854">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-854">IoT</span></span>
* <span data-ttu-id="68059-855">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-855">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="68059-856">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-856">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="68059-858">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-858">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="68059-859">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-859">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-860">RDBMS</span><span class="sxs-lookup"><span data-stu-id="68059-860">RDBMS</span></span>
* <span data-ttu-id="68059-861">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-861">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="68059-862">RBAC</span><span class="sxs-lookup"><span data-stu-id="68059-862">RBAC</span></span>
* <span data-ttu-id="68059-863">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-863">Added support for management group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-864">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-864">Storage</span></span>
* <span data-ttu-id="68059-865">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="68059-865">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="68059-866">Compute</span><span class="sxs-lookup"><span data-stu-id="68059-866">Compute</span></span>
* <span data-ttu-id="68059-867">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-867">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="68059-868">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-868">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="68059-869">__注__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="68059-869">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="68059-870">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-870">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="68059-871">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="68059-871">May 6, 2019</span></span>

<span data-ttu-id="68059-872">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="68059-872">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="68059-873">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-873">ACS</span></span>
* <span data-ttu-id="68059-874">[重大な変更]`--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-874">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="68059-875">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-875">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="68059-876">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-876">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="68059-877">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-877">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-878">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-878">Appservice</span></span>
* <span data-ttu-id="68059-879">[非推奨]`functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-879">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="68059-880">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-880">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="68059-881">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="68059-881">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="68059-882">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-882">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="68059-883">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-883">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="68059-884">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-884">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="68059-885">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-885">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="68059-886">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-886">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="68059-887">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-887">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="68059-888">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-888">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="68059-889">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-889">Batch</span></span>
* <span data-ttu-id="68059-890">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-890">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="68059-891">Botservice</span><span class="sxs-lookup"><span data-stu-id="68059-891">Botservice</span></span>
* <span data-ttu-id="68059-892">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="68059-892">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="68059-893">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-893">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="68059-894">[重大な変更]`--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-894">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="68059-895">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="68059-895">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="68059-896">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-896">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="68059-897">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="68059-897">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="68059-898">[重大な変更]`bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-898">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="68059-899">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-899">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="68059-900">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-900">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="68059-901">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-901">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="68059-902">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-902">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="68059-903">[重大な変更]`Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-903">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="68059-904">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-904">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="68059-905">[重大な変更]`SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-905">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="68059-906">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="68059-906">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="68059-907">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-907">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="68059-908">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-908">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="68059-909">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-909">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="68059-910">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-910">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="68059-911">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-911">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="68059-912">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-912">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="68059-913">[構成]</span><span class="sxs-lookup"><span data-stu-id="68059-913">Configure</span></span>
* <span data-ttu-id="68059-914">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-914">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="68059-915">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="68059-915">Eventhubs</span></span>
* <span data-ttu-id="68059-916">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-916">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="68059-917">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-917">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="68059-918">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-918">Network</span></span>
* <span data-ttu-id="68059-919">[重大な変更]`vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="68059-919">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="68059-920">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="68059-920">Policy Insights</span></span>
* <span data-ttu-id="68059-921">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-921">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="68059-922">Role</span><span class="sxs-lookup"><span data-stu-id="68059-922">Role</span></span>
* <span data-ttu-id="68059-923">[非推奨]`create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="68059-923">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="68059-924">Service Bus</span><span class="sxs-lookup"><span data-stu-id="68059-924">Service Bus</span></span>
* <span data-ttu-id="68059-925">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-925">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="68059-926">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-926">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="68059-927">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-927">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="68059-928">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-928">SQL</span></span>
* <span data-ttu-id="68059-929">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-929">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="68059-930">VM</span><span class="sxs-lookup"><span data-stu-id="68059-930">VM</span></span>
* <span data-ttu-id="68059-931">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-931">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="68059-932">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-932">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="68059-933">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-933">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="68059-934">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-934">Added new `ppg` command group for managing Proximity Placement Groups</span></span>
* <span data-ttu-id="68059-935">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-935">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="68059-936">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-936">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="68059-937">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="68059-937">April 23, 2019</span></span>

<span data-ttu-id="68059-938">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="68059-938">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="68059-939">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-939">ACS</span></span>
* <span data-ttu-id="68059-940">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-940">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="68059-941">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-941">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="68059-942">AMS</span><span class="sxs-lookup"><span data-stu-id="68059-942">AMS</span></span>
* <span data-ttu-id="68059-943">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-943">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-944">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-944">AppService</span></span>
* <span data-ttu-id="68059-945">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-945">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="68059-946">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-946">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="68059-947">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-947">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="68059-948">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-948">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="68059-949">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-949">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="68059-950">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-950">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="68059-951">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-951">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="68059-952">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-952">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="68059-953">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-953">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="68059-954">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="68059-954">Deployment Manager</span></span>
* <span data-ttu-id="68059-955">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="68059-955">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="68059-956">ラボ</span><span class="sxs-lookup"><span data-stu-id="68059-956">Lab</span></span>
* <span data-ttu-id="68059-957">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-957">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="68059-958">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-958">Network</span></span>
* <span data-ttu-id="68059-959">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-959">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="68059-960">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-960">Resource</span></span>
* <span data-ttu-id="68059-961">[非推奨]`resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="68059-961">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="68059-962">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="68059-962">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="68059-963">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-963">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="68059-964">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-964">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="68059-965">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-965">SQL</span></span>
* <span data-ttu-id="68059-966">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-966">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="68059-967">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-967">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="68059-968">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-968">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="68059-969">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-969">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-970">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-970">Storage</span></span>
* <span data-ttu-id="68059-971">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-971">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="68059-972">VM</span><span class="sxs-lookup"><span data-stu-id="68059-972">VM</span></span>
* <span data-ttu-id="68059-973">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-973">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="68059-974">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-974">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="68059-975">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-975">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="68059-976">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="68059-976">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="68059-977">コア</span><span class="sxs-lookup"><span data-stu-id="68059-977">Core</span></span>
* <span data-ttu-id="68059-978">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-978">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="68059-979">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-979">ACR</span></span>
* <span data-ttu-id="68059-980">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-980">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="68059-981">AMS</span><span class="sxs-lookup"><span data-stu-id="68059-981">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="68059-984">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-984">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="68059-985">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-985">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-986">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-986">AppService</span></span>
* <span data-ttu-id="68059-987">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-987">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="68059-988">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-988">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="68059-989">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-989">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="68059-990">[重大な変更]`devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="68059-990">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="68059-991">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-991">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="68059-992">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-992">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="68059-993">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-993">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="68059-994">CDN</span><span class="sxs-lookup"><span data-stu-id="68059-994">CDN</span></span>
* <span data-ttu-id="68059-995">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-995">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="68059-996">フィードバック</span><span class="sxs-lookup"><span data-stu-id="68059-996">Feedback</span></span>
* <span data-ttu-id="68059-997">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-997">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="68059-998">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-998">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="68059-999">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-999">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-1000">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-1000">Monitor</span></span>
* <span data-ttu-id="68059-1001">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1001">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="68059-1002">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1002">Network</span></span>
* <span data-ttu-id="68059-1003">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1003">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="68059-1004">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1004">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="68059-1005">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1005">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="68059-1006">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1006">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="68059-1007">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="68059-1007">PrivateDNS</span></span>
* <span data-ttu-id="68059-1008">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1008">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="68059-1009">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-1009">Resource</span></span>
* <span data-ttu-id="68059-1010">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1010">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="68059-1011">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1011">Role</span></span>
* <span data-ttu-id="68059-1012">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1012">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="68059-1013">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1013">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="68059-1014">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-1014">SQL</span></span>
* <span data-ttu-id="68059-1015">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-1015">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1016">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1016">Storage</span></span>
* <span data-ttu-id="68059-1017">[重大な変更]`storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1017">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="68059-1018">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1018">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="68059-1019">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1019">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="68059-1020">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1020">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="68059-1021">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="68059-1021">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="68059-1022">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1022">Core</span></span>
* <span data-ttu-id="68059-1023">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1023">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="68059-1024">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1024">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="68059-1025">クラウド</span><span class="sxs-lookup"><span data-stu-id="68059-1025">Cloud</span></span>
* <span data-ttu-id="68059-1026">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1026">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1027">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1027">ACR</span></span>
* <span data-ttu-id="68059-1028">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1028">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="68059-1029">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1029">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="68059-1030">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1030">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="68059-1031">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1031">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1032">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1032">AppService</span></span>
* <span data-ttu-id="68059-1033">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1033">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="68059-1034">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1034">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="68059-1035">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="68059-1035">BOT Service</span></span>
* <span data-ttu-id="68059-1036">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1036">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="68059-1037">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1037">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="68059-1038">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1038">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="68059-1039">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1039">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="68059-1040">CDN</span><span class="sxs-lookup"><span data-stu-id="68059-1040">CDN</span></span>
* <span data-ttu-id="68059-1041">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1041">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="68059-1043">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="68059-1043">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="68059-1044">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1044">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-1045">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="68059-1045">Cosmosdb</span></span>
* <span data-ttu-id="68059-1046">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1046">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="68059-1047">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1047">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-1048">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-1048">Interactive</span></span>
* <span data-ttu-id="68059-1049">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1049">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-1050">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-1050">Monitor</span></span>
* <span data-ttu-id="68059-1051">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1051">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="68059-1052">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1052">Network</span></span>
* <span data-ttu-id="68059-1053">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1053">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="68059-1054">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-1054">Profile</span></span>
* <span data-ttu-id="68059-1055">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1055">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="68059-1056">Postgres</span><span class="sxs-lookup"><span data-stu-id="68059-1056">Postgres</span></span> 
* <span data-ttu-id="68059-1057">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1057">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="68059-1058">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="68059-1058">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="68059-1059">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-1059">Resource</span></span>
* <span data-ttu-id="68059-1060">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-1060">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="68059-1061">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1061">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="68059-1062">グラフ</span><span class="sxs-lookup"><span data-stu-id="68059-1062">Graph</span></span>
* <span data-ttu-id="68059-1063">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1063">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="68059-1064">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1064">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="68059-1065">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1065">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="68059-1066">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1066">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="68059-1067">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1067">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1068">storage</span><span class="sxs-lookup"><span data-stu-id="68059-1068">storage</span></span>
* <span data-ttu-id="68059-1069">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1069">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="68059-1070">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1070">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="68059-1071">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1071">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="68059-1072">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1072">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1073">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1073">VM</span></span>
* <span data-ttu-id="68059-1074">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1074">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="68059-1075">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="68059-1075">March 12, 2019</span></span>

<span data-ttu-id="68059-1076">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="68059-1076">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="68059-1077">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1077">Core</span></span>

* <span data-ttu-id="68059-1078">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1078">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1079">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1079">ACR</span></span>

* <span data-ttu-id="68059-1080">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1080">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1081">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1081">ACS</span></span>

* <span data-ttu-id="68059-1082">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1082">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="68059-1083">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1083">AppService</span></span>

* <span data-ttu-id="68059-1084">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1084">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="68059-1085">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1085">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="68059-1086">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1086">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="68059-1087">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1087">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="68059-1088">Botservice</span><span class="sxs-lookup"><span data-stu-id="68059-1088">Botservice</span></span>

* <span data-ttu-id="68059-1089">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1089">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="68059-1090">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1090">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="68059-1091">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1091">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="68059-1092">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1092">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="68059-1093">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-1093">Container</span></span>

* <span data-ttu-id="68059-1094">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1094">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="68059-1095">EventHub</span><span class="sxs-lookup"><span data-stu-id="68059-1095">EventHub</span></span>

* <span data-ttu-id="68059-1096">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1096">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="68059-1097">Find</span><span class="sxs-lookup"><span data-stu-id="68059-1097">Find</span></span>

* <span data-ttu-id="68059-1098">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="68059-1098">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="68059-1099">HDInsight</span><span class="sxs-lookup"><span data-stu-id="68059-1099">HDInsight</span></span>

* <span data-ttu-id="68059-1100">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1100">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="68059-1101">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1101">Network</span></span>

* <span data-ttu-id="68059-1102">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1102">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-1103">Rdbms</span><span class="sxs-lookup"><span data-stu-id="68059-1103">Rdbms</span></span>

* <span data-ttu-id="68059-1104">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="68059-1104">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="68059-1105">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1105">Role</span></span>

* <span data-ttu-id="68059-1106">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1106">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="68059-1107">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1107">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="68059-1108">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="68059-1108">Service Fabric</span></span>

* <span data-ttu-id="68059-1109">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1109">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="68059-1110">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="68059-1110">February 26, 2019</span></span>

<span data-ttu-id="68059-1111">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="68059-1111">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="68059-1112">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1112">Core</span></span>

* <span data-ttu-id="68059-1113">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1113">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1114">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1114">ACR</span></span>

* <span data-ttu-id="68059-1115">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1115">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="68059-1116">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1116">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1117">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1117">ACS</span></span>

* <span data-ttu-id="68059-1118">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1118">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1119">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1119">AppService</span></span>

* <span data-ttu-id="68059-1120">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1120">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="68059-1121">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-1121">Batch</span></span>
* <span data-ttu-id="68059-1122">[重大な変更]`batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1122">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="68059-1123">[重大な変更]`Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1123">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="68059-1124">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1124">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="68059-1125">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1125">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="68059-1126">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1126">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="68059-1127">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="68059-1127">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-1128">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-1128">CosmosDB</span></span>

* <span data-ttu-id="68059-1129">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1129">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="68059-1130">Kusto</span><span class="sxs-lookup"><span data-stu-id="68059-1130">Kusto</span></span>

* <span data-ttu-id="68059-1131">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1131">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="68059-1132">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1132">Network</span></span>

* <span data-ttu-id="68059-1133">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1133">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="68059-1134">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1134">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="68059-1135">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1135">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="68059-1136">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1136">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="68059-1137">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1137">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="68059-1138">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1138">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="68059-1139">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1139">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="68059-1140">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-1140">Resource</span></span>

* <span data-ttu-id="68059-1141">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1141">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="68059-1142">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1142">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="68059-1143">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1143">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="68059-1144">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1144">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="68059-1145">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1145">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="68059-1146">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1146">Role</span></span>

* <span data-ttu-id="68059-1147">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1147">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1148">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1148">VM</span></span>

* <span data-ttu-id="68059-1149">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1149">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="68059-1150">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="68059-1150">February 12, 2019</span></span>

<span data-ttu-id="68059-1151">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="68059-1151">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="68059-1152">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1152">Core</span></span>

* <span data-ttu-id="68059-1153">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1153">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="68059-1154">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1154">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1155">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1155">ACR</span></span>
* <span data-ttu-id="68059-1156">[重大な変更]`acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1156">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="68059-1157">[重大な変更]`acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1157">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1158">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1158">ACS</span></span>
* <span data-ttu-id="68059-1159">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1159">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="68059-1160">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1160">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="68059-1161">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1161">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="68059-1162">AMS</span><span class="sxs-lookup"><span data-stu-id="68059-1162">AMS</span></span>
* <span data-ttu-id="68059-1163">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1163">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="68059-1164">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1164">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1165">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-1165">Appservice</span></span>
* <span data-ttu-id="68059-1166">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1166">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="68059-1167">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-1167">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="68059-1168">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-1168">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="68059-1169">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1169">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="68059-1170">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1170">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="68059-1171">Botservice</span><span class="sxs-lookup"><span data-stu-id="68059-1171">Botservice</span></span>
* <span data-ttu-id="68059-1172">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-1172">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="68059-1173">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1173">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="68059-1174">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1174">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="68059-1175">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1175">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="68059-1176">[非推奨]`--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1176">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="68059-1177">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1177">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="68059-1178">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1178">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="68059-1179">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1179">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="68059-1180">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="68059-1180">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="68059-1181">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-1181">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="68059-1182">Key Vault</span><span class="sxs-lookup"><span data-stu-id="68059-1182">Key Vault</span></span>
* <span data-ttu-id="68059-1183">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1183">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-1184">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-1184">Monitor</span></span>
* <span data-ttu-id="68059-1185">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1185">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="68059-1186">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1186">Network</span></span>
* <span data-ttu-id="68059-1187">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1187">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="68059-1188">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1188">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="68059-1189">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1189">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="68059-1190">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1190">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="68059-1191">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="68059-1191">Policy Insights</span></span>
* <span data-ttu-id="68059-1192">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1192">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-1193">RDBMS</span><span class="sxs-lookup"><span data-stu-id="68059-1193">RDBMS</span></span>
* <span data-ttu-id="68059-1194">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-1194">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="68059-1195">Redis</span><span class="sxs-lookup"><span data-stu-id="68059-1195">Redis</span></span>
* <span data-ttu-id="68059-1196">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1196">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="68059-1197">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1197">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="68059-1198">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1198">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="68059-1199">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1199">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="68059-1200">[重大な変更]`redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1200">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="68059-1201">[重大な変更]`redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="68059-1201">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="68059-1202">[非推奨]`redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1202">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="68059-1203">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1203">Role</span></span>
* <span data-ttu-id="68059-1204">[重大な変更]`az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="68059-1204">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="68059-1205">SQL VM</span><span class="sxs-lookup"><span data-stu-id="68059-1205">SQL VM</span></span>
* <span data-ttu-id="68059-1206">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1206">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1207">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1207">VM</span></span>
* <span data-ttu-id="68059-1208">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1208">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="68059-1209">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1209">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="68059-1210">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1210">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="68059-1211">[重大な変更]`az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="68059-1211">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="68059-1212">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="68059-1212">January 31, 2019</span></span>

<span data-ttu-id="68059-1213">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="68059-1213">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="68059-1214">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1214">Core</span></span>

* <span data-ttu-id="68059-1215">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="68059-1215">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="68059-1216">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="68059-1216">January 28, 2019</span></span>

<span data-ttu-id="68059-1217">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="68059-1217">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1218">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1218">ACR</span></span>
* <span data-ttu-id="68059-1219">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1219">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1220">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1220">ACS</span></span>
* <span data-ttu-id="68059-1221">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1221">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="68059-1222">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1222">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="68059-1223">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1223">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="68059-1224">AMS</span><span class="sxs-lookup"><span data-stu-id="68059-1224">AMS</span></span>
* <span data-ttu-id="68059-1225">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1225">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="68059-1226">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1226">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1227">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-1227">Appservice</span></span>
* <span data-ttu-id="68059-1228">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1228">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="68059-1229">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1229">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="68059-1230">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1230">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="68059-1231">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-1231">Container</span></span>
* <span data-ttu-id="68059-1232">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1232">Added `container start` command</span></span>
* <span data-ttu-id="68059-1233">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1233">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="68059-1234">EventGrid</span><span class="sxs-lookup"><span data-stu-id="68059-1234">EventGrid</span></span>
* <span data-ttu-id="68059-1235">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1235">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="68059-1236">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1236">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="68059-1237">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1237">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="68059-1238">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1238">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="68059-1239">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="68059-1239">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="68059-1240">HDInsight</span><span class="sxs-lookup"><span data-stu-id="68059-1240">HDInsight</span></span>
* <span data-ttu-id="68059-1241">[重大な変更]`hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1241">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="68059-1242">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1242">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="68059-1243">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1243">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="68059-1244">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-1244">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="68059-1245">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1245">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="68059-1246">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1246">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="68059-1247">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-1247">IoT</span></span>
* <span data-ttu-id="68059-1248">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1248">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="68059-1249">Kusto</span><span class="sxs-lookup"><span data-stu-id="68059-1249">Kusto</span></span>
* <span data-ttu-id="68059-1250">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="68059-1250">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-1251">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-1251">Monitor</span></span>
* <span data-ttu-id="68059-1252">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1252">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="68059-1253">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-1253">Profile</span></span>
* <span data-ttu-id="68059-1254">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1254">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="68059-1255">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1255">Network</span></span>
* <span data-ttu-id="68059-1256">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1256">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="68059-1257">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1257">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="68059-1258">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-1258">Resource</span></span>
* <span data-ttu-id="68059-1259">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1259">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="68059-1260">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1260">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="68059-1261">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="68059-1261">SQL Virtual Machine</span></span>
* <span data-ttu-id="68059-1262">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="68059-1262">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1263">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1263">Storage</span></span>
* <span data-ttu-id="68059-1264">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1264">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="68059-1265">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="68059-1265">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1266">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1266">VM</span></span>
* <span data-ttu-id="68059-1267">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1267">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="68059-1268">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1268">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="68059-1269">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="68059-1269">January 15, 2019</span></span>

<span data-ttu-id="68059-1270">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="68059-1270">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1271">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1271">ACR</span></span>
* <span data-ttu-id="68059-1272">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1272">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="68059-1273">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1273">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="68059-1274">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1274">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="68059-1275">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1275">ACS</span></span>
* <span data-ttu-id="68059-1276">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1276">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1277">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-1277">Appservice</span></span>
* <span data-ttu-id="68059-1278">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1278">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="68059-1279">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1279">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="68059-1280">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1280">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="68059-1281">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1281">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="68059-1282">Botservice</span><span class="sxs-lookup"><span data-stu-id="68059-1282">Botservice</span></span>
* <span data-ttu-id="68059-1283">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1283">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="68059-1284">[構成]</span><span class="sxs-lookup"><span data-stu-id="68059-1284">Configure</span></span>
* <span data-ttu-id="68059-1285">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1285">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-1286">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-1286">CosmosDB</span></span>
* <span data-ttu-id="68059-1287">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1287">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="68059-1288">HDInsight</span><span class="sxs-lookup"><span data-stu-id="68059-1288">HDInsight</span></span>
* <span data-ttu-id="68059-1289">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1289">Added commands for managing applications</span></span>
* <span data-ttu-id="68059-1290">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1290">Added commands for managing script actions</span></span>
* <span data-ttu-id="68059-1291">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1291">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="68059-1292">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1292">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="68059-1293">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1293">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="68059-1294">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1294">Network</span></span>
* <span data-ttu-id="68059-1295">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1295">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="68059-1296">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1296">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="68059-1297">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1297">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="68059-1298">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1298">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="68059-1299">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1299">Role</span></span>
* <span data-ttu-id="68059-1300">[非推奨]`create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="68059-1300">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="68059-1301">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="68059-1301">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="68059-1302">Security</span><span class="sxs-lookup"><span data-stu-id="68059-1302">Security</span></span>
* <span data-ttu-id="68059-1303">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-1303">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1304">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1304">Storage</span></span>
* <span data-ttu-id="68059-1305">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1305">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="68059-1306">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="68059-1306">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="68059-1307">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1307">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="68059-1308">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1308">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="68059-1309">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1309">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1310">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1310">VM</span></span>
* <span data-ttu-id="68059-1311">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1311">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="68059-1312">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1312">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="68059-1313">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1313">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="68059-1314">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1314">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="68059-1315">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1315">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="68059-1316">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1316">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="68059-1317">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="68059-1317">December 20, 2018</span></span>

<span data-ttu-id="68059-1318">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="68059-1318">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="68059-1319">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-1319">Appservice</span></span>
* <span data-ttu-id="68059-1320">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1320">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="68059-1321">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1321">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="68059-1322">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1322">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="68059-1323">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="68059-1323">IoTCentral</span></span>
* <span data-ttu-id="68059-1324">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1324">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="68059-1325">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1325">Role</span></span>
* <span data-ttu-id="68059-1326">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1326">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="68059-1327">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-1327">SQL</span></span>
* <span data-ttu-id="68059-1328">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1328">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1329">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1329">VM</span></span>
* <span data-ttu-id="68059-1330">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1330">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="68059-1331">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="68059-1331">December 18, 2018</span></span>

<span data-ttu-id="68059-1332">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="68059-1332">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="68059-1333">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1333">ACR</span></span>
* <span data-ttu-id="68059-1334">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1334">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="68059-1335">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="68059-1335">Condensed the table layout for task list</span></span>
* <span data-ttu-id="68059-1336">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1336">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1337">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1337">ACS</span></span>
* <span data-ttu-id="68059-1338">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1338">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="68059-1339">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1339">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="68059-1340">[非推奨]`az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="68059-1340">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="68059-1341">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="68059-1341">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="68059-1342">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1342">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="68059-1343">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1343">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1344">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-1344">Appservice</span></span>
* <span data-ttu-id="68059-1345">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1345">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="68059-1346">Botservice</span><span class="sxs-lookup"><span data-stu-id="68059-1346">Botservice</span></span>
* <span data-ttu-id="68059-1347">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1347">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="68059-1348">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1348">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="68059-1349">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1349">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="68059-1350">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="68059-1350">Reduced Kudu network calls</span></span>
* <span data-ttu-id="68059-1351">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1351">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="68059-1352">従量課金</span><span class="sxs-lookup"><span data-stu-id="68059-1352">Consumption</span></span>
* <span data-ttu-id="68059-1353">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1353">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-1354">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-1354">CosmosDB</span></span>
* <span data-ttu-id="68059-1355">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1355">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="68059-1356">マップ</span><span class="sxs-lookup"><span data-stu-id="68059-1356">Maps</span></span>
* <span data-ttu-id="68059-1357">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1357">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="68059-1358">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1358">Network</span></span>
* <span data-ttu-id="68059-1359">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1359">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="68059-1360">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1360">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="68059-1361">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-1361">Resource</span></span>
* <span data-ttu-id="68059-1362">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1362">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="68059-1363">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1363">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1364">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1364">Storage</span></span>
*  <span data-ttu-id="68059-1365">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1365">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1366">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1366">VM</span></span>
* <span data-ttu-id="68059-1367">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1367">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="68059-1368">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="68059-1368">December 4, 2018</span></span>

<span data-ttu-id="68059-1369">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="68059-1369">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="68059-1370">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1370">Core</span></span>
* <span data-ttu-id="68059-1371">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1371">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="68059-1372">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1372">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1373">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-1373">Appservice</span></span>
* <span data-ttu-id="68059-1374">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1374">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="68059-1375">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1375">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="68059-1376">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1376">Network</span></span>
* <span data-ttu-id="68059-1377">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1377">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="68059-1378">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1378">Role</span></span>
* <span data-ttu-id="68059-1379">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1379">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="68059-1380">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1380">VM</span></span>
* <span data-ttu-id="68059-1381">[非推奨]`vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1381">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="68059-1382">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1382">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="68059-1383">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1383">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="68059-1384">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1384">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="68059-1385">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="68059-1385">November 20, 2018</span></span>

<span data-ttu-id="68059-1386">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="68059-1386">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="68059-1387">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1387">Core</span></span>
* <span data-ttu-id="68059-1388">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1388">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1389">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1389">ACR</span></span>
* <span data-ttu-id="68059-1390">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1390">Added context token to task step</span></span>
* <span data-ttu-id="68059-1391">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1391">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="68059-1392">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1392">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1393">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-1393">Appservice</span></span>
* <span data-ttu-id="68059-1394">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1394">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="68059-1395">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1395">Updated the default `node_version`.</span></span> <span data-ttu-id="68059-1396">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="68059-1396">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="68059-1397">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1397">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="68059-1398">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1398">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="68059-1399">IotCentral</span><span class="sxs-lookup"><span data-stu-id="68059-1399">IotCentral</span></span>
* <span data-ttu-id="68059-1400">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1400">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="68059-1401">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68059-1401">KeyVault</span></span>
* <span data-ttu-id="68059-1402">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1402">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="68059-1403">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1403">Network</span></span>
* <span data-ttu-id="68059-1404">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1404">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="68059-1405">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1405">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="68059-1406">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1406">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="68059-1407">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1407">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-1408">Rdbms</span><span class="sxs-lookup"><span data-stu-id="68059-1408">Rdbms</span></span>
* <span data-ttu-id="68059-1409">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1409">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="68059-1410">Rbac</span><span class="sxs-lookup"><span data-stu-id="68059-1410">Rbac</span></span>
* <span data-ttu-id="68059-1411">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1411">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="68059-1412">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1412">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="68059-1413">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1413">Storage</span></span>
* <span data-ttu-id="68059-1414">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1414">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="68059-1415">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1415">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="68059-1416">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1416">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="68059-1417">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="68059-1417">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1418">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1418">VM</span></span>
* <span data-ttu-id="68059-1419">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1419">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="68059-1420">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1420">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="68059-1421">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="68059-1421">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="68059-1422">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1422">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="68059-1423">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1423">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="68059-1424">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1424">Added `snapshot wait` command</span></span>
* <span data-ttu-id="68059-1425">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1425">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="68059-1426">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="68059-1426">November 6, 2018</span></span>

<span data-ttu-id="68059-1427">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="68059-1427">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="68059-1428">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1428">Core</span></span>
* <span data-ttu-id="68059-1429">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1429">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1430">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1430">ACR</span></span>
* <span data-ttu-id="68059-1431">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1431">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="68059-1432">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1432">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1433">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1433">ACS</span></span>
* <span data-ttu-id="68059-1434">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1434">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="68059-1435">Advisor</span><span class="sxs-lookup"><span data-stu-id="68059-1435">Advisor</span></span>
* <span data-ttu-id="68059-1436">GA リリース</span><span class="sxs-lookup"><span data-stu-id="68059-1436">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="68059-1437">AMS</span><span class="sxs-lookup"><span data-stu-id="68059-1437">AMS</span></span>
* <span data-ttu-id="68059-1438">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1438">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="68059-1439">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1439">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="68059-1440">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1440">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="68059-1441">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1441">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="68059-1442">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1442">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="68059-1443">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1443">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="68059-1444">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1444">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="68059-1445">[重大な変更]`ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="68059-1445">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="68059-1446">[重大な変更]`ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-1446">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="68059-1447">[重大な変更]`ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1447">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="68059-1448">[重大な変更]`ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="68059-1448">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="68059-1449">[重大な変更]`ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="68059-1449">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="68059-1450">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="68059-1450">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="68059-1451">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="68059-1451">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="68059-1452">[重大な変更]`ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1452">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="68059-1453">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="68059-1453">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="68059-1454">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="68059-1454">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1455">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1455">AppService</span></span>
* <span data-ttu-id="68059-1456">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1456">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="68059-1457">[構成]</span><span class="sxs-lookup"><span data-stu-id="68059-1457">Configure</span></span>
* <span data-ttu-id="68059-1458">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1458">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="68059-1459">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-1459">Container</span></span>
* <span data-ttu-id="68059-1460">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1460">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="68059-1461">EventHub</span><span class="sxs-lookup"><span data-stu-id="68059-1461">EventHub</span></span>
* <span data-ttu-id="68059-1462">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1462">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-1463">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-1463">Interactive</span></span>
* <span data-ttu-id="68059-1464">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="68059-1464">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-1465">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-1465">Monitor</span></span>
* <span data-ttu-id="68059-1466">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1466">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="68059-1467">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1467">Network</span></span>
* <span data-ttu-id="68059-1468">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1468">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="68059-1469">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1469">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="68059-1470">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1470">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="68059-1471">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-1471">Profile</span></span>
* <span data-ttu-id="68059-1472">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1472">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-1473">RDBMS</span><span class="sxs-lookup"><span data-stu-id="68059-1473">RDBMS</span></span>
* <span data-ttu-id="68059-1474">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1474">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="68059-1475">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-1475">Resource</span></span>
* <span data-ttu-id="68059-1476">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1476">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="68059-1477">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1477">Role</span></span>
* <span data-ttu-id="68059-1478">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-1478">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="68059-1479">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1479">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="68059-1480">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1480">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1481">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1481">Storage</span></span>
* <span data-ttu-id="68059-1482">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="68059-1482">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1483">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1483">VM</span></span>
* <span data-ttu-id="68059-1484">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1484">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="68059-1485">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1485">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="68059-1486">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1486">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="68059-1487">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1487">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="68059-1488">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="68059-1488">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="68059-1489">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1489">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="68059-1490">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="68059-1490">October 23, 2018</span></span>

<span data-ttu-id="68059-1491">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="68059-1491">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="68059-1492">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1492">Core</span></span>
* <span data-ttu-id="68059-1493">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1493">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="68059-1494">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1494">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1495">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1495">ACR</span></span>
* <span data-ttu-id="68059-1496">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1496">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="68059-1497">CDN</span><span class="sxs-lookup"><span data-stu-id="68059-1497">CDN</span></span>
* <span data-ttu-id="68059-1498">[重大な変更]`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="68059-1498">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="68059-1499">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1499">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="68059-1500">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-1500">Container</span></span>
* <span data-ttu-id="68059-1501">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1501">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="68059-1502">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1502">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="68059-1503">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1503">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="68059-1504">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1504">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="68059-1505">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1505">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="68059-1506">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1506">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="68059-1507">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1507">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-1508">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-1508">CosmosDB</span></span>
* <span data-ttu-id="68059-1509">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1509">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-1510">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-1510">Interactive</span></span>
* <span data-ttu-id="68059-1511">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1511">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="68059-1512">IoT Central</span><span class="sxs-lookup"><span data-stu-id="68059-1512">IoT Central</span></span>
* <span data-ttu-id="68059-1513">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1513">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="68059-1514">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="68059-1514">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-1515">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-1515">Monitor</span></span>
* <span data-ttu-id="68059-1516">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="68059-1516">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="68059-1517">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1517">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="68059-1518">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1518">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="68059-1519">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1519">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="68059-1520">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1520">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="68059-1521">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1521">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="68059-1522">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="68059-1522">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="68059-1523">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1523">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="68059-1524">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1524">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="68059-1525">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1525">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="68059-1526">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1526">Network</span></span>
* <span data-ttu-id="68059-1527">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1527">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="68059-1528">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1528">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="68059-1529">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="68059-1529">ServiceBus</span></span>
* <span data-ttu-id="68059-1530">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1530">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="68059-1531">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-1531">SQL</span></span>
* <span data-ttu-id="68059-1532">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1532">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1533">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1533">Storage</span></span>
* <span data-ttu-id="68059-1534">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1534">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="68059-1535">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1535">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1536">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1536">VM</span></span>
* <span data-ttu-id="68059-1537">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="68059-1537">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="68059-1538">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-1538">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="68059-1539">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1539">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="68059-1540">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="68059-1540">October 16, 2018</span></span>

<span data-ttu-id="68059-1541">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="68059-1541">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1542">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1542">VM</span></span>
* <span data-ttu-id="68059-1543">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1543">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="68059-1544">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="68059-1544">October 9, 2018</span></span>

<span data-ttu-id="68059-1545">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="68059-1545">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="68059-1546">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1546">Core</span></span>
* <span data-ttu-id="68059-1547">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1547">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1548">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1548">ACR</span></span>
* <span data-ttu-id="68059-1549">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1549">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1550">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1550">ACS</span></span>
* <span data-ttu-id="68059-1551">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="68059-1551">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="68059-1552">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1552">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="68059-1553">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1553">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="68059-1554">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1554">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="68059-1555">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-1555">Container</span></span>
* <span data-ttu-id="68059-1556">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1556">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="68059-1557">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1557">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="68059-1558">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="68059-1558">Event Hub</span></span>
* <span data-ttu-id="68059-1559">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1559">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="68059-1560">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1560">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="68059-1561">拡張機能</span><span class="sxs-lookup"><span data-stu-id="68059-1561">Extensions</span></span>
* <span data-ttu-id="68059-1562">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1562">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="68059-1563">HDInsight</span><span class="sxs-lookup"><span data-stu-id="68059-1563">HDInsight</span></span>
* <span data-ttu-id="68059-1564">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-1564">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="68059-1565">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-1565">IoT</span></span>
* <span data-ttu-id="68059-1566">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1566">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="68059-1567">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68059-1567">KeyVault</span></span>
* <span data-ttu-id="68059-1568">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1568">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="68059-1569">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1569">Network</span></span>
* <span data-ttu-id="68059-1570">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="68059-1570">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="68059-1571">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="68059-1571">See #6052</span></span>
* <span data-ttu-id="68059-1572">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1572">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="68059-1573">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="68059-1573">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="68059-1574">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1574">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="68059-1575">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1575">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="68059-1576">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1576">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="68059-1577">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1577">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="68059-1578">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1578">Role</span></span>
* <span data-ttu-id="68059-1579">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1579">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="68059-1580">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1580">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="68059-1581">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1581">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="68059-1582">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1582">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="68059-1583">Service Bus</span><span class="sxs-lookup"><span data-stu-id="68059-1583">Service Bus</span></span>
* <span data-ttu-id="68059-1584">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1584">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1585">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1585">VM</span></span>
* <span data-ttu-id="68059-1586">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1586">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="68059-1587">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1587">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="68059-1588">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1588">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="68059-1589">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1589">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="68059-1590">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1590">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="68059-1591">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1591">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="68059-1592">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="68059-1592">September 21, 2018</span></span>

<span data-ttu-id="68059-1593">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="68059-1593">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1594">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1594">ACR</span></span>
* <span data-ttu-id="68059-1595">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1595">Added ACR Task commands</span></span>
* <span data-ttu-id="68059-1596">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1596">Added quick run command</span></span>
* <span data-ttu-id="68059-1597">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1597">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="68059-1598">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1598">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="68059-1599">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1599">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="68059-1600">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1600">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1601">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1601">ACS</span></span>
* <span data-ttu-id="68059-1602">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1602">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="68059-1603">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1603">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1604">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1604">AppService</span></span>

* <span data-ttu-id="68059-1605">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1605">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="68059-1606">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1606">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="68059-1607">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1607">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="68059-1608">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1608">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="68059-1609">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-1609">Batch</span></span>
* <span data-ttu-id="68059-1610">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1610">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="68059-1611">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-1611">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="68059-1612">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1612">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="68059-1613">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1613">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="68059-1614">Batch AI</span><span class="sxs-lookup"><span data-stu-id="68059-1614">Batch AI</span></span> 
* <span data-ttu-id="68059-1615">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1615">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="68059-1616">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="68059-1616">Cognitive Services</span></span>
* <span data-ttu-id="68059-1617">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1617">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="68059-1618">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1618">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="68059-1619">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1619">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="68059-1620">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1620">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="68059-1621">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1621">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="68059-1622">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1622">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="68059-1623">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-1623">Container</span></span>
* <span data-ttu-id="68059-1624">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1624">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="68059-1625">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1625">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="68059-1626">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1626">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="68059-1627">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1627">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="68059-1628">DataLake</span><span class="sxs-lookup"><span data-stu-id="68059-1628">Datalake</span></span>
* <span data-ttu-id="68059-1629">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1629">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="68059-1630">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="68059-1630">Interactive Shell</span></span>
* <span data-ttu-id="68059-1631">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1631">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="68059-1632">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1632">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="68059-1633">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-1633">IoT</span></span>
* <span data-ttu-id="68059-1634">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1634">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="68059-1635">Key Vault</span><span class="sxs-lookup"><span data-stu-id="68059-1635">Key Vault</span></span>
* <span data-ttu-id="68059-1636">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1636">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="68059-1637">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1637">Network</span></span>
* <span data-ttu-id="68059-1638">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1638">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="68059-1639">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1639">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="68059-1640">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1640">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="68059-1641">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1641">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="68059-1642">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1642">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="68059-1643">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1643">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="68059-1644">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="68059-1644">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="68059-1645">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-1645">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="68059-1646">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1646">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="68059-1647">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1647">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="68059-1648">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1648">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="68059-1649">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1649">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="68059-1650">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1650">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="68059-1651">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="68059-1651">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="68059-1652">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1652">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="68059-1653">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1653">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="68059-1654">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1654">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="68059-1655">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1655">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-1656">RDBMS</span><span class="sxs-lookup"><span data-stu-id="68059-1656">RDBMS</span></span>
* <span data-ttu-id="68059-1657">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1657">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="68059-1658">予約</span><span class="sxs-lookup"><span data-stu-id="68059-1658">Reservation</span></span>
* <span data-ttu-id="68059-1659">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1659">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="68059-1660">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1660">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="68059-1661">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="68059-1661">Manage App</span></span>
* <span data-ttu-id="68059-1662">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1662">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="68059-1663">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1663">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="68059-1664">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1664">Role</span></span>
* <span data-ttu-id="68059-1665">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1665">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="68059-1666">SignalR</span><span class="sxs-lookup"><span data-stu-id="68059-1666">SignalR</span></span>
* <span data-ttu-id="68059-1667">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-1667">First release</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1668">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1668">Storage</span></span>
* <span data-ttu-id="68059-1669">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1669">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="68059-1670">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1670">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1671">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1671">VM</span></span>
* <span data-ttu-id="68059-1672">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="68059-1672">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="68059-1673">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1673">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="68059-1674">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="68059-1674">August 28, 2018</span></span>

<span data-ttu-id="68059-1675">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="68059-1675">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="68059-1676">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1676">Core</span></span>

* <span data-ttu-id="68059-1677">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1677">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="68059-1678">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1678">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1679">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1679">ACR</span></span>

* <span data-ttu-id="68059-1680">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1680">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="68059-1681">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1681">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1682">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1682">ACS</span></span>

* <span data-ttu-id="68059-1683">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1683">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="68059-1684">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1684">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1685">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1685">AppService</span></span>

* <span data-ttu-id="68059-1686">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1686">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="68059-1687">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1687">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="68059-1688">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1688">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="68059-1689">バックアップ</span><span class="sxs-lookup"><span data-stu-id="68059-1689">Backup</span></span>

* <span data-ttu-id="68059-1690">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1690">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="68059-1691">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="68059-1691">Bot Service</span></span>

* <span data-ttu-id="68059-1692">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="68059-1692">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="68059-1693">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="68059-1693">Cognitive Services</span></span>

* <span data-ttu-id="68059-1694">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1694">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="68059-1695">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-1695">IoT</span></span>

* <span data-ttu-id="68059-1696">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1696">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-1697">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-1697">Monitor</span></span>

* <span data-ttu-id="68059-1698">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1698">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="68059-1699">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1699">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="68059-1700">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1700">Network</span></span>

* <span data-ttu-id="68059-1701">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1701">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="68059-1702">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-1702">Resource</span></span>

* <span data-ttu-id="68059-1703">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1703">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1704">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1704">Storage</span></span>

* <span data-ttu-id="68059-1705">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1705">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1706">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1706">VM</span></span>

* <span data-ttu-id="68059-1707">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1707">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="68059-1708">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1708">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="68059-1709">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="68059-1709">Auguest 14, 2018</span></span>

<span data-ttu-id="68059-1710">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="68059-1710">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="68059-1711">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1711">Core</span></span>

* <span data-ttu-id="68059-1712">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1712">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="68059-1713">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1713">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="68059-1714">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="68059-1714">Telemetry</span></span>

* <span data-ttu-id="68059-1715">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1715">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1716">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1716">ACR</span></span>

* <span data-ttu-id="68059-1717">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1717">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="68059-1718">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1718">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1719">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1719">ACS</span></span>

* <span data-ttu-id="68059-1720">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1720">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="68059-1721">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1721">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="68059-1722">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1722">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="68059-1723">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1723">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="68059-1724">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1724">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="68059-1725">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1725">AppService</span></span>

* <span data-ttu-id="68059-1726">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1726">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="68059-1727">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1727">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="68059-1728">BatchAI</span><span class="sxs-lookup"><span data-stu-id="68059-1728">BatchAI</span></span>

* <span data-ttu-id="68059-1729">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1729">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="68059-1730">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-1730">Container</span></span>

* <span data-ttu-id="68059-1731">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1731">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="68059-1732">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-1732">IoT</span></span>

* <span data-ttu-id="68059-1733">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1733">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="68059-1734">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-1734">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="68059-1735">Iot Central</span><span class="sxs-lookup"><span data-stu-id="68059-1735">Iot Central</span></span>

* <span data-ttu-id="68059-1736">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-1736">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="68059-1737">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68059-1737">KeyVault</span></span>


* <span data-ttu-id="68059-1738">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1738">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="68059-1739">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1739">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="68059-1740">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1740">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="68059-1741">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1741">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="68059-1742">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1742">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="68059-1743">リレー</span><span class="sxs-lookup"><span data-stu-id="68059-1743">Relay</span></span>

* <span data-ttu-id="68059-1744">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-1744">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="68059-1745">Sql</span><span class="sxs-lookup"><span data-stu-id="68059-1745">Sql</span></span>

* <span data-ttu-id="68059-1746">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1746">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1747">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1747">Storage</span></span>

* <span data-ttu-id="68059-1748">[重大な変更]`--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="68059-1748">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="68059-1749">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1749">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="68059-1750">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="68059-1750">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="68059-1751">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1751">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="68059-1752">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1752">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1753">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1753">VM</span></span>

* <span data-ttu-id="68059-1754">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1754">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="68059-1755">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="68059-1755">July 31, 2018</span></span>

<span data-ttu-id="68059-1756">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="68059-1756">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1757">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1757">ACR</span></span>

* <span data-ttu-id="68059-1758">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1758">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="68059-1759">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1759">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1760">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1760">ACS</span></span>

* <span data-ttu-id="68059-1761">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1761">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="68059-1762">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-1762">Batch</span></span>

* <span data-ttu-id="68059-1763">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1763">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="68059-1764">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-1764">Container</span></span>

* <span data-ttu-id="68059-1765">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1765">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="68059-1766">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1766">Network</span></span>

* <span data-ttu-id="68059-1767">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1767">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="68059-1768">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-1768">Resource</span></span>

* <span data-ttu-id="68059-1769">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1769">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="68059-1770">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1770">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="68059-1771">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1771">Role</span></span>

* <span data-ttu-id="68059-1772">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1772">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="68059-1773">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1773">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="68059-1774">検索</span><span class="sxs-lookup"><span data-stu-id="68059-1774">Search</span></span>

* <span data-ttu-id="68059-1775">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1775">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="68059-1776">Service Bus</span><span class="sxs-lookup"><span data-stu-id="68059-1776">Service Bus</span></span>

* <span data-ttu-id="68059-1777">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1777">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="68059-1778">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1778">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="68059-1779">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="68059-1779">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="68059-1780">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="68059-1780">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1781">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1781">Storage</span></span>

* <span data-ttu-id="68059-1782">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1782">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="68059-1783">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="68059-1783">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1784">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1784">VM</span></span>

* <span data-ttu-id="68059-1785">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1785">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="68059-1786">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1786">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="68059-1787">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1787">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="68059-1788">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1788">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="68059-1789">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="68059-1789">July 18, 2018</span></span>

<span data-ttu-id="68059-1790">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="68059-1790">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="68059-1791">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1791">Core</span></span>

* <span data-ttu-id="68059-1792">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1792">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="68059-1793">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1793">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="68059-1794">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1794">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1795">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1795">ACR</span></span>

* <span data-ttu-id="68059-1796">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-1796">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="68059-1797">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1797">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="68059-1798">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1798">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="68059-1799">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1799">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1800">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1800">ACS</span></span>

* <span data-ttu-id="68059-1801">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1801">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1802">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1802">AppService</span></span>

* <span data-ttu-id="68059-1803">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1803">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="68059-1804">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-1804">Batch</span></span>

* <span data-ttu-id="68059-1805">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1805">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="68059-1806">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1806">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="68059-1807">Batch AI</span><span class="sxs-lookup"><span data-stu-id="68059-1807">Batch AI</span></span>

* <span data-ttu-id="68059-1808">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1808">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="68059-1809">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-1809">Container</span></span>

* <span data-ttu-id="68059-1810">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1810">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="68059-1811">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1811">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="68059-1812">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1812">Network</span></span>

* <span data-ttu-id="68059-1813">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1813">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="68059-1814">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1814">Added `network nic wait`</span></span>
* <span data-ttu-id="68059-1815">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1815">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="68059-1816">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1816">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="68059-1817">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-1817">Resource</span></span>

* <span data-ttu-id="68059-1818">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1818">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="68059-1819">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1819">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="68059-1820">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1820">Added `deployment wait` command</span></span>
* <span data-ttu-id="68059-1821">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1821">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="68059-1822">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-1822">SQL</span></span>

* <span data-ttu-id="68059-1823">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1823">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="68059-1824">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1824">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="68059-1825">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="68059-1825">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1826">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1826">Storage</span></span>

* <span data-ttu-id="68059-1827">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1827">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1828">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1828">VM</span></span>

* <span data-ttu-id="68059-1829">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1829">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="68059-1830">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1830">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="68059-1831">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1831">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="68059-1832">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="68059-1832">July 3, 2018</span></span>

<span data-ttu-id="68059-1833">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="68059-1833">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="68059-1834">AKS</span><span class="sxs-lookup"><span data-stu-id="68059-1834">AKS</span></span>

* <span data-ttu-id="68059-1835">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1835">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="68059-1836">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="68059-1836">July 3, 2018</span></span>

<span data-ttu-id="68059-1837">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="68059-1837">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="68059-1838">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1838">Core</span></span>

* <span data-ttu-id="68059-1839">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1839">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1840">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1840">ACR</span></span>

* <span data-ttu-id="68059-1841">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1841">Added polling build status</span></span>
* <span data-ttu-id="68059-1842">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1842">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="68059-1843">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1843">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1844">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1844">ACS</span></span>

* <span data-ttu-id="68059-1845">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1845">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="68059-1846">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1846">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="68059-1847">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1847">Updated options for `aks browse` command.</span></span> <span data-ttu-id="68059-1848">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1848">Added `--listen-port` support</span></span>
* <span data-ttu-id="68059-1849">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1849">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="68059-1850">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="68059-1850">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="68059-1851">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1851">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1852">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1852">AppService</span></span>

* <span data-ttu-id="68059-1853">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1853">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="68059-1854">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1854">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="68059-1855">バックアップ</span><span class="sxs-lookup"><span data-stu-id="68059-1855">Backup</span></span>

* <span data-ttu-id="68059-1856">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-1856">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="68059-1857">BatchAI</span><span class="sxs-lookup"><span data-stu-id="68059-1857">BatchAI</span></span>

* <span data-ttu-id="68059-1858">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1858">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="68059-1859">クラウド</span><span class="sxs-lookup"><span data-stu-id="68059-1859">Cloud</span></span>

* <span data-ttu-id="68059-1860">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1860">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="68059-1861">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-1861">Container</span></span>

* <span data-ttu-id="68059-1862">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1862">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="68059-1863">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1863">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="68059-1864">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1864">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="68059-1865">拡張機能</span><span class="sxs-lookup"><span data-stu-id="68059-1865">Extension</span></span>

* <span data-ttu-id="68059-1866">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1866">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="68059-1867">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1867">Network</span></span>

* <span data-ttu-id="68059-1868">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1868">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-1869">Rdbms</span><span class="sxs-lookup"><span data-stu-id="68059-1869">Rdbms</span></span>

* <span data-ttu-id="68059-1870">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1870">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="68059-1871">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-1871">Resource</span></span>

* <span data-ttu-id="68059-1872">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1872">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1873">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1873">VM</span></span>

* <span data-ttu-id="68059-1874">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-1874">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="68059-1875">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="68059-1875">June 25, 2018</span></span>

<span data-ttu-id="68059-1876">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="68059-1876">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="68059-1877">CLI</span><span class="sxs-lookup"><span data-stu-id="68059-1877">CLI</span></span>

* <span data-ttu-id="68059-1878">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-1878">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="68059-1879">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="68059-1879">June 19, 2018</span></span>

<span data-ttu-id="68059-1880">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="68059-1880">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="68059-1881">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1881">Core</span></span>

* <span data-ttu-id="68059-1882">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1882">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1883">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1883">ACR</span></span>

* <span data-ttu-id="68059-1884">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1884">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="68059-1885">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1885">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1886">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1886">ACS</span></span>

* <span data-ttu-id="68059-1887">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1887">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="68059-1888">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1888">Added `--update` support</span></span>
* <span data-ttu-id="68059-1889">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1889">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="68059-1890">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="68059-1890">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="68059-1891">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1891">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="68059-1892">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1892">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="68059-1893">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1893">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="68059-1894">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1894">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1895">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1895">AppService</span></span>

* <span data-ttu-id="68059-1896">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1896">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="68059-1897">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1897">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="68059-1898">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-1898">Batch</span></span>

* <span data-ttu-id="68059-1899">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1899">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="68059-1900">Batch AI</span><span class="sxs-lookup"><span data-stu-id="68059-1900">Batch AI</span></span>

* <span data-ttu-id="68059-1901">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1901">Added support for workspaces.</span></span> <span data-ttu-id="68059-1902">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="68059-1902">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="68059-1903">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1903">Added support for experiments.</span></span> <span data-ttu-id="68059-1904">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="68059-1904">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="68059-1905">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1905">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="68059-1906">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1906">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="68059-1907">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="68059-1907">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="68059-1908">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1908">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="68059-1909">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="68059-1909">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="68059-1910">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="68059-1910">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="68059-1911">[重大な変更]`--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1911">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="68059-1912">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="68059-1912">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="68059-1913">[重大な変更]`--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1913">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="68059-1914">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="68059-1914">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="68059-1915">[重大な変更]`location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1915">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="68059-1916">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="68059-1916">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="68059-1917">[重大な変更]`--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1917">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="68059-1918">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1918">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="68059-1919">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1919">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="68059-1920">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1920">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="68059-1921">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1921">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="68059-1922">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1922">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="68059-1923">マップ</span><span class="sxs-lookup"><span data-stu-id="68059-1923">Maps</span></span>

* <span data-ttu-id="68059-1924">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1924">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="68059-1925">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1925">Network</span></span>

* <span data-ttu-id="68059-1926">`https` のサポートを `network lb probe create` に追加しました ([#6571](https://github.com/Azure/azure-cli/issues/6571))</span><span class="sxs-lookup"><span data-stu-id="68059-1926">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="68059-1927">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1927">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="68059-1928">#6502</span><span class="sxs-lookup"><span data-stu-id="68059-1928">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="68059-1929">Reservations</span><span class="sxs-lookup"><span data-stu-id="68059-1929">Reservations</span></span>

* <span data-ttu-id="68059-1930">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1930">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="68059-1931">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1931">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="68059-1932">[重大な変更]`kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1932">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="68059-1933">[重大な変更]`Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1933">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="68059-1934">[重大な変更]`Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-1934">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="68059-1935">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1935">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="68059-1936">Role</span><span class="sxs-lookup"><span data-stu-id="68059-1936">Role</span></span>

* <span data-ttu-id="68059-1937">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1937">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="68059-1938">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-1938">SQL</span></span>

* <span data-ttu-id="68059-1939">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1939">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="68059-1940">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1940">Storage</span></span>

* <span data-ttu-id="68059-1941">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="68059-1941">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1942">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1942">VM</span></span>

* <span data-ttu-id="68059-1943">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1943">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="68059-1944">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1944">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="68059-1945">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1945">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="68059-1946">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="68059-1946">June 13, 2018</span></span>

<span data-ttu-id="68059-1947">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="68059-1947">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="68059-1948">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1948">Core</span></span>

* <span data-ttu-id="68059-1949">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-1949">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="68059-1950">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="68059-1950">June 13, 2018</span></span>

<span data-ttu-id="68059-1951">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="68059-1951">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="68059-1952">AKS</span><span class="sxs-lookup"><span data-stu-id="68059-1952">AKS</span></span>

* <span data-ttu-id="68059-1953">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1953">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="68059-1954">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-1954">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="68059-1955">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1955">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="68059-1956">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1956">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="68059-1957">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1957">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-1958">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-1958">AppService</span></span>

* <span data-ttu-id="68059-1959">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1959">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="68059-1960">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="68059-1960">June 5, 2018</span></span>

<span data-ttu-id="68059-1961">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="68059-1961">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-1962">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-1962">Interactive</span></span>

* <span data-ttu-id="68059-1963">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1963">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="68059-1964">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="68059-1964">June 5, 2018</span></span>

<span data-ttu-id="68059-1965">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="68059-1965">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="68059-1966">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1966">Core</span></span>

* <span data-ttu-id="68059-1967">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1967">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="68059-1968">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-1968">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="68059-1969">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-1969">ACR</span></span>

* <span data-ttu-id="68059-1970">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1970">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="68059-1971">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1971">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="68059-1972">AKS</span><span class="sxs-lookup"><span data-stu-id="68059-1972">AKS</span></span>

* <span data-ttu-id="68059-1973">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-1973">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="68059-1974">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-1974">Batch</span></span>

* <span data-ttu-id="68059-1975">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1975">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="68059-1976">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-1976">IOT</span></span>

* <span data-ttu-id="68059-1977">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1977">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="68059-1978">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-1978">Network</span></span>

* <span data-ttu-id="68059-1979">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-1979">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="68059-1980">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="68059-1980">Policy Insights</span></span>

* <span data-ttu-id="68059-1981">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-1981">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="68059-1982">ARM</span><span class="sxs-lookup"><span data-stu-id="68059-1982">ARM</span></span>

* <span data-ttu-id="68059-1983">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1983">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="68059-1984">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-1984">SQL</span></span>

* <span data-ttu-id="68059-1985">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1985">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="68059-1986">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-1986">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="68059-1987">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-1987">Storage</span></span>

* <span data-ttu-id="68059-1988">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1988">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="68059-1989">VM</span><span class="sxs-lookup"><span data-stu-id="68059-1989">VM</span></span>

* <span data-ttu-id="68059-1990">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1990">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="68059-1991">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1991">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="68059-1992">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1992">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="68059-1993">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="68059-1993">May 22, 2018</span></span>

<span data-ttu-id="68059-1994">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="68059-1994">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="68059-1995">コア</span><span class="sxs-lookup"><span data-stu-id="68059-1995">Core</span></span>

* <span data-ttu-id="68059-1996">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1996">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="68059-1997">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-1997">ACS</span></span>

* <span data-ttu-id="68059-1998">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-1998">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="68059-1999">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-1999">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2000">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-2000">AppService</span></span>

* <span data-ttu-id="68059-2001">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-2001">Improved generic update commands</span></span>
* <span data-ttu-id="68059-2002">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2002">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="68059-2003">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-2003">Container</span></span>

* <span data-ttu-id="68059-2004">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2004">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="68059-2005">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2005">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="68059-2006">拡張機能</span><span class="sxs-lookup"><span data-stu-id="68059-2006">Extension</span></span>

* <span data-ttu-id="68059-2007">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-2007">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-2008">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-2008">Interactive</span></span>

* <span data-ttu-id="68059-2009">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2009">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="68059-2010">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-2010">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="68059-2011">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68059-2011">KeyVault</span></span>

* <span data-ttu-id="68059-2012">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2012">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="68059-2013">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2013">Network</span></span>

* <span data-ttu-id="68059-2014">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2014">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="68059-2015">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2015">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="68059-2016">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-2016">SQL</span></span>

* <span data-ttu-id="68059-2017">[重大な変更]`db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2017">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="68059-2018">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2018">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="68059-2019">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2019">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="68059-2020">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2020">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="68059-2021">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2021">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="68059-2022">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="68059-2022">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="68059-2023">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="68059-2023">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="68059-2024">`edition`</span><span class="sxs-lookup"><span data-stu-id="68059-2024">`edition`.</span></span> <span data-ttu-id="68059-2025">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="68059-2025">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="68059-2026">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="68059-2026">`elasticPoolName`.</span></span> <span data-ttu-id="68059-2027">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="68059-2027">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="68059-2028">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2028">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="68059-2029">`edition`</span><span class="sxs-lookup"><span data-stu-id="68059-2029">`edition`.</span></span> <span data-ttu-id="68059-2030">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="68059-2030">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="68059-2031">`dtu`</span><span class="sxs-lookup"><span data-stu-id="68059-2031">`dtu`.</span></span> <span data-ttu-id="68059-2032">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="68059-2032">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="68059-2033">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="68059-2033">`databaseDtuMin`.</span></span> <span data-ttu-id="68059-2034">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="68059-2034">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="68059-2035">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="68059-2035">`databaseDtuMax`.</span></span> <span data-ttu-id="68059-2036">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="68059-2036">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="68059-2037">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2037">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="68059-2038">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2038">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2039">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2039">Storage</span></span>

* <span data-ttu-id="68059-2040">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2040">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="68059-2041">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2041">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2042">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2042">VM</span></span>

* <span data-ttu-id="68059-2043">[重大な変更]`--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2043">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="68059-2044">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="68059-2044">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="68059-2045">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2045">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="68059-2046">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2046">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="68059-2047">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2047">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="68059-2048">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="68059-2048">May 7, 2018</span></span>

<span data-ttu-id="68059-2049">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="68059-2049">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="68059-2050">コア</span><span class="sxs-lookup"><span data-stu-id="68059-2050">Core</span></span>

* <span data-ttu-id="68059-2051">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2051">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="68059-2052">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2052">Added limited support for positional arguments</span></span>
* <span data-ttu-id="68059-2053">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2053">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="68059-2054">#5591</span><span class="sxs-lookup"><span data-stu-id="68059-2054">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="68059-2055">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2055">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="68059-2056">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="68059-2056">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="68059-2057">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2057">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="68059-2058">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2058">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="68059-2059">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2059">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="68059-2060">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-2060">ACR</span></span>

* <span data-ttu-id="68059-2061">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2061">Added ACR Build commands</span></span>
* <span data-ttu-id="68059-2062">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2062">Improved resource not found error messages</span></span>
* <span data-ttu-id="68059-2063">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2063">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="68059-2064">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2064">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="68059-2065">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2065">Improved repository commands error messages</span></span>
* <span data-ttu-id="68059-2066">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2066">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2067">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2067">ACS</span></span>

* <span data-ttu-id="68059-2068">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2068">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="68059-2069">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2069">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="68059-2070">AMS</span><span class="sxs-lookup"><span data-stu-id="68059-2070">AMS</span></span>

* <span data-ttu-id="68059-2071">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="68059-2071">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2072">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2072">Appservice</span></span>

* <span data-ttu-id="68059-2073">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2073">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="68059-2074">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2074">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="68059-2075">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2075">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="68059-2076">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2076">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="68059-2077">Batch AI</span><span class="sxs-lookup"><span data-stu-id="68059-2077">Batch AI</span></span>

* <span data-ttu-id="68059-2078">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2078">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="68059-2079">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="68059-2079">Cognitive Services</span></span>

* <span data-ttu-id="68059-2080">`cognitiveservices account create` の例の誤りを修正しました ([#5603](https://github.com/Azure/azure-cli/issues/5603))</span><span class="sxs-lookup"><span data-stu-id="68059-2080">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="68059-2081">従量課金</span><span class="sxs-lookup"><span data-stu-id="68059-2081">Consumption</span></span>

* <span data-ttu-id="68059-2082">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2082">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="68059-2083">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-2083">Container</span></span>

* <span data-ttu-id="68059-2084">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2084">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="68059-2085">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-2085">Cosmos DB</span></span>

* <span data-ttu-id="68059-2086">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="68059-2086">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="68059-2087">DMS</span><span class="sxs-lookup"><span data-stu-id="68059-2087">DMS</span></span>

* <span data-ttu-id="68059-2088">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2088">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="68059-2089">拡張機能</span><span class="sxs-lookup"><span data-stu-id="68059-2089">Extension</span></span>

* <span data-ttu-id="68059-2090">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2090">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-2091">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-2091">Interactive</span></span>

* <span data-ttu-id="68059-2092">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-2092">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="68059-2093">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="68059-2093">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="68059-2094">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2094">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="68059-2095">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2095">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="68059-2096">ラボ</span><span class="sxs-lookup"><span data-stu-id="68059-2096">Lab</span></span>

* <span data-ttu-id="68059-2097">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2097">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="68059-2098">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2098">Network</span></span>

* <span data-ttu-id="68059-2099">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2099">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="68059-2100">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-2100">Profile</span></span>

* <span data-ttu-id="68059-2101">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2101">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="68059-2102">[重大な変更]`--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2102">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="68059-2103">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2103">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="68059-2104">Redis</span><span class="sxs-lookup"><span data-stu-id="68059-2104">Redis</span></span>

* <span data-ttu-id="68059-2105">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2105">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="68059-2106">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="68059-2106">Deprecated `redis list-all`.</span></span> <span data-ttu-id="68059-2107">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="68059-2107">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="68059-2108">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2108">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="68059-2109">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2109">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="68059-2110">Role</span><span class="sxs-lookup"><span data-stu-id="68059-2110">Role</span></span>

* <span data-ttu-id="68059-2111">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2111">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2112">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2112">Storage</span></span>

* <span data-ttu-id="68059-2113">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="68059-2113">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="68059-2114">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="68059-2114">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="68059-2115">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="68059-2115">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="68059-2116">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="68059-2116">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="68059-2117">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2117">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2118">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2118">VM</span></span>

* <span data-ttu-id="68059-2119">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2119">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="68059-2120">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2120">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="68059-2121">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="68059-2121">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="68059-2122">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2122">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="68059-2123">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2123">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="68059-2124">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2124">Added write accelerator support</span></span>
* <span data-ttu-id="68059-2125">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2125">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="68059-2126">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2126">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="68059-2127">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2127">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="68059-2128">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="68059-2128">April 10, 2018</span></span>

<span data-ttu-id="68059-2129">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="68059-2129">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="68059-2130">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-2130">ACR</span></span>

* <span data-ttu-id="68059-2131">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2131">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2132">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2132">ACS</span></span>

* <span data-ttu-id="68059-2133">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2133">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2134">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2134">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="68059-2136">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2136">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="68059-2137">BatchAI</span><span class="sxs-lookup"><span data-stu-id="68059-2137">BatchAI</span></span>

* <span data-ttu-id="68059-2138">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2138">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="68059-2139">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="68059-2139">Job level mounting</span></span>
  - <span data-ttu-id="68059-2140">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="68059-2140">Environment variables with secret values</span></span>
  - <span data-ttu-id="68059-2141">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="68059-2141">Performance counters settings</span></span>
  - <span data-ttu-id="68059-2142">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="68059-2142">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="68059-2143">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="68059-2143">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="68059-2144">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="68059-2144">Usage and limits reporting</span></span>
  - <span data-ttu-id="68059-2145">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="68059-2145">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="68059-2146">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="68059-2146">Support for custom images</span></span>
  - <span data-ttu-id="68059-2147">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2147">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="68059-2148">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2148">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="68059-2149">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="68059-2149">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="68059-2150">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="68059-2150">National clouds are supported</span></span>
* <span data-ttu-id="68059-2151">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2151">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="68059-2152">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2152">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="68059-2153">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2153">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="68059-2154">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2154">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="68059-2155">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="68059-2155">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="68059-2156">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="68059-2156">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="68059-2157">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2157">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="68059-2158">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2158">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="68059-2159">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="68059-2159">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="68059-2160">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2160">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="68059-2161">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="68059-2161">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="68059-2162">[重大な変更]`job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="68059-2162">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="68059-2163">[重大な変更]`cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2163">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="68059-2164">課金</span><span class="sxs-lookup"><span data-stu-id="68059-2164">Billing</span></span>

* <span data-ttu-id="68059-2165">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2165">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="68059-2166">従量課金</span><span class="sxs-lookup"><span data-stu-id="68059-2166">Consumption</span></span>

* <span data-ttu-id="68059-2167">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2167">Added `marketplace` commands</span></span>
* <span data-ttu-id="68059-2168">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2168">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="68059-2169">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2169">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="68059-2170">[重大な変更]`reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2170">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="68059-2171">[重大な変更]`reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2171">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="68059-2172">[重大な変更]`pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2172">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="68059-2173">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-2173">Container</span></span>

* <span data-ttu-id="68059-2174">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2174">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="68059-2175">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2175">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="68059-2176">拡張機能</span><span class="sxs-lookup"><span data-stu-id="68059-2176">Extension</span></span>

* <span data-ttu-id="68059-2177">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2177">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-2178">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-2178">Interactive</span></span>

* <span data-ttu-id="68059-2179">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2179">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="68059-2180">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2180">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="68059-2181">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2181">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="68059-2182">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2182">Network</span></span>

* <span data-ttu-id="68059-2183">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2183">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="68059-2184">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2184">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="68059-2185">#4910</span><span class="sxs-lookup"><span data-stu-id="68059-2185">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="68059-2186">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2186">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="68059-2187">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="68059-2187">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="68059-2188">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2188">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="68059-2189">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2189">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="68059-2190">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2190">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="68059-2191">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-2191">Profile</span></span>

* <span data-ttu-id="68059-2192">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2192">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="68059-2193">[重大な変更]`--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2193">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-2194">RDBMS</span><span class="sxs-lookup"><span data-stu-id="68059-2194">RDBMS</span></span>

* <span data-ttu-id="68059-2195">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2195">Added `georestore` command</span></span>
* <span data-ttu-id="68059-2196">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2196">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2197">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2197">Resource</span></span>

* <span data-ttu-id="68059-2198">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2198">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="68059-2199">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2199">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="68059-2200">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-2200">SQL</span></span>

* <span data-ttu-id="68059-2201">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2201">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2202">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2202">Storage</span></span>

* <span data-ttu-id="68059-2203">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2203">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2204">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2204">VM</span></span>

* <span data-ttu-id="68059-2205">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2205">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="68059-2206">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2206">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="68059-2208">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2208">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="68059-2209">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2209">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="68059-2210">#5718</span><span class="sxs-lookup"><span data-stu-id="68059-2210">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="68059-2211">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2211">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="68059-2212">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="68059-2212">March 27, 2018</span></span>

<span data-ttu-id="68059-2213">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="68059-2213">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="68059-2214">コア</span><span class="sxs-lookup"><span data-stu-id="68059-2214">Core</span></span>

* <span data-ttu-id="68059-2215">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="68059-2215">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2216">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2216">ACS</span></span>

* <span data-ttu-id="68059-2217">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2217">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2218">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2218">Appservice</span></span>

* <span data-ttu-id="68059-2219">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2219">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="68059-2220">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2220">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="68059-2221">バックアップ</span><span class="sxs-lookup"><span data-stu-id="68059-2221">Backup</span></span>

* <span data-ttu-id="68059-2222">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2222">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="68059-2223">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="68059-2223">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="68059-2224">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2224">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="68059-2225">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2225">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="68059-2226">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-2226">Container</span></span>

* <span data-ttu-id="68059-2227">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2227">Added `container exec` command.</span></span> <span data-ttu-id="68059-2228">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="68059-2228">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="68059-2229">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="68059-2229">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="68059-2230">拡張機能</span><span class="sxs-lookup"><span data-stu-id="68059-2230">Extension</span></span>

* <span data-ttu-id="68059-2231">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2231">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="68059-2232">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2232">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="68059-2233">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2233">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-2234">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-2234">Interactive</span></span>

* <span data-ttu-id="68059-2235">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2235">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="68059-2236">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2236">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="68059-2237">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="68059-2237">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="68059-2238">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-2238">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="68059-2239">ラボ</span><span class="sxs-lookup"><span data-stu-id="68059-2239">Lab</span></span>

* <span data-ttu-id="68059-2240">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2240">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-2241">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-2241">Monitor</span></span>

* <span data-ttu-id="68059-2242">`--top`、`--orderby`、および `--namespace` のサポートを `metrics list` に追加しました ([#5785](https://github.com/Azure/azure-cli/issues/5785))</span><span class="sxs-lookup"><span data-stu-id="68059-2242">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="68059-2243">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="68059-2243">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="68059-2244">`--namespace` のサポートを `metrics list-definitions` に追加しました ([#5785](https://github.com/Azure/azure-cli/issues/5785))</span><span class="sxs-lookup"><span data-stu-id="68059-2244">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="68059-2245">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2245">Network</span></span>

* <span data-ttu-id="68059-2246">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2246">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="68059-2247">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-2247">Profile</span></span>

* <span data-ttu-id="68059-2248">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2248">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-2249">RDBMS</span><span class="sxs-lookup"><span data-stu-id="68059-2249">RDBMS</span></span>

* <span data-ttu-id="68059-2250">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2250">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2251">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2251">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="68059-2253">Role</span><span class="sxs-lookup"><span data-stu-id="68059-2253">Role</span></span>

* <span data-ttu-id="68059-2254">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2254">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="68059-2255">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2255">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="68059-2256">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2256">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="68059-2257">[重大な変更]`az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2257">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="68059-2258">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2258">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2259">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2259">Storage</span></span>

* <span data-ttu-id="68059-2260">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2260">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="68059-2261">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="68059-2261">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2262">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2262">VM</span></span>

* <span data-ttu-id="68059-2263">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2263">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="68059-2264">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2264">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="68059-2265">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2265">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="68059-2266">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2266">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="68059-2267">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="68059-2267">March 13, 2018</span></span>

<span data-ttu-id="68059-2268">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="68059-2268">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="68059-2269">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-2269">ACR</span></span>

* <span data-ttu-id="68059-2270">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2270">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="68059-2271">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2271">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="68059-2272">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2272">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2273">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2273">ACS</span></span>

* <span data-ttu-id="68059-2274">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2274">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="68059-2275">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2275">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="68059-2276">Advisor</span><span class="sxs-lookup"><span data-stu-id="68059-2276">Advisor</span></span>

* <span data-ttu-id="68059-2277">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2277">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="68059-2278">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2278">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="68059-2279">[重大な変更]`advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2279">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="68059-2280">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2280">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="68059-2281">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2281">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2282">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2282">Appservice</span></span>

* <span data-ttu-id="68059-2283">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2283">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="68059-2284">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2284">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="68059-2285">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="68059-2285">Eventhubs</span></span>

* <span data-ttu-id="68059-2286">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-2286">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="68059-2287">拡張機能</span><span class="sxs-lookup"><span data-stu-id="68059-2287">Extension</span></span>

* <span data-ttu-id="68059-2288">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2288">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-2289">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-2289">Interactive</span></span>

* <span data-ttu-id="68059-2290">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="68059-2290">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="68059-2291">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="68059-2291">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="68059-2292">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="68059-2292">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="68059-2293">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2293">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-2294">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-2294">Monitor</span></span>

* <span data-ttu-id="68059-2295">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2295">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="68059-2296">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2296">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="68059-2297">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2297">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="68059-2298">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2298">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="68059-2299">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2299">Network</span></span>

* <span data-ttu-id="68059-2300">[重大な変更]`route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2300">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="68059-2301">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2301">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="68059-2302">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2302">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="68059-2303">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2303">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="68059-2304">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-2304">Profile</span></span>

* <span data-ttu-id="68059-2305">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2305">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="68059-2306">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2306">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-2307">RDBMS</span><span class="sxs-lookup"><span data-stu-id="68059-2307">RDBMS</span></span>

* <span data-ttu-id="68059-2308">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2308">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="68059-2309">Service Bus</span><span class="sxs-lookup"><span data-stu-id="68059-2309">Service Bus</span></span>

* <span data-ttu-id="68059-2310">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-2310">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2311">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2311">Storage</span></span>

* <span data-ttu-id="68059-2312">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-2312">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="68059-2313">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="68059-2313">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2314">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2314">VM</span></span>

* <span data-ttu-id="68059-2315">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2315">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="68059-2316">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2316">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="68059-2317">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2317">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="68059-2318">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2318">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="68059-2319">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="68059-2319">February 27, 2018</span></span>

<span data-ttu-id="68059-2320">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="68059-2320">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="68059-2321">コア</span><span class="sxs-lookup"><span data-stu-id="68059-2321">Core</span></span>

* <span data-ttu-id="68059-2322">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="68059-2322">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="68059-2323">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2323">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="68059-2324">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2324">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2325">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2325">ACS</span></span>

* <span data-ttu-id="68059-2326">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2326">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="68059-2327">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="68059-2327">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="68059-2328">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2328">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="68059-2329">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2329">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2330">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2330">Appservice</span></span>

* <span data-ttu-id="68059-2331">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="68059-2331">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="68059-2332">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="68059-2332">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="68059-2333">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="68059-2333">Cognitive Services</span></span>

* <span data-ttu-id="68059-2334">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2334">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="68059-2335">従量課金</span><span class="sxs-lookup"><span data-stu-id="68059-2335">Consumption</span></span>

* <span data-ttu-id="68059-2336">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2336">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="68059-2337">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2337">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="68059-2338">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-2338">Container</span></span>

* <span data-ttu-id="68059-2339">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2339">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="68059-2340">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2340">Network</span></span>

* <span data-ttu-id="68059-2341">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="68059-2341">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2342">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2342">Resource</span></span>

* <span data-ttu-id="68059-2343">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2343">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="68059-2344">Role</span><span class="sxs-lookup"><span data-stu-id="68059-2344">Role</span></span>

* <span data-ttu-id="68059-2345">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2345">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="68059-2346">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-2346">SQL</span></span>

* <span data-ttu-id="68059-2347">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2347">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2348">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2348">Storage</span></span>

* <span data-ttu-id="68059-2349">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2349">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2350">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2350">VM</span></span>

* <span data-ttu-id="68059-2351">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2351">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="68059-2352">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="68059-2352">February 13, 2018</span></span>

<span data-ttu-id="68059-2353">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="68059-2353">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="68059-2354">コア</span><span class="sxs-lookup"><span data-stu-id="68059-2354">Core</span></span>

* <span data-ttu-id="68059-2355">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2355">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2356">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2356">ACS</span></span>

* <span data-ttu-id="68059-2357">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2357">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="68059-2358">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2358">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="68059-2359">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2359">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="68059-2360">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2360">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="68059-2361">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2361">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="68059-2362">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="68059-2362">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="68059-2363">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2363">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="68059-2364">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="68059-2364">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2365">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2365">Appservice</span></span>

* <span data-ttu-id="68059-2366">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2366">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="68059-2367">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2367">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="68059-2368">CDN</span><span class="sxs-lookup"><span data-stu-id="68059-2368">CDN</span></span>

* <span data-ttu-id="68059-2369">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2369">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="68059-2370">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-2370">Container</span></span>

* <span data-ttu-id="68059-2371">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2371">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="68059-2372">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2372">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-2373">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-2373">CosmosDB</span></span>

* <span data-ttu-id="68059-2374">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2374">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="68059-2375">拡張機能</span><span class="sxs-lookup"><span data-stu-id="68059-2375">Extension</span></span>

* <span data-ttu-id="68059-2376">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2376">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="68059-2377">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2377">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="68059-2378">フィードバック</span><span class="sxs-lookup"><span data-stu-id="68059-2378">Feedback</span></span>

* <span data-ttu-id="68059-2379">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2379">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-2380">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-2380">Interactive</span></span>

* <span data-ttu-id="68059-2381">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2381">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="68059-2382">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2382">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="68059-2383">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-2383">IoT</span></span>

* <span data-ttu-id="68059-2384">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2384">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="68059-2385">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2385">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="68059-2386">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2386">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="68059-2387">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2387">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-2388">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-2388">Monitor</span></span>

* <span data-ttu-id="68059-2389">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2389">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="68059-2390">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2390">Network</span></span>

* <span data-ttu-id="68059-2391">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2391">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="68059-2392">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-2392">Profile</span></span>

* <span data-ttu-id="68059-2393">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2393">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2394">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2394">Resource</span></span>

* <span data-ttu-id="68059-2395">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2395">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="68059-2396">Role</span><span class="sxs-lookup"><span data-stu-id="68059-2396">Role</span></span>

* <span data-ttu-id="68059-2397">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2397">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="68059-2398">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-2398">SQL</span></span>

* <span data-ttu-id="68059-2399">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2399">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="68059-2400">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2400">Added `sql db rename`</span></span>
* <span data-ttu-id="68059-2401">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2401">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2402">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2402">Storage</span></span>

* <span data-ttu-id="68059-2403">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2403">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2404">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2404">VM</span></span>

* <span data-ttu-id="68059-2405">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2405">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="68059-2406">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2406">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="68059-2407">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="68059-2407">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="68059-2408">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="68059-2408">January 31, 2018</span></span>

<span data-ttu-id="68059-2409">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="68059-2409">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="68059-2410">コア</span><span class="sxs-lookup"><span data-stu-id="68059-2410">Core</span></span>

* <span data-ttu-id="68059-2411">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2411">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="68059-2412">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2412">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="68059-2413">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2413">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="68059-2414">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="68059-2414">Use `--verbose` to see</span></span>
* <span data-ttu-id="68059-2415">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-2415">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2416">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2416">ACS</span></span>

* <span data-ttu-id="68059-2417">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="68059-2417">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="68059-2418">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-2418">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2419">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2419">Appservice</span></span>

* <span data-ttu-id="68059-2420">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="68059-2420">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="68059-2421">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2421">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="68059-2422">CDN</span><span class="sxs-lookup"><span data-stu-id="68059-2422">CDN</span></span>

* <span data-ttu-id="68059-2423">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2423">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-2424">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-2424">CosmosDB</span></span>

* <span data-ttu-id="68059-2425">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2425">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-2426">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-2426">Interactive</span></span>

* <span data-ttu-id="68059-2427">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2427">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="68059-2428">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2428">Network</span></span>

* <span data-ttu-id="68059-2429">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2429">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="68059-2430">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2430">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="68059-2431">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2431">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="68059-2432">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2432">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="68059-2433">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2433">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="68059-2434">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2434">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="68059-2435">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2435">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="68059-2436">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2436">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="68059-2437">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2437">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="68059-2438">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="68059-2438">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="68059-2439">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-2439">Profile</span></span>

* <span data-ttu-id="68059-2440">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2440">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2441">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2441">Resource</span></span>

* <span data-ttu-id="68059-2442">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2442">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2443">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2443">Storage</span></span>

* <span data-ttu-id="68059-2444">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2444">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="68059-2445">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2445">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="68059-2446">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2446">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="68059-2447">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2447">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="68059-2448">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2448">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2449">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2449">VM</span></span>

* <span data-ttu-id="68059-2450">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2450">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="68059-2451">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2451">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="68059-2452">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2452">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="68059-2453">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2453">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="68059-2454">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="68059-2454">January 17, 2018</span></span>

<span data-ttu-id="68059-2455">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="68059-2455">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="68059-2456">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-2456">ACR</span></span>

* <span data-ttu-id="68059-2457">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2457">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="68059-2458">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2458">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2459">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2459">ACS</span></span>

* <span data-ttu-id="68059-2460">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2460">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="68059-2461">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2461">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2462">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2462">Appservice</span></span>

* <span data-ttu-id="68059-2463">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2463">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="68059-2464">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2464">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="68059-2465">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2465">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="68059-2466">バックアップ</span><span class="sxs-lookup"><span data-stu-id="68059-2466">Backup</span></span>

* <span data-ttu-id="68059-2467">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2467">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="68059-2468">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2468">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="68059-2469">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2469">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="68059-2470">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2470">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="68059-2471">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2471">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="68059-2472">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-2472">Batch</span></span>

* <span data-ttu-id="68059-2473">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2473">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="68059-2474">クラウド</span><span class="sxs-lookup"><span data-stu-id="68059-2474">Cloud</span></span>

* <span data-ttu-id="68059-2475">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2475">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="68059-2476">従量課金</span><span class="sxs-lookup"><span data-stu-id="68059-2476">Consumption</span></span>

* <span data-ttu-id="68059-2477">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2477">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="68059-2478">Event Grid</span><span class="sxs-lookup"><span data-stu-id="68059-2478">Event Grid</span></span>

* <span data-ttu-id="68059-2479">[重大な変更]`az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="68059-2479">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="68059-2480">[重大な変更]`az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="68059-2480">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="68059-2481">[重大な変更]`eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2481">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="68059-2482">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="68059-2482">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="68059-2483">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2483">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="68059-2484">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2484">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="68059-2485">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2485">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="68059-2486">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2486">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-2487">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-2487">Interactive</span></span>

* <span data-ttu-id="68059-2488">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="68059-2488">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="68059-2489">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2489">Fixed errors on startup</span></span>
* <span data-ttu-id="68059-2490">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2490">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="68059-2491">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-2491">IoT</span></span>

* <span data-ttu-id="68059-2492">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2492">Added support for device provisioning service</span></span>
* <span data-ttu-id="68059-2493">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2493">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="68059-2494">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2494">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-2495">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-2495">Monitor</span></span>

* <span data-ttu-id="68059-2496">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2496">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="68059-2497">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="68059-2497">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="68059-2498">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2498">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="68059-2499">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2499">Network</span></span>

* <span data-ttu-id="68059-2500">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2500">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="68059-2501">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2501">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="68059-2502">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-2502">Profile</span></span>

* <span data-ttu-id="68059-2503">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2503">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="68059-2504">Role</span><span class="sxs-lookup"><span data-stu-id="68059-2504">Role</span></span>

* <span data-ttu-id="68059-2505">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2505">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="68059-2506">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="68059-2506">Service Fabric</span></span>

* <span data-ttu-id="68059-2507">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2507">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="68059-2508">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2508">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2509">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2509">VM</span></span>

* <span data-ttu-id="68059-2510">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="68059-2510">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="68059-2511">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2511">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="68059-2512">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2512">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="68059-2513">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2513">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="68059-2514">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2514">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="68059-2515">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2515">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="68059-2516">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2516">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="68059-2517">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2517">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="68059-2518">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="68059-2518">December 19, 2017</span></span>

<span data-ttu-id="68059-2519">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="68059-2519">Version 2.0.23</span></span>

* <span data-ttu-id="68059-2520">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2520">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="68059-2521">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-2521">Container</span></span>

* <span data-ttu-id="68059-2522">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2522">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="68059-2523">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2523">Network</span></span>

* <span data-ttu-id="68059-2524">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2524">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="68059-2525">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2525">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2526">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2526">Storage</span></span>

* <span data-ttu-id="68059-2527">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2527">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2528">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2528">VM</span></span>

* <span data-ttu-id="68059-2529">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2529">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="68059-2530">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="68059-2530">December 5, 2017</span></span>

<span data-ttu-id="68059-2531">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="68059-2531">Version 2.0.22</span></span>

* <span data-ttu-id="68059-2532">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2532">Removed `az component` commands.</span></span> <span data-ttu-id="68059-2533">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="68059-2533">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="68059-2534">コア</span><span class="sxs-lookup"><span data-stu-id="68059-2534">Core</span></span>
* <span data-ttu-id="68059-2535">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2535">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="68059-2536">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2536">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2537">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2537">ACS</span></span>

* <span data-ttu-id="68059-2538">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2538">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="68059-2539">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2539">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="68059-2540">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2540">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="68059-2541">Advisor</span><span class="sxs-lookup"><span data-stu-id="68059-2541">Advisor</span></span>

* <span data-ttu-id="68059-2542">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-2542">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2543">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2543">Appservice</span></span>

* <span data-ttu-id="68059-2544">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2544">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="68059-2545">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2545">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="68059-2546">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2546">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="68059-2547">従量課金</span><span class="sxs-lookup"><span data-stu-id="68059-2547">Consumption</span></span>

* <span data-ttu-id="68059-2548">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2548">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="68059-2549">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-2549">Container</span></span>

* <span data-ttu-id="68059-2550">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2550">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-2551">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-2551">Monitor</span></span>

* <span data-ttu-id="68059-2552">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2552">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2553">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2553">Resource</span></span>

* <span data-ttu-id="68059-2554">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2554">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="68059-2555">Role</span><span class="sxs-lookup"><span data-stu-id="68059-2555">Role</span></span>

* <span data-ttu-id="68059-2556">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2556">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="68059-2557">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="68059-2557">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="68059-2558">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2558">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="68059-2559">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-2559">SQL</span></span>

* <span data-ttu-id="68059-2560">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2560">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="68059-2561">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2561">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2562">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2562">VM</span></span>

* <span data-ttu-id="68059-2563">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2563">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="68059-2564">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="68059-2564">November 14, 2017</span></span>

<span data-ttu-id="68059-2565">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="68059-2565">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="68059-2566">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-2566">ACR</span></span>

* <span data-ttu-id="68059-2567">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2567">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="68059-2568">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2568">ACS</span></span>

* <span data-ttu-id="68059-2569">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2569">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="68059-2570">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2570">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="68059-2571">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2571">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="68059-2572">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2572">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="68059-2573">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2573">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2574">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2574">Appservice</span></span>

* <span data-ttu-id="68059-2575">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2575">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="68059-2576">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2576">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="68059-2577">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2577">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="68059-2578">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2578">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="68059-2579">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2579">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="68059-2580">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="68059-2580">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="68059-2581">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-2581">Batch</span></span>

* <span data-ttu-id="68059-2582">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2582">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="68059-2583">Batchai</span><span class="sxs-lookup"><span data-stu-id="68059-2583">Batchai</span></span>

* <span data-ttu-id="68059-2584">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2584">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="68059-2585">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2585">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="68059-2586">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2586">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="68059-2587">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2587">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="68059-2588">クラウド</span><span class="sxs-lookup"><span data-stu-id="68059-2588">Cloud</span></span>

* <span data-ttu-id="68059-2589">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2589">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="68059-2590">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-2590">Container</span></span>

* <span data-ttu-id="68059-2591">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2591">Added support to open multiple ports</span></span>
* <span data-ttu-id="68059-2592">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2592">Added container group restart policy</span></span>
* <span data-ttu-id="68059-2593">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2593">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="68059-2594">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2594">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="68059-2595">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="68059-2595">Data Lake Analytics</span></span>

* <span data-ttu-id="68059-2596">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2596">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="68059-2597">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="68059-2597">Data Lake Store</span></span>

* <span data-ttu-id="68059-2598">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2598">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="68059-2599">拡張機能</span><span class="sxs-lookup"><span data-stu-id="68059-2599">Extension</span></span>

* <span data-ttu-id="68059-2600">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2600">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="68059-2601">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2601">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="68059-2602">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-2602">IoT</span></span>

* <span data-ttu-id="68059-2603">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2603">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-2604">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-2604">Monitor</span></span>

* <span data-ttu-id="68059-2605">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2605">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="68059-2606">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2606">Network</span></span>

* <span data-ttu-id="68059-2607">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2607">Added support for CAA DNS records</span></span>
* <span data-ttu-id="68059-2608">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2608">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="68059-2609">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2609">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="68059-2610">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2610">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="68059-2611">Reservations</span><span class="sxs-lookup"><span data-stu-id="68059-2611">Reservations</span></span>

* <span data-ttu-id="68059-2612">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="68059-2612">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2613">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2613">Resource</span></span>

* <span data-ttu-id="68059-2614">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2614">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="68059-2615">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-2615">SQL</span></span>

* <span data-ttu-id="68059-2616">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2616">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2617">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2617">Storage</span></span>

* <span data-ttu-id="68059-2618">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2618">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="68059-2619">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2619">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="68059-2620">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2620">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="68059-2621">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2621">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="68059-2622">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2622">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="68059-2623">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2623">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="68059-2624">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2624">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2625">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2625">VM</span></span>

* <span data-ttu-id="68059-2626">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2626">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="68059-2627">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2627">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="68059-2628">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2628">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="68059-2629">`vm format-secret` から `vm secret format` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-2629">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="68059-2630">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2630">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="68059-2631">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="68059-2631">October 24, 2017</span></span>

<span data-ttu-id="68059-2632">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="68059-2632">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="68059-2633">コア</span><span class="sxs-lookup"><span data-stu-id="68059-2633">Core</span></span>

* <span data-ttu-id="68059-2634">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2634">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="68059-2635">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-2635">ACR</span></span>

* <span data-ttu-id="68059-2636">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2636">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="68059-2637">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2637">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="68059-2638">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2638">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2639">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2639">ACS</span></span>

* <span data-ttu-id="68059-2640">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2640">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="68059-2641">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2641">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2642">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2642">Appservice</span></span>

* <span data-ttu-id="68059-2643">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2643">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="68059-2644">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="68059-2644">Component</span></span>

* <span data-ttu-id="68059-2645">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2645">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-2646">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-2646">Monitor</span></span>

* <span data-ttu-id="68059-2647">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2647">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2648">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2648">Resource</span></span>

* <span data-ttu-id="68059-2649">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2649">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="68059-2650">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2650">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2651">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2651">VM</span></span>

* <span data-ttu-id="68059-2652">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2652">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="68059-2653">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="68059-2653">October 9, 2017</span></span>

<span data-ttu-id="68059-2654">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="68059-2654">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="68059-2655">コア</span><span class="sxs-lookup"><span data-stu-id="68059-2655">Core</span></span>

* <span data-ttu-id="68059-2656">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2656">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2657">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2657">Appservice</span></span>

* <span data-ttu-id="68059-2658">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2658">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="68059-2659">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-2659">Batch</span></span>

* <span data-ttu-id="68059-2660">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2660">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="68059-2661">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2661">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="68059-2662">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2662">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="68059-2663">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2663">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="68059-2664">Batchai</span><span class="sxs-lookup"><span data-stu-id="68059-2664">Batchai</span></span>

* <span data-ttu-id="68059-2665">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-2665">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="68059-2666">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68059-2666">Keyvault</span></span>

* <span data-ttu-id="68059-2667">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2667">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="68059-2668">(#4448)</span><span class="sxs-lookup"><span data-stu-id="68059-2668">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="68059-2669">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2669">Network</span></span>

* <span data-ttu-id="68059-2670">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2670">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="68059-2671">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2671">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2672">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2672">Resource</span></span>

* <span data-ttu-id="68059-2673">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2673">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="68059-2674">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2674">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="68059-2675">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2675">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="68059-2676">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2676">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="68059-2677">Sql</span><span class="sxs-lookup"><span data-stu-id="68059-2677">Sql</span></span>

* <span data-ttu-id="68059-2678">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2678">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="68059-2679">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="68059-2679">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="68059-2680">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="68059-2680">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2681">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2681">Storage</span></span>

* <span data-ttu-id="68059-2682">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2682">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2683">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2683">Vm</span></span>

* <span data-ttu-id="68059-2684">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2684">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="68059-2685">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2685">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="68059-2686">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2686">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="68059-2687">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2687">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="68059-2688">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2688">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="68059-2689">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="68059-2689">September 22, 2017</span></span>

<span data-ttu-id="68059-2690">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="68059-2690">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2691">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2691">Resource</span></span>

* <span data-ttu-id="68059-2692">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2692">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="68059-2693">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2693">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="68059-2694">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2694">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="68059-2695">[重大な変更]`managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2695">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="68059-2696">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2696">Network</span></span>

* <span data-ttu-id="68059-2697">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2697">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="68059-2698">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2698">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="68059-2699">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2699">Added `asg` application security group commands</span></span>
* <span data-ttu-id="68059-2700">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2700">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="68059-2701">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2701">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="68059-2702">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2702">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="68059-2703">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2703">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2704">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2704">Storage</span></span>

* <span data-ttu-id="68059-2705">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2705">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="68059-2706">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="68059-2706">Eventgrid</span></span>

* <span data-ttu-id="68059-2707">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2707">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="68059-2708">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-2708">SQL</span></span>

* <span data-ttu-id="68059-2709">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2709">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="68059-2710">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="68059-2710">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="68059-2711">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2711">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="68059-2712">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68059-2712">Keyvault</span></span>

* <span data-ttu-id="68059-2713">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2713">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2714">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2714">VM</span></span>

* <span data-ttu-id="68059-2715">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2715">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="68059-2716">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2716">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="68059-2717">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2717">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="68059-2718">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2718">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="68059-2719">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2719">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="68059-2720">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2720">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2721">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2721">ACS</span></span>

* <span data-ttu-id="68059-2722">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2722">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2723">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2723">Appservice</span></span>

* <span data-ttu-id="68059-2724">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2724">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="68059-2725">バックアップ</span><span class="sxs-lookup"><span data-stu-id="68059-2725">Backup</span></span>

* <span data-ttu-id="68059-2726">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="68059-2726">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="68059-2727">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="68059-2727">September 11, 2017</span></span>

<span data-ttu-id="68059-2728">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="68059-2728">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="68059-2729">コア</span><span class="sxs-lookup"><span data-stu-id="68059-2729">Core</span></span>

* <span data-ttu-id="68059-2730">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2730">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="68059-2731">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2731">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2732">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2732">Acs</span></span>

* <span data-ttu-id="68059-2733">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2733">Added `acs list-locations` command</span></span>
* <span data-ttu-id="68059-2734">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="68059-2734">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2735">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2735">Appservice</span></span>

* <span data-ttu-id="68059-2736">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2736">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="68059-2737">CDN</span><span class="sxs-lookup"><span data-stu-id="68059-2737">CDN</span></span>

* <span data-ttu-id="68059-2738">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2738">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="68059-2739">拡張機能</span><span class="sxs-lookup"><span data-stu-id="68059-2739">Extension</span></span>

* <span data-ttu-id="68059-2740">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-2740">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="68059-2741">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68059-2741">Keyvault</span></span>

* <span data-ttu-id="68059-2742">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2742">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="68059-2743">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2743">Network</span></span>

* <span data-ttu-id="68059-2744">`vnet list-private-access-services` から `vnet list-endpoint-services` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-2744">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="68059-2745">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2745">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="68059-2746">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2746">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="68059-2747">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2747">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="68059-2748">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2748">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="68059-2749">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-2749">Resource</span></span>

* <span data-ttu-id="68059-2750">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="68059-2750">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="68059-2751">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="68059-2751">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="68059-2752">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="68059-2752">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="68059-2753">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="68059-2753">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="68059-2754">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-2754">SQL</span></span>

* <span data-ttu-id="68059-2755">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2755">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2756">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2756">VM</span></span>

* <span data-ttu-id="68059-2757">固定:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="68059-2757">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="68059-2758">固定:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="68059-2758">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="68059-2759">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2759">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="68059-2760">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="68059-2760">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="68059-2761">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="68059-2761">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="68059-2762">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="68059-2762">August 31, 2017</span></span>

<span data-ttu-id="68059-2763">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="68059-2763">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="68059-2764">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68059-2764">Keyvault</span></span>

* <span data-ttu-id="68059-2765">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2765">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="68059-2766">SF</span><span class="sxs-lookup"><span data-stu-id="68059-2766">Sf</span></span>

* <span data-ttu-id="68059-2767">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="68059-2767">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2768">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2768">Storage</span></span>

* <span data-ttu-id="68059-2769">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2769">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="68059-2770">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="68059-2770">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="68059-2771">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="68059-2771">August 28, 2017</span></span>

<span data-ttu-id="68059-2772">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="68059-2772">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="68059-2773">CLI</span><span class="sxs-lookup"><span data-stu-id="68059-2773">CLI</span></span>

* <span data-ttu-id="68059-2774">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2774">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2775">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2775">ACS</span></span>

* <span data-ttu-id="68059-2776">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2776">Corrected preview regions</span></span>
* <span data-ttu-id="68059-2777">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2777">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="68059-2778">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="68059-2778">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2779">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2779">Appservice</span></span>

* <span data-ttu-id="68059-2780">[重大な変更]`az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2780">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="68059-2781">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2781">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="68059-2782">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="68059-2782">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="68059-2783">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="68059-2783">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="68059-2784">固定:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="68059-2784">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="68059-2785">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-2785">IoT</span></span>

* <span data-ttu-id="68059-2786">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="68059-2786">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="68059-2787">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2787">Network</span></span>

* <span data-ttu-id="68059-2788">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2788">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="68059-2789">[重大な変更]`vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2789">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="68059-2790">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2790">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="68059-2791">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2791">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="68059-2792">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2792">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="68059-2793">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-2793">Profile</span></span>

* <span data-ttu-id="68059-2794">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="68059-2794">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="68059-2795">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="68059-2795">Service Fabric</span></span>

* <span data-ttu-id="68059-2796">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="68059-2796">Preview release</span></span>
* <span data-ttu-id="68059-2797">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="68059-2797">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="68059-2798">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2798">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="68059-2799">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2799">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2800">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2800">Storage</span></span>

* <span data-ttu-id="68059-2801">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2801">Enabled setting blob tier</span></span>
* <span data-ttu-id="68059-2802">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2802">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="68059-2803">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2803">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="68059-2804">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2804">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="68059-2805">[重大な変更]`az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2805">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="68059-2806">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="68059-2806">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2807">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2807">VM</span></span>

* <span data-ttu-id="68059-2808">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2808">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="68059-2809">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2809">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="68059-2810">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2810">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="68059-2811">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2811">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="68059-2812">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2812">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="68059-2813">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2813">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="68059-2814">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="68059-2814">August 15, 2017</span></span>

<span data-ttu-id="68059-2815">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="68059-2815">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2816">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2816">ACS</span></span>

* <span data-ttu-id="68059-2817">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2817">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2818">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2818">Appservice</span></span>

* <span data-ttu-id="68059-2819">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2819">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="68059-2820">Event Grid</span><span class="sxs-lookup"><span data-stu-id="68059-2820">Event Grid</span></span>

* <span data-ttu-id="68059-2821">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2821">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="68059-2822">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="68059-2822">August 11, 2017</span></span>

<span data-ttu-id="68059-2823">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="68059-2823">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2824">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2824">ACS</span></span>

* <span data-ttu-id="68059-2825">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2825">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="68059-2826">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-2826">Batch</span></span>

* <span data-ttu-id="68059-2827">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="68059-2827">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="68059-2828">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2828">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="68059-2829">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2829">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="68059-2830">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-2830">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="68059-2831">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2831">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="68059-2832">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2832">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="68059-2833">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="68059-2833">Component</span></span>

* <span data-ttu-id="68059-2834">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2834">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="68059-2835">コンテナー</span><span class="sxs-lookup"><span data-stu-id="68059-2835">Container</span></span>

* <span data-ttu-id="68059-2836">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2836">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="68059-2837">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="68059-2837">Data Lake Store</span></span>

* <span data-ttu-id="68059-2838">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2838">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="68059-2839">Event Grid</span><span class="sxs-lookup"><span data-stu-id="68059-2839">Event Grid</span></span>

* <span data-ttu-id="68059-2840">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-2840">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="68059-2841">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2841">Network</span></span>

* <span data-ttu-id="68059-2842">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2842">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="68059-2843">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2843">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="68059-2844">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2844">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="68059-2845">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2845">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="68059-2846">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-2846">Profile</span></span>

* <span data-ttu-id="68059-2847">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2847">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="68059-2848">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-2848">Storage</span></span>

* <span data-ttu-id="68059-2849">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="68059-2849">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="68059-2850">VM</span><span class="sxs-lookup"><span data-stu-id="68059-2850">VM</span></span>

* <span data-ttu-id="68059-2851">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="68059-2851">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="68059-2852">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="68059-2852">Exposed `list-skus` command</span></span>
* <span data-ttu-id="68059-2853">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2853">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="68059-2854">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="68059-2854">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="68059-2855">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2855">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="68059-2856">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="68059-2856">July 28, 2017</span></span>

<span data-ttu-id="68059-2857">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="68059-2857">Version 2.0.12</span></span>

* <span data-ttu-id="68059-2858">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2858">Added container commands</span></span>
* <span data-ttu-id="68059-2859">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2859">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="68059-2860">コア</span><span class="sxs-lookup"><span data-stu-id="68059-2860">Core</span></span>

* <span data-ttu-id="68059-2861">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="68059-2861">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="68059-2862">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2862">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="68059-2863">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="68059-2863">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="68059-2864">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="68059-2864">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="68059-2865">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="68059-2865">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="68059-2866">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="68059-2866">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="68059-2867">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="68059-2867">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="68059-2868">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="68059-2868">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="68059-2869">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="68059-2869">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="68059-2870">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="68059-2870">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="68059-2871">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="68059-2871">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="68059-2872">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="68059-2872">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="68059-2873">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="68059-2873">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="68059-2874">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="68059-2874">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="68059-2875">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2875">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="68059-2876">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="68059-2876">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="68059-2877">ACR</span><span class="sxs-lookup"><span data-stu-id="68059-2877">ACR</span></span>

* <span data-ttu-id="68059-2878">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2878">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="68059-2879">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2879">Support SKU update for managed registries</span></span>
* <span data-ttu-id="68059-2880">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2880">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="68059-2881">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2881">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="68059-2882">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2882">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="68059-2883">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2883">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="68059-2884">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-2884">ACS</span></span>

* <span data-ttu-id="68059-2885">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2885">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-2886">Appservice</span><span class="sxs-lookup"><span data-stu-id="68059-2886">Appservice</span></span>

* <span data-ttu-id="68059-2887">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2887">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="68059-2888">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2888">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="68059-2889">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="68059-2889">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="68059-2890">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="68059-2890">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="68059-2891">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="68059-2891">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="68059-2892">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="68059-2892">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="68059-2893">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="68059-2893">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="68059-2894">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="68059-2894">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="68059-2895">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2895">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="68059-2896">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="68059-2896">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="68059-2897">Batch</span><span class="sxs-lookup"><span data-stu-id="68059-2897">Batch</span></span>

* <span data-ttu-id="68059-2898">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="68059-2898">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="68059-2899">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2899">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="68059-2900">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2900">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="68059-2901">CDN</span><span class="sxs-lookup"><span data-stu-id="68059-2901">CDN</span></span>

* <span data-ttu-id="68059-2902">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2902">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="68059-2903">クラウド</span><span class="sxs-lookup"><span data-stu-id="68059-2903">Cloud</span></span>

* <span data-ttu-id="68059-2904">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="68059-2904">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="68059-2905">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="68059-2905">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="68059-2906">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2906">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="68059-2907">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="68059-2907">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="68059-2908">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="68059-2908">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-2909">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-2909">CosmosDB</span></span>

* <span data-ttu-id="68059-2910">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2910">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="68059-2911">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2911">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="68059-2912">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="68059-2912">Data Lake Analytics</span></span>

* <span data-ttu-id="68059-2913">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2913">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="68059-2914">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2914">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="68059-2915">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2915">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="68059-2916">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="68059-2916">Data Lake Store</span></span>

* <span data-ttu-id="68059-2917">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2917">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="68059-2918">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="68059-2918">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="68059-2919">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2919">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="68059-2920">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="68059-2920">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="68059-2921">Interactive</span><span class="sxs-lookup"><span data-stu-id="68059-2921">Interactive</span></span>

* <span data-ttu-id="68059-2922">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="68059-2922">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="68059-2923">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="68059-2923">Increased test coverage</span></span>
* <span data-ttu-id="68059-2924">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="68059-2924">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="68059-2925">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="68059-2925">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="68059-2926">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="68059-2926">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="68059-2927">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="68059-2927">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="68059-2928">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="68059-2928">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="68059-2929">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2929">Added `--progress` flag</span></span>
* <span data-ttu-id="68059-2930">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2930">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="68059-2931">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="68059-2931">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="68059-2932">IoT</span><span class="sxs-lookup"><span data-stu-id="68059-2932">IoT</span></span>

* <span data-ttu-id="68059-2933">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2933">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="68059-2934">(#3934)</span><span class="sxs-lookup"><span data-stu-id="68059-2934">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="68059-2935">Key Vault</span><span class="sxs-lookup"><span data-stu-id="68059-2935">Key vault</span></span>

* <span data-ttu-id="68059-2936">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2936">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="68059-2937">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="68059-2937">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="68059-2938">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="68059-2938">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="68059-2939">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="68059-2939">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="68059-2940">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="68059-2940">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="68059-2941">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="68059-2941">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="68059-2942">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2942">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="68059-2943">(#3307)</span><span class="sxs-lookup"><span data-stu-id="68059-2943">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="68059-2944">ラボ</span><span class="sxs-lookup"><span data-stu-id="68059-2944">Lab</span></span>

* <span data-ttu-id="68059-2945">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2945">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="68059-2946">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2946">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-2947">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-2947">Monitor</span></span>

* <span data-ttu-id="68059-2948">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="68059-2948">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="68059-2949">`monitor alert-rule-incidents list` から `monitor alert list-incidents` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-2949">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="68059-2950">`monitor alert-rule-incidents show` から `monitor alert show-incident` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-2950">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="68059-2951">`monitor metric-defintions list` から `monitor metrics list-definitions` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-2951">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="68059-2952">`monitor alert-rules` から `monitor alert` への名称変更</span><span class="sxs-lookup"><span data-stu-id="68059-2952">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="68059-2953">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="68059-2953">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="68059-2954">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="68059-2954">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="68059-2955">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-2955">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="68059-2956">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="68059-2956">`location` no longer required</span></span>
  * <span data-ttu-id="68059-2957">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="68059-2957">Add name and ID support for target</span></span>
  * <span data-ttu-id="68059-2958">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="68059-2958">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="68059-2959">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="68059-2959">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="68059-2960">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-2960">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="68059-2961">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="68059-2961">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="68059-2962">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2962">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="68059-2963">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2963">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="68059-2964">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-2964">Network</span></span>

* <span data-ttu-id="68059-2965">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2965">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="68059-2966">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2966">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="68059-2967">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2967">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="68059-2968">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2968">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="68059-2969">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2969">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="68059-2970">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2970">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="68059-2971">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2971">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="68059-2972">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2972">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="68059-2973">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2973">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="68059-2974">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2974">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="68059-2975">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2975">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="68059-2976">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2976">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="68059-2977">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2977">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="68059-2978">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2978">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="68059-2979">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2979">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="68059-2980">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-2980">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="68059-2981">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2981">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="68059-2982">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2982">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="68059-2983">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2983">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="68059-2984">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2984">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="68059-2985">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2985">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="68059-2986">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-2986">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="68059-2987">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-2987">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="68059-2988">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="68059-2988">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="68059-2989">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="68059-2989">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="68059-2990">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="68059-2990">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="68059-2991">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="68059-2991">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="68059-2992">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-2992">Profile</span></span>

* <span data-ttu-id="68059-2993">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2993">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="68059-2994">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2994">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="68059-2995">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="68059-2995">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="68059-2996">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-2996">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="68059-2997">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-2997">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="68059-2998">RDBMS</span><span class="sxs-lookup"><span data-stu-id="68059-2998">RDBMS</span></span>

* <span data-ttu-id="68059-2999">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="68059-2999">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="68059-3000">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="68059-3000">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="68059-3001">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="68059-3001">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="68059-3002">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="68059-3002">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="68059-3003">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-3003">Resource</span></span>

* <span data-ttu-id="68059-3004">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-3004">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="68059-3005">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="68059-3005">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="68059-3006">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-3006">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="68059-3007">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-3007">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="68059-3008">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="68059-3008">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="68059-3009">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-3009">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="68059-3010">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="68059-3010">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="68059-3011">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-3011">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="68059-3012">Role</span><span class="sxs-lookup"><span data-stu-id="68059-3012">Role</span></span>

* <span data-ttu-id="68059-3013">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-3013">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="68059-3014">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="68059-3014">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="68059-3015">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="68059-3015">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="68059-3016">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="68059-3016">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="68059-3017">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-3017">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="68059-3018">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="68059-3018">Service Fabric</span></span>
* <span data-ttu-id="68059-3019">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="68059-3019">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="68059-3020">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="68059-3020">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="68059-3021">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="68059-3021">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="68059-3022">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-3022">SQL</span></span>

* <span data-ttu-id="68059-3023">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-3023">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="68059-3024">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="68059-3024">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="68059-3025">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-3025">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="68059-3026">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-3026">Storage</span></span>

* <span data-ttu-id="68059-3027">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="68059-3027">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="68059-3028">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="68059-3028">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="68059-3029">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="68059-3029">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="68059-3030">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="68059-3030">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="68059-3031">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="68059-3031">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="68059-3032">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="68059-3032">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="68059-3033">VM</span><span class="sxs-lookup"><span data-stu-id="68059-3033">VM</span></span>

* <span data-ttu-id="68059-3034">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-3034">Support configuring nsg</span></span>
* <span data-ttu-id="68059-3035">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-3035">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="68059-3036">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="68059-3036">Support managed service identities</span></span>
* <span data-ttu-id="68059-3037">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-3037">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="68059-3038">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="68059-3038">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="68059-3039">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="68059-3039">May 10, 2017</span></span>

<span data-ttu-id="68059-3040">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="68059-3040">Version 2.0.6</span></span>

* <span data-ttu-id="68059-3041">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="68059-3041">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="68059-3042">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3042">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="68059-3043">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3043">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="68059-3044">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3044">Include Cognitive Services module</span></span>
* <span data-ttu-id="68059-3045">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3045">Include Service Fabric module</span></span>
* <span data-ttu-id="68059-3046">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="68059-3046">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="68059-3047">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3047">Add support for CDN commands</span></span>
* <span data-ttu-id="68059-3048">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="68059-3048">Remove Container module</span></span>
* <span data-ttu-id="68059-3049">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="68059-3049">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="68059-3050">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="68059-3050">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="68059-3051">コア</span><span class="sxs-lookup"><span data-stu-id="68059-3051">Core</span></span>

* <span data-ttu-id="68059-3052">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="68059-3052">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="68059-3053">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="68059-3053">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="68059-3054">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="68059-3054">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="68059-3055">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="68059-3055">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="68059-3056">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="68059-3056">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="68059-3057">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="68059-3057">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="68059-3058">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="68059-3058">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="68059-3059">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="68059-3059">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="68059-3060">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="68059-3060">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="68059-3061">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="68059-3061">core: Improved performance</span></span>
* <span data-ttu-id="68059-3062">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="68059-3062">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="68059-3063">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="68059-3063">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="68059-3064">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-3064">ACS</span></span>

* <span data-ttu-id="68059-3065">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-3065">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="68059-3066">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="68059-3066">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="68059-3067">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="68059-3067">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="68059-3068">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="68059-3068">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-3069">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-3069">AppService</span></span>

* <span data-ttu-id="68059-3070">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3070">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="68059-3071">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3071">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="68059-3072">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="68059-3072">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="68059-3073">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="68059-3073">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="68059-3074">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="68059-3074">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="68059-3075">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="68059-3075">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="68059-3076">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="68059-3076">support slot swap with preview</span></span>
* <span data-ttu-id="68059-3077">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="68059-3077">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="68059-3078">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="68059-3078">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="68059-3079">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="68059-3079">CosmosDB</span></span>

* <span data-ttu-id="68059-3080">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="68059-3080">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="68059-3081">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3081">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="68059-3082">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3082">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="68059-3083">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3083">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="68059-3084">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="68059-3084">Data Lake Analytics</span></span>

* <span data-ttu-id="68059-3085">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-3085">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="68059-3086">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="68059-3086">Add support for new catalog item type: package.</span></span> <span data-ttu-id="68059-3087">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="68059-3087">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="68059-3088">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="68059-3088">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="68059-3089">テーブル</span><span class="sxs-lookup"><span data-stu-id="68059-3089">Table</span></span>
  * <span data-ttu-id="68059-3090">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="68059-3090">Table valued function</span></span>
  * <span data-ttu-id="68059-3091">表示</span><span class="sxs-lookup"><span data-stu-id="68059-3091">View</span></span>
  * <span data-ttu-id="68059-3092">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="68059-3092">Table Statistics.</span></span> <span data-ttu-id="68059-3093">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="68059-3093">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="68059-3094">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="68059-3094">Data Lake Store</span></span>

* <span data-ttu-id="68059-3095">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="68059-3095">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="68059-3096">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="68059-3096">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="68059-3097">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="68059-3097">missed help for access show.</span></span> <span data-ttu-id="68059-3098">追加しました</span><span class="sxs-lookup"><span data-stu-id="68059-3098">adding it.</span></span> <span data-ttu-id="68059-3099">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="68059-3099">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="68059-3100">Find</span><span class="sxs-lookup"><span data-stu-id="68059-3100">Find</span></span>

* <span data-ttu-id="68059-3101">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="68059-3101">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="68059-3102">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68059-3102">KeyVault</span></span>

* <span data-ttu-id="68059-3103">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="68059-3103">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="68059-3104">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="68059-3104">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="68059-3105">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="68059-3105">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="68059-3106">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-3106">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="68059-3107">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="68059-3107">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="68059-3108">ラボ</span><span class="sxs-lookup"><span data-stu-id="68059-3108">Lab</span></span>

* <span data-ttu-id="68059-3109">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3109">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="68059-3110">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3110">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="68059-3111">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3111">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="68059-3112">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3112">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="68059-3113">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3113">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="68059-3114">モニター</span><span class="sxs-lookup"><span data-stu-id="68059-3114">Monitor</span></span>

* <span data-ttu-id="68059-3115">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="68059-3115">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="68059-3116">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="68059-3116">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="68059-3117">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-3117">Network</span></span>

* <span data-ttu-id="68059-3118">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3118">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="68059-3119">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3119">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="68059-3120">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3120">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="68059-3121">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3121">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="68059-3122">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3122">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="68059-3123">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3123">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="68059-3124">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3124">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="68059-3125">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3125">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="68059-3126">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-3126">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="68059-3127">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3127">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="68059-3128">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="68059-3128">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="68059-3129">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-3129">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="68059-3130">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-3130">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="68059-3131">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-3131">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="68059-3132">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="68059-3132">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="68059-3133">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3133">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="68059-3134">プロファイル</span><span class="sxs-lookup"><span data-stu-id="68059-3134">Profile</span></span>

* <span data-ttu-id="68059-3135">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="68059-3135">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="68059-3136">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="68059-3136">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="68059-3137">Redis</span><span class="sxs-lookup"><span data-stu-id="68059-3137">Redis</span></span>

* <span data-ttu-id="68059-3138">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3138">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="68059-3139">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="68059-3139">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="68059-3140">リソース</span><span class="sxs-lookup"><span data-stu-id="68059-3140">Resource</span></span>

* <span data-ttu-id="68059-3141">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="68059-3141">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="68059-3142">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="68059-3142">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="68059-3143">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="68059-3143">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="68059-3144">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="68059-3144">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="68059-3145">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="68059-3145">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="68059-3146">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3146">Add docs for az lock update.</span></span> <span data-ttu-id="68059-3147">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="68059-3147">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="68059-3148">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="68059-3148">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="68059-3149">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="68059-3149">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="68059-3150">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="68059-3150">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="68059-3151">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="68059-3151">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="68059-3152">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="68059-3152">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="68059-3153">Role</span><span class="sxs-lookup"><span data-stu-id="68059-3153">Role</span></span>

* <span data-ttu-id="68059-3154">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="68059-3154">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="68059-3155">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="68059-3155">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="68059-3156">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="68059-3156">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="68059-3157">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="68059-3157">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="68059-3158">SQL</span><span class="sxs-lookup"><span data-stu-id="68059-3158">SQL</span></span>

* <span data-ttu-id="68059-3159">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="68059-3159">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="68059-3160">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="68059-3160">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="68059-3161">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-3161">Storage</span></span>

* <span data-ttu-id="68059-3162">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="68059-3162">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="68059-3163">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3163">Add support for incremental blob copy</span></span>
* <span data-ttu-id="68059-3164">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="68059-3164">Add support for large block blob upload</span></span>
* <span data-ttu-id="68059-3165">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="68059-3165">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="68059-3166">VM</span><span class="sxs-lookup"><span data-stu-id="68059-3166">VM</span></span>

* <span data-ttu-id="68059-3167">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="68059-3167">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="68059-3168">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="68059-3168">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="68059-3169">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="68059-3169">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="68059-3170">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="68059-3170">az vm/vmss disk</span></span>
  3. <span data-ttu-id="68059-3171">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="68059-3171">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="68059-3172">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="68059-3172">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="68059-3173">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="68059-3173">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="68059-3174">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="68059-3174">April 3, 2017</span></span>

<span data-ttu-id="68059-3175">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="68059-3175">Version 2.0.2</span></span>

<span data-ttu-id="68059-3176">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="68059-3176">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="68059-3177">コア</span><span class="sxs-lookup"><span data-stu-id="68059-3177">Core</span></span>

* <span data-ttu-id="68059-3178">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="68059-3178">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="68059-3179">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="68059-3179">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="68059-3180">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="68059-3180">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="68059-3181">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="68059-3181">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="68059-3182">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="68059-3182">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="68059-3183">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="68059-3183">Add prompting for missing template parameters.</span></span> <span data-ttu-id="68059-3184">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="68059-3184">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="68059-3185">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="68059-3185">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="68059-3186">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="68059-3186">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="68059-3187">ACS</span><span class="sxs-lookup"><span data-stu-id="68059-3187">ACS</span></span>

* <span data-ttu-id="68059-3188">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="68059-3188">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="68059-3189">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="68059-3189">Add support for ssh key password prompting.</span></span> <span data-ttu-id="68059-3190">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="68059-3190">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="68059-3191">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="68059-3191">Add support for windows clusters.</span></span> <span data-ttu-id="68059-3192">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="68059-3192">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="68059-3193">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="68059-3193">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="68059-3194">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="68059-3194">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="68059-3195">AppService</span><span class="sxs-lookup"><span data-stu-id="68059-3195">AppService</span></span>

* <span data-ttu-id="68059-3196">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="68059-3196">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="68059-3197">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="68059-3197">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="68059-3198">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="68059-3198">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="68059-3199">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="68059-3199">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="68059-3200">DataLake</span><span class="sxs-lookup"><span data-stu-id="68059-3200">DataLake</span></span>

* <span data-ttu-id="68059-3201">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-3201">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="68059-3202">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="68059-3202">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="68059-3203">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="68059-3203">DocuemntDB</span></span>

* <span data-ttu-id="68059-3204">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="68059-3204">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="68059-3205">VM</span><span class="sxs-lookup"><span data-stu-id="68059-3205">VM</span></span>

* <span data-ttu-id="68059-3206">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="68059-3206">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="68059-3207">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="68059-3207">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="68059-3208">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="68059-3208">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="68059-3209">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="68059-3209">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="68059-3210">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="68059-3210">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="68059-3211">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="68059-3211">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="68059-3212">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="68059-3212">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="68059-3213">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="68059-3213">February 27, 2017</span></span>

<span data-ttu-id="68059-3214">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="68059-3214">Version 2.0.0</span></span>

<span data-ttu-id="68059-3215">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="68059-3215">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="68059-3216">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="68059-3216">Container Service (acs)</span></span>
- <span data-ttu-id="68059-3217">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="68059-3217">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="68059-3218">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="68059-3218">Networking</span></span>
- <span data-ttu-id="68059-3219">ストレージ</span><span class="sxs-lookup"><span data-stu-id="68059-3219">Storage</span></span>

<span data-ttu-id="68059-3220">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="68059-3220">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="68059-3221">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="68059-3221">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="68059-3222">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="68059-3222">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="68059-3223">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="68059-3223">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="68059-3224">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="68059-3224">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="68059-3225">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="68059-3225">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="68059-3226">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="68059-3226">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="68059-3227">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="68059-3227">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="68059-3228">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="68059-3228">Provide feedback from the command line with the `az feedback` command</span></span>

