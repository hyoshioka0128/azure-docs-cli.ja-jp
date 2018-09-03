---
title: Azure CLI 2.0 リリース ノート
description: Azure CLI 2.0 の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 08/28/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 62e57d048666f478b670f182bb9348dba90de6a0
ms.sourcegitcommit: 8f060bc009278eafc0ed448bad4b7d08c742ff63
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/29/2018
ms.locfileid: "43145092"
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="07aba-103">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="07aba-103">Azure CLI 2.0 release notes</span></span>

## <a name="auguest-28-2018"></a><span data-ttu-id="07aba-104">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="07aba-104">Auguest 28, 2018</span></span>

<span data-ttu-id="07aba-105">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="07aba-105">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="07aba-106">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-106">Core</span></span>

* <span data-ttu-id="07aba-107">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-107">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="07aba-108">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-108">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-109">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-109">ACR</span></span>

* <span data-ttu-id="07aba-110">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-110">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="07aba-111">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-111">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-112">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-112">ACS</span></span>

* <span data-ttu-id="07aba-113">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-113">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="07aba-114">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-114">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-115">AppService</span><span class="sxs-lookup"><span data-stu-id="07aba-115">AppService</span></span>

* <span data-ttu-id="07aba-116">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-116">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="07aba-117">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-117">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="07aba-118">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-118">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="07aba-119">Backup</span><span class="sxs-lookup"><span data-stu-id="07aba-119">Backup</span></span>

* <span data-ttu-id="07aba-120">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-120">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="07aba-121">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="07aba-121">Bot Service</span></span>

* <span data-ttu-id="07aba-122">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="07aba-122">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="07aba-123">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="07aba-123">Cognitive Services</span></span>

* <span data-ttu-id="07aba-124">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-124">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="07aba-125">IoT</span><span class="sxs-lookup"><span data-stu-id="07aba-125">IoT</span></span>

* <span data-ttu-id="07aba-126">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-126">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="07aba-127">監視</span><span class="sxs-lookup"><span data-stu-id="07aba-127">Monitor</span></span>

* <span data-ttu-id="07aba-128">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-128">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="07aba-129">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-129">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="07aba-130">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-130">Network</span></span>

* <span data-ttu-id="07aba-131">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-131">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-132">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-132">Resource</span></span>

* <span data-ttu-id="07aba-133">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-133">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-134">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-134">Storage</span></span>

* <span data-ttu-id="07aba-135">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-135">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-136">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-136">VM</span></span>

* <span data-ttu-id="07aba-137">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-137">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="07aba-138">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-138">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="07aba-139">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="07aba-139">Auguest 14, 2018</span></span>

<span data-ttu-id="07aba-140">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="07aba-140">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="07aba-141">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-141">Core</span></span>

* <span data-ttu-id="07aba-142">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-142">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="07aba-143">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-143">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="07aba-144">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="07aba-144">Telemetry</span></span>

* <span data-ttu-id="07aba-145">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-145">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-146">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-146">ACR</span></span>

* <span data-ttu-id="07aba-147">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-147">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="07aba-148">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-148">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-149">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-149">ACS</span></span>

* <span data-ttu-id="07aba-150">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-150">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="07aba-151">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-151">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="07aba-152">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-152">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="07aba-153">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-153">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="07aba-154">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-154">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="07aba-155">AppService</span><span class="sxs-lookup"><span data-stu-id="07aba-155">AppService</span></span>

* <span data-ttu-id="07aba-156">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-156">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="07aba-157">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-157">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="07aba-158">BatchAI</span><span class="sxs-lookup"><span data-stu-id="07aba-158">BatchAI</span></span>

* <span data-ttu-id="07aba-159">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-159">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="07aba-160">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-160">Container</span></span>

* <span data-ttu-id="07aba-161">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-161">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="07aba-162">IoT</span><span class="sxs-lookup"><span data-stu-id="07aba-162">IoT</span></span>

* <span data-ttu-id="07aba-163">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-163">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="07aba-164">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-164">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="07aba-165">Iot Central</span><span class="sxs-lookup"><span data-stu-id="07aba-165">Iot Central</span></span>

* <span data-ttu-id="07aba-166">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-166">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="07aba-167">KeyVault</span><span class="sxs-lookup"><span data-stu-id="07aba-167">KeyVault</span></span>


* <span data-ttu-id="07aba-168">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-168">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="07aba-169">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-169">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="07aba-170">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-170">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="07aba-171">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-171">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="07aba-172">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-172">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="07aba-173">リレー</span><span class="sxs-lookup"><span data-stu-id="07aba-173">Relay</span></span>

* <span data-ttu-id="07aba-174">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-174">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-175">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-175">Sql</span></span>

* <span data-ttu-id="07aba-176">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-176">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-177">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-177">Storage</span></span>

* <span data-ttu-id="07aba-178">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="07aba-178">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="07aba-179">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-179">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="07aba-180">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="07aba-180">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="07aba-181">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-181">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="07aba-182">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-182">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-183">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-183">VM</span></span>

* <span data-ttu-id="07aba-184">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-184">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="07aba-185">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="07aba-185">July 31, 2018</span></span>

<span data-ttu-id="07aba-186">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="07aba-186">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-187">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-187">ACR</span></span>

* <span data-ttu-id="07aba-188">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-188">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="07aba-189">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-189">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-190">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-190">ACS</span></span>

* <span data-ttu-id="07aba-191">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-191">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="07aba-192">Batch</span><span class="sxs-lookup"><span data-stu-id="07aba-192">Batch</span></span>

* <span data-ttu-id="07aba-193">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-193">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="07aba-194">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-194">Container</span></span>

* <span data-ttu-id="07aba-195">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-195">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="07aba-196">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-196">Network</span></span>

* <span data-ttu-id="07aba-197">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-197">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="07aba-198">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-198">Resource</span></span>

* <span data-ttu-id="07aba-199">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-199">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="07aba-200">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-200">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="07aba-201">Role</span><span class="sxs-lookup"><span data-stu-id="07aba-201">Role</span></span>

* <span data-ttu-id="07aba-202">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-202">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="07aba-203">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-203">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="07aba-204">Search</span><span class="sxs-lookup"><span data-stu-id="07aba-204">Search</span></span>

* <span data-ttu-id="07aba-205">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-205">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="07aba-206">Service Bus</span><span class="sxs-lookup"><span data-stu-id="07aba-206">Service Bus</span></span>

* <span data-ttu-id="07aba-207">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-207">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="07aba-208">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-208">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="07aba-209">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="07aba-209">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="07aba-210">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="07aba-210">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-211">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-211">Storage</span></span>

* <span data-ttu-id="07aba-212">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-212">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="07aba-213">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="07aba-213">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-214">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-214">VM</span></span>

* <span data-ttu-id="07aba-215">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-215">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="07aba-216">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-216">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="07aba-217">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-217">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="07aba-218">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-218">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="07aba-219">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="07aba-219">July 18, 2018</span></span>

<span data-ttu-id="07aba-220">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="07aba-220">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="07aba-221">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-221">Core</span></span>

* <span data-ttu-id="07aba-222">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-222">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="07aba-223">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-223">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="07aba-224">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-224">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-225">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-225">ACR</span></span>

* <span data-ttu-id="07aba-226">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-226">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="07aba-227">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-227">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="07aba-228">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-228">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="07aba-229">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-229">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-230">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-230">ACS</span></span>

* <span data-ttu-id="07aba-231">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-231">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-232">AppService</span><span class="sxs-lookup"><span data-stu-id="07aba-232">AppService</span></span>

* <span data-ttu-id="07aba-233">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-233">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="07aba-234">Batch</span><span class="sxs-lookup"><span data-stu-id="07aba-234">Batch</span></span>

* <span data-ttu-id="07aba-235">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-235">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="07aba-236">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-236">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="07aba-237">Batch AI</span><span class="sxs-lookup"><span data-stu-id="07aba-237">Batch AI</span></span>

* <span data-ttu-id="07aba-238">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-238">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="07aba-239">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-239">Container</span></span>

* <span data-ttu-id="07aba-240">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-240">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="07aba-241">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-241">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="07aba-242">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-242">Network</span></span>

* <span data-ttu-id="07aba-243">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-243">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="07aba-244">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-244">Added `network nic wait`</span></span>
* <span data-ttu-id="07aba-245">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-245">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="07aba-246">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-246">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="07aba-247">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-247">Resource</span></span>

* <span data-ttu-id="07aba-248">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-248">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="07aba-249">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-249">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="07aba-250">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-250">Added `deployment wait` command</span></span>
* <span data-ttu-id="07aba-251">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-251">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-252">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-252">SQL</span></span>

* <span data-ttu-id="07aba-253">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-253">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="07aba-254">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-254">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="07aba-255">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="07aba-255">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-256">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-256">Storage</span></span>

* <span data-ttu-id="07aba-257">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-257">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-258">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-258">VM</span></span>

* <span data-ttu-id="07aba-259">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-259">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="07aba-260">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-260">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="07aba-261">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-261">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="07aba-262">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="07aba-262">July 3, 2018</span></span>

<span data-ttu-id="07aba-263">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="07aba-263">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="07aba-264">AKS</span><span class="sxs-lookup"><span data-stu-id="07aba-264">AKS</span></span>

* <span data-ttu-id="07aba-265">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-265">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="07aba-266">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="07aba-266">July 3, 2018</span></span>

<span data-ttu-id="07aba-267">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="07aba-267">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="07aba-268">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-268">Core</span></span>

* <span data-ttu-id="07aba-269">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-269">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-270">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-270">ACR</span></span>

* <span data-ttu-id="07aba-271">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-271">Added polling build status</span></span>
* <span data-ttu-id="07aba-272">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-272">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="07aba-273">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-273">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-274">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-274">ACS</span></span>

* <span data-ttu-id="07aba-275">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-275">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="07aba-276">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-276">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="07aba-277">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-277">Updated options for `aks browse` command.</span></span> <span data-ttu-id="07aba-278">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-278">Added `--listen-port` support</span></span>
* <span data-ttu-id="07aba-279">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-279">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="07aba-280">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="07aba-280">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="07aba-281">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-281">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-282">AppService</span><span class="sxs-lookup"><span data-stu-id="07aba-282">AppService</span></span>

* <span data-ttu-id="07aba-283">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-283">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="07aba-284">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-284">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="07aba-285">Backup</span><span class="sxs-lookup"><span data-stu-id="07aba-285">Backup</span></span>

* <span data-ttu-id="07aba-286">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-286">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="07aba-287">BatchAI</span><span class="sxs-lookup"><span data-stu-id="07aba-287">BatchAI</span></span>

* <span data-ttu-id="07aba-288">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-288">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="07aba-289">クラウド</span><span class="sxs-lookup"><span data-stu-id="07aba-289">Cloud</span></span>

* <span data-ttu-id="07aba-290">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-290">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="07aba-291">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-291">Container</span></span>

* <span data-ttu-id="07aba-292">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-292">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="07aba-293">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-293">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="07aba-294">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-294">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="07aba-295">内線番号</span><span class="sxs-lookup"><span data-stu-id="07aba-295">Extension</span></span>

* <span data-ttu-id="07aba-296">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-296">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="07aba-297">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-297">Network</span></span>

* <span data-ttu-id="07aba-298">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-298">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="07aba-299">Rdbms</span><span class="sxs-lookup"><span data-stu-id="07aba-299">Rdbms</span></span>

* <span data-ttu-id="07aba-300">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-300">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-301">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-301">Resource</span></span>

* <span data-ttu-id="07aba-302">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-302">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-303">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-303">VM</span></span>

* <span data-ttu-id="07aba-304">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-304">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="07aba-305">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="07aba-305">June 25, 2018</span></span>

<span data-ttu-id="07aba-306">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="07aba-306">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="07aba-307">CLI</span><span class="sxs-lookup"><span data-stu-id="07aba-307">CLI</span></span>

* <span data-ttu-id="07aba-308">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-308">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="07aba-309">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="07aba-309">June 19, 2018</span></span>

<span data-ttu-id="07aba-310">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="07aba-310">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="07aba-311">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-311">Core</span></span>

* <span data-ttu-id="07aba-312">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-312">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-313">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-313">ACR</span></span>

* <span data-ttu-id="07aba-314">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-314">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="07aba-315">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-315">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-316">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-316">ACS</span></span>

* <span data-ttu-id="07aba-317">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-317">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="07aba-318">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-318">Added `--update` support</span></span>
* <span data-ttu-id="07aba-319">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-319">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="07aba-320">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="07aba-320">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="07aba-321">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-321">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="07aba-322">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-322">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="07aba-323">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-323">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="07aba-324">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-324">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-325">AppService</span><span class="sxs-lookup"><span data-stu-id="07aba-325">AppService</span></span>

* <span data-ttu-id="07aba-326">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-326">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="07aba-327">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-327">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="07aba-328">Batch</span><span class="sxs-lookup"><span data-stu-id="07aba-328">Batch</span></span>

* <span data-ttu-id="07aba-329">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-329">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="07aba-330">Batch AI</span><span class="sxs-lookup"><span data-stu-id="07aba-330">Batch AI</span></span>

* <span data-ttu-id="07aba-331">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-331">Added support for workspaces.</span></span> <span data-ttu-id="07aba-332">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="07aba-332">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="07aba-333">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-333">Added support for experiments.</span></span> <span data-ttu-id="07aba-334">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="07aba-334">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="07aba-335">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-335">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="07aba-336">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-336">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="07aba-337">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="07aba-337">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="07aba-338">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-338">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="07aba-339">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="07aba-339">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="07aba-340">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="07aba-340">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="07aba-341">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-341">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="07aba-342">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="07aba-342">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="07aba-343">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-343">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="07aba-344">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="07aba-344">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="07aba-345">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-345">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="07aba-346">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="07aba-346">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="07aba-347">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-347">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="07aba-348">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-348">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
 - <span data-ttu-id="07aba-349">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-349">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
 - <span data-ttu-id="07aba-350">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-350">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="07aba-351">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-351">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="07aba-352">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-352">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="07aba-353">マップ</span><span class="sxs-lookup"><span data-stu-id="07aba-353">Maps</span></span>

* <span data-ttu-id="07aba-354">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-354">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="07aba-355">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-355">Network</span></span>

* <span data-ttu-id="07aba-356">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="07aba-356">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="07aba-357">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-357">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="07aba-358">#6502</span><span class="sxs-lookup"><span data-stu-id="07aba-358">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="07aba-359">Reservations</span><span class="sxs-lookup"><span data-stu-id="07aba-359">Reservations</span></span>

* <span data-ttu-id="07aba-360">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-360">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="07aba-361">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-361">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="07aba-362">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-362">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="07aba-363">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-363">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="07aba-364">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-364">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="07aba-365">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-365">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="07aba-366">Role</span><span class="sxs-lookup"><span data-stu-id="07aba-366">Role</span></span>

* <span data-ttu-id="07aba-367">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-367">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-368">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-368">SQL</span></span>

* <span data-ttu-id="07aba-369">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-369">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-370">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-370">Storage</span></span>

* <span data-ttu-id="07aba-371">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="07aba-371">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-372">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-372">VM</span></span>

* <span data-ttu-id="07aba-373">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-373">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="07aba-374">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-374">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="07aba-375">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-375">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="07aba-376">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="07aba-376">June 13, 2018</span></span>

<span data-ttu-id="07aba-377">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="07aba-377">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="07aba-378">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-378">Core</span></span>

* <span data-ttu-id="07aba-379">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-379">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="07aba-380">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="07aba-380">June 13, 2018</span></span>

<span data-ttu-id="07aba-381">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="07aba-381">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="07aba-382">AKS</span><span class="sxs-lookup"><span data-stu-id="07aba-382">AKS</span></span>

* <span data-ttu-id="07aba-383">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-383">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="07aba-384">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-384">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="07aba-385">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-385">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="07aba-386">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-386">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="07aba-387">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-387">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-388">AppService</span><span class="sxs-lookup"><span data-stu-id="07aba-388">AppService</span></span>

* <span data-ttu-id="07aba-389">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-389">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="07aba-390">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="07aba-390">June 5, 2018</span></span>

<span data-ttu-id="07aba-391">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="07aba-391">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="07aba-392">Interactive</span><span class="sxs-lookup"><span data-stu-id="07aba-392">Interactive</span></span>

* <span data-ttu-id="07aba-393">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-393">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="07aba-394">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="07aba-394">June 5, 2018</span></span>

<span data-ttu-id="07aba-395">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="07aba-395">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="07aba-396">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-396">Core</span></span>

* <span data-ttu-id="07aba-397">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-397">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="07aba-398">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-398">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-399">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-399">ACR</span></span>

* <span data-ttu-id="07aba-400">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-400">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="07aba-401">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-401">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="07aba-402">AKS</span><span class="sxs-lookup"><span data-stu-id="07aba-402">AKS</span></span>

* <span data-ttu-id="07aba-403">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-403">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="07aba-404">Batch</span><span class="sxs-lookup"><span data-stu-id="07aba-404">Batch</span></span>

* <span data-ttu-id="07aba-405">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-405">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="07aba-406">IoT</span><span class="sxs-lookup"><span data-stu-id="07aba-406">IOT</span></span>

* <span data-ttu-id="07aba-407">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-407">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="07aba-408">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-408">Network</span></span>

* <span data-ttu-id="07aba-409">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-409">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="07aba-410">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="07aba-410">Policy Insights</span></span>

* <span data-ttu-id="07aba-411">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-411">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="07aba-412">ARM</span><span class="sxs-lookup"><span data-stu-id="07aba-412">ARM</span></span>

* <span data-ttu-id="07aba-413">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-413">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-414">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-414">SQL</span></span>

* <span data-ttu-id="07aba-415">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-415">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="07aba-416">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-416">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="07aba-417">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-417">Storage</span></span>

* <span data-ttu-id="07aba-418">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-418">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-419">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-419">VM</span></span>

* <span data-ttu-id="07aba-420">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-420">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="07aba-421">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-421">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="07aba-422">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-422">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="07aba-423">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="07aba-423">May 22, 2018</span></span>

<span data-ttu-id="07aba-424">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="07aba-424">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="07aba-425">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-425">Core</span></span>

* <span data-ttu-id="07aba-426">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-426">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-427">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-427">ACS</span></span>

* <span data-ttu-id="07aba-428">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-428">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="07aba-429">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-429">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-430">AppService</span><span class="sxs-lookup"><span data-stu-id="07aba-430">AppService</span></span>

* <span data-ttu-id="07aba-431">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-431">Improved generic update commands</span></span>
* <span data-ttu-id="07aba-432">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-432">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="07aba-433">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-433">Container</span></span>

* <span data-ttu-id="07aba-434">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-434">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="07aba-435">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-435">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="07aba-436">内線番号</span><span class="sxs-lookup"><span data-stu-id="07aba-436">Extension</span></span>

* <span data-ttu-id="07aba-437">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-437">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="07aba-438">Interactive</span><span class="sxs-lookup"><span data-stu-id="07aba-438">Interactive</span></span>

* <span data-ttu-id="07aba-439">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-439">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="07aba-440">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-440">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="07aba-441">KeyVault</span><span class="sxs-lookup"><span data-stu-id="07aba-441">KeyVault</span></span>

* <span data-ttu-id="07aba-442">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-442">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="07aba-443">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-443">Network</span></span>

* <span data-ttu-id="07aba-444">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-444">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="07aba-445">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-445">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-446">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-446">SQL</span></span>

* <span data-ttu-id="07aba-447">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-447">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="07aba-448">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-448">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="07aba-449">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-449">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="07aba-450">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-450">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="07aba-451">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-451">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="07aba-452">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="07aba-452">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="07aba-453">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="07aba-453">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="07aba-454">`edition`</span><span class="sxs-lookup"><span data-stu-id="07aba-454">`edition`.</span></span> <span data-ttu-id="07aba-455">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="07aba-455">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="07aba-456">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="07aba-456">`elasticPoolName`.</span></span> <span data-ttu-id="07aba-457">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="07aba-457">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="07aba-458">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-458">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="07aba-459">`edition`</span><span class="sxs-lookup"><span data-stu-id="07aba-459">`edition`.</span></span> <span data-ttu-id="07aba-460">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="07aba-460">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="07aba-461">`dtu`</span><span class="sxs-lookup"><span data-stu-id="07aba-461">`dtu`.</span></span> <span data-ttu-id="07aba-462">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="07aba-462">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="07aba-463">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="07aba-463">`databaseDtuMin`.</span></span> <span data-ttu-id="07aba-464">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="07aba-464">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="07aba-465">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="07aba-465">`databaseDtuMax`.</span></span> <span data-ttu-id="07aba-466">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="07aba-466">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="07aba-467">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-467">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="07aba-468">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-468">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-469">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-469">Storage</span></span>

* <span data-ttu-id="07aba-470">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-470">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="07aba-471">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-471">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-472">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-472">VM</span></span>

* <span data-ttu-id="07aba-473">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-473">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="07aba-474">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="07aba-474">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="07aba-475">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-475">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="07aba-476">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-476">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="07aba-477">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-477">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="07aba-478">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="07aba-478">May 7, 2018</span></span>

<span data-ttu-id="07aba-479">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="07aba-479">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="07aba-480">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-480">Core</span></span>

* <span data-ttu-id="07aba-481">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-481">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="07aba-482">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-482">Added limited support for positional arguments</span></span>
* <span data-ttu-id="07aba-483">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-483">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="07aba-484">#5591</span><span class="sxs-lookup"><span data-stu-id="07aba-484">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="07aba-485">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-485">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="07aba-486">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="07aba-486">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="07aba-487">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-487">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="07aba-488">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-488">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="07aba-489">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-489">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-490">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-490">ACR</span></span>

* <span data-ttu-id="07aba-491">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-491">Added ACR Build commands</span></span>
* <span data-ttu-id="07aba-492">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-492">Improved resource not found error messages</span></span>
* <span data-ttu-id="07aba-493">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-493">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="07aba-494">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-494">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="07aba-495">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-495">Improved repository commands error messages</span></span>
* <span data-ttu-id="07aba-496">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-496">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-497">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-497">ACS</span></span>

* <span data-ttu-id="07aba-498">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-498">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="07aba-499">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-499">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="07aba-500">AMS</span><span class="sxs-lookup"><span data-stu-id="07aba-500">AMS</span></span>

* <span data-ttu-id="07aba-501">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="07aba-501">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-502">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-502">Appservice</span></span>

* <span data-ttu-id="07aba-503">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-503">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="07aba-504">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-504">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="07aba-505">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-505">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="07aba-506">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-506">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="07aba-507">Batch AI</span><span class="sxs-lookup"><span data-stu-id="07aba-507">Batch AI</span></span>

* <span data-ttu-id="07aba-508">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-508">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="07aba-509">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="07aba-509">Cognitive Services</span></span>

* <span data-ttu-id="07aba-510">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-510">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="07aba-511">消費</span><span class="sxs-lookup"><span data-stu-id="07aba-511">Consumption</span></span>

* <span data-ttu-id="07aba-512">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-512">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="07aba-513">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-513">Container</span></span>

* <span data-ttu-id="07aba-514">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-514">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="07aba-515">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="07aba-515">Cosmos DB</span></span>

* <span data-ttu-id="07aba-516">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="07aba-516">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="07aba-517">DMS</span><span class="sxs-lookup"><span data-stu-id="07aba-517">DMS</span></span>

* <span data-ttu-id="07aba-518">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-518">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="07aba-519">内線番号</span><span class="sxs-lookup"><span data-stu-id="07aba-519">Extension</span></span>

* <span data-ttu-id="07aba-520">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-520">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="07aba-521">Interactive</span><span class="sxs-lookup"><span data-stu-id="07aba-521">Interactive</span></span>

* <span data-ttu-id="07aba-522">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-522">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="07aba-523">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="07aba-523">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="07aba-524">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-524">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="07aba-525">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-525">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="07aba-526">ラボ</span><span class="sxs-lookup"><span data-stu-id="07aba-526">Lab</span></span>

* <span data-ttu-id="07aba-527">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-527">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="07aba-528">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-528">Network</span></span>

* <span data-ttu-id="07aba-529">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-529">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="07aba-530">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-530">Profile</span></span>

* <span data-ttu-id="07aba-531">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-531">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="07aba-532">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-532">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="07aba-533">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-533">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="07aba-534">Redis</span><span class="sxs-lookup"><span data-stu-id="07aba-534">Redis</span></span>

* <span data-ttu-id="07aba-535">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-535">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="07aba-536">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="07aba-536">Deprecated `redis list-all`.</span></span> <span data-ttu-id="07aba-537">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="07aba-537">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="07aba-538">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-538">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="07aba-539">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-539">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="07aba-540">Role</span><span class="sxs-lookup"><span data-stu-id="07aba-540">Role</span></span>

* <span data-ttu-id="07aba-541">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-541">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-542">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-542">Storage</span></span>

* <span data-ttu-id="07aba-543">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="07aba-543">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="07aba-544">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="07aba-544">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="07aba-545">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="07aba-545">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="07aba-546">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="07aba-546">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="07aba-547">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-547">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-548">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-548">VM</span></span>

* <span data-ttu-id="07aba-549">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-549">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="07aba-550">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-550">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="07aba-551">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="07aba-551">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="07aba-552">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-552">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="07aba-553">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-553">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="07aba-554">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-554">Added write accelerator support</span></span>
* <span data-ttu-id="07aba-555">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-555">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="07aba-556">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-556">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="07aba-557">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-557">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="07aba-558">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="07aba-558">April 10, 2018</span></span>

<span data-ttu-id="07aba-559">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="07aba-559">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-560">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-560">ACR</span></span>

* <span data-ttu-id="07aba-561">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-561">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-562">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-562">ACS</span></span>

* <span data-ttu-id="07aba-563">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-563">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-564">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-564">Appservice</span></span>

* [重大な変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="07aba-566">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-566">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="07aba-567">BatchAI</span><span class="sxs-lookup"><span data-stu-id="07aba-567">BatchAI</span></span>

* <span data-ttu-id="07aba-568">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-568">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="07aba-569">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="07aba-569">Job level mounting</span></span>
 - <span data-ttu-id="07aba-570">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="07aba-570">Environment variables with secret values</span></span>
 - <span data-ttu-id="07aba-571">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="07aba-571">Performance counters settings</span></span>
 - <span data-ttu-id="07aba-572">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="07aba-572">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="07aba-573">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="07aba-573">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="07aba-574">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="07aba-574">Usage and limits reporting</span></span>
 - <span data-ttu-id="07aba-575">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="07aba-575">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="07aba-576">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="07aba-576">Support for custom images</span></span>
 - <span data-ttu-id="07aba-577">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-577">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="07aba-578">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-578">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="07aba-579">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="07aba-579">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="07aba-580">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="07aba-580">National clouds are supported</span></span>
* <span data-ttu-id="07aba-581">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-581">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="07aba-582">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-582">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="07aba-583">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-583">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="07aba-584">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-584">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="07aba-585">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="07aba-585">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="07aba-586">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="07aba-586">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="07aba-587">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-587">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="07aba-588">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-588">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="07aba-589">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="07aba-589">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="07aba-590">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-590">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="07aba-591">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="07aba-591">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="07aba-592">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="07aba-592">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="07aba-593">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-593">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="07aba-594">課金</span><span class="sxs-lookup"><span data-stu-id="07aba-594">Billing</span></span>

* <span data-ttu-id="07aba-595">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-595">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="07aba-596">消費</span><span class="sxs-lookup"><span data-stu-id="07aba-596">Consumption</span></span>

* <span data-ttu-id="07aba-597">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-597">Added `marketplace` commands</span></span>
* <span data-ttu-id="07aba-598">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-598">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="07aba-599">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-599">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="07aba-600">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-600">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="07aba-601">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-601">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="07aba-602">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-602">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="07aba-603">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-603">Container</span></span>

* <span data-ttu-id="07aba-604">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-604">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="07aba-605">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-605">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="07aba-606">内線番号</span><span class="sxs-lookup"><span data-stu-id="07aba-606">Extension</span></span>

* <span data-ttu-id="07aba-607">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-607">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="07aba-608">Interactive</span><span class="sxs-lookup"><span data-stu-id="07aba-608">Interactive</span></span>

* <span data-ttu-id="07aba-609">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-609">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="07aba-610">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-610">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="07aba-611">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-611">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="07aba-612">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-612">Network</span></span>

* <span data-ttu-id="07aba-613">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-613">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="07aba-614">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-614">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="07aba-615">#4910</span><span class="sxs-lookup"><span data-stu-id="07aba-615">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="07aba-616">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-616">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="07aba-617">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="07aba-617">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="07aba-618">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-618">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="07aba-619">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-619">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="07aba-620">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-620">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="07aba-621">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-621">Profile</span></span>

* <span data-ttu-id="07aba-622">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-622">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="07aba-623">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-623">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="07aba-624">RDBMS</span><span class="sxs-lookup"><span data-stu-id="07aba-624">RDBMS</span></span>

* <span data-ttu-id="07aba-625">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-625">Added `georestore` command</span></span>
* <span data-ttu-id="07aba-626">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-626">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-627">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-627">Resource</span></span>

* <span data-ttu-id="07aba-628">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-628">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="07aba-629">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-629">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-630">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-630">SQL</span></span>

* <span data-ttu-id="07aba-631">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-631">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-632">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-632">Storage</span></span>

* <span data-ttu-id="07aba-633">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-633">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-634">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-634">VM</span></span>

* <span data-ttu-id="07aba-635">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-635">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="07aba-636">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-636">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大な変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="07aba-638">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-638">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="07aba-639">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-639">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="07aba-640">#5718</span><span class="sxs-lookup"><span data-stu-id="07aba-640">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="07aba-641">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-641">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="07aba-642">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="07aba-642">March 27, 2018</span></span>

<span data-ttu-id="07aba-643">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="07aba-643">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="07aba-644">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-644">Core</span></span>

* <span data-ttu-id="07aba-645">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="07aba-645">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-646">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-646">ACS</span></span>

* <span data-ttu-id="07aba-647">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-647">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-648">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-648">Appservice</span></span>

* <span data-ttu-id="07aba-649">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-649">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="07aba-650">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-650">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="07aba-651">Backup</span><span class="sxs-lookup"><span data-stu-id="07aba-651">Backup</span></span>

* <span data-ttu-id="07aba-652">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-652">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="07aba-653">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="07aba-653">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="07aba-654">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-654">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="07aba-655">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-655">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="07aba-656">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-656">Container</span></span>

* <span data-ttu-id="07aba-657">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-657">Added `container exec` command.</span></span> <span data-ttu-id="07aba-658">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="07aba-658">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="07aba-659">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="07aba-659">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="07aba-660">内線番号</span><span class="sxs-lookup"><span data-stu-id="07aba-660">Extension</span></span>

* <span data-ttu-id="07aba-661">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-661">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="07aba-662">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-662">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="07aba-663">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-663">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="07aba-664">Interactive</span><span class="sxs-lookup"><span data-stu-id="07aba-664">Interactive</span></span>

* <span data-ttu-id="07aba-665">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-665">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="07aba-666">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-666">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="07aba-667">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="07aba-667">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="07aba-668">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-668">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="07aba-669">ラボ</span><span class="sxs-lookup"><span data-stu-id="07aba-669">Lab</span></span>

* <span data-ttu-id="07aba-670">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-670">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="07aba-671">監視</span><span class="sxs-lookup"><span data-stu-id="07aba-671">Monitor</span></span>

* <span data-ttu-id="07aba-672">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="07aba-672">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="07aba-673">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="07aba-673">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="07aba-674">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="07aba-674">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="07aba-675">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-675">Network</span></span>

* <span data-ttu-id="07aba-676">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-676">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="07aba-677">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-677">Profile</span></span>

* <span data-ttu-id="07aba-678">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-678">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="07aba-679">RDBMS</span><span class="sxs-lookup"><span data-stu-id="07aba-679">RDBMS</span></span>

* <span data-ttu-id="07aba-680">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-680">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-681">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-681">Resource</span></span>

* [重大な変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="07aba-683">Role</span><span class="sxs-lookup"><span data-stu-id="07aba-683">Role</span></span>

* <span data-ttu-id="07aba-684">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-684">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="07aba-685">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-685">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="07aba-686">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-686">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="07aba-687">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-687">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="07aba-688">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-688">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-689">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-689">Storage</span></span>

* <span data-ttu-id="07aba-690">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-690">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="07aba-691">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-691">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-692">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-692">VM</span></span>

* <span data-ttu-id="07aba-693">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-693">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="07aba-694">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-694">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="07aba-695">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-695">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="07aba-696">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-696">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="07aba-697">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="07aba-697">March 13, 2018</span></span>

<span data-ttu-id="07aba-698">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="07aba-698">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-699">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-699">ACR</span></span>

* <span data-ttu-id="07aba-700">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-700">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="07aba-701">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-701">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="07aba-702">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-702">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-703">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-703">ACS</span></span>

* <span data-ttu-id="07aba-704">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-704">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="07aba-705">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-705">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="07aba-706">Advisor</span><span class="sxs-lookup"><span data-stu-id="07aba-706">Advisor</span></span>

* <span data-ttu-id="07aba-707">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-707">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="07aba-708">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-708">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="07aba-709">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-709">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="07aba-710">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-710">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="07aba-711">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-711">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-712">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-712">Appservice</span></span>

* <span data-ttu-id="07aba-713">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-713">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="07aba-714">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-714">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="07aba-715">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="07aba-715">Eventhubs</span></span>

* <span data-ttu-id="07aba-716">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-716">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="07aba-717">内線番号</span><span class="sxs-lookup"><span data-stu-id="07aba-717">Extension</span></span>

* <span data-ttu-id="07aba-718">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-718">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="07aba-719">Interactive</span><span class="sxs-lookup"><span data-stu-id="07aba-719">Interactive</span></span>

* <span data-ttu-id="07aba-720">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="07aba-720">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="07aba-721">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="07aba-721">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="07aba-722">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="07aba-722">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="07aba-723">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-723">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="07aba-724">監視</span><span class="sxs-lookup"><span data-stu-id="07aba-724">Monitor</span></span>

* <span data-ttu-id="07aba-725">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-725">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="07aba-726">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-726">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="07aba-727">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-727">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="07aba-728">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-728">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="07aba-729">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-729">Network</span></span>

* <span data-ttu-id="07aba-730">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-730">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="07aba-731">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-731">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="07aba-732">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-732">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="07aba-733">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-733">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="07aba-734">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-734">Profile</span></span>

* <span data-ttu-id="07aba-735">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-735">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="07aba-736">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-736">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="07aba-737">RDBMS</span><span class="sxs-lookup"><span data-stu-id="07aba-737">RDBMS</span></span>

* <span data-ttu-id="07aba-738">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-738">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="07aba-739">Service Bus</span><span class="sxs-lookup"><span data-stu-id="07aba-739">Service Bus</span></span>

* <span data-ttu-id="07aba-740">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-740">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-741">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-741">Storage</span></span>

* <span data-ttu-id="07aba-742">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-742">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="07aba-743">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="07aba-743">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-744">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-744">VM</span></span>

* <span data-ttu-id="07aba-745">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-745">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="07aba-746">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-746">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="07aba-747">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-747">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="07aba-748">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-748">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="07aba-749">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="07aba-749">February 27, 2018</span></span>

<span data-ttu-id="07aba-750">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="07aba-750">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="07aba-751">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-751">Core</span></span>

* <span data-ttu-id="07aba-752">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="07aba-752">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="07aba-753">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-753">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="07aba-754">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-754">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-755">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-755">ACS</span></span>

* <span data-ttu-id="07aba-756">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-756">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="07aba-757">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="07aba-757">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="07aba-758">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-758">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="07aba-759">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-759">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-760">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-760">Appservice</span></span>

* <span data-ttu-id="07aba-761">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="07aba-761">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="07aba-762">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="07aba-762">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="07aba-763">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="07aba-763">Cognitive Services</span></span>

* <span data-ttu-id="07aba-764">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-764">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="07aba-765">消費</span><span class="sxs-lookup"><span data-stu-id="07aba-765">Consumption</span></span>

* <span data-ttu-id="07aba-766">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-766">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="07aba-767">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-767">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="07aba-768">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-768">Container</span></span>

* <span data-ttu-id="07aba-769">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-769">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="07aba-770">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-770">Network</span></span>

* <span data-ttu-id="07aba-771">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="07aba-771">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-772">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-772">Resource</span></span>

* <span data-ttu-id="07aba-773">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-773">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="07aba-774">Role</span><span class="sxs-lookup"><span data-stu-id="07aba-774">Role</span></span>

* <span data-ttu-id="07aba-775">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-775">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-776">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-776">SQL</span></span>

* <span data-ttu-id="07aba-777">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-777">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-778">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-778">Storage</span></span>

* <span data-ttu-id="07aba-779">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-779">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-780">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-780">VM</span></span>

* <span data-ttu-id="07aba-781">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-781">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="07aba-782">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="07aba-782">February 13, 2018</span></span>

<span data-ttu-id="07aba-783">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="07aba-783">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="07aba-784">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-784">Core</span></span>

* <span data-ttu-id="07aba-785">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-785">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-786">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-786">ACS</span></span>

* <span data-ttu-id="07aba-787">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-787">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="07aba-788">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-788">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="07aba-789">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-789">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="07aba-790">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-790">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="07aba-791">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-791">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="07aba-792">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="07aba-792">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="07aba-793">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-793">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="07aba-794">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="07aba-794">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-795">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-795">Appservice</span></span>

* <span data-ttu-id="07aba-796">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-796">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="07aba-797">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-797">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="07aba-798">CDN</span><span class="sxs-lookup"><span data-stu-id="07aba-798">CDN</span></span>

* <span data-ttu-id="07aba-799">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-799">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="07aba-800">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-800">Container</span></span>

* <span data-ttu-id="07aba-801">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-801">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="07aba-802">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-802">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="07aba-803">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="07aba-803">CosmosDB</span></span>

* <span data-ttu-id="07aba-804">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-804">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="07aba-805">内線番号</span><span class="sxs-lookup"><span data-stu-id="07aba-805">Extension</span></span>

* <span data-ttu-id="07aba-806">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-806">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="07aba-807">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-807">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="07aba-808">フィードバック</span><span class="sxs-lookup"><span data-stu-id="07aba-808">Feedback</span></span>

* <span data-ttu-id="07aba-809">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-809">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="07aba-810">Interactive</span><span class="sxs-lookup"><span data-stu-id="07aba-810">Interactive</span></span>

* <span data-ttu-id="07aba-811">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-811">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="07aba-812">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-812">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="07aba-813">IoT</span><span class="sxs-lookup"><span data-stu-id="07aba-813">IoT</span></span>

* <span data-ttu-id="07aba-814">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-814">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="07aba-815">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-815">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="07aba-816">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-816">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="07aba-817">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-817">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="07aba-818">監視</span><span class="sxs-lookup"><span data-stu-id="07aba-818">Monitor</span></span>

* <span data-ttu-id="07aba-819">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-819">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="07aba-820">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-820">Network</span></span>

* <span data-ttu-id="07aba-821">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-821">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="07aba-822">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-822">Profile</span></span>

* <span data-ttu-id="07aba-823">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-823">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-824">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-824">Resource</span></span>

* <span data-ttu-id="07aba-825">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-825">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="07aba-826">Role</span><span class="sxs-lookup"><span data-stu-id="07aba-826">Role</span></span>

* <span data-ttu-id="07aba-827">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-827">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-828">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-828">SQL</span></span>

* <span data-ttu-id="07aba-829">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-829">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="07aba-830">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-830">Added `sql db rename`</span></span>
* <span data-ttu-id="07aba-831">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-831">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-832">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-832">Storage</span></span>

* <span data-ttu-id="07aba-833">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-833">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-834">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-834">VM</span></span>

* <span data-ttu-id="07aba-835">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-835">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="07aba-836">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-836">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="07aba-837">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="07aba-837">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="07aba-838">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="07aba-838">January 31, 2018</span></span>

<span data-ttu-id="07aba-839">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="07aba-839">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="07aba-840">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-840">Core</span></span>

* <span data-ttu-id="07aba-841">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-841">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="07aba-842">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-842">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="07aba-843">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-843">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="07aba-844">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="07aba-844">Use `--verbose` to see</span></span>
* <span data-ttu-id="07aba-845">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="07aba-845">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-846">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-846">ACS</span></span>

* <span data-ttu-id="07aba-847">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-847">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="07aba-848">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-848">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-849">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-849">Appservice</span></span>

* <span data-ttu-id="07aba-850">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="07aba-850">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="07aba-851">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-851">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="07aba-852">CDN</span><span class="sxs-lookup"><span data-stu-id="07aba-852">CDN</span></span>

* <span data-ttu-id="07aba-853">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-853">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="07aba-854">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="07aba-854">CosmosDB</span></span>

* <span data-ttu-id="07aba-855">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-855">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="07aba-856">Interactive</span><span class="sxs-lookup"><span data-stu-id="07aba-856">Interactive</span></span>

* <span data-ttu-id="07aba-857">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-857">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="07aba-858">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-858">Network</span></span>

* <span data-ttu-id="07aba-859">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-859">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="07aba-860">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-860">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="07aba-861">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-861">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="07aba-862">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-862">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="07aba-863">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-863">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="07aba-864">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-864">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="07aba-865">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-865">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="07aba-866">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-866">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="07aba-867">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-867">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="07aba-868">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="07aba-868">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="07aba-869">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-869">Profile</span></span>

* <span data-ttu-id="07aba-870">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-870">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-871">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-871">Resource</span></span>

* <span data-ttu-id="07aba-872">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-872">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-873">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-873">Storage</span></span>

* <span data-ttu-id="07aba-874">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-874">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="07aba-875">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-875">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="07aba-876">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-876">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="07aba-877">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-877">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="07aba-878">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-878">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-879">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-879">VM</span></span>

* <span data-ttu-id="07aba-880">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-880">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="07aba-881">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-881">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="07aba-882">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-882">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="07aba-883">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-883">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="07aba-884">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="07aba-884">January 17, 2018</span></span>

<span data-ttu-id="07aba-885">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="07aba-885">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-886">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-886">ACR</span></span>

* <span data-ttu-id="07aba-887">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-887">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="07aba-888">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-888">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-889">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-889">ACS</span></span>

* <span data-ttu-id="07aba-890">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-890">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="07aba-891">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-891">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-892">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-892">Appservice</span></span>

* <span data-ttu-id="07aba-893">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-893">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="07aba-894">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-894">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="07aba-895">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-895">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="07aba-896">Backup</span><span class="sxs-lookup"><span data-stu-id="07aba-896">Backup</span></span>

* <span data-ttu-id="07aba-897">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-897">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="07aba-898">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-898">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="07aba-899">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-899">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="07aba-900">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-900">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="07aba-901">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-901">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="07aba-902">Batch</span><span class="sxs-lookup"><span data-stu-id="07aba-902">Batch</span></span>

* <span data-ttu-id="07aba-903">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-903">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="07aba-904">クラウド</span><span class="sxs-lookup"><span data-stu-id="07aba-904">Cloud</span></span>

* <span data-ttu-id="07aba-905">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-905">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="07aba-906">消費</span><span class="sxs-lookup"><span data-stu-id="07aba-906">Consumption</span></span>

* <span data-ttu-id="07aba-907">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-907">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="07aba-908">Event Grid</span><span class="sxs-lookup"><span data-stu-id="07aba-908">Event Grid</span></span>

* <span data-ttu-id="07aba-909">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="07aba-909">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="07aba-910">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="07aba-910">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="07aba-911">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-911">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="07aba-912">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="07aba-912">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="07aba-913">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-913">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="07aba-914">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-914">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="07aba-915">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-915">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="07aba-916">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-916">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="07aba-917">Interactive</span><span class="sxs-lookup"><span data-stu-id="07aba-917">Interactive</span></span>

* <span data-ttu-id="07aba-918">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="07aba-918">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="07aba-919">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-919">Fixed errors on startup</span></span>
* <span data-ttu-id="07aba-920">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-920">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="07aba-921">IoT</span><span class="sxs-lookup"><span data-stu-id="07aba-921">IoT</span></span>

* <span data-ttu-id="07aba-922">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-922">Added support for device provisioning service</span></span>
* <span data-ttu-id="07aba-923">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-923">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="07aba-924">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-924">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="07aba-925">監視</span><span class="sxs-lookup"><span data-stu-id="07aba-925">Monitor</span></span>

* <span data-ttu-id="07aba-926">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-926">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="07aba-927">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="07aba-927">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="07aba-928">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-928">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="07aba-929">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-929">Network</span></span>

* <span data-ttu-id="07aba-930">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-930">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="07aba-931">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-931">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="07aba-932">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-932">Profile</span></span>

* <span data-ttu-id="07aba-933">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-933">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="07aba-934">Role</span><span class="sxs-lookup"><span data-stu-id="07aba-934">Role</span></span>

* <span data-ttu-id="07aba-935">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-935">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="07aba-936">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="07aba-936">Service Fabric</span></span>

* <span data-ttu-id="07aba-937">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-937">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="07aba-938">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-938">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-939">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-939">VM</span></span>

* <span data-ttu-id="07aba-940">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="07aba-940">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="07aba-941">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-941">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="07aba-942">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-942">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="07aba-943">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-943">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="07aba-944">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-944">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="07aba-945">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-945">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="07aba-946">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-946">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="07aba-947">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-947">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="07aba-948">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="07aba-948">December 19, 2017</span></span>

<span data-ttu-id="07aba-949">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="07aba-949">Version 2.0.23</span></span>

* <span data-ttu-id="07aba-950">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-950">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="07aba-951">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-951">Container</span></span>

* <span data-ttu-id="07aba-952">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-952">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="07aba-953">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-953">Network</span></span>

* <span data-ttu-id="07aba-954">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-954">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="07aba-955">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-955">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-956">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-956">Storage</span></span>

* <span data-ttu-id="07aba-957">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-957">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-958">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-958">VM</span></span>

* <span data-ttu-id="07aba-959">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-959">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="07aba-960">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="07aba-960">December 5, 2017</span></span>

<span data-ttu-id="07aba-961">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="07aba-961">Version 2.0.22</span></span>

* <span data-ttu-id="07aba-962">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-962">Removed `az component` commands.</span></span> <span data-ttu-id="07aba-963">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="07aba-963">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="07aba-964">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-964">Core</span></span>
* <span data-ttu-id="07aba-965">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-965">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="07aba-966">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-966">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-967">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-967">ACS</span></span>

* <span data-ttu-id="07aba-968">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-968">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="07aba-969">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-969">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="07aba-970">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-970">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="07aba-971">Advisor</span><span class="sxs-lookup"><span data-stu-id="07aba-971">Advisor</span></span>

* <span data-ttu-id="07aba-972">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-972">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-973">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-973">Appservice</span></span>

* <span data-ttu-id="07aba-974">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-974">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="07aba-975">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-975">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="07aba-976">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-976">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="07aba-977">消費</span><span class="sxs-lookup"><span data-stu-id="07aba-977">Consumption</span></span>

* <span data-ttu-id="07aba-978">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-978">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="07aba-979">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-979">Container</span></span>

* <span data-ttu-id="07aba-980">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-980">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="07aba-981">監視</span><span class="sxs-lookup"><span data-stu-id="07aba-981">Monitor</span></span>

* <span data-ttu-id="07aba-982">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-982">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-983">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-983">Resource</span></span>

* <span data-ttu-id="07aba-984">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-984">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="07aba-985">Role</span><span class="sxs-lookup"><span data-stu-id="07aba-985">Role</span></span>

* <span data-ttu-id="07aba-986">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-986">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="07aba-987">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="07aba-987">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="07aba-988">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-988">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-989">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-989">SQL</span></span>

* <span data-ttu-id="07aba-990">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-990">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="07aba-991">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-991">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-992">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-992">VM</span></span>

* <span data-ttu-id="07aba-993">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-993">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="07aba-994">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="07aba-994">November 14, 2017</span></span>

<span data-ttu-id="07aba-995">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="07aba-995">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-996">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-996">ACR</span></span>

* <span data-ttu-id="07aba-997">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-997">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="07aba-998">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-998">ACS</span></span>

* <span data-ttu-id="07aba-999">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-999">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="07aba-1000">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1000">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="07aba-1001">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1001">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="07aba-1002">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1002">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="07aba-1003">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1003">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-1004">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-1004">Appservice</span></span>

* <span data-ttu-id="07aba-1005">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1005">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="07aba-1006">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1006">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="07aba-1007">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1007">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="07aba-1008">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1008">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="07aba-1009">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1009">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="07aba-1010">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="07aba-1010">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="07aba-1011">Batch</span><span class="sxs-lookup"><span data-stu-id="07aba-1011">Batch</span></span>

* <span data-ttu-id="07aba-1012">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1012">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="07aba-1013">Batchai</span><span class="sxs-lookup"><span data-stu-id="07aba-1013">Batchai</span></span>

* <span data-ttu-id="07aba-1014">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1014">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="07aba-1015">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1015">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="07aba-1016">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1016">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="07aba-1017">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1017">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="07aba-1018">クラウド</span><span class="sxs-lookup"><span data-stu-id="07aba-1018">Cloud</span></span>

* <span data-ttu-id="07aba-1019">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1019">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="07aba-1020">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-1020">Container</span></span>

* <span data-ttu-id="07aba-1021">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1021">Added support to open multiple ports</span></span>
* <span data-ttu-id="07aba-1022">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1022">Added container group restart policy</span></span>
* <span data-ttu-id="07aba-1023">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1023">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="07aba-1024">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1024">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="07aba-1025">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="07aba-1025">Data Lake Analytics</span></span>

* <span data-ttu-id="07aba-1026">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1026">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="07aba-1027">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="07aba-1027">Data Lake Store</span></span>

* <span data-ttu-id="07aba-1028">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1028">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="07aba-1029">内線番号</span><span class="sxs-lookup"><span data-stu-id="07aba-1029">Extension</span></span>

* <span data-ttu-id="07aba-1030">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1030">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="07aba-1031">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1031">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="07aba-1032">IoT</span><span class="sxs-lookup"><span data-stu-id="07aba-1032">IoT</span></span>

* <span data-ttu-id="07aba-1033">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1033">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="07aba-1034">監視</span><span class="sxs-lookup"><span data-stu-id="07aba-1034">Monitor</span></span>

* <span data-ttu-id="07aba-1035">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1035">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="07aba-1036">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-1036">Network</span></span>

* <span data-ttu-id="07aba-1037">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1037">Added support for CAA DNS records</span></span>
* <span data-ttu-id="07aba-1038">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1038">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="07aba-1039">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1039">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="07aba-1040">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1040">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="07aba-1041">Reservations</span><span class="sxs-lookup"><span data-stu-id="07aba-1041">Reservations</span></span>

* <span data-ttu-id="07aba-1042">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="07aba-1042">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-1043">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-1043">Resource</span></span>

* <span data-ttu-id="07aba-1044">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1044">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-1045">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-1045">SQL</span></span>

* <span data-ttu-id="07aba-1046">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1046">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-1047">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-1047">Storage</span></span>

* <span data-ttu-id="07aba-1048">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1048">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="07aba-1049">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1049">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="07aba-1050">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1050">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="07aba-1051">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1051">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="07aba-1052">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1052">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="07aba-1053">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1053">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="07aba-1054">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1054">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-1055">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-1055">VM</span></span>

* <span data-ttu-id="07aba-1056">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1056">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="07aba-1057">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1057">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="07aba-1058">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1058">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="07aba-1059">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1059">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="07aba-1060">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1060">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="07aba-1061">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1061">October 24, 2017</span></span>

<span data-ttu-id="07aba-1062">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="07aba-1062">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="07aba-1063">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-1063">Core</span></span>

* <span data-ttu-id="07aba-1064">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1064">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-1065">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-1065">ACR</span></span>

* <span data-ttu-id="07aba-1066">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1066">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="07aba-1067">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1067">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="07aba-1068">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1068">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-1069">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-1069">ACS</span></span>

* <span data-ttu-id="07aba-1070">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1070">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="07aba-1071">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1071">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-1072">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-1072">Appservice</span></span>

* <span data-ttu-id="07aba-1073">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1073">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="07aba-1074">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="07aba-1074">Component</span></span>

* <span data-ttu-id="07aba-1075">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1075">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="07aba-1076">監視</span><span class="sxs-lookup"><span data-stu-id="07aba-1076">Monitor</span></span>

* <span data-ttu-id="07aba-1077">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1077">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-1078">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-1078">Resource</span></span>

* <span data-ttu-id="07aba-1079">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1079">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="07aba-1080">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1080">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-1081">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-1081">VM</span></span>

* <span data-ttu-id="07aba-1082">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1082">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="07aba-1083">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1083">October 9, 2017</span></span>

<span data-ttu-id="07aba-1084">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="07aba-1084">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="07aba-1085">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-1085">Core</span></span>

* <span data-ttu-id="07aba-1086">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1086">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-1087">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-1087">Appservice</span></span>

* <span data-ttu-id="07aba-1088">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1088">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="07aba-1089">Batch</span><span class="sxs-lookup"><span data-stu-id="07aba-1089">Batch</span></span>

* <span data-ttu-id="07aba-1090">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1090">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="07aba-1091">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1091">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="07aba-1092">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1092">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="07aba-1093">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1093">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="07aba-1094">Batchai</span><span class="sxs-lookup"><span data-stu-id="07aba-1094">Batchai</span></span>

* <span data-ttu-id="07aba-1095">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-1095">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="07aba-1096">KeyVault</span><span class="sxs-lookup"><span data-stu-id="07aba-1096">Keyvault</span></span>

* <span data-ttu-id="07aba-1097">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1097">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="07aba-1098">(#4448)</span><span class="sxs-lookup"><span data-stu-id="07aba-1098">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="07aba-1099">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-1099">Network</span></span>

* <span data-ttu-id="07aba-1100">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1100">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="07aba-1101">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1101">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-1102">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-1102">Resource</span></span>

* <span data-ttu-id="07aba-1103">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1103">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="07aba-1104">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1104">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="07aba-1105">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1105">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="07aba-1106">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1106">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-1107">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-1107">Sql</span></span>

* <span data-ttu-id="07aba-1108">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1108">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="07aba-1109">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1109">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="07aba-1110">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1110">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-1111">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-1111">Storage</span></span>

* <span data-ttu-id="07aba-1112">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1112">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-1113">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-1113">Vm</span></span>

* <span data-ttu-id="07aba-1114">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1114">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="07aba-1115">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1115">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="07aba-1116">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1116">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="07aba-1117">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1117">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="07aba-1118">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1118">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="07aba-1119">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1119">September 22, 2017</span></span>

<span data-ttu-id="07aba-1120">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="07aba-1120">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-1121">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-1121">Resource</span></span>

* <span data-ttu-id="07aba-1122">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1122">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="07aba-1123">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1123">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="07aba-1124">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1124">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="07aba-1125">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1125">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="07aba-1126">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-1126">Network</span></span>

* <span data-ttu-id="07aba-1127">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1127">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="07aba-1128">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1128">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="07aba-1129">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1129">Added `asg` application security group commands</span></span>
* <span data-ttu-id="07aba-1130">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1130">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="07aba-1131">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1131">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="07aba-1132">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1132">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="07aba-1133">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1133">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-1134">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-1134">Storage</span></span>

* <span data-ttu-id="07aba-1135">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1135">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="07aba-1136">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="07aba-1136">Eventgrid</span></span>

* <span data-ttu-id="07aba-1137">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1137">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-1138">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-1138">SQL</span></span>

* <span data-ttu-id="07aba-1139">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1139">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="07aba-1140">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="07aba-1140">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="07aba-1141">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1141">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="07aba-1142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="07aba-1142">Keyvault</span></span>

* <span data-ttu-id="07aba-1143">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1143">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-1144">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-1144">VM</span></span>

* <span data-ttu-id="07aba-1145">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1145">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="07aba-1146">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1146">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="07aba-1147">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1147">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="07aba-1148">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1148">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="07aba-1149">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1149">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="07aba-1150">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1150">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-1151">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-1151">ACS</span></span>

* <span data-ttu-id="07aba-1152">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1152">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-1153">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-1153">Appservice</span></span>

* <span data-ttu-id="07aba-1154">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1154">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="07aba-1155">Backup</span><span class="sxs-lookup"><span data-stu-id="07aba-1155">Backup</span></span>

* <span data-ttu-id="07aba-1156">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="07aba-1156">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="07aba-1157">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1157">September 11, 2017</span></span>

<span data-ttu-id="07aba-1158">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="07aba-1158">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="07aba-1159">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-1159">Core</span></span>

* <span data-ttu-id="07aba-1160">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1160">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="07aba-1161">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1161">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-1162">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-1162">Acs</span></span>

* <span data-ttu-id="07aba-1163">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1163">Added `acs list-locations` command</span></span>
* <span data-ttu-id="07aba-1164">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1164">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-1165">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-1165">Appservice</span></span>

* <span data-ttu-id="07aba-1166">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1166">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="07aba-1167">CDN</span><span class="sxs-lookup"><span data-stu-id="07aba-1167">CDN</span></span>

* <span data-ttu-id="07aba-1168">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1168">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="07aba-1169">内線番号</span><span class="sxs-lookup"><span data-stu-id="07aba-1169">Extension</span></span>

* <span data-ttu-id="07aba-1170">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-1170">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="07aba-1171">KeyVault</span><span class="sxs-lookup"><span data-stu-id="07aba-1171">Keyvault</span></span>

* <span data-ttu-id="07aba-1172">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1172">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="07aba-1173">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-1173">Network</span></span>

* <span data-ttu-id="07aba-1174">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1174">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="07aba-1175">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1175">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="07aba-1176">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1176">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="07aba-1177">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1177">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="07aba-1178">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1178">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-1179">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-1179">Resource</span></span>

* <span data-ttu-id="07aba-1180">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="07aba-1180">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="07aba-1181">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="07aba-1181">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="07aba-1182">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="07aba-1182">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="07aba-1183">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1183">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-1184">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-1184">SQL</span></span>

* <span data-ttu-id="07aba-1185">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1185">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-1186">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-1186">VM</span></span>

* <span data-ttu-id="07aba-1187">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="07aba-1187">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="07aba-1188">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="07aba-1188">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="07aba-1189">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1189">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="07aba-1190">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="07aba-1190">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="07aba-1191">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="07aba-1191">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="07aba-1192">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1192">August 31, 2017</span></span>

<span data-ttu-id="07aba-1193">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="07aba-1193">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="07aba-1194">KeyVault</span><span class="sxs-lookup"><span data-stu-id="07aba-1194">Keyvault</span></span>

* <span data-ttu-id="07aba-1195">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1195">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="07aba-1196">SF</span><span class="sxs-lookup"><span data-stu-id="07aba-1196">Sf</span></span>

* <span data-ttu-id="07aba-1197">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="07aba-1197">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-1198">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-1198">Storage</span></span>

* <span data-ttu-id="07aba-1199">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1199">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="07aba-1200">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="07aba-1200">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="07aba-1201">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1201">August 28, 2017</span></span>

<span data-ttu-id="07aba-1202">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="07aba-1202">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="07aba-1203">CLI</span><span class="sxs-lookup"><span data-stu-id="07aba-1203">CLI</span></span>

* <span data-ttu-id="07aba-1204">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1204">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-1205">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-1205">ACS</span></span>

* <span data-ttu-id="07aba-1206">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1206">Corrected preview regions</span></span>
* <span data-ttu-id="07aba-1207">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1207">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="07aba-1208">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1208">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-1209">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-1209">Appservice</span></span>

* <span data-ttu-id="07aba-1210">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1210">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="07aba-1211">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1211">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="07aba-1212">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1212">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="07aba-1213">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1213">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="07aba-1214">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="07aba-1214">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="07aba-1215">IoT</span><span class="sxs-lookup"><span data-stu-id="07aba-1215">IoT</span></span>

* <span data-ttu-id="07aba-1216">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1216">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="07aba-1217">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-1217">Network</span></span>

* <span data-ttu-id="07aba-1218">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1218">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="07aba-1219">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1219">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="07aba-1220">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1220">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="07aba-1221">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1221">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="07aba-1222">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1222">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="07aba-1223">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-1223">Profile</span></span>

* <span data-ttu-id="07aba-1224">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1224">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="07aba-1225">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="07aba-1225">Service Fabric</span></span>

* <span data-ttu-id="07aba-1226">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="07aba-1226">Preview release</span></span>
* <span data-ttu-id="07aba-1227">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1227">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="07aba-1228">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1228">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="07aba-1229">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1229">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-1230">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-1230">Storage</span></span>

* <span data-ttu-id="07aba-1231">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1231">Enabled setting blob tier</span></span>
* <span data-ttu-id="07aba-1232">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1232">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="07aba-1233">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1233">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="07aba-1234">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1234">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="07aba-1235">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1235">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="07aba-1236">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="07aba-1236">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-1237">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-1237">VM</span></span>

* <span data-ttu-id="07aba-1238">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1238">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="07aba-1239">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1239">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="07aba-1240">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1240">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="07aba-1241">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1241">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="07aba-1242">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1242">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="07aba-1243">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1243">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="07aba-1244">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1244">August 15, 2017</span></span>

<span data-ttu-id="07aba-1245">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="07aba-1245">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-1246">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-1246">ACS</span></span>

* <span data-ttu-id="07aba-1247">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1247">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-1248">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-1248">Appservice</span></span>

* <span data-ttu-id="07aba-1249">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1249">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="07aba-1250">Event Grid</span><span class="sxs-lookup"><span data-stu-id="07aba-1250">Event Grid</span></span>

* <span data-ttu-id="07aba-1251">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1251">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="07aba-1252">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1252">August 11, 2017</span></span>

<span data-ttu-id="07aba-1253">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="07aba-1253">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-1254">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-1254">ACS</span></span>

* <span data-ttu-id="07aba-1255">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1255">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="07aba-1256">Batch</span><span class="sxs-lookup"><span data-stu-id="07aba-1256">Batch</span></span>

* <span data-ttu-id="07aba-1257">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1257">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="07aba-1258">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1258">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="07aba-1259">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1259">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="07aba-1260">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1260">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="07aba-1261">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1261">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="07aba-1262">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1262">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="07aba-1263">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="07aba-1263">Component</span></span>

* <span data-ttu-id="07aba-1264">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1264">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="07aba-1265">コンテナー</span><span class="sxs-lookup"><span data-stu-id="07aba-1265">Container</span></span>

* <span data-ttu-id="07aba-1266">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1266">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="07aba-1267">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="07aba-1267">Data Lake Store</span></span>

* <span data-ttu-id="07aba-1268">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1268">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="07aba-1269">Event Grid</span><span class="sxs-lookup"><span data-stu-id="07aba-1269">Event Grid</span></span>

* <span data-ttu-id="07aba-1270">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-1270">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="07aba-1271">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-1271">Network</span></span>

* <span data-ttu-id="07aba-1272">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1272">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="07aba-1273">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1273">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="07aba-1274">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1274">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="07aba-1275">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1275">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="07aba-1276">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-1276">Profile</span></span>

* <span data-ttu-id="07aba-1277">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1277">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-1278">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-1278">Storage</span></span>

* <span data-ttu-id="07aba-1279">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="07aba-1279">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-1280">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-1280">VM</span></span>

* <span data-ttu-id="07aba-1281">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1281">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="07aba-1282">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1282">Exposed `list-skus` command</span></span>
* <span data-ttu-id="07aba-1283">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1283">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="07aba-1284">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="07aba-1284">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="07aba-1285">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1285">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="07aba-1286">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1286">July 28, 2017</span></span>

<span data-ttu-id="07aba-1287">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="07aba-1287">Version 2.0.12</span></span>

* <span data-ttu-id="07aba-1288">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1288">Added container commands</span></span>
* <span data-ttu-id="07aba-1289">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1289">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="07aba-1290">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-1290">Core</span></span>

* <span data-ttu-id="07aba-1291">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="07aba-1291">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="07aba-1292">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1292">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="07aba-1293">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="07aba-1293">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="07aba-1294">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="07aba-1294">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="07aba-1295">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="07aba-1295">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="07aba-1296">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="07aba-1296">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="07aba-1297">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="07aba-1297">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="07aba-1298">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="07aba-1298">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="07aba-1299">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="07aba-1299">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="07aba-1300">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="07aba-1300">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="07aba-1301">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="07aba-1301">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="07aba-1302">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="07aba-1302">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="07aba-1303">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1303">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="07aba-1304">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1304">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="07aba-1305">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1305">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="07aba-1306">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="07aba-1306">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="07aba-1307">ACR</span><span class="sxs-lookup"><span data-stu-id="07aba-1307">ACR</span></span>

* <span data-ttu-id="07aba-1308">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1308">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="07aba-1309">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1309">Support SKU update for managed registries</span></span>
* <span data-ttu-id="07aba-1310">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1310">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="07aba-1311">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1311">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="07aba-1312">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1312">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="07aba-1313">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1313">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-1314">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-1314">ACS</span></span>

* <span data-ttu-id="07aba-1315">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1315">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-1316">Appservice</span><span class="sxs-lookup"><span data-stu-id="07aba-1316">Appservice</span></span>

* <span data-ttu-id="07aba-1317">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1317">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="07aba-1318">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1318">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="07aba-1319">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="07aba-1319">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="07aba-1320">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="07aba-1320">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="07aba-1321">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="07aba-1321">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="07aba-1322">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="07aba-1322">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="07aba-1323">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="07aba-1323">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="07aba-1324">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="07aba-1324">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="07aba-1325">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1325">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="07aba-1326">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="07aba-1326">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="07aba-1327">Batch</span><span class="sxs-lookup"><span data-stu-id="07aba-1327">Batch</span></span>

* <span data-ttu-id="07aba-1328">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1328">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="07aba-1329">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1329">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="07aba-1330">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1330">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="07aba-1331">CDN</span><span class="sxs-lookup"><span data-stu-id="07aba-1331">CDN</span></span>

* <span data-ttu-id="07aba-1332">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1332">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="07aba-1333">クラウド</span><span class="sxs-lookup"><span data-stu-id="07aba-1333">Cloud</span></span>

* <span data-ttu-id="07aba-1334">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1334">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="07aba-1335">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="07aba-1335">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="07aba-1336">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1336">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="07aba-1337">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1337">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="07aba-1338">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1338">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="07aba-1339">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="07aba-1339">CosmosDB</span></span>

* <span data-ttu-id="07aba-1340">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1340">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="07aba-1341">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1341">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="07aba-1342">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="07aba-1342">Data Lake Analytics</span></span>

* <span data-ttu-id="07aba-1343">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1343">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="07aba-1344">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1344">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="07aba-1345">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1345">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="07aba-1346">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="07aba-1346">Data Lake Store</span></span>

* <span data-ttu-id="07aba-1347">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1347">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="07aba-1348">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1348">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="07aba-1349">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1349">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="07aba-1350">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="07aba-1350">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="07aba-1351">対話</span><span class="sxs-lookup"><span data-stu-id="07aba-1351">Interactive</span></span>

* <span data-ttu-id="07aba-1352">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1352">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="07aba-1353">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="07aba-1353">Increased test coverage</span></span>
* <span data-ttu-id="07aba-1354">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1354">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="07aba-1355">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="07aba-1355">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="07aba-1356">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="07aba-1356">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="07aba-1357">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="07aba-1357">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="07aba-1358">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="07aba-1358">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="07aba-1359">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1359">Added `--progress` flag</span></span>
* <span data-ttu-id="07aba-1360">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1360">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="07aba-1361">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="07aba-1361">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="07aba-1362">IoT</span><span class="sxs-lookup"><span data-stu-id="07aba-1362">IoT</span></span>

* <span data-ttu-id="07aba-1363">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1363">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="07aba-1364">(#3934)</span><span class="sxs-lookup"><span data-stu-id="07aba-1364">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="07aba-1365">Key Vault</span><span class="sxs-lookup"><span data-stu-id="07aba-1365">Key vault</span></span>

* <span data-ttu-id="07aba-1366">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1366">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="07aba-1367">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="07aba-1367">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="07aba-1368">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="07aba-1368">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="07aba-1369">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="07aba-1369">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="07aba-1370">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="07aba-1370">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="07aba-1371">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="07aba-1371">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="07aba-1372">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1372">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="07aba-1373">(#3307)</span><span class="sxs-lookup"><span data-stu-id="07aba-1373">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="07aba-1374">ラボ</span><span class="sxs-lookup"><span data-stu-id="07aba-1374">Lab</span></span>

* <span data-ttu-id="07aba-1375">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1375">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="07aba-1376">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1376">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="07aba-1377">監視</span><span class="sxs-lookup"><span data-stu-id="07aba-1377">Monitor</span></span>

* <span data-ttu-id="07aba-1378">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="07aba-1378">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="07aba-1379">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1379">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="07aba-1380">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1380">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="07aba-1381">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1381">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="07aba-1382">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1382">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="07aba-1383">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1383">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="07aba-1384">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1384">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="07aba-1385">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="07aba-1385">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="07aba-1386">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1386">`location` no longer required</span></span>
  * <span data-ttu-id="07aba-1387">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="07aba-1387">Add name and ID support for target</span></span>
  * <span data-ttu-id="07aba-1388">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="07aba-1388">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="07aba-1389">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1389">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="07aba-1390">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1390">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="07aba-1391">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="07aba-1391">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="07aba-1392">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1392">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="07aba-1393">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1393">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="07aba-1394">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-1394">Network</span></span>

* <span data-ttu-id="07aba-1395">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1395">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="07aba-1396">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1396">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="07aba-1397">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1397">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="07aba-1398">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1398">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="07aba-1399">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1399">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="07aba-1400">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1400">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="07aba-1401">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1401">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="07aba-1402">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1402">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="07aba-1403">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1403">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="07aba-1404">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1404">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="07aba-1405">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1405">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="07aba-1406">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1406">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="07aba-1407">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1407">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="07aba-1408">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1408">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="07aba-1409">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1409">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="07aba-1410">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1410">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="07aba-1411">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1411">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="07aba-1412">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1412">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="07aba-1413">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1413">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="07aba-1414">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1414">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="07aba-1415">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1415">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="07aba-1416">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1416">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="07aba-1417">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1417">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="07aba-1418">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="07aba-1418">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="07aba-1419">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="07aba-1419">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="07aba-1420">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="07aba-1420">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="07aba-1421">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="07aba-1421">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="07aba-1422">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-1422">Profile</span></span>

* <span data-ttu-id="07aba-1423">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1423">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="07aba-1424">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1424">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="07aba-1425">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="07aba-1425">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="07aba-1426">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1426">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="07aba-1427">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1427">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="07aba-1428">RDBMS</span><span class="sxs-lookup"><span data-stu-id="07aba-1428">RDBMS</span></span>

* <span data-ttu-id="07aba-1429">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="07aba-1429">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="07aba-1430">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="07aba-1430">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="07aba-1431">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="07aba-1431">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="07aba-1432">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="07aba-1432">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-1433">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-1433">Resource</span></span>

* <span data-ttu-id="07aba-1434">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1434">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="07aba-1435">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1435">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="07aba-1436">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1436">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="07aba-1437">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1437">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="07aba-1438">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="07aba-1438">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="07aba-1439">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1439">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="07aba-1440">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="07aba-1440">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="07aba-1441">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1441">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="07aba-1442">Role</span><span class="sxs-lookup"><span data-stu-id="07aba-1442">Role</span></span>

* <span data-ttu-id="07aba-1443">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1443">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="07aba-1444">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="07aba-1444">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="07aba-1445">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="07aba-1445">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="07aba-1446">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="07aba-1446">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="07aba-1447">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1447">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="07aba-1448">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="07aba-1448">Service Fabric</span></span>
* <span data-ttu-id="07aba-1449">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="07aba-1449">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="07aba-1450">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="07aba-1450">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="07aba-1451">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="07aba-1451">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-1452">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-1452">SQL</span></span>

* <span data-ttu-id="07aba-1453">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1453">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="07aba-1454">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1454">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="07aba-1455">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1455">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-1456">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-1456">Storage</span></span>

* <span data-ttu-id="07aba-1457">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="07aba-1457">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="07aba-1458">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1458">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="07aba-1459">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="07aba-1459">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="07aba-1460">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="07aba-1460">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="07aba-1461">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="07aba-1461">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="07aba-1462">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="07aba-1462">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-1463">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-1463">VM</span></span>

* <span data-ttu-id="07aba-1464">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1464">Support configuring nsg</span></span>
* <span data-ttu-id="07aba-1465">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1465">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="07aba-1466">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="07aba-1466">Support managed service identities</span></span>
* <span data-ttu-id="07aba-1467">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1467">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="07aba-1468">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="07aba-1468">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="07aba-1469">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1469">May 10, 2017</span></span>

<span data-ttu-id="07aba-1470">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="07aba-1470">Version 2.0.6</span></span>

* <span data-ttu-id="07aba-1471">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1471">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="07aba-1472">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1472">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="07aba-1473">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1473">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="07aba-1474">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1474">Include Cognitive Services module</span></span>
* <span data-ttu-id="07aba-1475">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1475">Include Service Fabric module</span></span>
* <span data-ttu-id="07aba-1476">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="07aba-1476">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="07aba-1477">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1477">Add support for CDN commands</span></span>
* <span data-ttu-id="07aba-1478">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1478">Remove Container module</span></span>
* <span data-ttu-id="07aba-1479">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="07aba-1479">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="07aba-1480">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="07aba-1480">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="07aba-1481">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-1481">Core</span></span>

* <span data-ttu-id="07aba-1482">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="07aba-1482">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="07aba-1483">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="07aba-1483">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="07aba-1484">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="07aba-1484">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="07aba-1485">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="07aba-1485">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="07aba-1486">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="07aba-1486">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="07aba-1487">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="07aba-1487">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="07aba-1488">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="07aba-1488">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="07aba-1489">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="07aba-1489">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="07aba-1490">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="07aba-1490">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="07aba-1491">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="07aba-1491">core: Improved performance</span></span>
* <span data-ttu-id="07aba-1492">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="07aba-1492">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="07aba-1493">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="07aba-1493">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-1494">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-1494">ACS</span></span>

* <span data-ttu-id="07aba-1495">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1495">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="07aba-1496">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1496">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="07aba-1497">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1497">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="07aba-1498">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="07aba-1498">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-1499">AppService</span><span class="sxs-lookup"><span data-stu-id="07aba-1499">AppService</span></span>

* <span data-ttu-id="07aba-1500">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1500">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="07aba-1501">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1501">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="07aba-1502">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="07aba-1502">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="07aba-1503">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1503">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="07aba-1504">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1504">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="07aba-1505">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="07aba-1505">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="07aba-1506">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="07aba-1506">support slot swap with preview</span></span>
* <span data-ttu-id="07aba-1507">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="07aba-1507">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="07aba-1508">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="07aba-1508">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="07aba-1509">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="07aba-1509">CosmosDB</span></span>

* <span data-ttu-id="07aba-1510">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1510">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="07aba-1511">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1511">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="07aba-1512">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1512">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="07aba-1513">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1513">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="07aba-1514">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="07aba-1514">Data Lake Analytics</span></span>

* <span data-ttu-id="07aba-1515">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1515">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="07aba-1516">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1516">Add support for new catalog item type: package.</span></span> <span data-ttu-id="07aba-1517">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="07aba-1517">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="07aba-1518">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="07aba-1518">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="07aba-1519">テーブル</span><span class="sxs-lookup"><span data-stu-id="07aba-1519">Table</span></span>
  * <span data-ttu-id="07aba-1520">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="07aba-1520">Table valued function</span></span>
  * <span data-ttu-id="07aba-1521">表示</span><span class="sxs-lookup"><span data-stu-id="07aba-1521">View</span></span>
  * <span data-ttu-id="07aba-1522">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="07aba-1522">Table Statistics.</span></span> <span data-ttu-id="07aba-1523">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="07aba-1523">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="07aba-1524">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="07aba-1524">Data Lake Store</span></span>

* <span data-ttu-id="07aba-1525">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1525">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="07aba-1526">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="07aba-1526">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="07aba-1527">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="07aba-1527">missed help for access show.</span></span> <span data-ttu-id="07aba-1528">追加しました </span><span class="sxs-lookup"><span data-stu-id="07aba-1528">adding it.</span></span> <span data-ttu-id="07aba-1529">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="07aba-1529">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="07aba-1530">検索</span><span class="sxs-lookup"><span data-stu-id="07aba-1530">Find</span></span>

* <span data-ttu-id="07aba-1531">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1531">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="07aba-1532">KeyVault</span><span class="sxs-lookup"><span data-stu-id="07aba-1532">KeyVault</span></span>

* <span data-ttu-id="07aba-1533">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1533">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="07aba-1534">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1534">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="07aba-1535">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="07aba-1535">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="07aba-1536">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1536">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="07aba-1537">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="07aba-1537">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="07aba-1538">ラボ</span><span class="sxs-lookup"><span data-stu-id="07aba-1538">Lab</span></span>

* <span data-ttu-id="07aba-1539">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1539">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="07aba-1540">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1540">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="07aba-1541">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1541">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="07aba-1542">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1542">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="07aba-1543">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1543">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="07aba-1544">監視</span><span class="sxs-lookup"><span data-stu-id="07aba-1544">Monitor</span></span>

* <span data-ttu-id="07aba-1545">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="07aba-1545">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="07aba-1546">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="07aba-1546">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="07aba-1547">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-1547">Network</span></span>

* <span data-ttu-id="07aba-1548">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1548">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="07aba-1549">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1549">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="07aba-1550">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1550">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="07aba-1551">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1551">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="07aba-1552">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1552">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="07aba-1553">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1553">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="07aba-1554">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1554">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="07aba-1555">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1555">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="07aba-1556">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1556">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="07aba-1557">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1557">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="07aba-1558">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1558">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="07aba-1559">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1559">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="07aba-1560">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1560">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="07aba-1561">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1561">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="07aba-1562">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="07aba-1562">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="07aba-1563">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1563">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="07aba-1564">プロファイル</span><span class="sxs-lookup"><span data-stu-id="07aba-1564">Profile</span></span>

* <span data-ttu-id="07aba-1565">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="07aba-1565">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="07aba-1566">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="07aba-1566">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="07aba-1567">Redis</span><span class="sxs-lookup"><span data-stu-id="07aba-1567">Redis</span></span>

* <span data-ttu-id="07aba-1568">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1568">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="07aba-1569">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1569">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="07aba-1570">リソース</span><span class="sxs-lookup"><span data-stu-id="07aba-1570">Resource</span></span>

* <span data-ttu-id="07aba-1571">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="07aba-1571">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="07aba-1572">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="07aba-1572">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="07aba-1573">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="07aba-1573">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="07aba-1574">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="07aba-1574">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="07aba-1575">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="07aba-1575">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="07aba-1576">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="07aba-1576">Add docs for az lock update.</span></span> <span data-ttu-id="07aba-1577">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="07aba-1577">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="07aba-1578">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="07aba-1578">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="07aba-1579">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="07aba-1579">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="07aba-1580">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="07aba-1580">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="07aba-1581">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="07aba-1581">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="07aba-1582">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="07aba-1582">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="07aba-1583">Role</span><span class="sxs-lookup"><span data-stu-id="07aba-1583">Role</span></span>

* <span data-ttu-id="07aba-1584">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="07aba-1584">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="07aba-1585">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="07aba-1585">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="07aba-1586">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="07aba-1586">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="07aba-1587">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="07aba-1587">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="07aba-1588">SQL</span><span class="sxs-lookup"><span data-stu-id="07aba-1588">SQL</span></span>

* <span data-ttu-id="07aba-1589">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="07aba-1589">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="07aba-1590">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="07aba-1590">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="07aba-1591">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-1591">Storage</span></span>

* <span data-ttu-id="07aba-1592">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="07aba-1592">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="07aba-1593">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1593">Add support for incremental blob copy</span></span>
* <span data-ttu-id="07aba-1594">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1594">Add support for large block blob upload</span></span>
* <span data-ttu-id="07aba-1595">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="07aba-1595">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-1596">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-1596">VM</span></span>

* <span data-ttu-id="07aba-1597">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="07aba-1597">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="07aba-1598">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="07aba-1598">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="07aba-1599">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="07aba-1599">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="07aba-1600">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="07aba-1600">az vm/vmss disk</span></span>
  3. <span data-ttu-id="07aba-1601">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="07aba-1601">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="07aba-1602">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="07aba-1602">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="07aba-1603">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="07aba-1603">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="07aba-1604">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1604">April 3, 2017</span></span>

<span data-ttu-id="07aba-1605">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="07aba-1605">Version 2.0.2</span></span>

<span data-ttu-id="07aba-1606">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="07aba-1606">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="07aba-1607">コア</span><span class="sxs-lookup"><span data-stu-id="07aba-1607">Core</span></span>

* <span data-ttu-id="07aba-1608">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="07aba-1608">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="07aba-1609">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="07aba-1609">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="07aba-1610">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="07aba-1610">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="07aba-1611">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="07aba-1611">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="07aba-1612">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="07aba-1612">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="07aba-1613">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="07aba-1613">Add prompting for missing template parameters.</span></span> <span data-ttu-id="07aba-1614">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="07aba-1614">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="07aba-1615">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="07aba-1615">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="07aba-1616">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="07aba-1616">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="07aba-1617">ACS</span><span class="sxs-lookup"><span data-stu-id="07aba-1617">ACS</span></span>

* <span data-ttu-id="07aba-1618">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="07aba-1618">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="07aba-1619">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="07aba-1619">Add support for ssh key password prompting.</span></span> <span data-ttu-id="07aba-1620">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="07aba-1620">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="07aba-1621">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="07aba-1621">Add support for windows clusters.</span></span> <span data-ttu-id="07aba-1622">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="07aba-1622">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="07aba-1623">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="07aba-1623">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="07aba-1624">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="07aba-1624">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="07aba-1625">AppService</span><span class="sxs-lookup"><span data-stu-id="07aba-1625">AppService</span></span>

* <span data-ttu-id="07aba-1626">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="07aba-1626">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="07aba-1627">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="07aba-1627">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="07aba-1628">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="07aba-1628">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="07aba-1629">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="07aba-1629">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="07aba-1630">DataLake</span><span class="sxs-lookup"><span data-stu-id="07aba-1630">DataLake</span></span>

* <span data-ttu-id="07aba-1631">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-1631">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="07aba-1632">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="07aba-1632">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="07aba-1633">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="07aba-1633">DocuemntDB</span></span>

* <span data-ttu-id="07aba-1634">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="07aba-1634">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="07aba-1635">VM</span><span class="sxs-lookup"><span data-stu-id="07aba-1635">VM</span></span>

* <span data-ttu-id="07aba-1636">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="07aba-1636">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="07aba-1637">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="07aba-1637">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="07aba-1638">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="07aba-1638">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="07aba-1639">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="07aba-1639">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="07aba-1640">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="07aba-1640">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="07aba-1641">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="07aba-1641">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="07aba-1642">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="07aba-1642">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="07aba-1643">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="07aba-1643">February 27, 2017</span></span>

<span data-ttu-id="07aba-1644">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="07aba-1644">Version 2.0.0</span></span>

<span data-ttu-id="07aba-1645">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="07aba-1645">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="07aba-1646">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="07aba-1646">Container Service (acs)</span></span>
- <span data-ttu-id="07aba-1647">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="07aba-1647">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="07aba-1648">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07aba-1648">Networking</span></span>
- <span data-ttu-id="07aba-1649">Storage</span><span class="sxs-lookup"><span data-stu-id="07aba-1649">Storage</span></span>

<span data-ttu-id="07aba-1650">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="07aba-1650">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="07aba-1651">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="07aba-1651">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="07aba-1652">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="07aba-1652">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="07aba-1653">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="07aba-1653">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="07aba-1654">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="07aba-1654">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="07aba-1655">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="07aba-1655">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="07aba-1656">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="07aba-1656">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="07aba-1657">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="07aba-1657">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="07aba-1658">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="07aba-1658">Provide feedback from the command line with the `az feedback` command</span></span>

