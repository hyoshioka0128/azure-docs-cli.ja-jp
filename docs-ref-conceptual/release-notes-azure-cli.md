---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 04/01/2020
ms.topic: article
ms.service: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: cca6f42f29467126553c6e8a332907b1ad1ebc74
ms.sourcegitcommit: 712c8ca6457552b6b7a8866c1370a6ec51d07f2c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "80525262"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="4567b-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="4567b-103">Azure CLI release notes</span></span>

## <a name="april-01-2020"></a><span data-ttu-id="4567b-104">2020 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="4567b-104">April 01, 2020</span></span>

<span data-ttu-id="4567b-105">バージョン 2.3.1</span><span class="sxs-lookup"><span data-stu-id="4567b-105">Version 2.3.1</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-106">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-106">ACR</span></span>

* <span data-ttu-id="4567b-107">Linux の azure-mgmt-containerregistry の間違ったバージョンを修正します</span><span class="sxs-lookup"><span data-stu-id="4567b-107">Fix wrong version of azure-mgmt-containerregistry for Linux</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-108">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-108">Profile</span></span>

* <span data-ttu-id="4567b-109">az login:`latest` 以外のクラウド プロファイルでのログイン エラーを修正します</span><span class="sxs-lookup"><span data-stu-id="4567b-109">az login: Fix login failure with cloud profiles other than `latest`</span></span>

## <a name="march-31-2020"></a><span data-ttu-id="4567b-110">2020 年 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4567b-110">March 31, 2020</span></span>

<span data-ttu-id="4567b-111">バージョン 2.3.0</span><span class="sxs-lookup"><span data-stu-id="4567b-111">Version 2.3.0</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-112">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-112">ACR</span></span>

* <span data-ttu-id="4567b-113">'az acr task update': null ポインター例外</span><span class="sxs-lookup"><span data-stu-id="4567b-113">'az acr task update': null pointer exception</span></span>
* <span data-ttu-id="4567b-114">`az acr import`:--source と --registry の使用法を明確にするために、ヘルプとエラー メッセージを修正します</span><span class="sxs-lookup"><span data-stu-id="4567b-114">`az acr import`: Modify help and error message to clarify the usage of --source and --registry</span></span>
* <span data-ttu-id="4567b-115">引数 'registry_name' の検証コントロールを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-115">Add a validator for argument 'registry_name'</span></span>
* <span data-ttu-id="4567b-116">`az acr login`: '--expose-token' のプレビュー フラグを削除します</span><span class="sxs-lookup"><span data-stu-id="4567b-116">`az acr login`:Remove the preview flag on '--expose-token'</span></span>
* <span data-ttu-id="4567b-117">[重大な変更] 'az acr task create/update' の Branch パラメーターは削除されています</span><span class="sxs-lookup"><span data-stu-id="4567b-117">[BREAKING CHANGE] 'az acr task create/update' Branch parameter is removed</span></span>
* <span data-ttu-id="4567b-118">'az acr task update' ではコンテキスト、git-token、トリガーを個別に更新できるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-118">'az acr task update' Customer now can update context, git-token, and or triggers individually</span></span>
* <span data-ttu-id="4567b-119">'az acr agentpool': 新機能</span><span class="sxs-lookup"><span data-stu-id="4567b-119">'az acr agentpool': new feature</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-120">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-120">AKS</span></span>

* <span data-ttu-id="4567b-121">--api-server-authorized-ip-ranges の更新時の apiServerAccessProfile を修正します</span><span class="sxs-lookup"><span data-stu-id="4567b-121">Fix apiServerAccessProfile when updating --api-server-authorized-ip-ranges</span></span>
* <span data-ttu-id="4567b-122">aks update:更新時に送信 IP を入力値でオーバーライドします</span><span class="sxs-lookup"><span data-stu-id="4567b-122">aks update: Override outbound IPs with input values when update</span></span>
* <span data-ttu-id="4567b-123">MSI クラスターに SPN を作成しないようにし、MSI クラスターへの ACR のアタッチをサポートしてください</span><span class="sxs-lookup"><span data-stu-id="4567b-123">Do not create SPN for MSI clusters and support attach acr to MSI clusters</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-124">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-124">AMS</span></span>

* <span data-ttu-id="4567b-125">#12469 の修正: 'ask' パラメーターの問題が原因で、Fairplay content-key-policy の追加が失敗します</span><span class="sxs-lookup"><span data-stu-id="4567b-125">Fix #12469: adding Fairplay content-key-policy fails due to problems with 'ask' parameter</span></span>

### <a name="appconfig"></a><span data-ttu-id="4567b-126">AppConfig</span><span class="sxs-lookup"><span data-stu-id="4567b-126">AppConfig</span></span>

* <span data-ttu-id="4567b-127">kv export に --skip-keyvault を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-127">Add --skip-keyvault for kv export</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-128">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-128">AppService</span></span>

* <span data-ttu-id="4567b-129">#12509 の修正:az webapp up へのタグを既定で削除します</span><span class="sxs-lookup"><span data-stu-id="4567b-129">Fix #12509: Remove the tag to az webapp up by default</span></span>
* <span data-ttu-id="4567b-130">az functionapp create:--runtime-version ヘルプ メニューを更新し、ユーザーが dotnet に --runtime-version を指定した場合の警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-130">az functionapp create: Updated --runtime-version help menu and added warning when user specifies --runtime-version for dotnet</span></span>
* <span data-ttu-id="4567b-131">az functionapp create:javaVersion が Windows 関数アプリに設定される方法を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-131">az functionapp create: Updated the way javaVersion was being set for Windows function apps</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-132">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-132">ARM</span></span>

* <span data-ttu-id="4567b-133">az deployment create/validate:既定で --handle-extended-json-format を使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-133">az deployment create/validate: Use --handle-extended-json-format by default</span></span>
* <span data-ttu-id="4567b-134">az lock create:ヘルプ ドキュメントにサブリソースの作成例を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-134">az lock create: Add examples of creating subresource in the help documentation</span></span>
* <span data-ttu-id="4567b-135">az deployment {group/mg/sub/tenant} list:provisioningState フィルターをサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-135">az deployment {group/mg/sub/tenant} list: Support provisioningState filtering</span></span>
* <span data-ttu-id="4567b-136">az deployment:最後の引数の後に書かれたコメントの解析バグを修正します</span><span class="sxs-lookup"><span data-stu-id="4567b-136">az deployment: Fix the parse bug for comment under the last argument</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-137">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-137">Backup</span></span>

* <span data-ttu-id="4567b-138">複数ファイルの復元機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-138">Added multiple files restore capabilities</span></span>
* <span data-ttu-id="4567b-139">OS ディスクのみのバックアップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-139">Added support for Backing up OS Disks only</span></span>
* <span data-ttu-id="4567b-140">アンマネージドとしての復元を指定するための restore-as-unmanaged-disk パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-140">Added restore-as-unmanaged-disk parameter to specify unmanaged restore</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-141">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-141">Compute</span></span>

* <span data-ttu-id="4567b-142">az vm create:--nsg-rule の NONE オプションを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-142">az vm create: Add NONE option of --nsg-rule</span></span>
* <span data-ttu-id="4567b-143">az vmss create/update: VMSS 自動修復のプレビュー タグを削除します</span><span class="sxs-lookup"><span data-stu-id="4567b-143">az vmss create/update: remove vmss automatic repairs preview tag</span></span>
* <span data-ttu-id="4567b-144">az vm update:--workspace をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-144">az vm update: Support --workspace</span></span>
* <span data-ttu-id="4567b-145">VirtualMachineScaleSetExtension 初期化コードのバグを修正します</span><span class="sxs-lookup"><span data-stu-id="4567b-145">Fix a bug in VirtualMachineScaleSetExtension initialization code</span></span>
* <span data-ttu-id="4567b-146">VMAccessAgent のバージョンを 2.4 にアップグレードします</span><span class="sxs-lookup"><span data-stu-id="4567b-146">Upgrade VMAccessAgent version to 2.4</span></span>
* <span data-ttu-id="4567b-147">az vmss set-orchestration-service-state: VMSS オーケストレーション サービス状態の設定をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-147">az vmss set-orchestration-service-state: support vmss set orchestration service state</span></span>
* <span data-ttu-id="4567b-148">ディスク API のバージョンを 2019-11-01 にアップグレードします</span><span class="sxs-lookup"><span data-stu-id="4567b-148">Upgrade disk API version to 2019-11-01</span></span>
* <span data-ttu-id="4567b-149">az disk create: --disk-iops-read-only、--disk-mbps-read-only、--max-shares、--image-reference、--image-reference-lun、--gallery-image-reference、--gallery-image-reference-lun を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-149">az disk create: add --disk-iops-read-only, --disk-mbps-read-only, --max-shares, --image-reference, --image-reference-lun, --gallery-image-reference, --gallery-image-reference-lun</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="4567b-150">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-150">Cosmos DB</span></span>

* <span data-ttu-id="4567b-151">非推奨リダイレクトの --type オプションの欠落を修正します</span><span class="sxs-lookup"><span data-stu-id="4567b-151">Fix missing --type option for deprecation redirections</span></span>

### <a name="docker"></a><span data-ttu-id="4567b-152">Docker</span><span class="sxs-lookup"><span data-stu-id="4567b-152">Docker</span></span>

* <span data-ttu-id="4567b-153">Alpine 3.11 および Python 3.6.10 へ更新します</span><span class="sxs-lookup"><span data-stu-id="4567b-153">Update to Alpine 3.11 and Python 3.6.10</span></span>

### <a name="extension"></a><span data-ttu-id="4567b-154">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-154">Extension</span></span>

* <span data-ttu-id="4567b-155">パッケージを使用してシステム パスに拡張機能を読み込むことを許可します</span><span class="sxs-lookup"><span data-stu-id="4567b-155">Allow to load extensions in the system path via packages</span></span>

### <a name="hdinsight"></a><span data-ttu-id="4567b-156">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4567b-156">HDInsight</span></span>

* <span data-ttu-id="4567b-157">(az hdinsight create:)パラメーター `--minimal-tls-version`を使用した、最低限サポートされている tls バージョンの指定をサポートします。</span><span class="sxs-lookup"><span data-stu-id="4567b-157">(az hdinsight create:) Support customers specify minimal supported tls version by using parameter `--minimal-tls-version`.</span></span> <span data-ttu-id="4567b-158">使用可能な値は、1.0、1.1、1.2 です</span><span class="sxs-lookup"><span data-stu-id="4567b-158">The allowed value is 1.0,1.1,1.2</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-159">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-159">IoT</span></span>

* <span data-ttu-id="4567b-160">codeowner を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-160">Add codeowner</span></span>
* <span data-ttu-id="4567b-161">az iot hub create:既定の SKU を F1 から S1 に変更します</span><span class="sxs-lookup"><span data-stu-id="4567b-161">az iot hub create : Change default sku to S1 from F1</span></span>
* <span data-ttu-id="4567b-162">iot hub:2019-03-01-hybrid のプロファイルで IotHub をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-162">iot hub: Support IotHub in the profile of 2019-03-01-hybrid</span></span>

### <a name="iotcentral"></a><span data-ttu-id="4567b-163">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="4567b-163">IoTCentral</span></span>

* <span data-ttu-id="4567b-164">エラーの詳細を更新し、既定のアプリケーション テンプレートと確認メッセージを更新します</span><span class="sxs-lookup"><span data-stu-id="4567b-164">Update error details, update default application template and prompt message</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-165">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-165">KeyVault</span></span>

* <span data-ttu-id="4567b-166">証明書のバックアップ/復元をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-166">Support certificate backup/restore</span></span>
* <span data-ttu-id="4567b-167">keyvault create/update:--retention-days をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-167">keyvault create/update: Support --retention-days</span></span>
* <span data-ttu-id="4567b-168">一覧表示中にマネージド キー/シークレットは表示されなくなります</span><span class="sxs-lookup"><span data-stu-id="4567b-168">No longer display managed keys/secrets while listing</span></span>
* <span data-ttu-id="4567b-169">az keyvault create: コンテナーの作成中にネットワーク ルールを指定するための `--network-acls`、`--network-acls-ips`、`--network-acls-vnets`をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-169">az keyvault create: support `--network-acls`, `--network-acls-ips` and `--network-acls-vnets` for specifying network rules while creating vault</span></span>

### <a name="lock"></a><span data-ttu-id="4567b-170">ロック</span><span class="sxs-lookup"><span data-stu-id="4567b-170">Lock</span></span>

* <span data-ttu-id="4567b-171">az lock delete のバグの修正: az lock delete は Microsoft.DocumentDB では機能しません</span><span class="sxs-lookup"><span data-stu-id="4567b-171">az lock delete fix bug: az lock delete does not work on Microsoft.DocumentDB</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-172">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-172">Monitor</span></span>

* <span data-ttu-id="4567b-173">az monitor clone: あるリソースから別のリソースへのメトリック ルールの複製をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-173">az monitor clone: support clone metric rules from one resource to another</span></span>
* <span data-ttu-id="4567b-174">IcM179210086 の修正: Application Insights メトリックのカスタム メトリック アラートを作成できません</span><span class="sxs-lookup"><span data-stu-id="4567b-174">Fix IcM179210086: unable to create custom metric alert for their Application Insights metric</span></span>

### <a name="netappfiles"></a><span data-ttu-id="4567b-175">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="4567b-175">NetAppFiles</span></span>

* <span data-ttu-id="4567b-176">az volume create:レプリケーション操作 (許可、保留、再開、状態、削除) を追加して、データ保護ボリュームを許可します</span><span class="sxs-lookup"><span data-stu-id="4567b-176">az volume create: Allow data protection volumes adding replication operations: approve, suspend, resume, status, remove</span></span>

### <a name="network"></a><span data-ttu-id="4567b-177">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-177">Network</span></span>

* <span data-ttu-id="4567b-178">az network application-gateway waf-policy managed-rule rule-set add: Microsoft_BotManagerRuleSet をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-178">az network application-gateway waf-policy managed-rule rule-set add: support Microsoft_BotManagerRuleSet</span></span>
* <span data-ttu-id="4567b-179">network watcher flow-log show:</span><span class="sxs-lookup"><span data-stu-id="4567b-179">network watcher flow-log show: fix wrong deprecating info</span></span>
* <span data-ttu-id="4567b-180">Application Gateway リスナーでホスト名をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-180">support host names in application gateway listener</span></span>
* <span data-ttu-id="4567b-181">az network nat gateway: パブリック IP またはパブリック IP プレフィックスなしの空のリソースの作成をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-181">az network nat gateway: support create empty resource without public ip or public ip prefix</span></span>
* <span data-ttu-id="4567b-182">VPN ゲートウェイの世代をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-182">Support vpn gateway generation</span></span>
* <span data-ttu-id="4567b-183">`az network dns record-set {} add-record`で `--if-none-match` をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-183">Support `--if-none-match` in `az network dns record-set {} add-record`</span></span>

### <a name="packaging"></a><span data-ttu-id="4567b-184">梱包</span><span class="sxs-lookup"><span data-stu-id="4567b-184">Packaging</span></span>

* <span data-ttu-id="4567b-185">Python 3.5 のサポートは終了します</span><span class="sxs-lookup"><span data-stu-id="4567b-185">Drop support for python 3.5</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-186">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-186">Profile</span></span>

* <span data-ttu-id="4567b-187">az login:MFA エラーの警告を表示します</span><span class="sxs-lookup"><span data-stu-id="4567b-187">az login: Show warning for MFA error</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-188">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-188">RDBMS</span></span>

* <span data-ttu-id="4567b-189">PostgreSQL および MySQL 用のサーバー データ暗号化キー管理コマンドを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-189">Add server data encryption key management commands for PostgreSQL and MySQL</span></span>

## <a name="march-10-2020"></a><span data-ttu-id="4567b-190">2020 年 3 月 10 日</span><span class="sxs-lookup"><span data-stu-id="4567b-190">March 10, 2020</span></span>

<span data-ttu-id="4567b-191">バージョン 2.2.0</span><span class="sxs-lookup"><span data-stu-id="4567b-191">Version 2.2.0</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-192">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-192">ACR</span></span>

* <span data-ttu-id="4567b-193">修正: `az acr login` で誤ってエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="4567b-193">Fix: `az acr login` wrongly raise error</span></span>
* <span data-ttu-id="4567b-194">新しいコマンド `az acr helm install-cli` を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-194">Add new command `az acr helm install-cli`</span></span>
* <span data-ttu-id="4567b-195">プライベート リンクと CMK のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="4567b-195">Add private link and CMK support</span></span>
* <span data-ttu-id="4567b-196">'private-link-resource list' コマンドの追加</span><span class="sxs-lookup"><span data-stu-id="4567b-196">add 'private-link-resource list' command</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-197">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-197">AKS</span></span>

* <span data-ttu-id="4567b-198">クラウド シェルでの aks browse の修正</span><span class="sxs-lookup"><span data-stu-id="4567b-198">fix the aks browse in cloud shell</span></span>
* <span data-ttu-id="4567b-199">az aks:addon および agentpool NoneType エラーの監視を修正</span><span class="sxs-lookup"><span data-stu-id="4567b-199">az aks: Fix monitoring addon and agentpool NoneType errors</span></span>
* <span data-ttu-id="4567b-200">Azure Kubernetes クラスターの作成時にノード プールに --nodepool-tags を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-200">Add --nodepool-tags to node pool when creating azure kubernetes cluster</span></span>
* <span data-ttu-id="4567b-201">クラスターへの nodepool の追加または更新時に --tags を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-201">Add --tags when adding or updating a nodepool to cluster</span></span>
* <span data-ttu-id="4567b-202">aks create: `--enable-private-cluster` の追加</span><span class="sxs-lookup"><span data-stu-id="4567b-202">aks create: add `--enable-private-cluster`</span></span>
* <span data-ttu-id="4567b-203">Azure Kubernetes クラスターの作成時に --nodepool-labels を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-203">add --nodepool-labels when creating azure kubernetes cluster</span></span>
* <span data-ttu-id="4567b-204">Azure Kubernetes クラスターへの新しい nodepool 追加時に --labels を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-204">add --labels when adding a new nodepool to azure kubernetes cluster</span></span>
* <span data-ttu-id="4567b-205">ダッシュボード URL に欠落していた / を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-205">add missing / in the dashboard url</span></span>
* <span data-ttu-id="4567b-206">マネージド ID を有効にする aks クラスターの作成のサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-206">Support create aks clusters enabling managed identity</span></span>
* <span data-ttu-id="4567b-207">az aks:ネットワーク プラグインが "azure" または "kubernet" のいずれかであることを検証</span><span class="sxs-lookup"><span data-stu-id="4567b-207">az aks: Validate network plugin to be either "azure" or "kubenet"</span></span>
* <span data-ttu-id="4567b-208">az aks:aad セッション キーのサポートの追加</span><span class="sxs-lookup"><span data-stu-id="4567b-208">az aks: Add aad session key support</span></span>
* <span data-ttu-id="4567b-209">[重大な変更] az aks: omsagent での GF と BF に対する msi 変更のサポート (コンテナー監視)(#1)</span><span class="sxs-lookup"><span data-stu-id="4567b-209">[BREAKING CHANGE] az aks: support msi changes for GF and BF for omsagent (Container monitoring)(#1)</span></span>
* <span data-ttu-id="4567b-210">az aks use-dev-spaces:Azure Dev Spaces コントローラー上に作成されたエンドポイントをカスタマイズするために、use-dev-spaces コマンドにエンドポイントの種類オプションを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-210">az aks use-dev-spaces: Adding endpoint type option to the use-dev-spaces command to customize the endpoint created on an Azure Dev Spaces controller</span></span>

### <a name="appconfig"></a><span data-ttu-id="4567b-211">AppConfig</span><span class="sxs-lookup"><span data-stu-id="4567b-211">AppConfig</span></span>

* <span data-ttu-id="4567b-212">keyvault 参照および機能の追加のための "kv set" を使用したブロック解除</span><span class="sxs-lookup"><span data-stu-id="4567b-212">Unblock using "kv set" to add keyvault reference and feature …</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-213">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-213">AppService</span></span>

* <span data-ttu-id="4567b-214">az webapp create:--runtime を指定したコマンドの実行時の問題を修正</span><span class="sxs-lookup"><span data-stu-id="4567b-214">az webapp create : Fix issue when running the command with --runtime</span></span>
* <span data-ttu-id="4567b-215">az functionapp deployment source config-zip:リソース グループまたは関数名が無効であるか存在しない場合のエラー メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="4567b-215">az functionapp deployment source config-zip: Add an error message if resource group or function name are invalid/don't exist</span></span>
* <span data-ttu-id="4567b-216">functionapp create:`functionapp create` で表示される警告メッセージの修正 (現在、これは`--functions_version` フラグを示しますが、誤ってフラグ名の `-` ではなく `_` を使用します)</span><span class="sxs-lookup"><span data-stu-id="4567b-216">functionapp create: Fix the warning message that appears with `functionapp create` today which cites a `--functions_version` flag but erroneously uses a `_` instead of a `-` in the flag name</span></span>
* <span data-ttu-id="4567b-217">az functionapp create:Linux 関数アプリに linuxFxVersion とコンテナー イメージ名が設定されていた方法を更新</span><span class="sxs-lookup"><span data-stu-id="4567b-217">az functionapp create: Updated the way linuxFxVersion and container image name were being set for linux function apps</span></span>
* <span data-ttu-id="4567b-218">az functionapp deployment source config-zip:zip デプロイ中にアプリ設定の変更の競合状態によって発生する問題 (デプロイ時に 5xx エラーが表示される) を修正</span><span class="sxs-lookup"><span data-stu-id="4567b-218">az functionapp deployment source config-zip: Fix an issue caused by app settings change racing condition during zip deploy, giving 5xx errors during deployment</span></span>
* <span data-ttu-id="4567b-219">#5720946 の修正: az webapp backup で名前の設定に失敗する</span><span class="sxs-lookup"><span data-stu-id="4567b-219">Fix #5720946: az webapp backup fails to set name</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-220">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-220">ARM</span></span>

* <span data-ttu-id="4567b-221">az resource:リソース モジュールの例の改善</span><span class="sxs-lookup"><span data-stu-id="4567b-221">az resource: Improve the examples of the resource module</span></span>
* <span data-ttu-id="4567b-222">az policy assignment list:管理グループ スコープでのポリシー割り当ての一覧表示をサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-222">az policy assignment list: Support listing policy assignments at Management Group scope</span></span>
* <span data-ttu-id="4567b-223">リソース グループでのテンプレートのデプロイ用に `az deployment group` と `az deployment operation group` を追加。</span><span class="sxs-lookup"><span data-stu-id="4567b-223">Add `az deployment group` and `az deployment operation group` for template deployment at resource groups.</span></span> <span data-ttu-id="4567b-224">これは `az group deployment` と `az group deployment operation` の複製です</span><span class="sxs-lookup"><span data-stu-id="4567b-224">This is a duplicate of `az group deployment` and `az group deployment operation`</span></span>
* <span data-ttu-id="4567b-225">サブスクリプション スコープでのテンプレートのデプロイ用に `az deployment sub` と `az deployment operation sub` を追加。</span><span class="sxs-lookup"><span data-stu-id="4567b-225">Add `az deployment sub` and `az deployment operation sub` for template deployment at subscription scope.</span></span> <span data-ttu-id="4567b-226">これは `az deployment` と `az deployment operation` の複製です</span><span class="sxs-lookup"><span data-stu-id="4567b-226">This is a duplicate of `az deployment` and `az deployment operation`</span></span>
* <span data-ttu-id="4567b-227">管理グループでのテンプレートのデプロイ用に `az deployment mg` と `az deployment operation mg` を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-227">Add `az deployment mg` and `az deployment operation mg` for template deployment at management groups</span></span>
* <span data-ttu-id="4567b-228">テナント スコープでのテンプレートのデプロイ用に `az deployment tenant` と `az deployment operation tenant` を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-228">Add `az deployment tenant` and `az deployment operation tenant` for template deployment at tenant scope</span></span>
* <span data-ttu-id="4567b-229">az policy assignment create:`--location` パラメーターに対する説明の追加</span><span class="sxs-lookup"><span data-stu-id="4567b-229">az policy assignment create: Add a description to the `--location` parameter</span></span>
* <span data-ttu-id="4567b-230">az group deployment create:クロス テナントをサポートするためにパラメーター `--aux-tenants` を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-230">az group deployment create: Add parameter `--aux-tenants` to support cross tenants</span></span>

### <a name="cdn"></a><span data-ttu-id="4567b-231">CDN</span><span class="sxs-lookup"><span data-stu-id="4567b-231">CDN</span></span>

* <span data-ttu-id="4567b-232">CDN WAF コマンドの追加</span><span class="sxs-lookup"><span data-stu-id="4567b-232">Add CDN WAF commands</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-233">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-233">Compute</span></span>

* <span data-ttu-id="4567b-234">az sig image-version: --data-snapshot-luns の追加</span><span class="sxs-lookup"><span data-stu-id="4567b-234">az sig image-version: add --data-snapshot-luns</span></span>
* <span data-ttu-id="4567b-235">az ppg show: 近接配置グループ内のすべてのリソースのコロケーションの状態をフェッチできるように、--colocation-status を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-235">az ppg show: add --colocation-status to enable fetching the colocation status of all the resources in the proximity placement group</span></span>
* <span data-ttu-id="4567b-236">az vmss create/update: 自動修復のサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-236">az vmss create/update: support automatic repairs</span></span>
* <span data-ttu-id="4567b-237">[重大な変更] az image template: テンプレートの名前を builder に変更</span><span class="sxs-lookup"><span data-stu-id="4567b-237">[BREAKING CHANGE] az image template: rename template to builder</span></span>
* <span data-ttu-id="4567b-238">az image builder create: --image-template の追加</span><span class="sxs-lookup"><span data-stu-id="4567b-238">az image builder create: add --image-template</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="4567b-239">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-239">Cosmos DB</span></span>

* <span data-ttu-id="4567b-240">SQL ストアド プロシージャ、udf およびトリガーのコマンドレットの追加</span><span class="sxs-lookup"><span data-stu-id="4567b-240">Add Sql stored procedure, udf and trigger cmdlets</span></span>
* <span data-ttu-id="4567b-241">az cosmosdb create: キー コンテナーの暗号化情報の追加をサポートするために、--key-uri を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-241">az cosmosdb create: add --key-uri to support adding key vault encryption information</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-242">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-242">KeyVault</span></span>

* <span data-ttu-id="4567b-243">keyvault create: 論理的な削除を既定で有効化</span><span class="sxs-lookup"><span data-stu-id="4567b-243">keyvault create: enable soft-delete by default</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-244">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-244">Monitor</span></span>

* <span data-ttu-id="4567b-245">az monitor metrics alert create: `--condition` での `~` のサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-245">az monitor metrics alert create: support `~` in `--condition`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-246">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-246">Network</span></span>

* <span data-ttu-id="4567b-247">az network application-gateway rewrite-rule create: URL の構成のサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-247">az network application-gateway rewrite-rule create: support url configuration</span></span>
* <span data-ttu-id="4567b-248">az network dns zone import: 今後、--zone-name は大文字と小文字を区別する</span><span class="sxs-lookup"><span data-stu-id="4567b-248">az network dns zone import: --zone-name will be case insensitive in the future</span></span>
* <span data-ttu-id="4567b-249">az network private-endpoint/private-link-service: プレビュー ラベルの削除</span><span class="sxs-lookup"><span data-stu-id="4567b-249">az network private-endpoint/private-link-service: remove preview label</span></span>
* <span data-ttu-id="4567b-250">az network bastion: Bastion のサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-250">az network bastion: support bastion</span></span>
* <span data-ttu-id="4567b-251">az network vnet list-available-ips: VNet 内で使用可能な IP の一覧のサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-251">az network vnet list-available-ips: support list available ips in a vnet</span></span>
* <span data-ttu-id="4567b-252">az network watcher flow-log create/list/delete/update: Watcher フロー ログを管理するために新しいコマンドを追加し、Watcher を明示的に識別するために --location を公開</span><span class="sxs-lookup"><span data-stu-id="4567b-252">az network watcher flow-log create/list/delete/update: add new commands to manage watcher flow log and exposing --location to identify watcher explicitly</span></span>
* <span data-ttu-id="4567b-253">az network watcher flow-log configure: 非推奨</span><span class="sxs-lookup"><span data-stu-id="4567b-253">az network watcher flow-log configure: deprecated</span></span>
* <span data-ttu-id="4567b-254">az network watcher flow-log show: ARM 形式の結果 (非推奨の古い形式の出力) を取得するために --location および--name をサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-254">az network watcher flow-log show: support --location and --name to get ARM-formatted result, deprecated old formatted output</span></span>

### <a name="policy"></a><span data-ttu-id="4567b-255">ポリシー</span><span class="sxs-lookup"><span data-stu-id="4567b-255">Policy</span></span>

* <span data-ttu-id="4567b-256">az policy assignment create:ポリシー割り当ての自動生成された名前が制限を超えるというバグの修正</span><span class="sxs-lookup"><span data-stu-id="4567b-256">az policy assignment create: Fix the bug that automatically generated name of policy assignment exceeds the limit</span></span>

### <a name="rbac"></a><span data-ttu-id="4567b-257">RBAC</span><span class="sxs-lookup"><span data-stu-id="4567b-257">RBAC</span></span>

* <span data-ttu-id="4567b-258">az ad group show: RegEx の問題として扱われる --group 値の修正</span><span class="sxs-lookup"><span data-stu-id="4567b-258">az ad group show: fix --group value treated as regex problem</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-259">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-259">RDBMS</span></span>

* <span data-ttu-id="4567b-260">azure-mgmt-rdbms SDK のバージョンを 2.0.0 にバージョンアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-260">Bump the azure-mgmt-rdbms SDK version to 2.0.0</span></span>
* <span data-ttu-id="4567b-261">az postgres private-endpoint-connection: Postgres プライベート エンドポイント接続の管理</span><span class="sxs-lookup"><span data-stu-id="4567b-261">az postgres private-endpoint-connection: manage postgres private endpoint connections</span></span>
* <span data-ttu-id="4567b-262">az postgres private-link-resource: Postgres プライベート リンク リソースの管理</span><span class="sxs-lookup"><span data-stu-id="4567b-262">az postgres private-link-resource: manage postgres private link resources</span></span>
* <span data-ttu-id="4567b-263">az mysql private-endpoint-connection: MySQL プライベート エンドポイント接続の管理</span><span class="sxs-lookup"><span data-stu-id="4567b-263">az mysql private-endpoint-connection: manage mysql private endpoint connections</span></span>
* <span data-ttu-id="4567b-264">az mysql private-link-resource: MySQL プライベート リンク リソースの管理</span><span class="sxs-lookup"><span data-stu-id="4567b-264">az mysql private-link-resource: manage mysql private link resources</span></span>
* <span data-ttu-id="4567b-265">az mariadb private-endpoint-connection: MariaDB プライベート エンドポイント接続の管理</span><span class="sxs-lookup"><span data-stu-id="4567b-265">az mariadb private-endpoint-connection: manage mariadb private endpoint connections</span></span>
* <span data-ttu-id="4567b-266">az mariadb private-link-resource: MariaDB プライベート リンク リソースの管理</span><span class="sxs-lookup"><span data-stu-id="4567b-266">az mariadb private-link-resource: manage mariadb private link resources</span></span>
* <span data-ttu-id="4567b-267">RDBMS プライベート エンドポイント テストを更新中</span><span class="sxs-lookup"><span data-stu-id="4567b-267">Updating RDBMS Private Endpoint Tests</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-268">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-268">SQL</span></span>

* <span data-ttu-id="4567b-269">Sql midb Add: list-deleted、show-deleted、update-retention、show-retention</span><span class="sxs-lookup"><span data-stu-id="4567b-269">Sql midb Add: list-deleted, show-deleted, update-retention, show-retention</span></span>
* <span data-ttu-id="4567b-270">(sql server create:)オプションの public-network-access 'Enable'/'Disable' フラグを sql server create に追加</span><span class="sxs-lookup"><span data-stu-id="4567b-270">(sql server create:) Add optional public-network-access 'Enable'/'Disable' flag to sql server create</span></span>
* <span data-ttu-id="4567b-271">(sql server update:) 顧客向けの変更の実施</span><span class="sxs-lookup"><span data-stu-id="4567b-271">(sql server update:) make some customer-facing change</span></span>
* <span data-ttu-id="4567b-272">MI および SQL DB 用の minimal_tls_version プロパティの追加</span><span class="sxs-lookup"><span data-stu-id="4567b-272">Add minimal_tls_version property for MI and SQL DB</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-273">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-273">Storage</span></span>

* <span data-ttu-id="4567b-274">az storage blob delete-batch:`--dryrun` フラグの誤動作</span><span class="sxs-lookup"><span data-stu-id="4567b-274">az storage blob delete-batch: Misbehaving `--dryrun` flag</span></span>
* <span data-ttu-id="4567b-275">az storage account network-rule add (バグ修正): 追加操作は、べき等にする必要がある</span><span class="sxs-lookup"><span data-stu-id="4567b-275">az storage account network-rule add (bug fix): add operation should be idempotent</span></span>
* <span data-ttu-id="4567b-276">az storage account create/update:ルーティングの優先順位のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-276">az storage account create/update: Add Routing Preference support</span></span>
* <span data-ttu-id="4567b-277">azure-mgmt-storage のバージョンを 8.0.0 にアップグレード</span><span class="sxs-lookup"><span data-stu-id="4567b-277">Upgrade azure-mgmt-storage version to 8.0.0</span></span>
* <span data-ttu-id="4567b-278">az storage container immutability create: --allow-protected-append-write パラメーターの追加</span><span class="sxs-lookup"><span data-stu-id="4567b-278">az storage container immutability create: add --allow-protected-append-write parameter</span></span>
* <span data-ttu-id="4567b-279">az storage account private-link-resource list:ストレージ アカウントのプライベート リンク リソースを一覧表示するためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-279">az storage account private-link-resource list: Add support to list private link resources for storage account</span></span>
* <span data-ttu-id="4567b-280">az storage account private-endpoint-connection approve/reject/show/delete:プライベート エンドポイント接続の管理のサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-280">az storage account private-endpoint-connection approve/reject/show/delete: Support to manage private endpoint connections</span></span>
* <span data-ttu-id="4567b-281">az storage account blob-service-properties update: --enable-restore-policy と --restore-days の追加</span><span class="sxs-lookup"><span data-stu-id="4567b-281">az storage account blob-service-properties update: add --enable-restore-policy and --restore-days</span></span>
* <span data-ttu-id="4567b-282">az storage blob restore:BLOB 範囲を復元するためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-282">az storage blob restore: Add support to restore blob ranges</span></span>

## <a name="february-18-2020"></a><span data-ttu-id="4567b-283">2020 年 2 月 18 日</span><span class="sxs-lookup"><span data-stu-id="4567b-283">February 18, 2020</span></span>

<span data-ttu-id="4567b-284">バージョン 2.1.0</span><span class="sxs-lookup"><span data-stu-id="4567b-284">Version 2.1.0</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-285">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-285">ACR</span></span>

* <span data-ttu-id="4567b-286">`az acr login` の新しい引数 `--expose-token` を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-286">Add a new argument `--expose-token` for `az acr login`</span></span>
* <span data-ttu-id="4567b-287">`az acr task identity show -n Name -r Registry -o table` の正しくない出力を修正</span><span class="sxs-lookup"><span data-stu-id="4567b-287">Fix the incorrect output of `az acr task identity show -n Name -r Registry -o table`</span></span>
* <span data-ttu-id="4567b-288">az acr login:Docker コマンドによって返されたエラーが返された場合は CLIError をスロー</span><span class="sxs-lookup"><span data-stu-id="4567b-288">az acr login: Throw a CLIError if there are errors returned by docker command</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-289">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-289">ACS</span></span>

* <span data-ttu-id="4567b-290">aks create/update: `--vnet-subnet-id` の検証を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-290">aks create/update: add `--vnet-subnet-id` validation</span></span>

### <a name="aladdin"></a><span data-ttu-id="4567b-291">Aladdin</span><span class="sxs-lookup"><span data-stu-id="4567b-291">Aladdin</span></span>

* <span data-ttu-id="4567b-292">生成された例をコマンドの _help.py として解析</span><span class="sxs-lookup"><span data-stu-id="4567b-292">Parse generated examples into commands' _help.py</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-293">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-293">AMS</span></span>

* <span data-ttu-id="4567b-294">az ams の一般提供を開始</span><span class="sxs-lookup"><span data-stu-id="4567b-294">az ams is GA now</span></span>

### <a name="appconfig"></a><span data-ttu-id="4567b-295">AppConfig</span><span class="sxs-lookup"><span data-stu-id="4567b-295">AppConfig</span></span>

* <span data-ttu-id="4567b-296">サポートされていないキー/ラベル フィルターを除外するようにヘルプ メッセージを変更</span><span class="sxs-lookup"><span data-stu-id="4567b-296">Revise help message to exclude unsupported key/label filter</span></span>
* <span data-ttu-id="4567b-297">マネージド ID と機能フラグを除くほとんどのコマンドのプレビュー タグを削除</span><span class="sxs-lookup"><span data-stu-id="4567b-297">Remove preview tag for most commands excluding managed identity and feature flags</span></span>
* <span data-ttu-id="4567b-298">ストアの更新時にカスタマー マネージド キーを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-298">Add customer managed key when updating stores</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-299">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-299">AppService</span></span>

* <span data-ttu-id="4567b-300">az webapp list-runtimes:list-runtimes のバグを修正</span><span class="sxs-lookup"><span data-stu-id="4567b-300">az webapp list-runtimes: Fix the bug for list-runtimes</span></span>
* <span data-ttu-id="4567b-301">az webapp | functionapp config ssl create を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-301">Add az webapp|functionapp config ssl create</span></span>
* <span data-ttu-id="4567b-302">v3 関数アプリおよびノード 12 のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-302">Add support for v3 function apps and node 12</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-303">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-303">ARM</span></span>

* <span data-ttu-id="4567b-304">az policy assignment create:`--policy` パラメーターが無効な場合のエラー メッセージを修正</span><span class="sxs-lookup"><span data-stu-id="4567b-304">az policy assignment create: Fix the error message when the `--policy` parameter is invalid</span></span>
* <span data-ttu-id="4567b-305">az group deployment create:サイズの大きな parameters.json ファイルの使用時の "stat: path too long for Windows" エラーを修正</span><span class="sxs-lookup"><span data-stu-id="4567b-305">az group deployment create: Fix "stat: path too long for Windows" error when using large parameters.json file</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-306">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-306">Backup</span></span>

* <span data-ttu-id="4567b-307">OLR のアイテム レベルの回復フローを修正</span><span class="sxs-lookup"><span data-stu-id="4567b-307">Fix for item level recovery flow in OLR</span></span>
* <span data-ttu-id="4567b-308">SQL Database および SAP Database のファイルとしての復元のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-308">Add restore as files support for SQL and SAP Databases</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-309">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-309">Compute</span></span>

* <span data-ttu-id="4567b-310">vm/vmss/availability-set update: ProximityPlacementGroup を更新できるように --ppg を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-310">vm/vmss/availability-set update: add --ppg to allowing updating ProximityPlacementGroup</span></span>
* <span data-ttu-id="4567b-311">vmss create: --data-disk-iops および --data-disk-mbps を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-311">vmss create: add --data-disk-iops and --data-disk-mbps</span></span>
* <span data-ttu-id="4567b-312">az vm host: `vm host` および `vm host group` のプレビュー タグを削除</span><span class="sxs-lookup"><span data-stu-id="4567b-312">az vm host: remove preview tag for `vm host` and `vm host group`</span></span>
* <span data-ttu-id="4567b-313">[重大な変更] #10728 を修正: `az vm create`: vnet が指定されている場合、サブネットが存在しなければサブネットが自動的に作成される</span><span class="sxs-lookup"><span data-stu-id="4567b-313">[BREAKING CHANGE] Fix #10728: `az vm create`: create subnet automatically if vnet is specified and subnet not exists</span></span>
* <span data-ttu-id="4567b-314">vm イメージ リストの信頼性を向上</span><span class="sxs-lookup"><span data-stu-id="4567b-314">Increase robustness of vm image list</span></span>

### <a name="eventhub"></a><span data-ttu-id="4567b-315">Eventhub</span><span class="sxs-lookup"><span data-stu-id="4567b-315">Eventhub</span></span>

* <span data-ttu-id="4567b-316">2019-03-01-hybrid プロファイルに対する Azure Stack のサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-316">Azure Stack support for 2019-03-01-hybrid profile</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-317">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-317">KeyVault</span></span>

* <span data-ttu-id="4567b-318">az keyvault key create: パラメーター `--ops` の新しい値 `import` を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-318">az keyvault key create: add a new value `import` for parameter `--ops`</span></span>
* <span data-ttu-id="4567b-319">az keyvault key list-versions: キー指定のためのパラメーター `--id` をサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-319">az keyvault key list-versions: support parameter `--id` for specifying keys</span></span>
* <span data-ttu-id="4567b-320">プライベート エンドポイントの接続をサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-320">Support private endpoint connections</span></span>

### <a name="network"></a><span data-ttu-id="4567b-321">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-321">Network</span></span>

* <span data-ttu-id="4567b-322">azure-mgmt-network 9.0.0 にバージョンアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-322">Bump to azure-mgmt-network 9.0.0</span></span>
* <span data-ttu-id="4567b-323">az network private-link-service update/create: support --enable-proxy-protocol</span><span class="sxs-lookup"><span data-stu-id="4567b-323">az network private-link-service update/create: support --enable-proxy-protocol</span></span>
* <span data-ttu-id="4567b-324">接続モニター V2 の機能を追加</span><span class="sxs-lookup"><span data-stu-id="4567b-324">Add connection Monitor V2 feature</span></span>

### <a name="packaging"></a><span data-ttu-id="4567b-325">梱包</span><span class="sxs-lookup"><span data-stu-id="4567b-325">Packaging</span></span>

* <span data-ttu-id="4567b-326">[重大な変更] Python 2.7 のサポートを終了</span><span class="sxs-lookup"><span data-stu-id="4567b-326">[BREAKING CHANGE] Drop support for Python 2.7</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-327">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-327">Profile</span></span>

* <span data-ttu-id="4567b-328">プレビュー:サブスクリプション アカウントに新しい属性 `homeTenantId` および `managedByTenants` を追加。</span><span class="sxs-lookup"><span data-stu-id="4567b-328">Preview: Add new attributes `homeTenantId` and `managedByTenants` to subscription accounts.</span></span> <span data-ttu-id="4567b-329">変更を有効にするには、`az login` を再実行してください</span><span class="sxs-lookup"><span data-stu-id="4567b-329">Please re-run `az login` for the changes to take effect</span></span>
* <span data-ttu-id="4567b-330">az login:1 つのサブスクリプションが複数のテナントからリストされる場合は警告を表示して最初のものに既定で設定。</span><span class="sxs-lookup"><span data-stu-id="4567b-330">az login: Show a warning when a subscription is listed from more than one tenants and default to the first one.</span></span> <span data-ttu-id="4567b-331">このサブスクリプションにアクセスする際の特定のテナントを選択するには、`az login` に `--tenant` を含めてください</span><span class="sxs-lookup"><span data-stu-id="4567b-331">To select a specific tenant when accessing this subscription, please include `--tenant` in `az login`</span></span>

### <a name="role"></a><span data-ttu-id="4567b-332">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-332">Role</span></span>

* <span data-ttu-id="4567b-333">az role assignment create:表示名でサービス プリンシパルにロールを割り当てた場合に HTTP 400 が発生するエラーを修正</span><span class="sxs-lookup"><span data-stu-id="4567b-333">az role assignment create: Fix the error that assigning a role to a service principal by display name yields a HTTP 400</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-334">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-334">SQL</span></span>

* <span data-ttu-id="4567b-335">Update SQL Managed Instance のコマンドレット `az sql mi update` に 2 つのパラメーター tier および family を追加して更新</span><span class="sxs-lookup"><span data-stu-id="4567b-335">Update SQL Managed Instance cmdlet `az sql mi update` with two new parameters: tier and family</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-336">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-336">Storage</span></span>

* <span data-ttu-id="4567b-337">[破壊的変更] `az storage account create`:既定のストレージ アカウントの種類を StorageV2 に変更</span><span class="sxs-lookup"><span data-stu-id="4567b-337">[BREAKING CHANGE] `az storage account create`: Change default storage account kind to StorageV2</span></span>

## <a name="february-04-2020"></a><span data-ttu-id="4567b-338">2020 年 2 月 4 日</span><span class="sxs-lookup"><span data-stu-id="4567b-338">February 04, 2020</span></span>

<span data-ttu-id="4567b-339">バージョン 2.0.81</span><span class="sxs-lookup"><span data-stu-id="4567b-339">Version 2.0.81</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-340">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-340">ACS</span></span>

* <span data-ttu-id="4567b-341">Standard Load Balancer でアウトバウンド割当てポートとアイドル タイムアウトを設定するためのサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-341">Add support to set outbound allocated ports and idle timeouts on standard load balancer</span></span>
* <span data-ttu-id="4567b-342">API バージョン 2019-11-01 への更新を行います</span><span class="sxs-lookup"><span data-stu-id="4567b-342">Update to API Version 2019-11-01</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-343">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-343">ACR</span></span>

* <span data-ttu-id="4567b-344">[破壊的変更] `az acr delete` でプロンプトが表示されます</span><span class="sxs-lookup"><span data-stu-id="4567b-344">[BREAKING CHANGE] `az acr delete` will prompt</span></span>
* <span data-ttu-id="4567b-345">[重大な変更] 'az acr task delete' でプロンプトが表示されます</span><span class="sxs-lookup"><span data-stu-id="4567b-345">[BREAKING CHANGE] 'az acr task delete' will prompt</span></span>
* <span data-ttu-id="4567b-346">taskrun 管理用の新しいコマンド グループ 'az acr taskrun show/list/delete' を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-346">Add a new command group 'az acr taskrun show/list/delete' for taskrun management</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-347">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-347">AKS</span></span>

* <span data-ttu-id="4567b-348">各クラスターは、分離を向上させるために、個別のサービス プリンシパルを取得します</span><span class="sxs-lookup"><span data-stu-id="4567b-348">Each cluster gets a separate service principal to improve isolation</span></span>

### <a name="appconfig"></a><span data-ttu-id="4567b-349">AppConfig</span><span class="sxs-lookup"><span data-stu-id="4567b-349">AppConfig</span></span>

* <span data-ttu-id="4567b-350">appservice との間での keyvault 参照のインポート/エクスポートをサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-350">Support import/export of keyvault references from/to appservice</span></span>
* <span data-ttu-id="4567b-351">appconfig から appconfig へのすべてのラベルのインポート/エクスポートをサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-351">Support import/export of all labels from appconfig to appconfig</span></span>
* <span data-ttu-id="4567b-352">設定とインポートの前にキーと機能の名前を検証します</span><span class="sxs-lookup"><span data-stu-id="4567b-352">Validate key and feature names before setting and importing</span></span>
* <span data-ttu-id="4567b-353">構成ストアの SKU 変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="4567b-353">Expose sku modification for configuration store.</span></span>
* <span data-ttu-id="4567b-354">マネージド ID のコマンド グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="4567b-354">Add command group for managed identity.</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-355">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-355">AppService</span></span>

* <span data-ttu-id="4567b-356">Azure Stack: 2019-03-01-hybrid のプロファイルの下の surface コマンド</span><span class="sxs-lookup"><span data-stu-id="4567b-356">Azure Stack: surface commands under the profile of 2019-03-01-hybrid</span></span>
* <span data-ttu-id="4567b-357">functionapp:Linux で Java 関数アプリを作成する機能を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-357">functionapp: Add ability to create Java function apps in Linux</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-358">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-358">ARM</span></span>

* <span data-ttu-id="4567b-359">問題 #10246 を修正: 渡されたパラメーター `--ids` がリソース グループ ID の場合、`az resource tag` がクラッシュします</span><span class="sxs-lookup"><span data-stu-id="4567b-359">Fix issue #10246: `az resource tag` crashes when the parameter `--ids` passed in is resource group ID</span></span>
* <span data-ttu-id="4567b-360">問題 #11658 を修正: `az group export` コマンド が `--query` と `--output` パラメーターをサポートしません</span><span class="sxs-lookup"><span data-stu-id="4567b-360">Fix issue #11658: `az group export` command does not support `--query` and `--output` parameters</span></span>
* <span data-ttu-id="4567b-361">問題 #10279 を修正:検証が失敗した場合、`az group deployment validate` の終了コードは 0 になります</span><span class="sxs-lookup"><span data-stu-id="4567b-361">Fix issue #10279: The exit code of `az group deployment validate` is 0 when the verification fails</span></span>
* <span data-ttu-id="4567b-362">問題 #9916 を修正:`az resource list` コマンドのタグとその他のフィルター条件間の競合に関するエラー メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="4567b-362">Fix issue #9916: Improve the error message of the conflict between tag and other filter conditions for `az resource list` command</span></span>
* <span data-ttu-id="4567b-363">コマンド `az group create` の managedBy 情報の追加をサポートする新しいパラメーター `--managed-by` を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-363">Add new parameter `--managed-by` to support adding managedBy information for command `az group create`</span></span>

### <a name="azure-red-hat-openshift"></a><span data-ttu-id="4567b-364">Azure Red Hat OpenShift</span><span class="sxs-lookup"><span data-stu-id="4567b-364">Azure Red Hat OpenShift</span></span>

* <span data-ttu-id="4567b-365">Azure Red Hat OpensShift クラスターで Log Analytics 監視を管理するための `monitor` サブグループを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-365">Add `monitor` subgroup to manage Log Analytics monitoring in Azure Red Hat OpensShift cluster</span></span>

### <a name="botservice"></a><span data-ttu-id="4567b-366">BotService</span><span class="sxs-lookup"><span data-stu-id="4567b-366">BotService</span></span>

* <span data-ttu-id="4567b-367">問題 #11697 を修正: `az bot create` がべき等ではありません</span><span class="sxs-lookup"><span data-stu-id="4567b-367">Fix issue #11697: `az bot create` is not idempotent</span></span>
* <span data-ttu-id="4567b-368">名前修正テストをライブ モードでのみ実行するように変更します</span><span class="sxs-lookup"><span data-stu-id="4567b-368">Change name-correcting tests to run in Live-mode only</span></span>

### <a name="cdn"></a><span data-ttu-id="4567b-369">CDN</span><span class="sxs-lookup"><span data-stu-id="4567b-369">CDN</span></span>

* <span data-ttu-id="4567b-370">rulesEngine 機能のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-370">Add support for rulesEngine feature</span></span>
* <span data-ttu-id="4567b-371">規則を管理するための新しいコマンド グループ 'cdn endpoint rule' を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-371">Add new commands group 'cdn endpoint rule' to manage rules</span></span>
* <span data-ttu-id="4567b-372">API バージョン 2019-04-15 を使用するように azure-mgmt-cdn バージョンを 4.0.0 に更新します</span><span class="sxs-lookup"><span data-stu-id="4567b-372">Update azure-mgmt-cdn version to 4.0.0 to use api version 2019-04-15</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="4567b-373">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="4567b-373">Deployment Manager</span></span>

* <span data-ttu-id="4567b-374">すべてのリソースのリスト操作を追加します。</span><span class="sxs-lookup"><span data-stu-id="4567b-374">Add list operation for all resources.</span></span>
* <span data-ttu-id="4567b-375">新しい手順の種類に対する手順リソースを強化します。</span><span class="sxs-lookup"><span data-stu-id="4567b-375">Enhance step resource for new step type.</span></span>
* <span data-ttu-id="4567b-376">バージョン 0.2.0 を使用するように azure-mgmt-deploymentmanager パッケージを更新します。</span><span class="sxs-lookup"><span data-stu-id="4567b-376">Update azure-mgmt-deploymentmanager package to use version 0.2.0.</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-377">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-377">IoT</span></span>

* <span data-ttu-id="4567b-378">'IoT hub Job' コマンドを廃止します。</span><span class="sxs-lookup"><span data-stu-id="4567b-378">Deprecate 'IoT hub Job' commands.</span></span>

### <a name="iot-central"></a><span data-ttu-id="4567b-379">IoT Central</span><span class="sxs-lookup"><span data-stu-id="4567b-379">IoT Central</span></span>

* <span data-ttu-id="4567b-380">新しい SKU 名 ST0、ST1、ST2 でのアプリの作成/更新をサポートします。</span><span class="sxs-lookup"><span data-stu-id="4567b-380">Support app creation/update with the new sku name ST0, ST1, ST2.</span></span>

### <a name="key-vault"></a><span data-ttu-id="4567b-381">Key Vault</span><span class="sxs-lookup"><span data-stu-id="4567b-381">Key Vault</span></span>

* <span data-ttu-id="4567b-382">キーをダウンロードするための新しいコマンド `az keyvault key download` を追加します。</span><span class="sxs-lookup"><span data-stu-id="4567b-382">Add a new command `az keyvault key download` for downloading keys.</span></span>

### <a name="misc"></a><span data-ttu-id="4567b-383">その他</span><span class="sxs-lookup"><span data-stu-id="4567b-383">Misc</span></span>

* <span data-ttu-id="4567b-384">#6371 を修正:Bash でのファイル名と環境変数の補完をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-384">Fix #6371: Support filename and environment variable completion in Bash</span></span>

### <a name="network"></a><span data-ttu-id="4567b-385">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-385">Network</span></span>

* <span data-ttu-id="4567b-386">#2092 を修正: az network dns record-add/remove: レコード セットが見つからない場合に警告を追加します。</span><span class="sxs-lookup"><span data-stu-id="4567b-386">Fix #2092: az network dns record-set add/remove: add warning when record-set is not found.</span></span> <span data-ttu-id="4567b-387">今後、この自動作成を確認するための追加の引数がサポートされる予定です。</span><span class="sxs-lookup"><span data-stu-id="4567b-387">In the future, an extra argument will be supported to confirm this auto creation.</span></span>

### <a name="policy"></a><span data-ttu-id="4567b-388">ポリシー</span><span class="sxs-lookup"><span data-stu-id="4567b-388">Policy</span></span>

* <span data-ttu-id="4567b-389">豊富なポリシー メタデータ リソースを取得するための新しいコマンド `az policy metadata` を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-389">Add new command `az policy metadata` to retrieve rich policy metadata resources</span></span>
* <span data-ttu-id="4567b-390">`az policy remediation create`:`--resource-discovery-mode` パラメーターを使用して、修復前にコンプライアンスを再評価する必要があるかどうかを指定します</span><span class="sxs-lookup"><span data-stu-id="4567b-390">`az policy remediation create`: Specify whether compliance should be re-evaluated prior to remediation with the `--resource-discovery-mode` parameter</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-391">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-391">Profile</span></span>

* <span data-ttu-id="4567b-392">`az account get-access-token`:サブスクリプションを指定することなく、テナントのトークンを直接取得するための `--tenant` パラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-392">`az account get-access-token`: Add `--tenant` parameter to acquire token for the tenant directly, needless to specify a subscription</span></span>

### <a name="rbac"></a><span data-ttu-id="4567b-393">RBAC</span><span class="sxs-lookup"><span data-stu-id="4567b-393">RBAC</span></span>

* <span data-ttu-id="4567b-394">[重大な変更] #11883 を修正: `az role assignment create`: 空のスコープの場合にエラーが表示されます</span><span class="sxs-lookup"><span data-stu-id="4567b-394">[BREAKING CHANGE] Fix #11883: `az role assignment create`: empty scope will prompt error</span></span>

### <a name="security"></a><span data-ttu-id="4567b-395">Security</span><span class="sxs-lookup"><span data-stu-id="4567b-395">Security</span></span>

* <span data-ttu-id="4567b-396">ストレージ アカウントの高度な脅威保護設定を表示および管理するための新しいコマンド `az atp show` と `az atp update` を追加します。</span><span class="sxs-lookup"><span data-stu-id="4567b-396">Add new commands `az atp show` and `az atp update` to view and manage advanced threat protection settings for storage accounts.</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-397">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-397">SQL</span></span>

* <span data-ttu-id="4567b-398">`sql dw create`: `--zone-redundant` と `--read-replica-count` パラメーターを廃止します。</span><span class="sxs-lookup"><span data-stu-id="4567b-398">`sql dw create`: deprecate `--zone-redundant` and `--read-replica-count` parameters.</span></span> <span data-ttu-id="4567b-399">これらのパラメーターは、DataWarehouse には適用されません。</span><span class="sxs-lookup"><span data-stu-id="4567b-399">These parameters do not apply to DataWarehouse.</span></span>
* <span data-ttu-id="4567b-400">[破壊的変更] `az sql db create`:"az sql db create --sample-name" に対して使用可能な値としてドキュメントに記載されている "WideWorldImportersStd" と "WideWorldImportersFull" を削除します。</span><span class="sxs-lookup"><span data-stu-id="4567b-400">[BREAKING CHANGE] `az sql db create`: Remove "WideWorldImportersStd" and "WideWorldImportersFull" as documented allowed values for "az sql db create --sample-name".</span></span> <span data-ttu-id="4567b-401">これらのサンプル データベースを使用すると、常に作成が失敗します。</span><span class="sxs-lookup"><span data-stu-id="4567b-401">These sample databases would always cause creation to fail.</span></span>
* <span data-ttu-id="4567b-402">SQL データベースの機密性分類を管理するための新しいコマンド `sql db classification show/list/update/delete` と `sql db classification recommendation list/enable/disable` を追加します。</span><span class="sxs-lookup"><span data-stu-id="4567b-402">Add New commands `sql db classification show/list/update/delete` and `sql db classification recommendation list/enable/disable` to manage sensitivity classifications for SQL databases.</span></span>
* <span data-ttu-id="4567b-403">`az sql db audit-policy`:空の監査アクションとグループの修正</span><span class="sxs-lookup"><span data-stu-id="4567b-403">`az sql db audit-policy`: Fix for empty audit actions and groups</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-404">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-404">Storage</span></span>

* <span data-ttu-id="4567b-405">Azure ファイル共有の管理操作に Microsoft.Storage リソース プロバイダーを使用するための新しいコマンド グループ `az storage share-rm` を追加します。</span><span class="sxs-lookup"><span data-stu-id="4567b-405">Add a new command group `az storage share-rm` to use the Microsoft.Storage resource provider for Azure file share management operations.</span></span>
* <span data-ttu-id="4567b-406">問題 #11415 を修正: `az storage blob update` のアクセス許可エラー</span><span class="sxs-lookup"><span data-stu-id="4567b-406">Fix issue #11415: permission error for `az storage blob update`</span></span>
* <span data-ttu-id="4567b-407">Azcopy 10.3.3 を統合し、Win32 をサポートします。</span><span class="sxs-lookup"><span data-stu-id="4567b-407">Integrate Azcopy 10.3.3 and support Win32.</span></span>
* <span data-ttu-id="4567b-408">`az storage copy`:`--include-path`、`--include-pattern`、`--exclude-path`、および `--exclude-pattern` パラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-408">`az storage copy`: Add `--include-path`, `--include-pattern`, `--exclude-path` and`--exclude-pattern` parameters</span></span>
* <span data-ttu-id="4567b-409">`az storage remove`:`--inlcude` および `--exclude` パラメーターを `--include-path`、`--include-pattern`、`--exclude-path`、および `--exclude-pattern` パラメーターに変更します</span><span class="sxs-lookup"><span data-stu-id="4567b-409">`az storage remove`: Change `--inlcude` and `--exclude` parameters to `--include-path`, `--include-pattern`, `--exclude-path` and`--exclude-pattern` parameters</span></span>
* <span data-ttu-id="4567b-410">`az storage sync`:`--include-pattern`、`--exclude-path`、および `--exclude-pattern` パラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-410">`az storage sync`: Add `--include-pattern`, `--exclude-path` and`--exclude-pattern` parameters</span></span>

### <a name="servicefabric"></a><span data-ttu-id="4567b-411">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4567b-411">ServiceFabric</span></span>

* <span data-ttu-id="4567b-412">アプリケーションとサービスを管理するための新しいコマンドを追加します。</span><span class="sxs-lookup"><span data-stu-id="4567b-412">Add new commands to manage appliaction and services.</span></span>

## <a name="january-13-2020"></a><span data-ttu-id="4567b-413">2020 年 1 月 13 日</span><span class="sxs-lookup"><span data-stu-id="4567b-413">January 13, 2020</span></span>

<span data-ttu-id="4567b-414">バージョン 2.0.80</span><span class="sxs-lookup"><span data-stu-id="4567b-414">Version 2.0.80</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-415">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-415">Compute</span></span>

* <span data-ttu-id="4567b-416">disk update:--disk-encryption-set と --encryption-type を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-416">disk update: Add --disk-encryption-set and --encryption-type</span></span>
* <span data-ttu-id="4567b-417">snapshot create/update:--disk-encryption-set と --encryption-type を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-417">snapshot create/update: Add --disk-encryption-set and --encryption-type</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-418">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-418">Storage</span></span>

* <span data-ttu-id="4567b-419">azure-mgmt-storage のバージョンを 7.1.0 にアップグレードします</span><span class="sxs-lookup"><span data-stu-id="4567b-419">Upgrade azure-mgmt-storage version to 7.1.0</span></span>
* <span data-ttu-id="4567b-420">`az storage account create`:テーブルとキューの暗号化サービスをサポートするための `--encryption-key-type-for-table` と `--encryption-key-type-for-queue` を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-420">`az storage account create`: Add `--encryption-key-type-for-table` and `--encryption-key-type-for-queue` to support Table and Queue Encryption Service</span></span>

## <a name="january-07-2020"></a><span data-ttu-id="4567b-421">2020 年 1 月 7 日</span><span class="sxs-lookup"><span data-stu-id="4567b-421">January 07, 2020</span></span>

<span data-ttu-id="4567b-422">バージョン 2.0.79</span><span class="sxs-lookup"><span data-stu-id="4567b-422">Version 2.0.79</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-423">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-423">ACR</span></span>

* <span data-ttu-id="4567b-424">[重大な変更] 'acr build'、'acr task create/update'、'acr run'、および 'acr pack' の '--os' パラメーターを削除します。</span><span class="sxs-lookup"><span data-stu-id="4567b-424">[BREAKING CHANGE] Remove '--os' parameter for 'acr build', 'acr task create/update', 'acr run', and 'acr pack'.</span></span> <span data-ttu-id="4567b-425">代わりに、'--platform' を使用してください。</span><span class="sxs-lookup"><span data-stu-id="4567b-425">Use '--platform' instead.</span></span>

### <a name="appconfig"></a><span data-ttu-id="4567b-426">AppConfig</span><span class="sxs-lookup"><span data-stu-id="4567b-426">AppConfig</span></span>

* <span data-ttu-id="4567b-427">機能フラグのインポート/エクスポートのサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-427">Add support for importing/exporting feature flags</span></span>
* <span data-ttu-id="4567b-428">keyvault 参照を作成するための新しいコマンド 'az appconfig kv set-keyvault' を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-428">Add new command 'az appconfig kv set-keyvault' for creating keyvault reference</span></span>
* <span data-ttu-id="4567b-429">機能フラグをファイルにエクスポートするときに、さまざまな名前付け規則をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-429">Support various naming conventions when exporting feature flags to file</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-430">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-430">AppService</span></span>

* <span data-ttu-id="4567b-431">問題 #7154 を修正:単一引用符ではなく、アクサン グラーブを使用するように、コマンド < > のドキュメントを更新しています</span><span class="sxs-lookup"><span data-stu-id="4567b-431">Fix issue #7154: Updating documentation for command <> to use back ticks instead of single quotes</span></span>
* <span data-ttu-id="4567b-432">問題 #11287 を修正: webapp up:既定で、up を使用して作成されたアプリを 'SSL 有効' にする必要がある</span><span class="sxs-lookup"><span data-stu-id="4567b-432">Fix issue #11287: webapp up: By default make the app created using up 'should be 'SSL enabled'</span></span>
* <span data-ttu-id="4567b-433">問題 #11592 を修正:HTML 静的サイトに az webapp up フラグを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-433">Fix issue #11592: Add az webapp up flag for html static sites</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-434">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-434">ARM</span></span>

* <span data-ttu-id="4567b-435">`az resource tag` を修正:Recovery Services コンテナー タグを更新できない</span><span class="sxs-lookup"><span data-stu-id="4567b-435">Fix `az resource tag`: Recovery Services Vault tags cannot be updated</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-436">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-436">Backup</span></span>

* <span data-ttu-id="4567b-437">IaasVM ワークロードの論理的な削除機能を有効にするための新しいコマンド 'backup protection undelete' を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-437">Added new command 'backup protection undelete' to enable soft-delete feature for IaasVM workload</span></span>
* <span data-ttu-id="4567b-438">backup-properties コマンドを設定するための新しいパラメーター '--soft-delete-feature-state' を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-438">Added new parameter '--soft-delete-feature-state' to set backup-properties command</span></span>
* <span data-ttu-id="4567b-439">IaasVM ワークロードのディスク除外のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-439">Added disk exclusion support for IaasVM workload</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-440">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-440">Compute</span></span>

* <span data-ttu-id="4567b-441">Azure Stack プロファイルの `vm create` エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="4567b-441">Fix `vm create` failure in Azure Stack profile.</span></span>
* <span data-ttu-id="4567b-442">vm monitor metrics tail/list-definitions: VM のクエリ メトリックとリスト定義をサポートします。</span><span class="sxs-lookup"><span data-stu-id="4567b-442">vm monitor metrics tail/list-definitions: support query metric and list definitions for a vm.</span></span>
* <span data-ttu-id="4567b-443">az vm の新しい再適用コマンド アクションを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-443">Add new reapply command action for az vm</span></span>

### <a name="hdinsight"></a><span data-ttu-id="4567b-444">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4567b-444">HDInsight</span></span>

* <span data-ttu-id="4567b-445">Kafka REST プロキシを使用する Kafka クラスターの作成のサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-445">Support for creating a Kafka cluster with Kafka Rest Proxy</span></span>
* <span data-ttu-id="4567b-446">azure-mgmt-hdinsight を 1.3.0 にアップグレード</span><span class="sxs-lookup"><span data-stu-id="4567b-446">Upgrade azure-mgmt-hdinsight to 1.3.0</span></span>

### <a name="misc"></a><span data-ttu-id="4567b-447">その他</span><span class="sxs-lookup"><span data-stu-id="4567b-447">Misc.</span></span>

* <span data-ttu-id="4567b-448">既定の JSON 形式 または --output によって構成された形式で Azure CLI モジュールと拡張機能のバージョンを表示するプレビュー コマンド `az version show` を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-448">Add preview command `az version show` to show the versions of Azure CLI modules and extensions in JSON format by default or format configured by --output</span></span>

### <a name="event-hubs"></a><span data-ttu-id="4567b-449">Event Hubs</span><span class="sxs-lookup"><span data-stu-id="4567b-449">Event Hubs</span></span>

* <span data-ttu-id="4567b-450">[重大な変更] コマンド 'az eventhubs eventhub update' と 'az eventhubs eventhub create' から 'ReceiveDisabled' status オプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="4567b-450">[BREAKING CHANGE] Remove 'ReceiveDisabled' status option from command 'az eventhubs eventhub update' and 'az eventhubs eventhub create'.</span></span> <span data-ttu-id="4567b-451">このオプションは、イベント ハブ エンティティに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="4567b-451">This option is not valid for Event Hub entities.</span></span>

### <a name="service-bus"></a><span data-ttu-id="4567b-452">Service Bus</span><span class="sxs-lookup"><span data-stu-id="4567b-452">Service Bus</span></span>

* <span data-ttu-id="4567b-453">[重大な変更] コマンド 'az servicebus topic create'、'az servicebus topic update'、'az servicebus queue create'、および 'az servicebus queue update' から 'ReceiveDisabled' status オプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="4567b-453">[BREAKING CHANGE] Remove 'ReceiveDisabled' status option from command 'az servicebus topic create', 'az servicebus topic update', 'az servicebus queue create', and 'az servicebus queue update'.</span></span> <span data-ttu-id="4567b-454">このオプションは、Service Bus のトピックとキューに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="4567b-454">This option is not valid for Service Bus topics and queues.</span></span>

### <a name="rbac"></a><span data-ttu-id="4567b-455">RBAC</span><span class="sxs-lookup"><span data-stu-id="4567b-455">RBAC</span></span>

* <span data-ttu-id="4567b-456">#11712 を修正: アプリケーションまたはサービス プリンシパルが存在しない場合に `az ad app/sp show` で終了コード 3 が返されない</span><span class="sxs-lookup"><span data-stu-id="4567b-456">Fix #11712: `az ad app/sp show` does not return exit code 3 when the application or service principal does not exist</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-457">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-457">Storage</span></span>

* <span data-ttu-id="4567b-458">`az storage account create`:--enable-hierarchical-namespace パラメーターのプレビュー フラグを削除します</span><span class="sxs-lookup"><span data-stu-id="4567b-458">`az storage account create`: Remove preview flag for --enable-hierarchical-namespace parameter</span></span>
* <span data-ttu-id="4567b-459">API バージョン 2019-06-01 を使用するために azure-mgmt-storage バージョンを 7.0.0 に更新します</span><span class="sxs-lookup"><span data-stu-id="4567b-459">Update azure-mgmt-storage version to 7.0.0 to use api version 2019-06-01</span></span>
* <span data-ttu-id="4567b-460">ストレージ アカウント blob-service-properties の削除の保持ポリシーの管理をサポートするために、新しいパラメーター `--enable-delete-retention` と `--delete-retention-days` を追加します。</span><span class="sxs-lookup"><span data-stu-id="4567b-460">Add new parameters `--enable-delete-retention` and `--delete-retention-days` to support managing delete retention policy for storage account blob-service-properties.</span></span>

## <a name="december-17-2019"></a><span data-ttu-id="4567b-461">2019 年 12 月 17 日</span><span class="sxs-lookup"><span data-stu-id="4567b-461">December 17, 2019</span></span>

<span data-ttu-id="4567b-462">2.0.78</span><span class="sxs-lookup"><span data-stu-id="4567b-462">2.0.78</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-463">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-463">ACR</span></span>

* <span data-ttu-id="4567b-464">acr task run でのローカル コンテキストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-464">Added support Local context in acr task run</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-465">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-465">ACS</span></span>

* <span data-ttu-id="4567b-466">[重大な変更] az openshift create: `--workspace-resource-id` の名前を `--workspace-id` に変更します。</span><span class="sxs-lookup"><span data-stu-id="4567b-466">[BREAKING CHANGE]az openshift create: rename `--workspace-resource-id` to `--workspace-id`.</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-467">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-467">AMS</span></span>

* <span data-ttu-id="4567b-468">リソースが見つからない場合に 3 を返すように表示コマンドを更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-468">Updated show commands to return 3 when resource not found</span></span>

### <a name="appconfig"></a><span data-ttu-id="4567b-469">AppConfig</span><span class="sxs-lookup"><span data-stu-id="4567b-469">AppConfig</span></span>

* <span data-ttu-id="4567b-470">要求 URL に api-version を追加するときのバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-470">Fixed bug when appending api-version to request url.</span></span> <span data-ttu-id="4567b-471">既存のソリューションは、改ページ位置の自動修正で機能しません。</span><span class="sxs-lookup"><span data-stu-id="4567b-471">The existing solution doesn't work with pagination.</span></span>
* <span data-ttu-id="4567b-472">英語以外の言語を表示するためのサポートを追加しました。これは、Microsoft のバックエンド サービスがグローバリゼーション向けに unicode をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="4567b-472">Added support for showing languages besides English as our backend service support unicode for globalization.</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-473">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-473">AppService</span></span>

* <span data-ttu-id="4567b-474">問題 #11217 を修正: webapp: az webapp config ssl upload はスロット パラメーターをサポートする必要がある</span><span class="sxs-lookup"><span data-stu-id="4567b-474">Fixed issue #11217: webapp: az webapp config ssl upload should support slot parameter</span></span>
* <span data-ttu-id="4567b-475">問題 #10965 を修正:エラー:名前を空にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4567b-475">Fixed issue #10965: Error: Name cannot be empty.</span></span> <span data-ttu-id="4567b-476">ip_address とサブネットによる削除を許可します</span><span class="sxs-lookup"><span data-stu-id="4567b-476">Allow remove by ip_address and subnet</span></span>
* <span data-ttu-id="4567b-477">Key Vault `az webapp config ssl import` からの証明書のインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-477">Added support for importing certificates from Key Vault `az webapp config ssl import`</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-478">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-478">ARM</span></span>

* <span data-ttu-id="4567b-479">6\.0.0 を使用するように azure-mgmt-resource パッケージを更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-479">Updated azure-mgmt-resource package to use 6.0.0</span></span>
* <span data-ttu-id="4567b-480">新しいパラメーター `--aux-subs` の追加による `az group deployment create` コマンドのクロス テナントのサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-480">Cross Tenant Support for `az group deployment create` command by adding new parameter `--aux-subs`</span></span>
* <span data-ttu-id="4567b-481">ポリシー セット定義へのメタデータ情報の追加をサポートするために、新しいパラメーター `--metadata` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-481">Added new parameter `--metadata` to support adding metadata information for policy set definitions.</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-482">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-482">Backup</span></span>

* <span data-ttu-id="4567b-483">SQL および SAP Hana ワークロードのバックアップ サポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-483">Added Backup support for SQL and SAP Hana workload.</span></span>

### <a name="botservice"></a><span data-ttu-id="4567b-484">BotService</span><span class="sxs-lookup"><span data-stu-id="4567b-484">BotService</span></span>

* <span data-ttu-id="4567b-485">[重大な変更] プレビューコマンド 'az bot create' から '--version' フラグを削除します。</span><span class="sxs-lookup"><span data-stu-id="4567b-485">[Breaking change] Remove '--version' flag from preview command 'az bot create'.</span></span> <span data-ttu-id="4567b-486">v4 SDK ボットのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4567b-486">Only v4 SDK bots are supported.</span></span>
* <span data-ttu-id="4567b-487">名前を使用できるかどうかのチェックを 'sz bot create' に追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-487">Added name availability check for 'az bot create'.</span></span>
* <span data-ttu-id="4567b-488">'az bot update' を使用してボットのアイコン URL を更新するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-488">Added support for updating the icon URL for a bot via 'az bot update'.</span></span>
* <span data-ttu-id="4567b-489">'az bot directline update' を使用して Direct Line チャネルを更新するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-489">Added support for updating a Direct Line channel via 'az bot directline update'.</span></span>
* <span data-ttu-id="4567b-490">'az bot directline create' に '--enable-enhanced-auth' フラグのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-490">Added '--enable-enhanced-auth' flag support to 'az bot directline create'.</span></span>
* <span data-ttu-id="4567b-491">コマンド グループ 'az bot authsetting' は、プレビュー段階ではなく、GA です。</span><span class="sxs-lookup"><span data-stu-id="4567b-491">The following command groups are GA and not in preview: 'az bot authsetting'.</span></span>
* <span data-ttu-id="4567b-492">'az bot' の次のコマンドは、プレビュー段階ではなく、GA です: 'create'、'prepare-deploy'、'show'、'delete'、'update'。</span><span class="sxs-lookup"><span data-stu-id="4567b-492">The following commands in 'az bot' are GA and not in preview: 'create', 'prepare-deploy', 'show', 'delete', 'update'.</span></span>
* <span data-ttu-id="4567b-493">'az bot prepare-deploy' が修正され、 '--proj-file-path' 値が小文字に変更されます (例:"Test.csproj" が "test.csproj" に)。</span><span class="sxs-lookup"><span data-stu-id="4567b-493">Fixed 'az bot prepare-deploy' changing '--proj-file-path' value to lower case (e.g. "Test.csproj" to "test.csproj").</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-494">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-494">Compute</span></span>

* <span data-ttu-id="4567b-495">vmss create/update:--scale-in-policy を追加しました。これは、VMSS がスケールインされるときに削除対象として選択される仮想マシンを決定します。</span><span class="sxs-lookup"><span data-stu-id="4567b-495">vmss create/update: Added --scale-in-policy, which decides which virtual machines are chosen for removal when a VMSS is scaled-in.</span></span>
* <span data-ttu-id="4567b-496">vm/vmss update:--priority を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-496">vm/vmss update: Added --priority.</span></span>
* <span data-ttu-id="4567b-497">vm/vmss update:--max-price を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-497">vm/vmss update: Added --max-price.</span></span>
* <span data-ttu-id="4567b-498">disk-encryption-set コマンド グループ (create、show、update、delete、list) を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-498">Added disk-encryption-set command group (create, show, update, delete, list).</span></span>
* <span data-ttu-id="4567b-499">disk create:--encryption-type と --disk-encryption-set を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-499">disk create: Added --encryption-type and --disk-encryption-set.</span></span>
* <span data-ttu-id="4567b-500">vm/vmss create: --os-disk-encryption-set と --data-disk-encryption-sets を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-500">vm/vmss create: Added --os-disk-encryption-set and --data-disk-encryption-sets.</span></span>

### <a name="core"></a><span data-ttu-id="4567b-501">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-501">Core</span></span>

* <span data-ttu-id="4567b-502">Python 3.4 のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-502">Removed support for Python 3.4</span></span>
* <span data-ttu-id="4567b-503">複数のコマンドでの HaTS 調査のプラグイン</span><span class="sxs-lookup"><span data-stu-id="4567b-503">Plug in HaTS survey in multiple commands</span></span>

### <a name="dls"></a><span data-ttu-id="4567b-504">DLS</span><span class="sxs-lookup"><span data-stu-id="4567b-504">DLS</span></span>

* <span data-ttu-id="4567b-505">ADLS SDK バージョンを更新しました (0.0.48)。</span><span class="sxs-lookup"><span data-stu-id="4567b-505">Updated ADLS sdk version (0.0.48).</span></span>

### <a name="install"></a><span data-ttu-id="4567b-506">インストール</span><span class="sxs-lookup"><span data-stu-id="4567b-506">Install</span></span>

* <span data-ttu-id="4567b-507">インストール スクリプトで python 3.8 がサポートされます</span><span class="sxs-lookup"><span data-stu-id="4567b-507">Install script support python 3.8</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-508">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-508">IOT</span></span>

* <span data-ttu-id="4567b-509">[重大な変更] manual-failover から --failover-region パラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-509">[BREAKING CHANGE] Removed --failover-region parameter from manual-failover.</span></span> <span data-ttu-id="4567b-510">これで、割り当てられた geo ペアのセカンダリ リージョンにフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="4567b-510">Now it will failover to assigned geo-paired secondary region.</span></span>

### <a name="key-vault"></a><span data-ttu-id="4567b-511">Key Vault</span><span class="sxs-lookup"><span data-stu-id="4567b-511">Key Vault</span></span>

* <span data-ttu-id="4567b-512">#8095 を修正: `az keyvault storage remove`: ヘルプ メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="4567b-512">Fixed #8095: `az keyvault storage remove`: improve the help message</span></span>
* <span data-ttu-id="4567b-513">#8921 を修正: `az keyvault key/secret/certificate list/list-deleted/list-versions`: パラメーター `--maxresults` の検証のバグを修正します</span><span class="sxs-lookup"><span data-stu-id="4567b-513">Fixed #8921: `az keyvault key/secret/certificate list/list-deleted/list-versions`: fix the validation bug on parameter `--maxresults`</span></span>
* <span data-ttu-id="4567b-514">#10512 を修正: `az keyvault set-policy`: `--object-id`、`--spn`、`--upn` のいずれも指定されていない場合のエラー メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="4567b-514">Fixed #10512: `az keyvault set-policy`: improve the error message when none of `--object-id`, `--spn` or `--upn` is specified</span></span>
* <span data-ttu-id="4567b-515">#10846 を修正: `az keyvault secret show-deleted`: `--id` を指定した場合、`--name/-n` は必要ありません</span><span class="sxs-lookup"><span data-stu-id="4567b-515">Fixed #10846: `az keyvault secret show-deleted`: when `--id` is specified, `--name/-n` is not required</span></span>
* <span data-ttu-id="4567b-516">#11084 を修正: `az keyvault secret download`: パラメーター `--encoding` のヘルプ メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="4567b-516">Fixed #11084: `az keyvault secret download`: improve the help message of parameter `--encoding`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-517">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-517">Network</span></span>

* <span data-ttu-id="4567b-518">az network application-gateway probe:作成および更新時にバックエンド サーバーをプローブするためのポートを指定する --port オプションのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-518">az network application-gateway probe: Added support --port option to specify a port for probing backend servers when create and update</span></span>
* <span data-ttu-id="4567b-519">az network application-gateway url-path-map create/update: `--waf-policy` のバグ修正</span><span class="sxs-lookup"><span data-stu-id="4567b-519">az network application-gateway url-path-map create/update: bug fix for `--waf-policy`</span></span>
* <span data-ttu-id="4567b-520">az network application-gateway:`--rewrite-rule-set` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-520">az network application-gateway: Added support `--rewrite-rule-set`</span></span>
* <span data-ttu-id="4567b-521">az network list-service-aliases:サービス エンドポイント ポリシーに使用できるサービス別名を一覧表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-521">az network list-service-aliases: Added support list service aliases which can be used for Service Endpoint Policies</span></span>
* <span data-ttu-id="4567b-522">az network dns zone import:レコード名での .@ のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-522">az network dns zone import: Added support .@ in record name</span></span>

### <a name="packaging"></a><span data-ttu-id="4567b-523">梱包</span><span class="sxs-lookup"><span data-stu-id="4567b-523">Packaging</span></span>

* <span data-ttu-id="4567b-524">pip インストール用のバック エッジ ビルドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-524">Added back edge builds for pip install</span></span>
* <span data-ttu-id="4567b-525">Ubuntu eoan パッケージを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-525">Added Ubuntu eoan package</span></span>

### <a name="policy"></a><span data-ttu-id="4567b-526">ポリシー</span><span class="sxs-lookup"><span data-stu-id="4567b-526">Policy</span></span>

* <span data-ttu-id="4567b-527">ポリシー API バージョン 2019-09-01 のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-527">Added support for Policy API version 2019-09-01.</span></span>
* <span data-ttu-id="4567b-528">az policy set-definition:`--definition-groups` パラメーターを使用したポリシー セット定義内のグループ化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-528">az policy set-definition: Added support grouping within policy set definitions with `--definition-groups` parameter</span></span>

### <a name="redis"></a><span data-ttu-id="4567b-529">Redis</span><span class="sxs-lookup"><span data-stu-id="4567b-529">Redis</span></span>

* <span data-ttu-id="4567b-530">`az redis create` コマンドにプレビュー パラメーター `--replicas-per-master` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-530">Added preview param `--replicas-per-master` to `az redis create` command</span></span>
* <span data-ttu-id="4567b-531">azure-mgmt-redis を 6.0.0 から 7.0.0rc1 に更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-531">Updated azure-mgmt-redis from 6.0.0 to 7.0.0rc1</span></span>

### <a name="servicefabric"></a><span data-ttu-id="4567b-532">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4567b-532">ServiceFabric</span></span>

* <span data-ttu-id="4567b-533">#10963 を含む node-type 追加ロジックを修正:持続性レベル Gold で新しいノード タイプを追加すると、常に CLI エラーがスローされる</span><span class="sxs-lookup"><span data-stu-id="4567b-533">Fixed in node-type add logic including #10963: Adding new node type with durability level Gold will always throw CLI error</span></span>
* <span data-ttu-id="4567b-534">作成テンプレートの ServiceFabricNodeVmExt バージョンを 1.1 に更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-534">Updated ServiceFabricNodeVmExt version to 1.1 in creation template</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-535">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-535">SQL</span></span>

* <span data-ttu-id="4567b-536">読み取りスケール管理をサポートするために、sql db create および update コマンドに "--read-scale" と "--read-replicas" パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-536">Added "--read-scale" and "--read-replicas" parameters to sql db create and update commands, to support read scale management.</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-537">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-537">Storage</span></span>

* <span data-ttu-id="4567b-538">GA リリースでの storage account create および update コマンド用の大きいファイルの共有プロパティ</span><span class="sxs-lookup"><span data-stu-id="4567b-538">GA Release Large File Shares property for storage account create and update command</span></span>
* <span data-ttu-id="4567b-539">GA リリースでのユーザー委任 SAS トークンのサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-539">GA Release User Delegation SAS token Support</span></span>
* <span data-ttu-id="4567b-540">ストレージ アカウントの Blob service のプロパティを管理するための新しいコマンド `az storage account blob-service-properties show` と `az storage account blob-service-properties update --enable-change-feed` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="4567b-540">Added new commands `az storage account blob-service-properties show` and `az storage account blob-service-properties update --enable-change-feed` to manage blob service properties for storage account.</span></span>
* <span data-ttu-id="4567b-541">[今後の破壊的変更] `az storage copy`: `*` 文字は URL 内のワイルドカードとしてサポートされなくなりましたが、新しいパラメーターの --include-pattern と --exclude-pattern が `*` ワイルドカードをサポートして追加されます。</span><span class="sxs-lookup"><span data-stu-id="4567b-541">[COMING BREAKING CHANGE] `az storage copy`: `*` character is no longer supported as a wildcard in URL, but new parameters --include-pattern and --exclude-pattern will be added with `*` wildcard support.</span></span>
* <span data-ttu-id="4567b-542">問題 #11043 を修正:`az storage remove` コマンドでコンテナー/共有全体を削除するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-542">Fixed issue #11043: Added support to remove whole container/share in `az storage remove` command</span></span>

## <a name="november-26-2019"></a><span data-ttu-id="4567b-543">2019 年 11 月 26 日</span><span class="sxs-lookup"><span data-stu-id="4567b-543">November 26, 2019</span></span>

<span data-ttu-id="4567b-544">バージョン 2.0.77</span><span class="sxs-lookup"><span data-stu-id="4567b-544">Version 2.0.77</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-545">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-545">ACR</span></span>

* <span data-ttu-id="4567b-546">acr task create/update からパラメーター `--branch` が非推奨になりました</span><span class="sxs-lookup"><span data-stu-id="4567b-546">Deprecated parameter `--branch` from acr task create/update</span></span>

### <a name="azure-red-hat-openshift"></a><span data-ttu-id="4567b-547">Azure Red Hat OpenShift</span><span class="sxs-lookup"><span data-stu-id="4567b-547">Azure Red Hat OpenShift</span></span>

* <span data-ttu-id="4567b-548">監視を使用して Azure Red Hat Openshift クラスターを作成できるように、`--workspace-resource-id` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-548">Added `--workspace-resource-id` flag to allow creation of Azure Red Hat Openshift cluster with monitoring</span></span>
* <span data-ttu-id="4567b-549">監視を使用して Azure Red Hat OpenShift クラスターを作成するために `monitor_profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-549">Added `monitor_profile` to create Azure Red Hat OpenShift cluster with monitoring</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-550">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-550">AKS</span></span>

* <span data-ttu-id="4567b-551">"az aks rotate-certs" を使用したクラスター証明書ローテーション操作のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-551">Added support cluster certificate rotation operation using "az aks rotate-certs".</span></span>

### <a name="appconfig"></a><span data-ttu-id="4567b-552">AppConfig</span><span class="sxs-lookup"><span data-stu-id="4567b-552">AppConfig</span></span>

* <span data-ttu-id="4567b-553">`as az appconfig kv import` の区切り文字に ":" を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-553">Added support for using ":" for `as az appconfig kv import` separator</span></span>
* <span data-ttu-id="4567b-554">null ラベルを含む複数のラベルを持つキー値の一覧表示に関する問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-554">Fixed issue for listing key values with multiple labels including null label.</span></span> 
* <span data-ttu-id="4567b-555">管理プレーン SKD である azure-mgmt-appconfiguration を バージョン 0.3.0 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-555">Updated management plane sdk, azure-mgmt-appconfiguration, to version 0.3.0.</span></span> 

### <a name="appservice"></a><span data-ttu-id="4567b-556">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-556">AppService</span></span>

* <span data-ttu-id="4567b-557">問題 #11100 を修正:サービス プランの作成時の az webapp up の AttributeError</span><span class="sxs-lookup"><span data-stu-id="4567b-557">Fixed issue #11100: AttributeError for az webapp up when create service plan</span></span>
* <span data-ttu-id="4567b-558">az webapp up:サポートされている言語のサイトに作成またはデプロイを強制します。既定値は使用されません。</span><span class="sxs-lookup"><span data-stu-id="4567b-558">az webapp up: Forcing the creation or deployment to a site for supported languages, no defaults used.</span></span>
* <span data-ttu-id="4567b-559">App Service Environment のサポートを追加しました: az appservice ase show | list | list-addresses | list-plans | create | update | delete</span><span class="sxs-lookup"><span data-stu-id="4567b-559">Added support for App Service Environment: az appservice ase show | list | list-addresses | list-plans | create | update | delete</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-560">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-560">Backup</span></span>

* <span data-ttu-id="4567b-561">az backup policy list-associated-items の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-561">Fixed issue in az backup policy list-associated-items.</span></span> <span data-ttu-id="4567b-562">省略可能な BackupManagementType パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-562">Added optional BackupManagementType parameter.</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-563">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-563">Compute</span></span>

* <span data-ttu-id="4567b-564">コンピューティング、ディスク、スナップショットの API バージョンを 2019-07-01 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="4567b-564">Upgraded API version of compute, disks, snapshots to 2019-07-01</span></span>
* <span data-ttu-id="4567b-565">vmss create: --orchestration-mode の改善</span><span class="sxs-lookup"><span data-stu-id="4567b-565">vmss create: Improvement for --orchestration-mode</span></span>
* <span data-ttu-id="4567b-566">sig image-definition create: --os-state を追加して、このイメージの下に作成された仮想マシンを "一般化" するか、または "特殊化" するかを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-566">sig image-definition create: Added --os-state to allow specifying whether the virtual machines created under this image are 'Generalized' or 'Specialized'</span></span>
* <span data-ttu-id="4567b-567">sig image-definition create: --hyper-v-generation を追加して、ハイパーバイザーの生成を指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-567">sig image-definition create: Added --hyper-v-generation to allow specifying the hypervisor generation</span></span>
* <span data-ttu-id="4567b-568">sig image-version create: --os-snapshot と --data-snapshots のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-568">sig image-version create: Added support --os-snapshot and --data-snapshots</span></span>
* <span data-ttu-id="4567b-569">image create: --data-disk-caching を追加して、データ ディスクのキャッシュ設定を指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-569">image create: Added --data-disk-caching to allow specifying caching setting of data disks</span></span>
* <span data-ttu-id="4567b-570">Python Compute SDK を 10.0.0 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="4567b-570">Upgraded Python Compute SDK to 10.0.0</span></span>
* <span data-ttu-id="4567b-571">vm/vmss create: 'Priority' 列挙型プロパティに 'Spot' を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-571">vm/vmss create: Added 'Spot' to 'Priority' enum property</span></span>
* <span data-ttu-id="4567b-572">[重大な変更] Swagger と Powershell のコマンドレットとの一貫性を維持するために、VM と VMSS の両方で '--max-billing' パラメーターを '--max-price' に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-572">[Breaking change] Renamed '--max-billing' parameter to '--max-price', for both VM and VMSS, to be consistent with Swagger and Powershell cmdlets</span></span>
* <span data-ttu-id="4567b-573">vm monitor log show: リンクされた Log Analytics ワークスペースに対してログのクエリを実行するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-573">vm monitor log show: Added support for querying log over linked log analytics workspace.</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-574">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-574">IOT</span></span>

* <span data-ttu-id="4567b-575">#2531 の修正: ハブの更新に便利な引数を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-575">Fix #2531: Added convenience arguments for hub update.</span></span>
* <span data-ttu-id="4567b-576">#8323 の修正: ストレージ カスタム エンドポイントを作成するために不足しているパラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-576">Fix #8323: Added missing parameters to create storage custom endpoint.</span></span>
* <span data-ttu-id="4567b-577">回帰バグの修正: 既定のストレージ エンドポイントをオーバーライドする変更を元に戻しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-577">Fix regression bug: Reverted the changes which overrides the default storage endpoint.</span></span>

### <a name="key-vault"></a><span data-ttu-id="4567b-578">Key Vault</span><span class="sxs-lookup"><span data-stu-id="4567b-578">Key Vault</span></span>

* <span data-ttu-id="4567b-579">#11121 を修正しました: `az keyvault certificate list` を使用する場合、`--include-pending` を渡すときに `true` または `false` の値が必須ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="4567b-579">Fixed #11121: When using `az keyvault certificate list`, passing `--include-pending` now doesn't require a value of `true` or `false`</span></span>

### <a name="netappfiles"></a><span data-ttu-id="4567b-580">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="4567b-580">NetAppFiles</span></span>

* <span data-ttu-id="4567b-581">azure-mgmt-netapp を 0.7.0 にアップグレードしました。これには、今後のレプリケーション操作に関連した追加のボリューム プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4567b-581">Upgraded azure-mgmt-netapp to 0.7.0 which includes some additional volume properties associated with upcoming replication operations</span></span>

### <a name="network"></a><span data-ttu-id="4567b-582">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-582">Network</span></span>

* <span data-ttu-id="4567b-583">application-gateway waf-config: 非推奨になりました</span><span class="sxs-lookup"><span data-stu-id="4567b-583">application-gateway waf-config: deprecated</span></span>
* <span data-ttu-id="4567b-584">application-gateway waf-policy: 管理されているルール セットと除外ルールを管理するために、サブグループ managed-rules を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-584">application-gateway waf-policy: Added subgroup managed-rules to manage managed rule sets and exclusion rules</span></span>
* <span data-ttu-id="4567b-585">application-gateway waf-policy: waf-policy のグローバル構成を管理するために、サブグループ policy-setting を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-585">application-gateway waf-policy: Added subgroup policy-setting to manage global configuration of a waf-policy</span></span>
* <span data-ttu-id="4567b-586">[重大な変更] application-gateway waf-policy: subgroup rule を custom-rule に名前変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-586">[BREAKING CHANGE] application-gateway waf-policy: Renamed subgroup rule to custom-rule</span></span>
* <span data-ttu-id="4567b-587">application-gateway http-listener: 作成時の --firewall-policy を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-587">application-gateway http-listener: Added --firewall-policy when create</span></span>
* <span data-ttu-id="4567b-588">application-gateway url-path-map rule: 作成時の --firewall-policy を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-588">application-gateway url-path-map rule: Added --firewall-policy when create</span></span>

### <a name="packaging"></a><span data-ttu-id="4567b-589">梱包</span><span class="sxs-lookup"><span data-stu-id="4567b-589">Packaging</span></span>

* <span data-ttu-id="4567b-590">az ラッパーを Python で書き直しました</span><span class="sxs-lookup"><span data-stu-id="4567b-590">Rewrote the az wrapper in Python</span></span>
* <span data-ttu-id="4567b-591">Python 3.8 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-591">Added support for Python 3.8</span></span>
* <span data-ttu-id="4567b-592">RPM パッケージで Python 3 に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-592">Changed to Python 3 for RPM package</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-593">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-593">Profile</span></span>

* <span data-ttu-id="4567b-594">Microsoft アカウントで `az login -u {} -p {}` を実行するときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-594">Polished error when running `az login -u {} -p {}` with Microsoft account</span></span>
* <span data-ttu-id="4567b-595">自己署名ルート証明書使用してプロキシの背後で `az login` を実行するときの `SSLError` を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-595">Polished `SSLError` when running `az login` behind a proxy with self-signed root certificate</span></span>
* <span data-ttu-id="4567b-596">#10578 を修正: Windows または WSL で同時に複数のインスタンスを起動すると `az login` がハングする</span><span class="sxs-lookup"><span data-stu-id="4567b-596">Fixed #10578: `az login` hangs when more than one instances are launched at the same time on Windows or WSL</span></span>
* <span data-ttu-id="4567b-597">#11059 を修正: テナントにサブスクリプションがあると `az login --allow-no-subscriptions` が失敗する</span><span class="sxs-lookup"><span data-stu-id="4567b-597">Fixed #11059: `az login --allow-no-subscriptions` fails if there are subscriptions in the tenant</span></span>
* <span data-ttu-id="4567b-598">#11238 を修正: サブスクリプションの名前を変更した後、MSI を使用してログインすると、同じサブスクリプションが 2 回表示される</span><span class="sxs-lookup"><span data-stu-id="4567b-598">Fixed #11238: After renaming a subscription, logging in with MSI will result in the same subscription appearing twice</span></span>

### <a name="rbac"></a><span data-ttu-id="4567b-599">RBAC</span><span class="sxs-lookup"><span data-stu-id="4567b-599">RBAC</span></span>

* <span data-ttu-id="4567b-600">#10996 を修正: `--password` が指定されていないときの `az ad user update` での `--force-change-password-next-login` のエラーを改善</span><span class="sxs-lookup"><span data-stu-id="4567b-600">Fixed #10996: Polish error for `--force-change-password-next-login` in `az ad user update` when `--password` is not specified</span></span>

### <a name="redis"></a><span data-ttu-id="4567b-601">Redis</span><span class="sxs-lookup"><span data-stu-id="4567b-601">Redis</span></span>

* <span data-ttu-id="4567b-602">#2902 を修正: Basic SKU キャッシュの更新中、メモリ構成を設定しない</span><span class="sxs-lookup"><span data-stu-id="4567b-602">Fixed #2902: Avoid setting memory configs while updating Basic SKU cache</span></span>

### <a name="reservations"></a><span data-ttu-id="4567b-603">Reservations</span><span class="sxs-lookup"><span data-stu-id="4567b-603">Reservations</span></span>

* <span data-ttu-id="4567b-604">SDK バージョンを 0.6.0 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="4567b-604">Upgraded SDK Version to 0.6.0</span></span>
* <span data-ttu-id="4567b-605">Gat-Gatalogs を呼び出した後の billingplan の詳細情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-605">Added billingplan details info after calling Get-Gatalogs</span></span>
* <span data-ttu-id="4567b-606">予約の価格を計算するための新しいコマンド `az reservations reservation-order calculate` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-606">Added new command `az reservations reservation-order calculate` to calculate the price for a reservation</span></span>
* <span data-ttu-id="4567b-607">新しい予約を購入するための新しいコマンド `az reservations reservation-order purchase` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-607">Added new command `az reservations reservation-order purchase` to purchase a new reservation</span></span>

### <a name="rest"></a><span data-ttu-id="4567b-608">REST</span><span class="sxs-lookup"><span data-stu-id="4567b-608">Rest</span></span>
* <span data-ttu-id="4567b-609">`az rest` を GA に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-609">Changed `az rest` to GA</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-610">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-610">SQL</span></span>

* <span data-ttu-id="4567b-611">azure-mgmt-sql をバージョン 0.15.0 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-611">Updated azure-mgmt-sql to version 0.15.0.</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-612">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-612">Storage</span></span>

* <span data-ttu-id="4567b-613">storage account create: Blob service でのファイルシステムのセマンティクスをサポートするために、--enable-hierarchical-namespace を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-613">storage account create: Added --enable-hierarchical-namespace to support filesystem semantics in blob service.</span></span>
* <span data-ttu-id="4567b-614">エラー メッセージから関連性のない例外を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-614">Removed unrelated exception from error message</span></span>
* <span data-ttu-id="4567b-615">"この操作を実行するのに必要なアクセス許可がありません" という誤ったエラー メッセージが</span><span class="sxs-lookup"><span data-stu-id="4567b-615">Fixed issues with incorrect error message "You do not have the required permissions needed to perform this operation."</span></span> <span data-ttu-id="4567b-616">ネットワーク ルールまたは AuthenticationFailed によってブロックされた場合に表示される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-616">when blocked by network rules or AuthenticationFailed.</span></span>

## <a name="november-4-2019"></a><span data-ttu-id="4567b-617">2019 年 11 月 4 日</span><span class="sxs-lookup"><span data-stu-id="4567b-617">November 4, 2019</span></span>

<span data-ttu-id="4567b-618">バージョン 2.0.76</span><span class="sxs-lookup"><span data-stu-id="4567b-618">Version 2.0.76</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-619">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-619">ACR</span></span>

* <span data-ttu-id="4567b-620">コマンド `az acr pack build` にプレビュー パラメーター `--pack-image-tag` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-620">Added a preview parameter `--pack-image-tag` to command `az acr pack build`.</span></span>
* <span data-ttu-id="4567b-621">レジストリ作成時の監査を有効にするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-621">Added support for enabling auditing on creating a registry</span></span>
* <span data-ttu-id="4567b-622">レジストリ スコープが設定された RBAC のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-622">Added support for Repository-scoped RBAC</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-623">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-623">AKS</span></span>

* <span data-ttu-id="4567b-624">`az aks create` コマンドに `--enable-cluster-autoscaler`、`--min-count`、および `--max-count` を追加しました。これにより、ノード プールのクラスター オートスケーラーが有効になります。</span><span class="sxs-lookup"><span data-stu-id="4567b-624">Added `--enable-cluster-autoscaler`, `--min-count` and `--max-count` to the `az aks create` command, which enables cluster autoscaler for the node pool.</span></span>
* <span data-ttu-id="4567b-625">上記のフラグに加えて、`--update-cluster-autoscaler` および `--disable-cluster-autoscaler` を `az aks update` コマンドに追加し、クラスター オートスケーラーを更新できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="4567b-625">Added the above flags as well as `--update-cluster-autoscaler` and `--disable-cluster-autoscaler` to the `az aks update` command, allowing updates to cluster autoscaler.</span></span>

### <a name="appconfig"></a><span data-ttu-id="4567b-626">AppConfig</span><span class="sxs-lookup"><span data-stu-id="4567b-626">AppConfig</span></span>

* <span data-ttu-id="4567b-627">App Configuration に格納される機能フラグを管理するために、appconfig feature コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-627">Added appconfig feature command group to manage feature flags stored in an App Configuration.</span></span>
* <span data-ttu-id="4567b-628">ファイルに対する appconfig kv export コマンドの軽微なバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-628">Fixed minor bug for appconfig kv export to file command.</span></span> <span data-ttu-id="4567b-629">エクスポート中に宛先ファイルの内容を読み取らないようにしました。</span><span class="sxs-lookup"><span data-stu-id="4567b-629">Stop reading dest file contents during export.</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-630">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-630">AppService</span></span>

* <span data-ttu-id="4567b-631">`az appservice plan create`:appservice plan create に "persitescaling" を設定するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-631">`az appservice plan create`: Added support to set 'persitescaling' on appservice plan create.</span></span>
* <span data-ttu-id="4567b-632">webapp config ssl bind 操作がリソースから既存のタグを削除する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-632">Fixed an issue where webapp config ssl bind operation was removing existing tags from the resource</span></span>
* <span data-ttu-id="4567b-633">関数アプリのデプロイ時にリモート ビルド アクションをサポートするために、`az functionapp deployment source config-zip` に `--build-remote` フラグを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-633">Added `--build-remote` flag for `az functionapp deployment source config-zip` to support remote build action during function app deployment.</span></span>
* <span data-ttu-id="4567b-634">Windows 向けの関数アプリの既定のノードバージョンを 10 に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-634">Changed default node version on function apps to ~10 for Windows</span></span>
* <span data-ttu-id="4567b-635">`az functionapp create` に `--runtime-version` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-635">Added `--runtime-version` property to `az functionapp create`</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-636">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-636">ARM</span></span>

* <span data-ttu-id="4567b-637">`az deployment/group deployment validate`:デプロイ時に、json テンプレートで複数行とコメントをサポートするために `--handle-extended-json-format` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-637">`az deployment/group deployment validate`: Added `--handle-extended-json-format` parameter to support multiline and comments in json template when deployment.</span></span>
* <span data-ttu-id="4567b-638">azure-mgmt-resource を 2019-07-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="4567b-638">Bumped azure-mgmt-resource to 2019-07-01</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-639">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-639">Backup</span></span>

* <span data-ttu-id="4567b-640">AzureFiles のバックアップ サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-640">Added AzureFiles backup support</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-641">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-641">Compute</span></span>

* <span data-ttu-id="4567b-642">`az vm create`:高速ネットワークと既存の NIC を一緒に指定した場合の警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-642">`az vm create`: Added warning when specifying accelerated networking and an existing NIC together.</span></span>
* <span data-ttu-id="4567b-643">`az vm create`:仮想マシンを割り当てる必要がある既存の仮想マシン スケール セットを指定するための `--vmss` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-643">`az vm create`: Added `--vmss` to specify an existing virtual machine scale set that the virtual machine should be assigned to.</span></span>
* <span data-ttu-id="4567b-644">`az vm/vmss create`:イメージ エイリアス ファイルのローカル コピーを追加し、制限付きネットワーク環境でそれにアクセスできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="4567b-644">`az vm/vmss create`: Added a local copy of image alias file so that it can be accessed in a restricted network environment.</span></span>
* <span data-ttu-id="4567b-645">`az vmss create`:スケール セットによる仮想マシンの管理方法を指定するための `--orchestration-mode` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-645">`az vmss create`: Added `--orchestration-mode` to specify how virtual machines are managed by the scale set.</span></span>
* <span data-ttu-id="4567b-646">`az vm/vmss update`:Ultra SSD 設定を更新できるように `--ultra-ssd-enabled` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-646">`az vm/vmss update`: Added `--ultra-ssd-enabled` to allow updating ultra SSD setting.</span></span>
* <span data-ttu-id="4567b-647">[破壊的変更] `az vm extension set`:ユーザーが `--ids` を使用して、VM に拡張機能を設定できないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-647">[BREAKING CHANGE] `az vm extension set`: Fixed bug where users could not set an extension on a VM with `--ids`.</span></span>
* <span data-ttu-id="4567b-648">Azure Marketplace イメージの使用条件を管理するための新しいコマンド `az vm image terms accept/cancel/show` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-648">Added new commands `az vm image terms accept/cancel/show` to manage Azure Marketplace image terms.</span></span>
* <span data-ttu-id="4567b-649">VMAccessForLinux をバージョン 1.5 に更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-649">Updated VMAccessForLinux to version 1.5</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-650">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-650">CosmosDB</span></span>

* <span data-ttu-id="4567b-651">[破壊的変更] `az sql container create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-651">[BREAKING CHANGE] `az sql container create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="4567b-652">[破壊的変更] `az gremlin graph create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-652">[BREAKING CHANGE] `az gremlin graph create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="4567b-653">`az sql container create`:`--unique-key-policy` および `--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-653">`az sql container create`: Added `--unique-key-policy` and `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="4567b-654">`az sql container create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-654">`az sql container create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="4567b-655">`gremlin graph create`:`--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-655">`gremlin graph create`: Added `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="4567b-656">`gremlin graph create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-656">`gremlin graph create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="4567b-657">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-657">Fixed typo in help message</span></span>
* <span data-ttu-id="4567b-658">データベース:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-658">database: Added deprecation information</span></span>
* <span data-ttu-id="4567b-659">コレクション:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-659">collection: Added deprecation information</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-660">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-660">IoT</span></span>

* <span data-ttu-id="4567b-661">新しいルーティング ソースの種類を追加しました: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="4567b-661">Added new routing source type: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="4567b-662">`az iot hub create` の不十分な機能を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-662">Fixed missing features in `az iot hub create`</span></span>

### <a name="key-vault"></a><span data-ttu-id="4567b-663">Key Vault</span><span class="sxs-lookup"><span data-stu-id="4567b-663">Key Vault</span></span>

* <span data-ttu-id="4567b-664">証明書ファイルが存在しない場合の予期しないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-664">Fixed an unexpected error when certificate file does not exist</span></span>
* <span data-ttu-id="4567b-665">`az keyvault recover/purge` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-665">Fixed `az keyvault recover/purge` not working</span></span>

### <a name="netappfiles"></a><span data-ttu-id="4567b-666">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="4567b-666">NetAppFiles</span></span>

* <span data-ttu-id="4567b-667">API バージョン 2019-07-01 を使用するために azure-mgmt-netapp を 0.6.0 にアップグレードしました。</span><span class="sxs-lookup"><span data-stu-id="4567b-667">Upgraded azure-mgmt-netapp to 0.6.0 to use API version 2019-07-01.</span></span> <span data-ttu-id="4567b-668">この新しい API バージョンには以下の変更内容が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4567b-668">This new API version includes:</span></span>

    - <span data-ttu-id="4567b-669">ボリューム作成の `--protocol-types` が "NFSv4" ではなく "NFSv 4.1" を受け入れるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-669">Volume creation `--protocol-types` accepts now "NFSv4.1" not "NFSv4"</span></span>
    - <span data-ttu-id="4567b-670">ボリューム エクスポート ポリシー プロパティの名前が "nfsv4" ではなく "nfsv41" に変更されました</span><span class="sxs-lookup"><span data-stu-id="4567b-670">Volume export policy property now named 'nfsv41' not 'nfsv4'</span></span>
    - <span data-ttu-id="4567b-671">ボリュームの `--creation-token` の名前が `--file-path` に変更されました</span><span class="sxs-lookup"><span data-stu-id="4567b-671">Volume `--creation-token` renamed to `--file-path`</span></span>
    - <span data-ttu-id="4567b-672">スナップショット作成日の名前が単に "created" に変更されました</span><span class="sxs-lookup"><span data-stu-id="4567b-672">Snapshot creation date now named just 'created'</span></span>

### <a name="network"></a><span data-ttu-id="4567b-673">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-673">Network</span></span>

* <span data-ttu-id="4567b-674">`az network private-dns link vnet create/update`:テナント間の仮想ネットワーク リンクがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4567b-674">`az network private-dns link vnet create/update`: Support cross-tenant virtual network linking.</span></span>
* <span data-ttu-id="4567b-675">[破壊的変更] `az network vnet subnet list`:`--resource-group` と `--vnet-name` を必須に変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-675">[BREAKING CHANGE] `az network vnet subnet list`: Changed `--resource-group` and `--vnet-name` to be required now.</span></span>
* <span data-ttu-id="4567b-676">`az network public-ip prefix create`:作成時に IP アドレスのバージョン (IPv4、IPv6) を指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-676">`az network public-ip prefix create`: Added support to specify IP address version (IPv4, IPv6) when creation</span></span>
* <span data-ttu-id="4567b-677">azure-mgmt-network を 7.0.0 に、api-version を 2019-09-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="4567b-677">Bumped azure-mgmt-network to 7.0.0 and api-version to 2019-09-01</span></span>
* <span data-ttu-id="4567b-678">`az network vrouter`:新しいサービスの仮想ルーターと仮想ルーター ピアリングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-678">`az network vrouter`: Added support for new service virtual router and virtual router peering</span></span>
* <span data-ttu-id="4567b-679">`az network express-route gateway connection`:`--internet-security` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-679">`az network express-route gateway connection`: Added support for `--internet-security`</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-680">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-680">Profile</span></span>

* <span data-ttu-id="4567b-681">`az account get-access-token --resource-type ms-graph` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-681">Fixed `az account get-access-token --resource-type ms-graph` not working</span></span>
* <span data-ttu-id="4567b-682">`az login` からの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-682">Removed warning from `az login`</span></span>

### <a name="rbac"></a><span data-ttu-id="4567b-683">RBAC</span><span class="sxs-lookup"><span data-stu-id="4567b-683">RBAC</span></span>

* <span data-ttu-id="4567b-684">`az ad app update --id {} --display-name {}` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-684">Fixed `az ad app update --id {} --display-name {}` doesn't work</span></span>

### <a name="servicefabric"></a><span data-ttu-id="4567b-685">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4567b-685">ServiceFabric</span></span>

* <span data-ttu-id="4567b-686">`az sf cluster create`:Service Fabric の Linux と Windows の template.json コンピューティング vmss を標準からマネージド ディスクに変更することによって問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-686">`az sf cluster create`: Fixed an issue by modifying service fabric linux and windows template.json compute vmss from standard to managed disks</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-687">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-687">SQL</span></span>

* <span data-ttu-id="4567b-688">次の新しい SQL Database オファリングの CRUD 操作をサポートするために、`--compute-model`、`--auto-pause-delay`、および `--min-capacity` パラメーターを追加しました:サーバーレス コンピューティング モデル。</span><span class="sxs-lookup"><span data-stu-id="4567b-688">Added `--compute-model`, `--auto-pause-delay`, and `--min-capacity` parameters to support CRUD operations for new SQL Database offering: Serverless compute model.</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-689">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-689">Storage</span></span>

* <span data-ttu-id="4567b-690">`az storage account create/update`:Azure Files Active Directory Domain Services 認証をサポートするために、--enable-files-adds パラメーターと Azure Active Directory プロパティ引数グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-690">`az storage account create/update`: Added --enable-files-adds parameter and Azure Active Directory Properties Argument group to support Azure Files Active Directory Domain Service Authentication</span></span>
* <span data-ttu-id="4567b-691">ストレージ アカウントの Kerberos キーの一覧表示または再生成をサポートするために、`az storage account keys list/renew` を拡張しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-691">Expanded `az storage account keys list/renew` to support listing or regenerating Kerberos keys of storage account.</span></span>

## <a name="october-15-2019"></a><span data-ttu-id="4567b-692">2019 年 10 月 15 日</span><span class="sxs-lookup"><span data-stu-id="4567b-692">October 15, 2019</span></span>

<span data-ttu-id="4567b-693">バージョン 2.0.75</span><span class="sxs-lookup"><span data-stu-id="4567b-693">Version 2.0.75</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-694">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-694">AKS</span></span>

* <span data-ttu-id="4567b-695">Kubernetes のバージョンでサポートされている場合、`--load-balancer-sku` の既定値を `standard` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-695">Changed `--load-balancer-sku` default value to `standard` if supported by the kubernetes version</span></span>
* <span data-ttu-id="4567b-696">Kubernetes のバージョンでサポートされている場合、`--vm-set-type` の既定値を `virtualmachinescalesets` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-696">Changed `--vm-set-type` default value to `virtualmachinescalesets` if supported by the kubernetes version</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-697">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-697">AMS</span></span>

* <span data-ttu-id="4567b-698">[重大な変更]`job start` の名前を `job create` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-698">[BREAKING CHANGE] Changed the name of `job start` to `job create`</span></span>
* <span data-ttu-id="4567b-699">[重大な変更]`content-key-policy create` の `--ask` パラメーターが UTF8 ではなく 32 文字の 16 進文字列を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-699">[BREAKING CHANGE] Changed the `--ask` parameter of `content-key-policy create` to use a 32-character hex string instead of UTF8</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-700">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-700">AppService</span></span>

* <span data-ttu-id="4567b-701">コマンド `webapp config access-restriction show|set|add|remove` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-701">Added commands `webapp config access-restriction show|set|add|remove`</span></span>
* <span data-ttu-id="4567b-702">より優れたエラー処理を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-702">Added better error handling to `webapp up`</span></span>
* <span data-ttu-id="4567b-703">`Isolated` SKU のサポートを `appservice plan update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-703">Added support for `Isolated` SKU to `appservice plan update`</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-704">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-704">ARM</span></span>

* <span data-ttu-id="4567b-705">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `deployment create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-705">Added `--handle-extended-json-format` parameter `deployment create` to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-706">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-706">Compute</span></span>

* <span data-ttu-id="4567b-707">`--enable-agent` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-707">Added `--enable-agent` parameter to `vm create`</span></span>
* <span data-ttu-id="4567b-708">ゾーンを使用するときに標準のパブリック IP SKU を自動的に使用するように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-708">Changed `vm create` to use standard public IP SKU automatically when using zones</span></span>
* <span data-ttu-id="4567b-709">VM の有効なコンピューター名が指定されていない場合に自動的に作成されるように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-709">Changed `vm create` to automatically create a valid computer name for a VM if none is provided</span></span>
* <span data-ttu-id="4567b-710">VMSS 内の仮想マシンのカスタム コンピューター名プレフィックスをサポートするために `--computer-name-prefix` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-710">Added `--computer-name-prefix` parameter to `vmss create` to support custom computer name prefix of virtual machines in the VMSS</span></span>
* <span data-ttu-id="4567b-711">ログ分析ワークスペースを自動的に有効にする `--workspace` パラメーターを `vm create` に追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-711">Add `--workspace` parameter to `vm create` to enable log analytics workspace automatically</span></span>
* <span data-ttu-id="4567b-712">ギャラリーの API バージョンが 2019-07-01 に更新されました</span><span class="sxs-lookup"><span data-stu-id="4567b-712">Updated galleries API version to 2019-07-01</span></span>

### <a name="core"></a><span data-ttu-id="4567b-713">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-713">Core</span></span>

* <span data-ttu-id="4567b-714">汎用の update コマンドで `--set` パラメーターの構文チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-714">Added syntax check for `--set` parameter in generic update command</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-715">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-715">IoT</span></span>

* <span data-ttu-id="4567b-716">`iot hub show` で "リソースが見つかりません" のエラーが誤って発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-716">Fixed an issue where `iot hub show` would incorrectly error with "resource not found"</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-717">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-717">Monitor</span></span>

* <span data-ttu-id="4567b-718">CRUD のサポートを `monitor log-analytics workspace` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-718">Added support for CRUD to `monitor log-analytics workspace`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-719">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-719">Network</span></span>

* <span data-ttu-id="4567b-720">クロステナントの仮想リンクのサポートを `network private-dns link vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-720">Added support for cross-tenant virtual linking to `network private-dns link vnet [create|update]`</span></span>
* <span data-ttu-id="4567b-721">[重大な変更]`network vnet subnet list` で `--resource-group` および `--vnet-name` パラメーターが必須に変更になりました</span><span class="sxs-lookup"><span data-stu-id="4567b-721">[BREAKING CHANGE] Changed `network vnet subnet list` to require `--resource-group` and `--vnet-name` parameters</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-722">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-722">SQL</span></span>

* <span data-ttu-id="4567b-723">マネージ インスタンスの AAD 管理者の設定をサポートするコマンドを `sql mi ad-admin` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-723">Added commands to `sql mi ad-admin` that support setting an AAD administrator on managed instances</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-724">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-724">Storage</span></span>

* <span data-ttu-id="4567b-725">サービス間のコピー中にアクセス層を保持する `--preserve-s2s-access-tier` パラメーターを `storage copy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-725">Added `--preserve-s2s-access-tier` parameter `storage copy` to preserve access tier during service to service copy</span></span>
* <span data-ttu-id="4567b-726">ストレージ アカウントで大容量ファイルの共有をサポートするために `--enable-large-file-share` パラメーターを `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-726">Added `--enable-large-file-share` parameter to `storage account [create|update]` to support large file shares for storage account</span></span>

## <a name="september-24-2019"></a><span data-ttu-id="4567b-727">2019 年 9 月 24 日</span><span class="sxs-lookup"><span data-stu-id="4567b-727">September 24, 2019</span></span>

<span data-ttu-id="4567b-728">バージョン 2.0.74</span><span class="sxs-lookup"><span data-stu-id="4567b-728">Version 2.0.74</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-729">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-729">ACR</span></span>

* <span data-ttu-id="4567b-730">必須の `--type` パラメーターを `acr config retention update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-730">Added a required `--type` parameter to `acr config retention update`</span></span>
* <span data-ttu-id="4567b-731">[重大な変更] `acr config` コマンド グループでパラメーター `--name -n` の名前が `--registry -r ` に変更されました</span><span class="sxs-lookup"><span data-stu-id="4567b-731">[BREAKING CHANGE] Renamed parameter `--name -n` changed to `--registry -r ` for `acr config` command group</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-732">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-732">AKS</span></span>

* <span data-ttu-id="4567b-733">`--load-balancer-sku` パラメーターを `aks create` コマンドに追加しました。これにより、SLB を使用する AKS クラスターを作成できます</span><span class="sxs-lookup"><span data-stu-id="4567b-733">Added `--load-balancer-sku` parameter to `aks create` command, which allows for creating AKS cluster with SLB</span></span>
* <span data-ttu-id="4567b-734">`--load-balancer-managed-outbound-ip-count`、`--load-balancer-outbound-ips`、`--load-balancer-outbound-ip-prefixes` パラメーターを `aks [create|update]` コマンドに追加しました。これにより、SLB を使用する AKS クラスターのロード バランサー プロファイルを更新できます</span><span class="sxs-lookup"><span data-stu-id="4567b-734">Added `--load-balancer-managed-outbound-ip-count`, `--load-balancer-outbound-ips` and `--load-balancer-outbound-ip-prefixes` parameters to `aks [create|update]` commands, which allow for updating load balancer profile of an AKS cluster with SLB</span></span>
* <span data-ttu-id="4567b-735">`--vm-set-type` パラメーターを `aks create` コマンドに追加しました。これにより、AKS クラスターの VM の種類 (vmas または vmss) を指定できます</span><span class="sxs-lookup"><span data-stu-id="4567b-735">Added `--vm-set-type` parameter to `aks create` command, which allows to specify vm types of an AKS Cluster (vmas or vmss)</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-736">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-736">ARM</span></span>

* <span data-ttu-id="4567b-737">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `group deployment create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-737">Added `--handle-extended-json-format` parameter to `group deployment create` command to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-738">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-738">Compute</span></span>

* <span data-ttu-id="4567b-739">終了のスケジュール化されたイベントを構成しやすくするために `--terminate-notification-time` パラメーターを `vmss [create|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-739">Added `--terminate-notification-time` parameter to `vmss [create|update]` commands to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="4567b-740">終了のスケジュール化されたイベントを構成しやすくするために `--enable-terminate-notification` パラメーターを `vmss update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-740">Added `--enable-terminate-notification` parameter to `vmss update` command to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="4567b-741">`--priority,` `--eviction-policy,` `--max-billing` パラメーターを `[vm|vmss] create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-741">Added `--priority,` `--eviction-policy,` `--max-billing` parameters to `[vm|vmss] create` commands</span></span>
* <span data-ttu-id="4567b-742">`disk create` を変更し、ディスク アップロードの正確なサイズを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-742">Changed `disk create` to allow specifying the exact size of the disk upload</span></span>
* <span data-ttu-id="4567b-743">マネージド ディスクの増分スナップショットのサポートを `snapshot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-743">Added support for incremental snapshots for managed disks to `snapshot create`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="4567b-744">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-744">Cosmos DB</span></span>

* <span data-ttu-id="4567b-745">キー、読み取り専用キー、または接続文字列を表示する `--type <key-type>` パラメーターを `cosmosdb keys list` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-745">Added `--type <key-type>` parameter to `cosmosdb keys list` command to show key, read only keys or connection strings</span></span>
* <span data-ttu-id="4567b-746">`cosmosdb keys regenerate` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-746">Added `cosmosdb keys regenerate` command</span></span>
* <span data-ttu-id="4567b-747">[非推奨]`cosmosdb list-connection-strings`、`cosmosdb regenerate-key`、`cosmosdb list-read-only-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-747">[DEPRECATED] Deprecated `cosmosdb list-connection-strings`, `cosmosdb regenerate-key` and `cosmosdb list-read-only-keys` commands</span></span>

### <a name="eventgrid"></a><span data-ttu-id="4567b-748">EventGrid</span><span class="sxs-lookup"><span data-stu-id="4567b-748">EventGrid</span></span>

* <span data-ttu-id="4567b-749">正しいパラメーターを参照するようにエンドポイントのヘルプ テキストを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-749">Fixed the endpoint help text to refer to the right parameter</span></span>

### <a name="key-vault"></a><span data-ttu-id="4567b-750">Key Vault</span><span class="sxs-lookup"><span data-stu-id="4567b-750">Key Vault</span></span>

* <span data-ttu-id="4567b-751">テナントを使用してログインすると (`login -t`)、`keyvault create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-751">Fixed issue where logging in with a tenant (`login -t`) could cause `keyvault create` to fail</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-752">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-752">Monitor</span></span>

* <span data-ttu-id="4567b-753">`monitor metrics alert create` の `--condition` 引数で `:` 文字を使用できないという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-753">Fixed issue where `:` character was not allowed in `--condition` argument to `monitor metrics alert create`</span></span>

### <a name="policy"></a><span data-ttu-id="4567b-754">ポリシー</span><span class="sxs-lookup"><span data-stu-id="4567b-754">Policy</span></span>

* <span data-ttu-id="4567b-755">Policy API バージョン 2019-06-01 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-755">Added support for Policy API version 2019-06-01</span></span>
* <span data-ttu-id="4567b-756">`policy assignment create` コマンドに `--enforcement-mode` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-756">Added `--enforcement-mode` parameter to `policy assignment create` command</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-757">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-757">Storage</span></span>

* <span data-ttu-id="4567b-758">`az storage copy` コマンドに `--blob-type` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-758">Added `--blob-type` parameter to `az storage copy` command</span></span>

## <a name="september-10-2019"></a><span data-ttu-id="4567b-759">2019 年 9 月 10 日</span><span class="sxs-lookup"><span data-stu-id="4567b-759">September 10, 2019</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-760">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-760">ACR</span></span>

* <span data-ttu-id="4567b-761">アイテム保持ポリシーを構成するためのコマンド グループ `acr config retention` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-761">Added command group `acr config retention` to configure retention policy</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-762">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-762">AKS</span></span>

* <span data-ttu-id="4567b-763">次のコマンドを使用した ACR 統合のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="4567b-763">Added support for ACR integration with the following commands:</span></span>
  * <span data-ttu-id="4567b-764">AKS クラスターに ACR をアタッチするための `--attach-acr` パラメーターを `aks [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-764">Added `--attach-acr` parameter to `aks [create|update]` to attach an ACR to an AKS cluster</span></span>
  * <span data-ttu-id="4567b-765">AKS クラスターから ACR をデタッチするための `--detach-acr` パラメーターを `aks update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-765">Added `--detach-acr` parameter to `aks update` to detach the ACR from an AKS cluster</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-766">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-766">ARM</span></span>

* <span data-ttu-id="4567b-767">API バージョン 2019-05-10 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-767">Updated to use API version 2019-05-10</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-768">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-768">Batch</span></span>

* <span data-ttu-id="4567b-769">`batch pool create` の `--json-file` に新しい JSON 構成設定を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-769">Added new JSON configuration settings to `--json-file` for `batch pool create`:</span></span>
  * <span data-ttu-id="4567b-770">ファイル システム マウント用の `MountConfigurations` を追加しました (詳細については https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="4567b-770">Added `MountConfigurations` for file system mounts (see https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body for details)</span></span>
  * <span data-ttu-id="4567b-771">プール上のパブリック IP 用に、`NetworkConfiguration` にオプションのプロパティ `publicIPs` を追加しました (詳細については https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="4567b-771">Added optional property `publicIPs` on `NetworkConfiguration` for public IPs on pools (see https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body for details)</span></span>
* <span data-ttu-id="4567b-772">共有イメージ ギャラリーのサポートを `--image` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-772">Added support for shared image galleries to `--image`</span></span>
* <span data-ttu-id="4567b-773">[重大な変更]`batch pool create` の `--start-task-wait-for-success` の既定値を `true` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-773">[BREAKING CHANGE] Changed default value of `--start-task-wait-for-success` on `batch pool create` to be `true`</span></span>
* <span data-ttu-id="4567b-774">[重大な変更]`AutoUserSpecification` の `Scope` の既定値が常に Pool になるように変更しました (以前は Windows ノードでは `Task`、Linux ノードでは `Pool` でした)</span><span class="sxs-lookup"><span data-stu-id="4567b-774">[BREAKING CHANGE] Changed default value for `Scope` on `AutoUserSpecification` to always be Pool (was `Task` on Windows nodes, `Pool` on Linux nodes)</span></span>
  * <span data-ttu-id="4567b-775">この引数は、`--json-file` を使用して JSON 構成からのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="4567b-775">This argument can only be set from a JSON configuration with `--json-file`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="4567b-776">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4567b-776">HDInsight</span></span>

* <span data-ttu-id="4567b-777">GA リリース</span><span class="sxs-lookup"><span data-stu-id="4567b-777">GA release</span></span>
* <span data-ttu-id="4567b-778">[重大な変更]`az hdinsight resize` のパラメーター `--workernode-count/-c` が必須に変更されました。</span><span class="sxs-lookup"><span data-stu-id="4567b-778">[BREAKING CHANGE] Changed parameter `--workernode-count/-c` of `az hdinsight resize` to be required.</span></span>

### <a name="key-vault"></a><span data-ttu-id="4567b-779">Key Vault</span><span class="sxs-lookup"><span data-stu-id="4567b-779">Key Vault</span></span>

* <span data-ttu-id="4567b-780">ネットワーク ルールからサブネットを削除できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-780">Fixed issue where subnets couldn't be deleted from network rules</span></span>
* <span data-ttu-id="4567b-781">重複したサブネットと IP アドレスをネットワーク ルールに追加できる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-781">Fixed issue where duplicated subnets and IP addresses could be added to network rules</span></span>

### <a name="network"></a><span data-ttu-id="4567b-782">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-782">Network</span></span>

* <span data-ttu-id="4567b-783">トラフィック分析間隔の値を設定する `--interval` パラメーターを `network watcher flow-log` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-783">Added `--interval` parameter to `network watcher flow-log` to set traffic analysis interval value</span></span>
* <span data-ttu-id="4567b-784">ゲートウェイ ID を管理するための `network application-gateway identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-784">Added `network application-gateway identity` to manage gateway identity</span></span>
* <span data-ttu-id="4567b-785">Key Vault ID を設定するためのサポートを `network application-gateway ssl-cert` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-785">Added support for setting Key Vault ID to `network application-gateway ssl-cert`</span></span>
* <span data-ttu-id="4567b-786">`network express-route peering peer-connection [show|list]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-786">Added `network express-route peering peer-connection [show|list]`</span></span>

### <a name="policy"></a><span data-ttu-id="4567b-787">ポリシー</span><span class="sxs-lookup"><span data-stu-id="4567b-787">Policy</span></span>

* <span data-ttu-id="4567b-788">API バージョン 2019-01-01 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-788">Updated to use API version 2019-01-01</span></span>

## <a name="august-27-2019"></a><span data-ttu-id="4567b-789">2019 年 8 月 27 日</span><span class="sxs-lookup"><span data-stu-id="4567b-789">August 27, 2019</span></span>

<span data-ttu-id="4567b-790">バージョン 2.0.72</span><span class="sxs-lookup"><span data-stu-id="4567b-790">Version 2.0.72</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-791">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-791">ACR</span></span>

* <span data-ttu-id="4567b-792">[重大な変更]`classic` SKU のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-792">[BREAKING CHANGE] Removed support for the `classic` SKU</span></span>

### <a name="api-management"></a><span data-ttu-id="4567b-793">API Management</span><span class="sxs-lookup"><span data-stu-id="4567b-793">API Management</span></span>

* <span data-ttu-id="4567b-794">[プレビュー] `apim` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-794">[PREVIEW] Added `apim` command group</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-795">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-795">AppService</span></span>

* <span data-ttu-id="4567b-796">スロットを指定したときの `webapp webjob continuous start` コマンドに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-796">Fixed issue with `webapp webjob continuous start` command when specifying a slot</span></span>
* <span data-ttu-id="4567b-797">`env` フォルダーを検出してデプロイに使用されているファイルから削除するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-797">Changed `webapp up` to detect `env` folder and remove it from the file used for deployment</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-798">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-798">Keyvault</span></span>

* <span data-ttu-id="4567b-799">`--expires` 引数を無視する `keyvault secret set` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-799">Fixed a bug in `keyvault secret set` that igored the `--expires` argument</span></span>

### <a name="network"></a><span data-ttu-id="4567b-800">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-800">Network</span></span>

* <span data-ttu-id="4567b-801">`--private-ip-address-version` 引数に IPv6 アドレスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-801">Added support for IPv6 addresses to `--private-ip-address-version` arguments</span></span>
* <span data-ttu-id="4567b-802">プライベート エンドポイントの管理用に新しいコマンド `network private-endpoint [create|update|list-types]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-802">Added new commands `network private-endpoint [create|update|list-types]` for private endpoint management</span></span>
* <span data-ttu-id="4567b-803">コマンド グループ `network private-link-service` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-803">Added command group `network private-link-service`</span></span>
* <span data-ttu-id="4567b-804">`--private-endpoint-network-policies` 引数と `--private-link-service-network-policies` 引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-804">Added `--private-endpoint-network-policies` and `--private-link-service-network-policies` arguments to `network vnet subnet update`</span></span>

### <a name="rbac"></a><span data-ttu-id="4567b-805">RBAC</span><span class="sxs-lookup"><span data-stu-id="4567b-805">RBAC</span></span>

* <span data-ttu-id="4567b-806">ホームページが更新されない `ad app update --homepage` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-806">Fixed issue with `ad app update --homepage` where homepage would not be updated</span></span>

### <a name="servicefabric"></a><span data-ttu-id="4567b-807">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4567b-807">ServiceFabric</span></span>

* <span data-ttu-id="4567b-808">キー コンテナーの大文字と小文字が混在する名前のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-808">Added support for mixed-case Key Vault names</span></span>
* <span data-ttu-id="4567b-809">Key Vault で証明書を使用したときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-809">Fixed issue when using certificates in Key Vault</span></span>
* <span data-ttu-id="4567b-810">PFX 証明書ファイルの使用に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-810">Fixed issue with using PFX certificate files</span></span>
* <span data-ttu-id="4567b-811">Key Vault リソースグループが指定されていなかったときの `sf cluster certificate add` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-811">Fixed issue with `sf cluster certificate add` when Key Vault resource group wasn't specified</span></span>
* <span data-ttu-id="4567b-812">`sf cluster set` が動作しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-812">Fixed issue with `sf cluster set` not working</span></span>

### <a name="signalr"></a><span data-ttu-id="4567b-813">SignalR</span><span class="sxs-lookup"><span data-stu-id="4567b-813">SignalR</span></span>

* <span data-ttu-id="4567b-814">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-814">Added new commands:</span></span>
  * <span data-ttu-id="4567b-815">`signalr cors`:SignalR CORS の管理</span><span class="sxs-lookup"><span data-stu-id="4567b-815">`signalr cors`: Manage SignalR CORS</span></span>
  * <span data-ttu-id="4567b-816">`signalr restart`:SignalR Service の再起動</span><span class="sxs-lookup"><span data-stu-id="4567b-816">`signalr restart`: Restart a SignalR service</span></span>
  * <span data-ttu-id="4567b-817">`signalr update`:SignalR Service の更新</span><span class="sxs-lookup"><span data-stu-id="4567b-817">`signalr update`: Update a SignalR service</span></span>
* <span data-ttu-id="4567b-818">`--service-mode` 引数を `signalr create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-818">Added `--service-mode` argument to `signalr create`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-819">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-819">Storage</span></span>

* <span data-ttu-id="4567b-820">`storage account revoke-delegation-keys` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-820">Added `storage account revoke-delegation-keys` command</span></span>

## <a name="august-13-2019"></a><span data-ttu-id="4567b-821">2019 年 8 月 13 日</span><span class="sxs-lookup"><span data-stu-id="4567b-821">August 13, 2019</span></span>

<span data-ttu-id="4567b-822">バージョン 2.0.71</span><span class="sxs-lookup"><span data-stu-id="4567b-822">Version 2.0.71</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-823">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-823">AppService</span></span>

* <span data-ttu-id="4567b-824">`webapp webjob continuous` コマンドがスロットで失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-824">Fixed issue where `webapp webjob continuous` commands were failing for slots</span></span>

### <a name="botservice"></a><span data-ttu-id="4567b-825">BotService</span><span class="sxs-lookup"><span data-stu-id="4567b-825">BotService</span></span>

* <span data-ttu-id="4567b-826">[重大な変更] v3 SDK ボットの作成のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-826">[BREAKING CHANGE] Removed support for creating v3 SDK bots</span></span>

### <a name="cognitiveservices"></a><span data-ttu-id="4567b-827">CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4567b-827">CognitiveServices</span></span>

* <span data-ttu-id="4567b-828">`cognitiveservices account network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-828">Added `cognitiveservices account network-rule` commands</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="4567b-829">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-829">Cosmos DB</span></span>

* <span data-ttu-id="4567b-830">複数の書き込み場所を更新するときの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-830">Removed warning when updating multiple write locations</span></span>
* <span data-ttu-id="4567b-831">CosmosDB SQL、MongoDB、Cassandra、Gremlin、およびテーブル リソースとリソースのスループットのための CRUD コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-831">Added CRUD commands for CosmosDB SQL, MongoDB, Cassandra, Gremlin and Table resources and resource's throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="4567b-832">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4567b-832">HDInsight</span></span>

<span data-ttu-id="4567b-833">このリリースには、多数の破壊的変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4567b-833">This release contains a large number of breaking changes.</span></span>

* <span data-ttu-id="4567b-834">[重大な変更]`hdinsight create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-834">[BREAKING CHANGE] Renamed parameters for `hdinsight create`:</span></span>
  * <span data-ttu-id="4567b-835">`--storage-default-container` から `--storage-container` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-835">Renamed `--storage-default-container` to `--storage-container`</span></span>
  * <span data-ttu-id="4567b-836">`--storage-default-filesystem` から `--storage-filesystem` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-836">Renamed `--storage-default-filesystem` to `--storage-filesystem`</span></span>
* <span data-ttu-id="4567b-837">[重大な変更]`application create` の `--name` 引数が、クラスター名の代わりにアプリケーション名を表すように変更されました</span><span class="sxs-lookup"><span data-stu-id="4567b-837">[BREAKING CHANGE] Changed the `--name` argument of `application create` to represent the application name instead of the cluster name</span></span>
* <span data-ttu-id="4567b-838">`--cluster-name` 引数が `application create` に追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="4567b-838">Added `--cluster-name` argument to `application create` to replace old `--name` functionality</span></span>
* <span data-ttu-id="4567b-839">[重大な変更]`application create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-839">[BREAKING CHANGE] Renamed parameters for `application create`:</span></span>
  * <span data-ttu-id="4567b-840">`--application-type` から `--type` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-840">Renamed `--application-type` to `--type`</span></span>
  * <span data-ttu-id="4567b-841">`--marketplace-identifier` から `--marketplace-id` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-841">Renamed `--marketplace-identifier` to `--marketplace-id`</span></span>
  * <span data-ttu-id="4567b-842">`--https-endpoint-access-mode` から `--access-mode` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-842">Renamed `--https-endpoint-access-mode` to `--access-mode`</span></span>
  * <span data-ttu-id="4567b-843">`--https-endpoint-destination-port` の名前を `--destination-port` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-843">Renamed  `--https-endpoint-destination-port` to `--destination-port`</span></span>
* <span data-ttu-id="4567b-844">[重大な変更]`application create` のパラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-844">[BREAKING CHANGE] Removed parameters for `application create`:</span></span>
  * `--https-endpoint-location`
  * `--https-endpoint-public-port`
  * `--ssh-endpoint-destination-port`
  * `--ssh-endpoint-location`
  * `--ssh-endpoint-public-port`
* <span data-ttu-id="4567b-845">[破壊的変更] `hdinsight resize`の `--target-instance-count` の名前を `--workernode-count` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-845">[BREAKING CHNAGE] Renamed `--target-instance-count` to `--workernode-count` for `hdinsight resize`</span></span>
* <span data-ttu-id="4567b-846">[重大な変更]`hdinsight script-action` グループのすべてのコマンドが、スクリプト アクションの名前として `--name` パラメーターを使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="4567b-846">[BREAKING CHANGE] Changed all commands in the `hdinsight script-action` group to use the `--name` parameter as the name of the script action.</span></span>
* <span data-ttu-id="4567b-847">`--cluster-name` 引数がすべての `hdinsight script-action` コマンドに追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="4567b-847">Added `--cluster-name` argument to all `hdinsight script-action` commands to replace old `--name` functionality</span></span>
* <span data-ttu-id="4567b-848">[重大な変更] すべての `hdinsight script-action` コマンドで `--script-execution-id` の名前を `--execution-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-848">[BREAKING CHANGE] Renamed `--script-execution-id` to `--execution-id` for all `hdinsight script-action` commands</span></span>
* <span data-ttu-id="4567b-849">[重大な変更] 名前を `hdinsight script-action show` から `hdinsight script-action show-execution-details` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-849">[BREAKING CHANGE] Renamed `hdinsight script-action show` to `hdinsight script-action show-execution-details`</span></span>
* <span data-ttu-id="4567b-850">[破壊的変更] `hdinsight script-action execute --roles` に対するパラメーターを、コンマ区切りではなくスペース区切りにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-850">[BREAKING CHNAGE] Changed parameters to `hdinsight script-action execute --roles` to be space-separated instead of comma-separated</span></span>
* <span data-ttu-id="4567b-851">[重大な変更]`hdinsight script-action list`の `--persisted` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-851">[BREAKING CHANGE] Removed the `--persisted` parameter of `hdinsight script-action list`</span></span>
* <span data-ttu-id="4567b-852">ローカル JSON ファイルへのパスまたは JSON 文字列を受け入れるように `hdinsight create --cluster-configurations` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-852">Changed the `hdinsight create --cluster-configurations` parameter to accept a path to a local JSON file or a JSON string</span></span>
* <span data-ttu-id="4567b-853">`hdinsight script-action list-execution-history` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-853">Added command `hdinsight script-action list-execution-history`</span></span>
* <span data-ttu-id="4567b-854">Log Analytics ワークスペース ID またはワークスペース名を受け入れるように `hdinsight monitor enable --workspace` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-854">Changed `hdinsight monitor enable --workspace` to accept a Log Analytics workspace ID or workspace name</span></span>
* <span data-ttu-id="4567b-855">`hdinsight monitor enable --primary-key` 引数を追加しました。これは、ワークスペース ID がパラメーターとして指定されている場合に必要です</span><span class="sxs-lookup"><span data-stu-id="4567b-855">Added the `hdinsight monitor enable --primary-key` argument, which is needed if a workspace ID is provided as the parameter</span></span>
* <span data-ttu-id="4567b-856">例をさらに追加し、ヘルプ メッセージの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-856">Added more examples and updated descriptions for help messages</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-857">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-857">Interactive</span></span>

* <span data-ttu-id="4567b-858">読み込みエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-858">Fixed a loading error</span></span>

### <a name="kubernetes"></a><span data-ttu-id="4567b-859">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="4567b-859">Kubernetes</span></span>

* <span data-ttu-id="4567b-860">ダッシュボードのコンテナー ポートで `https` が使用されている場合に `https` を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-860">Changed to use `https` if dashboard container port is using `https`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-861">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-861">Network</span></span>

* <span data-ttu-id="4567b-862">`--yes` 引数を `network dns record-set cname delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-862">Added `--yes` argument `network dns record-set cname delete`</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-863">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-863">Profile</span></span>

* <span data-ttu-id="4567b-864">リソースのアクセス トークンを取得するための `account get-access-token` に `--resource-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-864">Added `--resource-type` argument to `account get-access-token` to get resource access tokens</span></span>

### <a name="servicefabric"></a><span data-ttu-id="4567b-865">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4567b-865">ServiceFabric</span></span>

* <span data-ttu-id="4567b-866">sf cluster create でサポートされているすべての OS バージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-866">Added all supported os version for sf cluster create</span></span>
* <span data-ttu-id="4567b-867">プライマリ証明書の検証のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-867">Fixed primary certificate validation bug</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-868">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-868">Storage</span></span>

* <span data-ttu-id="4567b-869">`storage copy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-869">Added command `storage copy`</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="4567b-870">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="4567b-870">July 30, 2019</span></span>

<span data-ttu-id="4567b-871">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="4567b-871">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-872">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-872">ACR</span></span>

* <span data-ttu-id="4567b-873">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-873">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="4567b-874">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-874">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-875">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-875">Appservice</span></span>

* <span data-ttu-id="4567b-876">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-876">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="4567b-877">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-877">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="4567b-878">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-878">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="4567b-879">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-879">Network</span></span>

* <span data-ttu-id="4567b-880">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="4567b-880">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="4567b-881">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-881">Fixes #9604.</span></span> <span data-ttu-id="4567b-882">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-882">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="4567b-883">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="4567b-883">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="4567b-884">RBAC</span><span class="sxs-lookup"><span data-stu-id="4567b-884">RBAC</span></span>

* <span data-ttu-id="4567b-885">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-885">Added `user update` command</span></span>
* <span data-ttu-id="4567b-886">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-886">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="4567b-887">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="4567b-887">Use replacement argument `--id`</span></span>
* <span data-ttu-id="4567b-888">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-888">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-889">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-889">SQL</span></span>

* <span data-ttu-id="4567b-890">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-890">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-891">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-891">Storage</span></span>

* <span data-ttu-id="4567b-892">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-892">Added `storage remove` command</span></span>
* <span data-ttu-id="4567b-893">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-893">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-894">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-894">VM</span></span>

* <span data-ttu-id="4567b-895">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-895">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="4567b-896">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-896">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="4567b-897">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-897">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="4567b-898">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-898">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="4567b-899">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-899">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="4567b-900">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="4567b-900">July 16, 2019</span></span>

<span data-ttu-id="4567b-901">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="4567b-901">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-902">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-902">Appservice</span></span>

* <span data-ttu-id="4567b-903">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="4567b-903">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="4567b-904">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-904">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="4567b-905">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-905">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="4567b-906">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-906">Core</span></span>

* <span data-ttu-id="4567b-907">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-907">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-908">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-908">Batch</span></span>

* <span data-ttu-id="4567b-909">[重大な変更]`batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="4567b-909">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="4567b-910">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-910">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="4567b-911">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-911">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="4567b-912">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-912">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="4567b-913">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="4567b-913">Eventhubs</span></span>

* <span data-ttu-id="4567b-914">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-914">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-915">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-915">RDBMS</span></span>

* <span data-ttu-id="4567b-916">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-916">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="4567b-917">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-917">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="4567b-918">リレー</span><span class="sxs-lookup"><span data-stu-id="4567b-918">Relay</span></span>

* <span data-ttu-id="4567b-919">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="4567b-919">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="4567b-920">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-920">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="4567b-921">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4567b-921">Servicebus</span></span>

* <span data-ttu-id="4567b-922">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-922">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-923">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-923">Storage</span></span>

* <span data-ttu-id="4567b-924">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="4567b-924">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="4567b-925">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="4567b-925">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="4567b-926">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="4567b-926">July 2, 2019</span></span>

<span data-ttu-id="4567b-927">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="4567b-927">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="4567b-928">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-928">Core</span></span>

* <span data-ttu-id="4567b-929">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="4567b-929">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="4567b-930">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="4567b-930">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="4567b-931">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="4567b-931">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-932">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-932">ACR</span></span>

* <span data-ttu-id="4567b-933">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-933">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-934">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-934">Appservice</span></span>

* <span data-ttu-id="4567b-935">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-935">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="4567b-936">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-936">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="4567b-937">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="4567b-937">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="4567b-938">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-938">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="4567b-939">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-939">Cosmos DB</span></span>

* <span data-ttu-id="4567b-940">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-940">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="4567b-941">DLS</span><span class="sxs-lookup"><span data-stu-id="4567b-941">DLS</span></span>

* <span data-ttu-id="4567b-942">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="4567b-942">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="4567b-943">フィードバック</span><span class="sxs-lookup"><span data-stu-id="4567b-943">Feedback</span></span>

* <span data-ttu-id="4567b-944">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-944">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="4567b-945">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4567b-945">HDInsight</span></span>

* <span data-ttu-id="4567b-946">[重大な変更]`oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-946">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="4567b-947">[重大な変更]`--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-947">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="4567b-948">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-948">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="4567b-949">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-949">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="4567b-950">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-950">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="4567b-951">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-951">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="4567b-952">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-952">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="4567b-953">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="4567b-953">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="4567b-954">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-954">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="4567b-955">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="4567b-955">Managed Services</span></span>

* <span data-ttu-id="4567b-956">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="4567b-956">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-957">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-957">Profile</span></span>
* <span data-ttu-id="4567b-958">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="4567b-958">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="4567b-959">RBAC</span><span class="sxs-lookup"><span data-stu-id="4567b-959">RBAC</span></span>

* <span data-ttu-id="4567b-960">[重大な変更]`create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-960">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="4567b-961">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-961">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="4567b-962">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-962">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="4567b-963">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-963">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-964">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-964">RDBMS</span></span>

* <span data-ttu-id="4567b-965">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-965">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-966">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-966">SQL</span></span>

* <span data-ttu-id="4567b-967">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-967">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-968">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-968">Storage</span></span>

* <span data-ttu-id="4567b-969">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-969">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="4567b-970">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-970">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="4567b-971">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-971">VM</span></span>

* <span data-ttu-id="4567b-972">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-972">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="4567b-973">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-973">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="4567b-974">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="4567b-974">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="4567b-975">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-975">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="4567b-976">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="4567b-976">June 18, 2019</span></span>

<span data-ttu-id="4567b-977">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="4567b-977">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="4567b-978">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-978">Core</span></span>

<span data-ttu-id="4567b-979">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4567b-979">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="4567b-980">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="4567b-980">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="4567b-981">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="4567b-981">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="4567b-982">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="4567b-982">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="4567b-983">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="4567b-983">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="4567b-984">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="4567b-984">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="4567b-985">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="4567b-985">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-986">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-986">ACR</span></span>
* <span data-ttu-id="4567b-987">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-987">Added 'acr check-health' command</span></span>
* <span data-ttu-id="4567b-988">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-988">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-989">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-989">ACS</span></span>
* <span data-ttu-id="4567b-990">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="4567b-990">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-991">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-991">AMS</span></span>
* <span data-ttu-id="4567b-992">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-992">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-993">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-993">AppService</span></span>
* <span data-ttu-id="4567b-994">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-994">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="4567b-995">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-995">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="4567b-996">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-996">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="4567b-997">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-997">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="4567b-998">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-998">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="4567b-999">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-999">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-1000">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-1000">Batch</span></span>
* <span data-ttu-id="4567b-1001">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1001">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="4567b-1002">BatchAI</span><span class="sxs-lookup"><span data-stu-id="4567b-1002">BatchAI</span></span>
* <span data-ttu-id="4567b-1003">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1003">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="4567b-1004">BotService</span><span class="sxs-lookup"><span data-stu-id="4567b-1004">BotService</span></span>
* <span data-ttu-id="4567b-1005">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1005">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-1006">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-1006">CosmosDB</span></span>
* <span data-ttu-id="4567b-1007">[非推奨]`cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1007">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="4567b-1008">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="4567b-1008">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="4567b-1009">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1009">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="4567b-1010">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1010">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="4567b-1011">EventGrid</span><span class="sxs-lookup"><span data-stu-id="4567b-1011">EventGrid</span></span>
* <span data-ttu-id="4567b-1012">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1012">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="4567b-1013">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1013">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="4567b-1014">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1014">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="4567b-1015">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1015">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="4567b-1016">[重大な変更]`eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1016">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="4567b-1017">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4567b-1017">HDInsight</span></span>
* <span data-ttu-id="4567b-1018">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1018">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-1019">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-1019">IoT</span></span>
* <span data-ttu-id="4567b-1020">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1020">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="4567b-1021">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1021">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1022">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1022">Network</span></span>
* <span data-ttu-id="4567b-1023">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1023">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="4567b-1024">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1024">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="4567b-1025">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1025">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="4567b-1026">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1026">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-1027">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-1027">Resource</span></span>
* <span data-ttu-id="4567b-1028">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1028">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="4567b-1029">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1029">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="4567b-1030">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4567b-1030">ServiceBus</span></span>
* <span data-ttu-id="4567b-1031">`servicebus topic create --max-size` での問題 [#9319](https://github.com/azure/azure-cli/issues/9319) を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1031">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-1032">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-1032">SQL</span></span>
* <span data-ttu-id="4567b-1033">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-1033">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="4567b-1034">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1034">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="4567b-1035">SQLVm</span><span class="sxs-lookup"><span data-stu-id="4567b-1035">SQLVm</span></span>
* <span data-ttu-id="4567b-1036">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1036">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="4567b-1037">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1037">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1038">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1038">Storage</span></span>
* <span data-ttu-id="4567b-1039">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1039">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="4567b-1040">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1040">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1041">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1041">VM</span></span>
* <span data-ttu-id="4567b-1042">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1042">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="4567b-1043">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1043">June 4, 2019</span></span>

<span data-ttu-id="4567b-1044">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="4567b-1044">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1045">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1045">Core</span></span>
* <span data-ttu-id="4567b-1046">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1046">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1047">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1047">ACR</span></span>
* <span data-ttu-id="4567b-1048">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1048">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1049">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1049">ACS</span></span>
* <span data-ttu-id="4567b-1050">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1050">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="4567b-1051">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="4567b-1051">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-1052">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-1052">Batch</span></span>
* <span data-ttu-id="4567b-1053">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1053">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-1054">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-1054">IoT</span></span>
* <span data-ttu-id="4567b-1055">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1055">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1056">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1056">Network</span></span>
* <span data-ttu-id="4567b-1057">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1057">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="4567b-1058">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1058">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="4567b-1059">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-1059">Resource</span></span>
* <span data-ttu-id="4567b-1060">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1060">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1061">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1061">Role</span></span>
* <span data-ttu-id="4567b-1062">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1062">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-1063">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-1063">Compute</span></span>
* <span data-ttu-id="4567b-1064">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1064">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="4567b-1065">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1065">May 21, 2019</span></span>

<span data-ttu-id="4567b-1066">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="4567b-1066">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1067">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1067">Core</span></span>
* <span data-ttu-id="4567b-1068">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1068">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="4567b-1069">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1069">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="4567b-1070">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1070">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1071">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1071">ACR</span></span>
* <span data-ttu-id="4567b-1072">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1072">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1073">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1073">ACS</span></span>
* <span data-ttu-id="4567b-1074">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1074">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1075">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-1075">AppService</span></span>
* <span data-ttu-id="4567b-1076">[非推奨]`functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="4567b-1076">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="4567b-1077">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1077">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="4567b-1078">[重大な変更]`--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="4567b-1078">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="4567b-1079">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1079">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="4567b-1080">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1080">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="4567b-1081">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1081">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="4567b-1082">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1082">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="4567b-1083">BotService</span><span class="sxs-lookup"><span data-stu-id="4567b-1083">BotService</span></span>
* <span data-ttu-id="4567b-1084">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1084">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="4567b-1085">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1085">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="4567b-1086">従量課金</span><span class="sxs-lookup"><span data-stu-id="4567b-1086">Consumption</span></span>
* <span data-ttu-id="4567b-1087">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1087">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-1088">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-1088">IoT</span></span>
* <span data-ttu-id="4567b-1089">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1089">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1090">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1090">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="4567b-1092">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1092">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="4567b-1093">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1093">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-1094">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-1094">RDBMS</span></span>
* <span data-ttu-id="4567b-1095">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1095">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="4567b-1096">RBAC</span><span class="sxs-lookup"><span data-stu-id="4567b-1096">RBAC</span></span>
* <span data-ttu-id="4567b-1097">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1097">Added support for management group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1098">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1098">Storage</span></span>
* <span data-ttu-id="4567b-1099">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-1099">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="4567b-1100">Compute</span><span class="sxs-lookup"><span data-stu-id="4567b-1100">Compute</span></span>
* <span data-ttu-id="4567b-1101">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1101">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="4567b-1102">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1102">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="4567b-1103">__注__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="4567b-1103">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="4567b-1104">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1104">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="4567b-1105">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1105">May 6, 2019</span></span>

<span data-ttu-id="4567b-1106">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="4567b-1106">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1107">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1107">ACS</span></span>
* <span data-ttu-id="4567b-1108">[重大な変更]`--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1108">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="4567b-1109">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1109">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="4567b-1110">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1110">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="4567b-1111">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1111">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1112">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1112">Appservice</span></span>
* <span data-ttu-id="4567b-1113">[非推奨]`functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1113">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="4567b-1114">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1114">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="4567b-1115">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1115">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="4567b-1116">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1116">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="4567b-1117">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1117">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="4567b-1118">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1118">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="4567b-1119">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1119">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="4567b-1120">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1120">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="4567b-1121">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1121">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="4567b-1122">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1122">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-1123">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-1123">Batch</span></span>
* <span data-ttu-id="4567b-1124">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1124">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="4567b-1125">Botservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1125">Botservice</span></span>
* <span data-ttu-id="4567b-1126">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="4567b-1126">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="4567b-1127">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1127">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="4567b-1128">[重大な変更]`--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1128">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="4567b-1129">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-1129">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="4567b-1130">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1130">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="4567b-1131">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="4567b-1131">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="4567b-1132">[重大な変更]`bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1132">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="4567b-1133">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1133">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="4567b-1134">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1134">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="4567b-1135">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1135">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="4567b-1136">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1136">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="4567b-1137">[重大な変更]`Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1137">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="4567b-1138">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1138">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="4567b-1139">[重大な変更]`SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1139">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="4567b-1140">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="4567b-1140">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="4567b-1141">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1141">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="4567b-1142">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1142">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="4567b-1143">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1143">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="4567b-1144">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1144">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="4567b-1145">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1145">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="4567b-1146">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1146">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="4567b-1147">構成</span><span class="sxs-lookup"><span data-stu-id="4567b-1147">Configure</span></span>
* <span data-ttu-id="4567b-1148">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1148">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="4567b-1149">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="4567b-1149">Eventhubs</span></span>
* <span data-ttu-id="4567b-1150">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1150">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="4567b-1151">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1151">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1152">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1152">Network</span></span>
* <span data-ttu-id="4567b-1153">[重大な変更]`vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="4567b-1153">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="4567b-1154">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="4567b-1154">Policy Insights</span></span>
* <span data-ttu-id="4567b-1155">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1155">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1156">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1156">Role</span></span>
* <span data-ttu-id="4567b-1157">[非推奨]`create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="4567b-1157">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="4567b-1158">Service Bus</span><span class="sxs-lookup"><span data-stu-id="4567b-1158">Service Bus</span></span>
* <span data-ttu-id="4567b-1159">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1159">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="4567b-1160">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1160">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="4567b-1161">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1161">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-1162">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-1162">SQL</span></span>
* <span data-ttu-id="4567b-1163">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1163">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1164">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1164">VM</span></span>
* <span data-ttu-id="4567b-1165">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1165">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="4567b-1166">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1166">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="4567b-1167">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1167">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="4567b-1168">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1168">Added new `ppg` command group for managing Proximity Placement Groups</span></span>
* <span data-ttu-id="4567b-1169">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1169">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="4567b-1170">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1170">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="4567b-1171">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1171">April 23, 2019</span></span>

<span data-ttu-id="4567b-1172">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="4567b-1172">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1173">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1173">ACS</span></span>
* <span data-ttu-id="4567b-1174">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1174">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="4567b-1175">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1175">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-1176">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-1176">AMS</span></span>
* <span data-ttu-id="4567b-1177">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1177">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1178">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-1178">AppService</span></span>
* <span data-ttu-id="4567b-1179">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1179">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="4567b-1180">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1180">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="4567b-1181">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1181">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="4567b-1182">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1182">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="4567b-1183">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1183">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="4567b-1184">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1184">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="4567b-1185">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1185">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="4567b-1186">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1186">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="4567b-1187">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1187">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="4567b-1188">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="4567b-1188">Deployment Manager</span></span>
* <span data-ttu-id="4567b-1189">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="4567b-1189">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="4567b-1190">ラボ</span><span class="sxs-lookup"><span data-stu-id="4567b-1190">Lab</span></span>
* <span data-ttu-id="4567b-1191">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1191">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1192">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1192">Network</span></span>
* <span data-ttu-id="4567b-1193">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1193">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-1194">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-1194">Resource</span></span>
* <span data-ttu-id="4567b-1195">[非推奨]`resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1195">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="4567b-1196">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-1196">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="4567b-1197">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1197">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="4567b-1198">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1198">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-1199">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-1199">SQL</span></span>
* <span data-ttu-id="4567b-1200">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1200">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="4567b-1201">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1201">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="4567b-1202">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1202">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="4567b-1203">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1203">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1204">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1204">Storage</span></span>
* <span data-ttu-id="4567b-1205">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1205">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1206">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1206">VM</span></span>
* <span data-ttu-id="4567b-1207">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1207">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="4567b-1208">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1208">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="4567b-1209">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1209">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="4567b-1210">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1210">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1211">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1211">Core</span></span>
* <span data-ttu-id="4567b-1212">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1212">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1213">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1213">ACR</span></span>
* <span data-ttu-id="4567b-1214">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-1214">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-1215">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-1215">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="4567b-1218">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1218">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="4567b-1219">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1219">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1220">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-1220">AppService</span></span>
* <span data-ttu-id="4567b-1221">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1221">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="4567b-1222">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1222">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="4567b-1223">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1223">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="4567b-1224">[重大な変更]`devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1224">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="4567b-1225">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1225">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="4567b-1226">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1226">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="4567b-1227">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1227">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="4567b-1228">CDN</span><span class="sxs-lookup"><span data-stu-id="4567b-1228">CDN</span></span>
* <span data-ttu-id="4567b-1229">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1229">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="4567b-1230">フィードバック</span><span class="sxs-lookup"><span data-stu-id="4567b-1230">Feedback</span></span>
* <span data-ttu-id="4567b-1231">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1231">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="4567b-1232">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1232">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="4567b-1233">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1233">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-1234">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-1234">Monitor</span></span>
* <span data-ttu-id="4567b-1235">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1235">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="4567b-1236">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1236">Network</span></span>
* <span data-ttu-id="4567b-1237">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1237">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="4567b-1238">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1238">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="4567b-1239">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1239">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="4567b-1240">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1240">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="4567b-1241">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="4567b-1241">PrivateDNS</span></span>
* <span data-ttu-id="4567b-1242">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1242">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-1243">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-1243">Resource</span></span>
* <span data-ttu-id="4567b-1244">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1244">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1245">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1245">Role</span></span>
* <span data-ttu-id="4567b-1246">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1246">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="4567b-1247">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1247">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-1248">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-1248">SQL</span></span>
* <span data-ttu-id="4567b-1249">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1249">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1250">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1250">Storage</span></span>
* <span data-ttu-id="4567b-1251">[重大な変更]`storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1251">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="4567b-1252">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1252">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="4567b-1253">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1253">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="4567b-1254">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1254">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="4567b-1255">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1255">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="4567b-1256">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1256">Core</span></span>
* <span data-ttu-id="4567b-1257">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1257">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="4567b-1258">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1258">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="4567b-1259">クラウド</span><span class="sxs-lookup"><span data-stu-id="4567b-1259">Cloud</span></span>
* <span data-ttu-id="4567b-1260">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1260">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1261">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1261">ACR</span></span>
* <span data-ttu-id="4567b-1262">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1262">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="4567b-1263">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1263">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="4567b-1264">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1264">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="4567b-1265">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1265">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1266">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-1266">AppService</span></span>
* <span data-ttu-id="4567b-1267">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1267">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="4567b-1268">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1268">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="4567b-1269">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="4567b-1269">BOT Service</span></span>
* <span data-ttu-id="4567b-1270">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1270">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="4567b-1271">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1271">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="4567b-1272">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1272">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="4567b-1273">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1273">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="4567b-1274">CDN</span><span class="sxs-lookup"><span data-stu-id="4567b-1274">CDN</span></span>
* <span data-ttu-id="4567b-1275">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1275">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="4567b-1277">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1277">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="4567b-1278">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1278">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-1279">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="4567b-1279">Cosmosdb</span></span>
* <span data-ttu-id="4567b-1280">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1280">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="4567b-1281">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1281">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-1282">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-1282">Interactive</span></span>
* <span data-ttu-id="4567b-1283">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1283">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-1284">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-1284">Monitor</span></span>
* <span data-ttu-id="4567b-1285">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1285">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1286">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1286">Network</span></span>
* <span data-ttu-id="4567b-1287">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1287">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-1288">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-1288">Profile</span></span>
* <span data-ttu-id="4567b-1289">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1289">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="4567b-1290">Postgres</span><span class="sxs-lookup"><span data-stu-id="4567b-1290">Postgres</span></span> 
* <span data-ttu-id="4567b-1291">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1291">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="4567b-1292">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="4567b-1292">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-1293">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-1293">Resource</span></span>
* <span data-ttu-id="4567b-1294">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1294">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="4567b-1295">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1295">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="4567b-1296">グラフ</span><span class="sxs-lookup"><span data-stu-id="4567b-1296">Graph</span></span>
* <span data-ttu-id="4567b-1297">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1297">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="4567b-1298">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1298">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="4567b-1299">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1299">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="4567b-1300">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1300">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="4567b-1301">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1301">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1302">storage</span><span class="sxs-lookup"><span data-stu-id="4567b-1302">storage</span></span>
* <span data-ttu-id="4567b-1303">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1303">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="4567b-1304">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1304">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="4567b-1305">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1305">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="4567b-1306">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1306">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1307">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1307">VM</span></span>
* <span data-ttu-id="4567b-1308">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1308">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="4567b-1309">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1309">March 12, 2019</span></span>

<span data-ttu-id="4567b-1310">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="4567b-1310">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1311">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1311">Core</span></span>

* <span data-ttu-id="4567b-1312">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1312">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1313">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1313">ACR</span></span>

* <span data-ttu-id="4567b-1314">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1314">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1315">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1315">ACS</span></span>

* <span data-ttu-id="4567b-1316">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1316">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="4567b-1317">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-1317">AppService</span></span>

* <span data-ttu-id="4567b-1318">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1318">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="4567b-1319">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1319">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="4567b-1320">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1320">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="4567b-1321">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1321">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="4567b-1322">Botservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1322">Botservice</span></span>

* <span data-ttu-id="4567b-1323">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1323">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="4567b-1324">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1324">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="4567b-1325">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1325">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="4567b-1326">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1326">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="4567b-1327">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-1327">Container</span></span>

* <span data-ttu-id="4567b-1328">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1328">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="4567b-1329">EventHub</span><span class="sxs-lookup"><span data-stu-id="4567b-1329">EventHub</span></span>

* <span data-ttu-id="4567b-1330">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1330">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="4567b-1331">Find</span><span class="sxs-lookup"><span data-stu-id="4567b-1331">Find</span></span>

* <span data-ttu-id="4567b-1332">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="4567b-1332">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="4567b-1333">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4567b-1333">HDInsight</span></span>

* <span data-ttu-id="4567b-1334">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1334">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1335">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1335">Network</span></span>

* <span data-ttu-id="4567b-1336">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1336">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-1337">Rdbms</span><span class="sxs-lookup"><span data-stu-id="4567b-1337">Rdbms</span></span>

* <span data-ttu-id="4567b-1338">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="4567b-1338">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1339">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1339">Role</span></span>

* <span data-ttu-id="4567b-1340">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1340">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="4567b-1341">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1341">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="4567b-1342">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4567b-1342">Service Fabric</span></span>

* <span data-ttu-id="4567b-1343">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1343">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="4567b-1344">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1344">February 26, 2019</span></span>

<span data-ttu-id="4567b-1345">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="4567b-1345">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1346">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1346">Core</span></span>

* <span data-ttu-id="4567b-1347">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1347">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1348">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1348">ACR</span></span>

* <span data-ttu-id="4567b-1349">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1349">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="4567b-1350">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1350">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1351">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1351">ACS</span></span>

* <span data-ttu-id="4567b-1352">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1352">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1353">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-1353">AppService</span></span>

* <span data-ttu-id="4567b-1354">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1354">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-1355">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-1355">Batch</span></span>
* <span data-ttu-id="4567b-1356">[重大な変更]`batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1356">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="4567b-1357">[重大な変更]`Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1357">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="4567b-1358">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1358">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="4567b-1359">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1359">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="4567b-1360">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1360">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="4567b-1361">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="4567b-1361">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-1362">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-1362">CosmosDB</span></span>

* <span data-ttu-id="4567b-1363">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1363">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="4567b-1364">Kusto</span><span class="sxs-lookup"><span data-stu-id="4567b-1364">Kusto</span></span>

* <span data-ttu-id="4567b-1365">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1365">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1366">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1366">Network</span></span>

* <span data-ttu-id="4567b-1367">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1367">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="4567b-1368">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1368">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="4567b-1369">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1369">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="4567b-1370">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1370">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="4567b-1371">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1371">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="4567b-1372">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1372">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="4567b-1373">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1373">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-1374">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-1374">Resource</span></span>

* <span data-ttu-id="4567b-1375">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1375">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="4567b-1376">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1376">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="4567b-1377">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1377">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="4567b-1378">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1378">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="4567b-1379">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1379">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1380">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1380">Role</span></span>

* <span data-ttu-id="4567b-1381">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1381">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1382">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1382">VM</span></span>

* <span data-ttu-id="4567b-1383">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1383">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="4567b-1384">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1384">February 12, 2019</span></span>

<span data-ttu-id="4567b-1385">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="4567b-1385">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1386">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1386">Core</span></span>

* <span data-ttu-id="4567b-1387">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1387">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="4567b-1388">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1388">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1389">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1389">ACR</span></span>
* <span data-ttu-id="4567b-1390">[重大な変更]`acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1390">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="4567b-1391">[重大な変更]`acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1391">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1392">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1392">ACS</span></span>
* <span data-ttu-id="4567b-1393">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1393">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="4567b-1394">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1394">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="4567b-1395">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1395">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-1396">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-1396">AMS</span></span>
* <span data-ttu-id="4567b-1397">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1397">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="4567b-1398">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1398">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1399">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1399">Appservice</span></span>
* <span data-ttu-id="4567b-1400">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1400">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="4567b-1401">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-1401">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="4567b-1402">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1402">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="4567b-1403">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1403">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="4567b-1404">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1404">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="4567b-1405">Botservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1405">Botservice</span></span>
* <span data-ttu-id="4567b-1406">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1406">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="4567b-1407">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1407">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="4567b-1408">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1408">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="4567b-1409">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1409">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="4567b-1410">[非推奨]`--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1410">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="4567b-1411">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1411">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="4567b-1412">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1412">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="4567b-1413">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1413">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="4567b-1414">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="4567b-1414">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="4567b-1415">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1415">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="4567b-1416">Key Vault</span><span class="sxs-lookup"><span data-stu-id="4567b-1416">Key Vault</span></span>
* <span data-ttu-id="4567b-1417">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1417">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-1418">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-1418">Monitor</span></span>
* <span data-ttu-id="4567b-1419">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1419">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1420">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1420">Network</span></span>
* <span data-ttu-id="4567b-1421">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1421">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="4567b-1422">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1422">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="4567b-1423">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1423">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="4567b-1424">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1424">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="4567b-1425">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="4567b-1425">Policy Insights</span></span>
* <span data-ttu-id="4567b-1426">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1426">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-1427">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-1427">RDBMS</span></span>
* <span data-ttu-id="4567b-1428">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1428">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="4567b-1429">Redis</span><span class="sxs-lookup"><span data-stu-id="4567b-1429">Redis</span></span>
* <span data-ttu-id="4567b-1430">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1430">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="4567b-1431">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1431">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="4567b-1432">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1432">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="4567b-1433">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1433">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="4567b-1434">[重大な変更]`redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1434">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="4567b-1435">[重大な変更]`redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1435">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="4567b-1436">[非推奨]`redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1436">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1437">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1437">Role</span></span>
* <span data-ttu-id="4567b-1438">[重大な変更]`az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1438">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="4567b-1439">SQL VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1439">SQL VM</span></span>
* <span data-ttu-id="4567b-1440">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1440">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1441">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1441">VM</span></span>
* <span data-ttu-id="4567b-1442">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1442">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="4567b-1443">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1443">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="4567b-1444">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1444">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="4567b-1445">[重大な変更]`az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1445">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="4567b-1446">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1446">January 31, 2019</span></span>

<span data-ttu-id="4567b-1447">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="4567b-1447">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1448">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1448">Core</span></span>

* <span data-ttu-id="4567b-1449">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="4567b-1449">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="4567b-1450">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1450">January 28, 2019</span></span>

<span data-ttu-id="4567b-1451">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="4567b-1451">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1452">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1452">ACR</span></span>
* <span data-ttu-id="4567b-1453">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1453">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1454">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1454">ACS</span></span>
* <span data-ttu-id="4567b-1455">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1455">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="4567b-1456">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1456">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="4567b-1457">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1457">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-1458">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-1458">AMS</span></span>
* <span data-ttu-id="4567b-1459">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1459">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="4567b-1460">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1460">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1461">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1461">Appservice</span></span>
* <span data-ttu-id="4567b-1462">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1462">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="4567b-1463">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1463">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="4567b-1464">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1464">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="4567b-1465">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-1465">Container</span></span>
* <span data-ttu-id="4567b-1466">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1466">Added `container start` command</span></span>
* <span data-ttu-id="4567b-1467">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1467">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="4567b-1468">EventGrid</span><span class="sxs-lookup"><span data-stu-id="4567b-1468">EventGrid</span></span>
* <span data-ttu-id="4567b-1469">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1469">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="4567b-1470">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1470">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="4567b-1471">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1471">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="4567b-1472">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1472">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="4567b-1473">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1473">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="4567b-1474">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4567b-1474">HDInsight</span></span>
* <span data-ttu-id="4567b-1475">[重大な変更]`hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1475">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="4567b-1476">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1476">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="4567b-1477">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1477">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="4567b-1478">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-1478">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="4567b-1479">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1479">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="4567b-1480">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1480">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-1481">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-1481">IoT</span></span>
* <span data-ttu-id="4567b-1482">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1482">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="4567b-1483">Kusto</span><span class="sxs-lookup"><span data-stu-id="4567b-1483">Kusto</span></span>
* <span data-ttu-id="4567b-1484">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="4567b-1484">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-1485">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-1485">Monitor</span></span>
* <span data-ttu-id="4567b-1486">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1486">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-1487">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-1487">Profile</span></span>
* <span data-ttu-id="4567b-1488">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1488">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1489">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1489">Network</span></span>
* <span data-ttu-id="4567b-1490">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1490">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="4567b-1491">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1491">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-1492">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-1492">Resource</span></span>
* <span data-ttu-id="4567b-1493">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1493">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="4567b-1494">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1494">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="4567b-1495">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="4567b-1495">SQL Virtual Machine</span></span>
* <span data-ttu-id="4567b-1496">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="4567b-1496">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1497">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1497">Storage</span></span>
* <span data-ttu-id="4567b-1498">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1498">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="4567b-1499">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="4567b-1499">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1500">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1500">VM</span></span>
* <span data-ttu-id="4567b-1501">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1501">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="4567b-1502">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1502">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="4567b-1503">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1503">January 15, 2019</span></span>

<span data-ttu-id="4567b-1504">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="4567b-1504">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1505">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1505">ACR</span></span>
* <span data-ttu-id="4567b-1506">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1506">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="4567b-1507">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1507">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="4567b-1508">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1508">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="4567b-1509">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1509">ACS</span></span>
* <span data-ttu-id="4567b-1510">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1510">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1511">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1511">Appservice</span></span>
* <span data-ttu-id="4567b-1512">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1512">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="4567b-1513">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1513">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="4567b-1514">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1514">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="4567b-1515">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1515">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="4567b-1516">Botservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1516">Botservice</span></span>
* <span data-ttu-id="4567b-1517">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1517">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="4567b-1518">構成</span><span class="sxs-lookup"><span data-stu-id="4567b-1518">Configure</span></span>
* <span data-ttu-id="4567b-1519">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1519">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-1520">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-1520">CosmosDB</span></span>
* <span data-ttu-id="4567b-1521">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1521">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="4567b-1522">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4567b-1522">HDInsight</span></span>
* <span data-ttu-id="4567b-1523">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1523">Added commands for managing applications</span></span>
* <span data-ttu-id="4567b-1524">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1524">Added commands for managing script actions</span></span>
* <span data-ttu-id="4567b-1525">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1525">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="4567b-1526">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1526">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="4567b-1527">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1527">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1528">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1528">Network</span></span>
* <span data-ttu-id="4567b-1529">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1529">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="4567b-1530">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1530">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="4567b-1531">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1531">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="4567b-1532">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1532">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1533">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1533">Role</span></span>
* <span data-ttu-id="4567b-1534">[非推奨]`create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1534">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="4567b-1535">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="4567b-1535">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="4567b-1536">Security</span><span class="sxs-lookup"><span data-stu-id="4567b-1536">Security</span></span>
* <span data-ttu-id="4567b-1537">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-1537">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1538">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1538">Storage</span></span>
* <span data-ttu-id="4567b-1539">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1539">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="4567b-1540">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="4567b-1540">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="4567b-1541">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1541">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="4567b-1542">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1542">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="4567b-1543">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1543">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1544">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1544">VM</span></span>
* <span data-ttu-id="4567b-1545">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1545">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="4567b-1546">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1546">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="4567b-1547">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1547">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="4567b-1548">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1548">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="4567b-1549">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1549">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="4567b-1550">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1550">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="4567b-1551">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1551">December 20, 2018</span></span>

<span data-ttu-id="4567b-1552">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="4567b-1552">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="4567b-1553">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1553">Appservice</span></span>
* <span data-ttu-id="4567b-1554">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1554">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="4567b-1555">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1555">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="4567b-1556">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1556">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="4567b-1557">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="4567b-1557">IoTCentral</span></span>
* <span data-ttu-id="4567b-1558">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1558">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1559">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1559">Role</span></span>
* <span data-ttu-id="4567b-1560">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1560">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-1561">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-1561">SQL</span></span>
* <span data-ttu-id="4567b-1562">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1562">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1563">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1563">VM</span></span>
* <span data-ttu-id="4567b-1564">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1564">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="4567b-1565">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1565">December 18, 2018</span></span>

<span data-ttu-id="4567b-1566">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="4567b-1566">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="4567b-1567">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1567">ACR</span></span>
* <span data-ttu-id="4567b-1568">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1568">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="4567b-1569">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1569">Condensed the table layout for task list</span></span>
* <span data-ttu-id="4567b-1570">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1570">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1571">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1571">ACS</span></span>
* <span data-ttu-id="4567b-1572">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1572">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="4567b-1573">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1573">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="4567b-1574">[非推奨]`az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1574">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="4567b-1575">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="4567b-1575">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="4567b-1576">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1576">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="4567b-1577">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1577">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1578">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1578">Appservice</span></span>
* <span data-ttu-id="4567b-1579">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1579">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="4567b-1580">Botservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1580">Botservice</span></span>
* <span data-ttu-id="4567b-1581">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1581">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="4567b-1582">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1582">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="4567b-1583">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1583">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="4567b-1584">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1584">Reduced Kudu network calls</span></span>
* <span data-ttu-id="4567b-1585">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1585">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="4567b-1586">従量課金</span><span class="sxs-lookup"><span data-stu-id="4567b-1586">Consumption</span></span>
* <span data-ttu-id="4567b-1587">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1587">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-1588">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-1588">CosmosDB</span></span>
* <span data-ttu-id="4567b-1589">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1589">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="4567b-1590">マップ</span><span class="sxs-lookup"><span data-stu-id="4567b-1590">Maps</span></span>
* <span data-ttu-id="4567b-1591">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1591">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1592">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1592">Network</span></span>
* <span data-ttu-id="4567b-1593">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1593">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="4567b-1594">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1594">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-1595">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-1595">Resource</span></span>
* <span data-ttu-id="4567b-1596">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1596">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="4567b-1597">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1597">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1598">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1598">Storage</span></span>
*  <span data-ttu-id="4567b-1599">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1599">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1600">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1600">VM</span></span>
* <span data-ttu-id="4567b-1601">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1601">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="4567b-1602">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1602">December 4, 2018</span></span>

<span data-ttu-id="4567b-1603">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="4567b-1603">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="4567b-1604">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1604">Core</span></span>
* <span data-ttu-id="4567b-1605">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1605">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="4567b-1606">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1606">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1607">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1607">Appservice</span></span>
* <span data-ttu-id="4567b-1608">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1608">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="4567b-1609">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1609">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1610">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1610">Network</span></span>
* <span data-ttu-id="4567b-1611">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1611">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1612">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1612">Role</span></span>
* <span data-ttu-id="4567b-1613">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1613">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="4567b-1614">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1614">VM</span></span>
* <span data-ttu-id="4567b-1615">[非推奨]`vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1615">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="4567b-1616">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1616">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="4567b-1617">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1617">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="4567b-1618">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1618">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="4567b-1619">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1619">November 20, 2018</span></span>

<span data-ttu-id="4567b-1620">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="4567b-1620">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="4567b-1621">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1621">Core</span></span>
* <span data-ttu-id="4567b-1622">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1622">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1623">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1623">ACR</span></span>
* <span data-ttu-id="4567b-1624">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1624">Added context token to task step</span></span>
* <span data-ttu-id="4567b-1625">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1625">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="4567b-1626">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1626">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1627">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-1627">Appservice</span></span>
* <span data-ttu-id="4567b-1628">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1628">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="4567b-1629">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1629">Updated the default `node_version`.</span></span> <span data-ttu-id="4567b-1630">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="4567b-1630">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="4567b-1631">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1631">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="4567b-1632">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1632">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="4567b-1633">IotCentral</span><span class="sxs-lookup"><span data-stu-id="4567b-1633">IotCentral</span></span>
* <span data-ttu-id="4567b-1634">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1634">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-1635">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-1635">KeyVault</span></span>
* <span data-ttu-id="4567b-1636">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1636">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1637">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1637">Network</span></span>
* <span data-ttu-id="4567b-1638">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1638">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="4567b-1639">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1639">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="4567b-1640">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1640">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="4567b-1641">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1641">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-1642">Rdbms</span><span class="sxs-lookup"><span data-stu-id="4567b-1642">Rdbms</span></span>
* <span data-ttu-id="4567b-1643">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1643">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="4567b-1644">Rbac</span><span class="sxs-lookup"><span data-stu-id="4567b-1644">Rbac</span></span>
* <span data-ttu-id="4567b-1645">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1645">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="4567b-1646">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1646">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="4567b-1647">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1647">Storage</span></span>
* <span data-ttu-id="4567b-1648">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1648">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="4567b-1649">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1649">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="4567b-1650">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1650">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="4567b-1651">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="4567b-1651">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1652">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1652">VM</span></span>
* <span data-ttu-id="4567b-1653">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1653">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="4567b-1654">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1654">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="4567b-1655">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="4567b-1655">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="4567b-1656">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1656">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="4567b-1657">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1657">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="4567b-1658">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1658">Added `snapshot wait` command</span></span>
* <span data-ttu-id="4567b-1659">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1659">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="4567b-1660">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1660">November 6, 2018</span></span>

<span data-ttu-id="4567b-1661">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="4567b-1661">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1662">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1662">Core</span></span>
* <span data-ttu-id="4567b-1663">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1663">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1664">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1664">ACR</span></span>
* <span data-ttu-id="4567b-1665">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1665">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="4567b-1666">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1666">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1667">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1667">ACS</span></span>
* <span data-ttu-id="4567b-1668">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1668">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="4567b-1669">Advisor</span><span class="sxs-lookup"><span data-stu-id="4567b-1669">Advisor</span></span>
* <span data-ttu-id="4567b-1670">GA リリース</span><span class="sxs-lookup"><span data-stu-id="4567b-1670">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-1671">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-1671">AMS</span></span>
* <span data-ttu-id="4567b-1672">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1672">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="4567b-1673">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1673">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="4567b-1674">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1674">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="4567b-1675">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1675">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="4567b-1676">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1676">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="4567b-1677">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1677">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="4567b-1678">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1678">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="4567b-1679">[重大な変更]`ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="4567b-1679">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="4567b-1680">[重大な変更]`ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1680">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="4567b-1681">[重大な変更]`ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1681">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="4567b-1682">[重大な変更]`ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="4567b-1682">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="4567b-1683">[重大な変更]`ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1683">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="4567b-1684">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="4567b-1684">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="4567b-1685">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="4567b-1685">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="4567b-1686">[重大な変更]`ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1686">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="4567b-1687">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1687">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="4567b-1688">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="4567b-1688">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1689">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-1689">AppService</span></span>
* <span data-ttu-id="4567b-1690">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1690">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="4567b-1691">構成</span><span class="sxs-lookup"><span data-stu-id="4567b-1691">Configure</span></span>
* <span data-ttu-id="4567b-1692">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1692">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="4567b-1693">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-1693">Container</span></span>
* <span data-ttu-id="4567b-1694">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1694">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="4567b-1695">EventHub</span><span class="sxs-lookup"><span data-stu-id="4567b-1695">EventHub</span></span>
* <span data-ttu-id="4567b-1696">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1696">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-1697">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-1697">Interactive</span></span>
* <span data-ttu-id="4567b-1698">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="4567b-1698">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-1699">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-1699">Monitor</span></span>
* <span data-ttu-id="4567b-1700">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1700">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1701">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1701">Network</span></span>
* <span data-ttu-id="4567b-1702">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1702">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="4567b-1703">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1703">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="4567b-1704">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1704">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="4567b-1705">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-1705">Profile</span></span>
* <span data-ttu-id="4567b-1706">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1706">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-1707">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-1707">RDBMS</span></span>
* <span data-ttu-id="4567b-1708">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1708">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-1709">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-1709">Resource</span></span>
* <span data-ttu-id="4567b-1710">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1710">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1711">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1711">Role</span></span>
* <span data-ttu-id="4567b-1712">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-1712">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="4567b-1713">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1713">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="4567b-1714">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1714">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1715">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1715">Storage</span></span>
* <span data-ttu-id="4567b-1716">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="4567b-1716">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1717">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1717">VM</span></span>
* <span data-ttu-id="4567b-1718">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1718">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="4567b-1719">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1719">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="4567b-1720">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1720">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="4567b-1721">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1721">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="4567b-1722">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="4567b-1722">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="4567b-1723">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1723">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="4567b-1724">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1724">October 23, 2018</span></span>

<span data-ttu-id="4567b-1725">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="4567b-1725">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1726">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1726">Core</span></span>
* <span data-ttu-id="4567b-1727">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1727">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="4567b-1728">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1728">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1729">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1729">ACR</span></span>
* <span data-ttu-id="4567b-1730">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1730">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="4567b-1731">CDN</span><span class="sxs-lookup"><span data-stu-id="4567b-1731">CDN</span></span>
* <span data-ttu-id="4567b-1732">[重大な変更]`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1732">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="4567b-1733">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-1733">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="4567b-1734">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-1734">Container</span></span>
* <span data-ttu-id="4567b-1735">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1735">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="4567b-1736">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1736">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="4567b-1737">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1737">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="4567b-1738">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1738">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="4567b-1739">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1739">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="4567b-1740">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1740">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="4567b-1741">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1741">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-1742">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-1742">CosmosDB</span></span>
* <span data-ttu-id="4567b-1743">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1743">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-1744">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-1744">Interactive</span></span>
* <span data-ttu-id="4567b-1745">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1745">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="4567b-1746">IoT Central</span><span class="sxs-lookup"><span data-stu-id="4567b-1746">IoT Central</span></span>
* <span data-ttu-id="4567b-1747">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1747">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="4567b-1748">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-1748">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-1749">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-1749">Monitor</span></span>
* <span data-ttu-id="4567b-1750">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="4567b-1750">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="4567b-1751">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1751">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="4567b-1752">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1752">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="4567b-1753">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1753">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="4567b-1754">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1754">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="4567b-1755">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1755">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="4567b-1756">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="4567b-1756">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="4567b-1757">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1757">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="4567b-1758">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1758">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="4567b-1759">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1759">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1760">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1760">Network</span></span>
* <span data-ttu-id="4567b-1761">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1761">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="4567b-1762">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1762">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="4567b-1763">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4567b-1763">ServiceBus</span></span>
* <span data-ttu-id="4567b-1764">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1764">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-1765">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-1765">SQL</span></span>
* <span data-ttu-id="4567b-1766">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1766">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1767">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1767">Storage</span></span>
* <span data-ttu-id="4567b-1768">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1768">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="4567b-1769">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1769">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1770">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1770">VM</span></span>
* <span data-ttu-id="4567b-1771">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="4567b-1771">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="4567b-1772">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1772">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="4567b-1773">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1773">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="4567b-1774">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1774">October 16, 2018</span></span>

<span data-ttu-id="4567b-1775">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="4567b-1775">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1776">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1776">VM</span></span>
* <span data-ttu-id="4567b-1777">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1777">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="4567b-1778">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1778">October 9, 2018</span></span>

<span data-ttu-id="4567b-1779">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="4567b-1779">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1780">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1780">Core</span></span>
* <span data-ttu-id="4567b-1781">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1781">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1782">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1782">ACR</span></span>
* <span data-ttu-id="4567b-1783">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1783">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1784">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1784">ACS</span></span>
* <span data-ttu-id="4567b-1785">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="4567b-1785">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="4567b-1786">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1786">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="4567b-1787">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1787">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="4567b-1788">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1788">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="4567b-1789">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-1789">Container</span></span>
* <span data-ttu-id="4567b-1790">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1790">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="4567b-1791">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1791">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="4567b-1792">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="4567b-1792">Event Hub</span></span>
* <span data-ttu-id="4567b-1793">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1793">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="4567b-1794">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1794">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="4567b-1795">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-1795">Extensions</span></span>
* <span data-ttu-id="4567b-1796">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1796">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="4567b-1797">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4567b-1797">HDInsight</span></span>
* <span data-ttu-id="4567b-1798">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-1798">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-1799">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-1799">IoT</span></span>
* <span data-ttu-id="4567b-1800">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1800">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-1801">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-1801">KeyVault</span></span>
* <span data-ttu-id="4567b-1802">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1802">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1803">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1803">Network</span></span>
* <span data-ttu-id="4567b-1804">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="4567b-1804">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="4567b-1805">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="4567b-1805">See #6052</span></span>
* <span data-ttu-id="4567b-1806">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1806">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="4567b-1807">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="4567b-1807">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="4567b-1808">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1808">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="4567b-1809">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1809">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="4567b-1810">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1810">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="4567b-1811">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1811">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1812">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1812">Role</span></span>
* <span data-ttu-id="4567b-1813">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1813">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="4567b-1814">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1814">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="4567b-1815">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1815">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="4567b-1816">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1816">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="4567b-1817">Service Bus</span><span class="sxs-lookup"><span data-stu-id="4567b-1817">Service Bus</span></span>
* <span data-ttu-id="4567b-1818">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1818">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1819">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1819">VM</span></span>
* <span data-ttu-id="4567b-1820">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1820">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="4567b-1821">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1821">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="4567b-1822">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1822">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="4567b-1823">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1823">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="4567b-1824">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1824">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="4567b-1825">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1825">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="4567b-1826">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1826">September 21, 2018</span></span>

<span data-ttu-id="4567b-1827">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="4567b-1827">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1828">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1828">ACR</span></span>
* <span data-ttu-id="4567b-1829">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1829">Added ACR Task commands</span></span>
* <span data-ttu-id="4567b-1830">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1830">Added quick run command</span></span>
* <span data-ttu-id="4567b-1831">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1831">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="4567b-1832">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1832">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="4567b-1833">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1833">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="4567b-1834">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1834">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1835">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1835">ACS</span></span>
* <span data-ttu-id="4567b-1836">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1836">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="4567b-1837">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1837">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1838">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-1838">AppService</span></span>

* <span data-ttu-id="4567b-1839">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1839">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="4567b-1840">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1840">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="4567b-1841">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1841">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="4567b-1842">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1842">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-1843">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-1843">Batch</span></span>
* <span data-ttu-id="4567b-1844">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1844">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="4567b-1845">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1845">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="4567b-1846">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1846">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="4567b-1847">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1847">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="4567b-1848">Batch AI</span><span class="sxs-lookup"><span data-stu-id="4567b-1848">Batch AI</span></span> 
* <span data-ttu-id="4567b-1849">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1849">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="4567b-1850">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="4567b-1850">Cognitive Services</span></span>
* <span data-ttu-id="4567b-1851">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1851">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="4567b-1852">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1852">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="4567b-1853">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1853">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="4567b-1854">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1854">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="4567b-1855">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1855">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="4567b-1856">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1856">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="4567b-1857">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-1857">Container</span></span>
* <span data-ttu-id="4567b-1858">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1858">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="4567b-1859">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1859">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="4567b-1860">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1860">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="4567b-1861">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1861">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="4567b-1862">DataLake</span><span class="sxs-lookup"><span data-stu-id="4567b-1862">Datalake</span></span>
* <span data-ttu-id="4567b-1863">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1863">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="4567b-1864">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="4567b-1864">Interactive Shell</span></span>
* <span data-ttu-id="4567b-1865">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1865">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="4567b-1866">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1866">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-1867">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-1867">IoT</span></span>
* <span data-ttu-id="4567b-1868">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1868">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="4567b-1869">Key Vault</span><span class="sxs-lookup"><span data-stu-id="4567b-1869">Key Vault</span></span>
* <span data-ttu-id="4567b-1870">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1870">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1871">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1871">Network</span></span>
* <span data-ttu-id="4567b-1872">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1872">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="4567b-1873">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1873">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="4567b-1874">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1874">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="4567b-1875">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1875">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="4567b-1876">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1876">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="4567b-1877">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1877">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="4567b-1878">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1878">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="4567b-1879">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-1879">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="4567b-1880">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1880">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="4567b-1881">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1881">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="4567b-1882">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1882">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="4567b-1883">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1883">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="4567b-1884">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1884">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="4567b-1885">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="4567b-1885">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="4567b-1886">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1886">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="4567b-1887">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1887">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="4567b-1888">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1888">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="4567b-1889">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1889">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-1890">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-1890">RDBMS</span></span>
* <span data-ttu-id="4567b-1891">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1891">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="4567b-1892">予約</span><span class="sxs-lookup"><span data-stu-id="4567b-1892">Reservation</span></span>
* <span data-ttu-id="4567b-1893">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1893">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="4567b-1894">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1894">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="4567b-1895">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="4567b-1895">Manage App</span></span>
* <span data-ttu-id="4567b-1896">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1896">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="4567b-1897">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1897">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="4567b-1898">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-1898">Role</span></span>
* <span data-ttu-id="4567b-1899">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1899">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="4567b-1900">SignalR</span><span class="sxs-lookup"><span data-stu-id="4567b-1900">SignalR</span></span>
* <span data-ttu-id="4567b-1901">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-1901">First release</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1902">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1902">Storage</span></span>
* <span data-ttu-id="4567b-1903">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1903">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="4567b-1904">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1904">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1905">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1905">VM</span></span>
* <span data-ttu-id="4567b-1906">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="4567b-1906">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="4567b-1907">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1907">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="4567b-1908">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1908">August 28, 2018</span></span>

<span data-ttu-id="4567b-1909">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="4567b-1909">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1910">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1910">Core</span></span>

* <span data-ttu-id="4567b-1911">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1911">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="4567b-1912">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1912">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1913">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1913">ACR</span></span>

* <span data-ttu-id="4567b-1914">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1914">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="4567b-1915">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1915">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1916">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1916">ACS</span></span>

* <span data-ttu-id="4567b-1917">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1917">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="4567b-1918">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1918">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-1919">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-1919">AppService</span></span>

* <span data-ttu-id="4567b-1920">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1920">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="4567b-1921">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1921">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="4567b-1922">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1922">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-1923">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-1923">Backup</span></span>

* <span data-ttu-id="4567b-1924">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1924">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="4567b-1925">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="4567b-1925">Bot Service</span></span>

* <span data-ttu-id="4567b-1926">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="4567b-1926">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="4567b-1927">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="4567b-1927">Cognitive Services</span></span>

* <span data-ttu-id="4567b-1928">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1928">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-1929">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-1929">IoT</span></span>

* <span data-ttu-id="4567b-1930">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1930">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-1931">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-1931">Monitor</span></span>

* <span data-ttu-id="4567b-1932">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1932">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="4567b-1933">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1933">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="4567b-1934">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-1934">Network</span></span>

* <span data-ttu-id="4567b-1935">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1935">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-1936">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-1936">Resource</span></span>

* <span data-ttu-id="4567b-1937">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1937">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1938">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1938">Storage</span></span>

* <span data-ttu-id="4567b-1939">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1939">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1940">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1940">VM</span></span>

* <span data-ttu-id="4567b-1941">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1941">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="4567b-1942">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-1942">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="4567b-1943">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="4567b-1943">Auguest 14, 2018</span></span>

<span data-ttu-id="4567b-1944">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="4567b-1944">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="4567b-1945">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-1945">Core</span></span>

* <span data-ttu-id="4567b-1946">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1946">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="4567b-1947">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1947">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="4567b-1948">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="4567b-1948">Telemetry</span></span>

* <span data-ttu-id="4567b-1949">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1949">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1950">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1950">ACR</span></span>

* <span data-ttu-id="4567b-1951">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1951">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="4567b-1952">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1952">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1953">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1953">ACS</span></span>

* <span data-ttu-id="4567b-1954">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1954">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="4567b-1955">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1955">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="4567b-1956">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1956">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="4567b-1957">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1957">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="4567b-1958">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1958">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="4567b-1959">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-1959">AppService</span></span>

* <span data-ttu-id="4567b-1960">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1960">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="4567b-1961">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1961">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="4567b-1962">BatchAI</span><span class="sxs-lookup"><span data-stu-id="4567b-1962">BatchAI</span></span>

* <span data-ttu-id="4567b-1963">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-1963">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="4567b-1964">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-1964">Container</span></span>

* <span data-ttu-id="4567b-1965">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1965">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="4567b-1966">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-1966">IoT</span></span>

* <span data-ttu-id="4567b-1967">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1967">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="4567b-1968">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1968">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="4567b-1969">Iot Central</span><span class="sxs-lookup"><span data-stu-id="4567b-1969">Iot Central</span></span>

* <span data-ttu-id="4567b-1970">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-1970">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-1971">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-1971">KeyVault</span></span>


* <span data-ttu-id="4567b-1972">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1972">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="4567b-1973">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1973">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="4567b-1974">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1974">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="4567b-1975">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1975">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="4567b-1976">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1976">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="4567b-1977">リレー</span><span class="sxs-lookup"><span data-stu-id="4567b-1977">Relay</span></span>

* <span data-ttu-id="4567b-1978">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-1978">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-1979">Sql</span><span class="sxs-lookup"><span data-stu-id="4567b-1979">Sql</span></span>

* <span data-ttu-id="4567b-1980">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1980">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-1981">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-1981">Storage</span></span>

* <span data-ttu-id="4567b-1982">[重大な変更]`--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="4567b-1982">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="4567b-1983">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1983">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="4567b-1984">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1984">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="4567b-1985">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1985">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="4567b-1986">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1986">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-1987">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-1987">VM</span></span>

* <span data-ttu-id="4567b-1988">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1988">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="4567b-1989">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="4567b-1989">July 31, 2018</span></span>

<span data-ttu-id="4567b-1990">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="4567b-1990">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-1991">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-1991">ACR</span></span>

* <span data-ttu-id="4567b-1992">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1992">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="4567b-1993">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1993">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-1994">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-1994">ACS</span></span>

* <span data-ttu-id="4567b-1995">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1995">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-1996">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-1996">Batch</span></span>

* <span data-ttu-id="4567b-1997">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1997">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="4567b-1998">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-1998">Container</span></span>

* <span data-ttu-id="4567b-1999">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-1999">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2000">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2000">Network</span></span>

* <span data-ttu-id="4567b-2001">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2001">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="4567b-2002">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2002">Resource</span></span>

* <span data-ttu-id="4567b-2003">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2003">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="4567b-2004">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2004">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="4567b-2005">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-2005">Role</span></span>

* <span data-ttu-id="4567b-2006">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2006">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="4567b-2007">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2007">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="4567b-2008">検索</span><span class="sxs-lookup"><span data-stu-id="4567b-2008">Search</span></span>

* <span data-ttu-id="4567b-2009">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2009">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="4567b-2010">Service Bus</span><span class="sxs-lookup"><span data-stu-id="4567b-2010">Service Bus</span></span>

* <span data-ttu-id="4567b-2011">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2011">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="4567b-2012">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2012">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="4567b-2013">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="4567b-2013">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="4567b-2014">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="4567b-2014">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2015">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2015">Storage</span></span>

* <span data-ttu-id="4567b-2016">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-2016">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="4567b-2017">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2017">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2018">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2018">VM</span></span>

* <span data-ttu-id="4567b-2019">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-2019">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="4567b-2020">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2020">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="4567b-2021">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2021">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="4567b-2022">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2022">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="4567b-2023">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2023">July 18, 2018</span></span>

<span data-ttu-id="4567b-2024">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="4567b-2024">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2025">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2025">Core</span></span>

* <span data-ttu-id="4567b-2026">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2026">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="4567b-2027">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2027">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="4567b-2028">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2028">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-2029">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-2029">ACR</span></span>

* <span data-ttu-id="4567b-2030">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2030">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="4567b-2031">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2031">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="4567b-2032">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2032">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="4567b-2033">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2033">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2034">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2034">ACS</span></span>

* <span data-ttu-id="4567b-2035">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2035">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2036">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-2036">AppService</span></span>

* <span data-ttu-id="4567b-2037">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2037">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-2038">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-2038">Batch</span></span>

* <span data-ttu-id="4567b-2039">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2039">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="4567b-2040">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2040">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="4567b-2041">Batch AI</span><span class="sxs-lookup"><span data-stu-id="4567b-2041">Batch AI</span></span>

* <span data-ttu-id="4567b-2042">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2042">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2043">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2043">Container</span></span>

* <span data-ttu-id="4567b-2044">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2044">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="4567b-2045">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2045">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2046">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2046">Network</span></span>

* <span data-ttu-id="4567b-2047">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2047">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="4567b-2048">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2048">Added `network nic wait`</span></span>
* <span data-ttu-id="4567b-2049">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2049">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="4567b-2050">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2050">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="4567b-2051">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2051">Resource</span></span>

* <span data-ttu-id="4567b-2052">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2052">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="4567b-2053">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2053">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="4567b-2054">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2054">Added `deployment wait` command</span></span>
* <span data-ttu-id="4567b-2055">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2055">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2056">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2056">SQL</span></span>

* <span data-ttu-id="4567b-2057">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2057">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="4567b-2058">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-2058">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="4567b-2059">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2059">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2060">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2060">Storage</span></span>

* <span data-ttu-id="4567b-2061">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2061">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2062">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2062">VM</span></span>

* <span data-ttu-id="4567b-2063">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2063">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="4567b-2064">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2064">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="4567b-2065">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2065">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="4567b-2066">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2066">July 3, 2018</span></span>

<span data-ttu-id="4567b-2067">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="4567b-2067">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-2068">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-2068">AKS</span></span>

* <span data-ttu-id="4567b-2069">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2069">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="4567b-2070">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2070">July 3, 2018</span></span>

<span data-ttu-id="4567b-2071">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="4567b-2071">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2072">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2072">Core</span></span>

* <span data-ttu-id="4567b-2073">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2073">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-2074">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-2074">ACR</span></span>

* <span data-ttu-id="4567b-2075">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2075">Added polling build status</span></span>
* <span data-ttu-id="4567b-2076">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2076">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="4567b-2077">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2077">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2078">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2078">ACS</span></span>

* <span data-ttu-id="4567b-2079">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2079">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="4567b-2080">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2080">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="4567b-2081">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2081">Updated options for `aks browse` command.</span></span> <span data-ttu-id="4567b-2082">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2082">Added `--listen-port` support</span></span>
* <span data-ttu-id="4567b-2083">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2083">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="4567b-2084">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-2084">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="4567b-2085">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2085">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2086">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-2086">AppService</span></span>

* <span data-ttu-id="4567b-2087">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-2087">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="4567b-2088">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2088">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-2089">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-2089">Backup</span></span>

* <span data-ttu-id="4567b-2090">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2090">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="4567b-2091">BatchAI</span><span class="sxs-lookup"><span data-stu-id="4567b-2091">BatchAI</span></span>

* <span data-ttu-id="4567b-2092">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2092">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="4567b-2093">クラウド</span><span class="sxs-lookup"><span data-stu-id="4567b-2093">Cloud</span></span>

* <span data-ttu-id="4567b-2094">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2094">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2095">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2095">Container</span></span>

* <span data-ttu-id="4567b-2096">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2096">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="4567b-2097">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2097">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="4567b-2098">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2098">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="4567b-2099">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-2099">Extension</span></span>

* <span data-ttu-id="4567b-2100">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2100">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2101">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2101">Network</span></span>

* <span data-ttu-id="4567b-2102">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2102">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-2103">Rdbms</span><span class="sxs-lookup"><span data-stu-id="4567b-2103">Rdbms</span></span>

* <span data-ttu-id="4567b-2104">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2104">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2105">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2105">Resource</span></span>

* <span data-ttu-id="4567b-2106">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2106">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2107">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2107">VM</span></span>

* <span data-ttu-id="4567b-2108">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-2108">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="4567b-2109">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2109">June 25, 2018</span></span>

<span data-ttu-id="4567b-2110">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="4567b-2110">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="4567b-2111">CLI</span><span class="sxs-lookup"><span data-stu-id="4567b-2111">CLI</span></span>

* <span data-ttu-id="4567b-2112">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2112">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="4567b-2113">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2113">June 19, 2018</span></span>

<span data-ttu-id="4567b-2114">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="4567b-2114">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2115">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2115">Core</span></span>

* <span data-ttu-id="4567b-2116">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2116">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-2117">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-2117">ACR</span></span>

* <span data-ttu-id="4567b-2118">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2118">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="4567b-2119">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2119">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2120">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2120">ACS</span></span>

* <span data-ttu-id="4567b-2121">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2121">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="4567b-2122">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2122">Added `--update` support</span></span>
* <span data-ttu-id="4567b-2123">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2123">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="4567b-2124">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2124">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="4567b-2125">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2125">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="4567b-2126">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2126">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="4567b-2127">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2127">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="4567b-2128">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2128">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2129">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-2129">AppService</span></span>

* <span data-ttu-id="4567b-2130">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2130">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="4567b-2131">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2131">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-2132">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-2132">Batch</span></span>

* <span data-ttu-id="4567b-2133">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2133">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="4567b-2134">Batch AI</span><span class="sxs-lookup"><span data-stu-id="4567b-2134">Batch AI</span></span>

* <span data-ttu-id="4567b-2135">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2135">Added support for workspaces.</span></span> <span data-ttu-id="4567b-2136">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="4567b-2136">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="4567b-2137">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2137">Added support for experiments.</span></span> <span data-ttu-id="4567b-2138">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="4567b-2138">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="4567b-2139">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2139">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="4567b-2140">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2140">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="4567b-2141">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="4567b-2141">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="4567b-2142">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2142">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="4567b-2143">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="4567b-2143">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="4567b-2144">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="4567b-2144">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="4567b-2145">[重大な変更]`--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2145">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="4567b-2146">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="4567b-2146">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="4567b-2147">[重大な変更]`--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2147">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="4567b-2148">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="4567b-2148">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="4567b-2149">[重大な変更]`location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2149">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="4567b-2150">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="4567b-2150">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="4567b-2151">[重大な変更]`--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2151">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="4567b-2152">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2152">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="4567b-2153">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2153">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="4567b-2154">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2154">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="4567b-2155">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2155">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="4567b-2156">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2156">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="4567b-2157">マップ</span><span class="sxs-lookup"><span data-stu-id="4567b-2157">Maps</span></span>

* <span data-ttu-id="4567b-2158">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2158">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2159">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2159">Network</span></span>

* <span data-ttu-id="4567b-2160">`https` のサポートを `network lb probe create` に追加しました ([#6571](https://github.com/Azure/azure-cli/issues/6571))</span><span class="sxs-lookup"><span data-stu-id="4567b-2160">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="4567b-2161">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2161">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="4567b-2162">#6502</span><span class="sxs-lookup"><span data-stu-id="4567b-2162">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="4567b-2163">Reservations</span><span class="sxs-lookup"><span data-stu-id="4567b-2163">Reservations</span></span>

* <span data-ttu-id="4567b-2164">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2164">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="4567b-2165">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2165">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="4567b-2166">[重大な変更]`kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2166">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="4567b-2167">[重大な変更]`Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2167">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="4567b-2168">[重大な変更]`Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2168">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="4567b-2169">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2169">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="4567b-2170">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-2170">Role</span></span>

* <span data-ttu-id="4567b-2171">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2171">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2172">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2172">SQL</span></span>

* <span data-ttu-id="4567b-2173">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2173">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2174">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2174">Storage</span></span>

* <span data-ttu-id="4567b-2175">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2175">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2176">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2176">VM</span></span>

* <span data-ttu-id="4567b-2177">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2177">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="4567b-2178">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2178">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="4567b-2179">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2179">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="4567b-2180">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2180">June 13, 2018</span></span>

<span data-ttu-id="4567b-2181">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="4567b-2181">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2182">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2182">Core</span></span>

* <span data-ttu-id="4567b-2183">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2183">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="4567b-2184">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2184">June 13, 2018</span></span>

<span data-ttu-id="4567b-2185">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="4567b-2185">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-2186">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-2186">AKS</span></span>

* <span data-ttu-id="4567b-2187">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2187">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="4567b-2188">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2188">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="4567b-2189">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2189">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="4567b-2190">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2190">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="4567b-2191">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2191">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2192">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-2192">AppService</span></span>

* <span data-ttu-id="4567b-2193">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2193">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="4567b-2194">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2194">June 5, 2018</span></span>

<span data-ttu-id="4567b-2195">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="4567b-2195">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-2196">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-2196">Interactive</span></span>

* <span data-ttu-id="4567b-2197">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2197">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="4567b-2198">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2198">June 5, 2018</span></span>

<span data-ttu-id="4567b-2199">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="4567b-2199">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2200">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2200">Core</span></span>

* <span data-ttu-id="4567b-2201">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2201">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="4567b-2202">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2202">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-2203">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-2203">ACR</span></span>

* <span data-ttu-id="4567b-2204">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2204">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="4567b-2205">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2205">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="4567b-2206">AKS</span><span class="sxs-lookup"><span data-stu-id="4567b-2206">AKS</span></span>

* <span data-ttu-id="4567b-2207">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2207">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-2208">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-2208">Batch</span></span>

* <span data-ttu-id="4567b-2209">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2209">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-2210">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-2210">IOT</span></span>

* <span data-ttu-id="4567b-2211">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2211">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2212">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2212">Network</span></span>

* <span data-ttu-id="4567b-2213">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2213">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="4567b-2214">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="4567b-2214">Policy Insights</span></span>

* <span data-ttu-id="4567b-2215">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-2215">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="4567b-2216">ARM</span><span class="sxs-lookup"><span data-stu-id="4567b-2216">ARM</span></span>

* <span data-ttu-id="4567b-2217">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2217">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2218">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2218">SQL</span></span>

* <span data-ttu-id="4567b-2219">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2219">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="4567b-2220">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2220">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="4567b-2221">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2221">Storage</span></span>

* <span data-ttu-id="4567b-2222">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2222">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2223">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2223">VM</span></span>

* <span data-ttu-id="4567b-2224">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2224">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="4567b-2225">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2225">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="4567b-2226">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2226">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="4567b-2227">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2227">May 22, 2018</span></span>

<span data-ttu-id="4567b-2228">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="4567b-2228">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2229">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2229">Core</span></span>

* <span data-ttu-id="4567b-2230">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2230">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2231">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2231">ACS</span></span>

* <span data-ttu-id="4567b-2232">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2232">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="4567b-2233">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2233">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2234">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-2234">AppService</span></span>

* <span data-ttu-id="4567b-2235">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2235">Improved generic update commands</span></span>
* <span data-ttu-id="4567b-2236">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2236">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2237">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2237">Container</span></span>

* <span data-ttu-id="4567b-2238">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2238">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="4567b-2239">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2239">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="4567b-2240">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-2240">Extension</span></span>

* <span data-ttu-id="4567b-2241">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2241">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-2242">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-2242">Interactive</span></span>

* <span data-ttu-id="4567b-2243">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2243">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="4567b-2244">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2244">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-2245">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-2245">KeyVault</span></span>

* <span data-ttu-id="4567b-2246">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2246">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2247">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2247">Network</span></span>

* <span data-ttu-id="4567b-2248">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2248">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="4567b-2249">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2249">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2250">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2250">SQL</span></span>

* <span data-ttu-id="4567b-2251">[重大な変更]`db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2251">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="4567b-2252">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2252">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="4567b-2253">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2253">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="4567b-2254">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2254">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="4567b-2255">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2255">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="4567b-2256">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="4567b-2256">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="4567b-2257">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="4567b-2257">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="4567b-2258">`edition`</span><span class="sxs-lookup"><span data-stu-id="4567b-2258">`edition`.</span></span> <span data-ttu-id="4567b-2259">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="4567b-2259">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="4567b-2260">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="4567b-2260">`elasticPoolName`.</span></span> <span data-ttu-id="4567b-2261">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="4567b-2261">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="4567b-2262">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2262">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="4567b-2263">`edition`</span><span class="sxs-lookup"><span data-stu-id="4567b-2263">`edition`.</span></span> <span data-ttu-id="4567b-2264">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-2264">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="4567b-2265">`dtu`</span><span class="sxs-lookup"><span data-stu-id="4567b-2265">`dtu`.</span></span> <span data-ttu-id="4567b-2266">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-2266">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="4567b-2267">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="4567b-2267">`databaseDtuMin`.</span></span> <span data-ttu-id="4567b-2268">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-2268">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="4567b-2269">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="4567b-2269">`databaseDtuMax`.</span></span> <span data-ttu-id="4567b-2270">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-2270">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="4567b-2271">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2271">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="4567b-2272">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2272">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2273">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2273">Storage</span></span>

* <span data-ttu-id="4567b-2274">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2274">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="4567b-2275">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2275">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2276">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2276">VM</span></span>

* <span data-ttu-id="4567b-2277">[重大な変更]`--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2277">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="4567b-2278">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="4567b-2278">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="4567b-2279">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2279">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="4567b-2280">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2280">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="4567b-2281">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2281">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="4567b-2282">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2282">May 7, 2018</span></span>

<span data-ttu-id="4567b-2283">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="4567b-2283">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2284">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2284">Core</span></span>

* <span data-ttu-id="4567b-2285">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2285">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="4567b-2286">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2286">Added limited support for positional arguments</span></span>
* <span data-ttu-id="4567b-2287">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2287">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="4567b-2288">#5591</span><span class="sxs-lookup"><span data-stu-id="4567b-2288">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="4567b-2289">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2289">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="4567b-2290">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="4567b-2290">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="4567b-2291">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2291">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="4567b-2292">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2292">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="4567b-2293">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2293">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-2294">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-2294">ACR</span></span>

* <span data-ttu-id="4567b-2295">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2295">Added ACR Build commands</span></span>
* <span data-ttu-id="4567b-2296">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2296">Improved resource not found error messages</span></span>
* <span data-ttu-id="4567b-2297">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2297">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="4567b-2298">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2298">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="4567b-2299">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2299">Improved repository commands error messages</span></span>
* <span data-ttu-id="4567b-2300">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2300">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2301">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2301">ACS</span></span>

* <span data-ttu-id="4567b-2302">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2302">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="4567b-2303">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2303">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="4567b-2304">AMS</span><span class="sxs-lookup"><span data-stu-id="4567b-2304">AMS</span></span>

* <span data-ttu-id="4567b-2305">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="4567b-2305">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2306">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2306">Appservice</span></span>

* <span data-ttu-id="4567b-2307">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2307">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="4567b-2308">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2308">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="4567b-2309">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2309">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="4567b-2310">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2310">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="4567b-2311">Batch AI</span><span class="sxs-lookup"><span data-stu-id="4567b-2311">Batch AI</span></span>

* <span data-ttu-id="4567b-2312">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2312">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="4567b-2313">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="4567b-2313">Cognitive Services</span></span>

* <span data-ttu-id="4567b-2314">`cognitiveservices account create` の例の誤りを修正しました ([#5603](https://github.com/Azure/azure-cli/issues/5603))</span><span class="sxs-lookup"><span data-stu-id="4567b-2314">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="4567b-2315">従量課金</span><span class="sxs-lookup"><span data-stu-id="4567b-2315">Consumption</span></span>

* <span data-ttu-id="4567b-2316">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2316">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2317">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2317">Container</span></span>

* <span data-ttu-id="4567b-2318">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2318">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="4567b-2319">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-2319">Cosmos DB</span></span>

* <span data-ttu-id="4567b-2320">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2320">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="4567b-2321">DMS</span><span class="sxs-lookup"><span data-stu-id="4567b-2321">DMS</span></span>

* <span data-ttu-id="4567b-2322">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2322">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="4567b-2323">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-2323">Extension</span></span>

* <span data-ttu-id="4567b-2324">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2324">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-2325">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-2325">Interactive</span></span>

* <span data-ttu-id="4567b-2326">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-2326">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="4567b-2327">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2327">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="4567b-2328">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2328">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="4567b-2329">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2329">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="4567b-2330">ラボ</span><span class="sxs-lookup"><span data-stu-id="4567b-2330">Lab</span></span>

* <span data-ttu-id="4567b-2331">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2331">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2332">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2332">Network</span></span>

* <span data-ttu-id="4567b-2333">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2333">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="4567b-2334">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-2334">Profile</span></span>

* <span data-ttu-id="4567b-2335">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2335">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="4567b-2336">[重大な変更]`--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2336">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="4567b-2337">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2337">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="4567b-2338">Redis</span><span class="sxs-lookup"><span data-stu-id="4567b-2338">Redis</span></span>

* <span data-ttu-id="4567b-2339">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2339">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="4567b-2340">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2340">Deprecated `redis list-all`.</span></span> <span data-ttu-id="4567b-2341">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="4567b-2341">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="4567b-2342">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2342">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="4567b-2343">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2343">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="4567b-2344">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-2344">Role</span></span>

* <span data-ttu-id="4567b-2345">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2345">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2346">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2346">Storage</span></span>

* <span data-ttu-id="4567b-2347">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="4567b-2347">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="4567b-2348">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2348">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="4567b-2349">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="4567b-2349">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="4567b-2350">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="4567b-2350">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="4567b-2351">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2351">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2352">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2352">VM</span></span>

* <span data-ttu-id="4567b-2353">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2353">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="4567b-2354">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2354">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="4567b-2355">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="4567b-2355">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="4567b-2356">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2356">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="4567b-2357">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2357">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="4567b-2358">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2358">Added write accelerator support</span></span>
* <span data-ttu-id="4567b-2359">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2359">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="4567b-2360">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2360">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="4567b-2361">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2361">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="4567b-2362">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2362">April 10, 2018</span></span>

<span data-ttu-id="4567b-2363">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="4567b-2363">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-2364">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-2364">ACR</span></span>

* <span data-ttu-id="4567b-2365">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2365">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2366">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2366">ACS</span></span>

* <span data-ttu-id="4567b-2367">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2367">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2368">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2368">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="4567b-2370">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2370">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="4567b-2371">BatchAI</span><span class="sxs-lookup"><span data-stu-id="4567b-2371">BatchAI</span></span>

* <span data-ttu-id="4567b-2372">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2372">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="4567b-2373">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="4567b-2373">Job level mounting</span></span>
  - <span data-ttu-id="4567b-2374">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="4567b-2374">Environment variables with secret values</span></span>
  - <span data-ttu-id="4567b-2375">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="4567b-2375">Performance counters settings</span></span>
  - <span data-ttu-id="4567b-2376">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="4567b-2376">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="4567b-2377">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-2377">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="4567b-2378">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="4567b-2378">Usage and limits reporting</span></span>
  - <span data-ttu-id="4567b-2379">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="4567b-2379">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="4567b-2380">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-2380">Support for custom images</span></span>
  - <span data-ttu-id="4567b-2381">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2381">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="4567b-2382">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-2382">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="4567b-2383">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="4567b-2383">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="4567b-2384">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="4567b-2384">National clouds are supported</span></span>
* <span data-ttu-id="4567b-2385">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2385">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="4567b-2386">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2386">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="4567b-2387">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2387">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="4567b-2388">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2388">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="4567b-2389">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="4567b-2389">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="4567b-2390">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="4567b-2390">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="4567b-2391">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2391">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="4567b-2392">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2392">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="4567b-2393">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="4567b-2393">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="4567b-2394">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2394">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="4567b-2395">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2395">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="4567b-2396">[重大な変更]`job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2396">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="4567b-2397">[重大な変更]`cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2397">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="4567b-2398">課金</span><span class="sxs-lookup"><span data-stu-id="4567b-2398">Billing</span></span>

* <span data-ttu-id="4567b-2399">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2399">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="4567b-2400">従量課金</span><span class="sxs-lookup"><span data-stu-id="4567b-2400">Consumption</span></span>

* <span data-ttu-id="4567b-2401">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2401">Added `marketplace` commands</span></span>
* <span data-ttu-id="4567b-2402">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2402">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="4567b-2403">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2403">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="4567b-2404">[重大な変更]`reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2404">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="4567b-2405">[重大な変更]`reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2405">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="4567b-2406">[重大な変更]`pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2406">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2407">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2407">Container</span></span>

* <span data-ttu-id="4567b-2408">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2408">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="4567b-2409">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2409">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="4567b-2410">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-2410">Extension</span></span>

* <span data-ttu-id="4567b-2411">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2411">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-2412">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-2412">Interactive</span></span>

* <span data-ttu-id="4567b-2413">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2413">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="4567b-2414">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2414">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="4567b-2415">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2415">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2416">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2416">Network</span></span>

* <span data-ttu-id="4567b-2417">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2417">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="4567b-2418">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2418">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="4567b-2419">#4910</span><span class="sxs-lookup"><span data-stu-id="4567b-2419">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="4567b-2420">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2420">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="4567b-2421">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="4567b-2421">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="4567b-2422">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2422">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="4567b-2423">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2423">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="4567b-2424">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2424">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-2425">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-2425">Profile</span></span>

* <span data-ttu-id="4567b-2426">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2426">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="4567b-2427">[重大な変更]`--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2427">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-2428">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-2428">RDBMS</span></span>

* <span data-ttu-id="4567b-2429">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2429">Added `georestore` command</span></span>
* <span data-ttu-id="4567b-2430">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2430">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2431">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2431">Resource</span></span>

* <span data-ttu-id="4567b-2432">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2432">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="4567b-2433">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2433">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2434">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2434">SQL</span></span>

* <span data-ttu-id="4567b-2435">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2435">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2436">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2436">Storage</span></span>

* <span data-ttu-id="4567b-2437">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2437">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2438">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2438">VM</span></span>

* <span data-ttu-id="4567b-2439">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2439">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="4567b-2440">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2440">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="4567b-2442">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2442">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="4567b-2443">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2443">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="4567b-2444">#5718</span><span class="sxs-lookup"><span data-stu-id="4567b-2444">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="4567b-2445">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2445">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="4567b-2446">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2446">March 27, 2018</span></span>

<span data-ttu-id="4567b-2447">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="4567b-2447">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2448">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2448">Core</span></span>

* <span data-ttu-id="4567b-2449">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="4567b-2449">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2450">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2450">ACS</span></span>

* <span data-ttu-id="4567b-2451">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2451">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2452">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2452">Appservice</span></span>

* <span data-ttu-id="4567b-2453">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2453">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="4567b-2454">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2454">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-2455">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-2455">Backup</span></span>

* <span data-ttu-id="4567b-2456">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2456">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="4567b-2457">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="4567b-2457">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="4567b-2458">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2458">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="4567b-2459">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2459">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2460">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2460">Container</span></span>

* <span data-ttu-id="4567b-2461">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2461">Added `container exec` command.</span></span> <span data-ttu-id="4567b-2462">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="4567b-2462">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="4567b-2463">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="4567b-2463">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="4567b-2464">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-2464">Extension</span></span>

* <span data-ttu-id="4567b-2465">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2465">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="4567b-2466">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2466">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="4567b-2467">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2467">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-2468">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-2468">Interactive</span></span>

* <span data-ttu-id="4567b-2469">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2469">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="4567b-2470">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2470">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="4567b-2471">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="4567b-2471">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="4567b-2472">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2472">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="4567b-2473">ラボ</span><span class="sxs-lookup"><span data-stu-id="4567b-2473">Lab</span></span>

* <span data-ttu-id="4567b-2474">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2474">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-2475">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-2475">Monitor</span></span>

* <span data-ttu-id="4567b-2476">`--top`、`--orderby`、および `--namespace` のサポートを `metrics list` に追加しました ([#5785](https://github.com/Azure/azure-cli/issues/5785))</span><span class="sxs-lookup"><span data-stu-id="4567b-2476">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="4567b-2477">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="4567b-2477">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="4567b-2478">`--namespace` のサポートを `metrics list-definitions` に追加しました ([#5785](https://github.com/Azure/azure-cli/issues/5785))</span><span class="sxs-lookup"><span data-stu-id="4567b-2478">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2479">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2479">Network</span></span>

* <span data-ttu-id="4567b-2480">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2480">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-2481">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-2481">Profile</span></span>

* <span data-ttu-id="4567b-2482">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2482">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-2483">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-2483">RDBMS</span></span>

* <span data-ttu-id="4567b-2484">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2484">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2485">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2485">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="4567b-2487">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-2487">Role</span></span>

* <span data-ttu-id="4567b-2488">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2488">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="4567b-2489">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2489">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="4567b-2490">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2490">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="4567b-2491">[重大な変更]`az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2491">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="4567b-2492">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2492">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2493">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2493">Storage</span></span>

* <span data-ttu-id="4567b-2494">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2494">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="4567b-2495">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="4567b-2495">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2496">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2496">VM</span></span>

* <span data-ttu-id="4567b-2497">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2497">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="4567b-2498">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2498">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="4567b-2499">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2499">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="4567b-2500">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2500">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="4567b-2501">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2501">March 13, 2018</span></span>

<span data-ttu-id="4567b-2502">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="4567b-2502">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-2503">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-2503">ACR</span></span>

* <span data-ttu-id="4567b-2504">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2504">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="4567b-2505">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2505">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="4567b-2506">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2506">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2507">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2507">ACS</span></span>

* <span data-ttu-id="4567b-2508">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2508">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="4567b-2509">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2509">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="4567b-2510">Advisor</span><span class="sxs-lookup"><span data-stu-id="4567b-2510">Advisor</span></span>

* <span data-ttu-id="4567b-2511">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2511">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="4567b-2512">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2512">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="4567b-2513">[重大な変更]`advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2513">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="4567b-2514">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2514">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="4567b-2515">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2515">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2516">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2516">Appservice</span></span>

* <span data-ttu-id="4567b-2517">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2517">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="4567b-2518">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2518">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="4567b-2519">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="4567b-2519">Eventhubs</span></span>

* <span data-ttu-id="4567b-2520">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-2520">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="4567b-2521">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-2521">Extension</span></span>

* <span data-ttu-id="4567b-2522">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2522">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-2523">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-2523">Interactive</span></span>

* <span data-ttu-id="4567b-2524">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="4567b-2524">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="4567b-2525">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="4567b-2525">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="4567b-2526">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="4567b-2526">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="4567b-2527">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2527">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-2528">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-2528">Monitor</span></span>

* <span data-ttu-id="4567b-2529">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2529">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="4567b-2530">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2530">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="4567b-2531">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2531">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="4567b-2532">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2532">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2533">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2533">Network</span></span>

* <span data-ttu-id="4567b-2534">[重大な変更]`route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2534">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="4567b-2535">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2535">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="4567b-2536">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2536">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="4567b-2537">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2537">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-2538">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-2538">Profile</span></span>

* <span data-ttu-id="4567b-2539">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2539">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="4567b-2540">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2540">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-2541">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-2541">RDBMS</span></span>

* <span data-ttu-id="4567b-2542">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2542">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="4567b-2543">Service Bus</span><span class="sxs-lookup"><span data-stu-id="4567b-2543">Service Bus</span></span>

* <span data-ttu-id="4567b-2544">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-2544">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2545">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2545">Storage</span></span>

* <span data-ttu-id="4567b-2546">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-2546">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="4567b-2547">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="4567b-2547">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2548">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2548">VM</span></span>

* <span data-ttu-id="4567b-2549">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2549">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="4567b-2550">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2550">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="4567b-2551">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2551">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="4567b-2552">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2552">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="4567b-2553">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2553">February 27, 2018</span></span>

<span data-ttu-id="4567b-2554">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="4567b-2554">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2555">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2555">Core</span></span>

* <span data-ttu-id="4567b-2556">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="4567b-2556">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="4567b-2557">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2557">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="4567b-2558">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2558">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2559">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2559">ACS</span></span>

* <span data-ttu-id="4567b-2560">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2560">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="4567b-2561">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="4567b-2561">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="4567b-2562">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2562">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="4567b-2563">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2563">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2564">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2564">Appservice</span></span>

* <span data-ttu-id="4567b-2565">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="4567b-2565">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="4567b-2566">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="4567b-2566">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="4567b-2567">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="4567b-2567">Cognitive Services</span></span>

* <span data-ttu-id="4567b-2568">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2568">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="4567b-2569">従量課金</span><span class="sxs-lookup"><span data-stu-id="4567b-2569">Consumption</span></span>

* <span data-ttu-id="4567b-2570">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2570">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="4567b-2571">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2571">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2572">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2572">Container</span></span>

* <span data-ttu-id="4567b-2573">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2573">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2574">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2574">Network</span></span>

* <span data-ttu-id="4567b-2575">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="4567b-2575">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2576">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2576">Resource</span></span>

* <span data-ttu-id="4567b-2577">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2577">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="4567b-2578">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-2578">Role</span></span>

* <span data-ttu-id="4567b-2579">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2579">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2580">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2580">SQL</span></span>

* <span data-ttu-id="4567b-2581">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2581">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2582">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2582">Storage</span></span>

* <span data-ttu-id="4567b-2583">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2583">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2584">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2584">VM</span></span>

* <span data-ttu-id="4567b-2585">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2585">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="4567b-2586">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2586">February 13, 2018</span></span>

<span data-ttu-id="4567b-2587">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="4567b-2587">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2588">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2588">Core</span></span>

* <span data-ttu-id="4567b-2589">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2589">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2590">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2590">ACS</span></span>

* <span data-ttu-id="4567b-2591">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2591">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="4567b-2592">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2592">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="4567b-2593">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2593">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="4567b-2594">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2594">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="4567b-2595">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2595">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="4567b-2596">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2596">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="4567b-2597">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2597">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="4567b-2598">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="4567b-2598">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2599">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2599">Appservice</span></span>

* <span data-ttu-id="4567b-2600">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2600">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="4567b-2601">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2601">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="4567b-2602">CDN</span><span class="sxs-lookup"><span data-stu-id="4567b-2602">CDN</span></span>

* <span data-ttu-id="4567b-2603">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2603">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2604">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2604">Container</span></span>

* <span data-ttu-id="4567b-2605">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2605">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="4567b-2606">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2606">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-2607">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-2607">CosmosDB</span></span>

* <span data-ttu-id="4567b-2608">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2608">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="4567b-2609">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-2609">Extension</span></span>

* <span data-ttu-id="4567b-2610">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2610">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="4567b-2611">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2611">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="4567b-2612">フィードバック</span><span class="sxs-lookup"><span data-stu-id="4567b-2612">Feedback</span></span>

* <span data-ttu-id="4567b-2613">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2613">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-2614">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-2614">Interactive</span></span>

* <span data-ttu-id="4567b-2615">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2615">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="4567b-2616">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2616">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-2617">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-2617">IoT</span></span>

* <span data-ttu-id="4567b-2618">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2618">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="4567b-2619">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2619">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="4567b-2620">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2620">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="4567b-2621">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2621">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-2622">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-2622">Monitor</span></span>

* <span data-ttu-id="4567b-2623">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2623">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2624">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2624">Network</span></span>

* <span data-ttu-id="4567b-2625">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2625">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="4567b-2626">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-2626">Profile</span></span>

* <span data-ttu-id="4567b-2627">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2627">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2628">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2628">Resource</span></span>

* <span data-ttu-id="4567b-2629">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2629">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="4567b-2630">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-2630">Role</span></span>

* <span data-ttu-id="4567b-2631">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2631">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2632">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2632">SQL</span></span>

* <span data-ttu-id="4567b-2633">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2633">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="4567b-2634">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2634">Added `sql db rename`</span></span>
* <span data-ttu-id="4567b-2635">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2635">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2636">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2636">Storage</span></span>

* <span data-ttu-id="4567b-2637">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2637">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2638">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2638">VM</span></span>

* <span data-ttu-id="4567b-2639">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2639">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="4567b-2640">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2640">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="4567b-2641">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="4567b-2641">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="4567b-2642">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2642">January 31, 2018</span></span>

<span data-ttu-id="4567b-2643">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="4567b-2643">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2644">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2644">Core</span></span>

* <span data-ttu-id="4567b-2645">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2645">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="4567b-2646">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2646">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="4567b-2647">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2647">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="4567b-2648">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-2648">Use `--verbose` to see</span></span>
* <span data-ttu-id="4567b-2649">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-2649">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2650">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2650">ACS</span></span>

* <span data-ttu-id="4567b-2651">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2651">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="4567b-2652">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2652">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2653">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2653">Appservice</span></span>

* <span data-ttu-id="4567b-2654">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="4567b-2654">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="4567b-2655">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2655">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="4567b-2656">CDN</span><span class="sxs-lookup"><span data-stu-id="4567b-2656">CDN</span></span>

* <span data-ttu-id="4567b-2657">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2657">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-2658">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-2658">CosmosDB</span></span>

* <span data-ttu-id="4567b-2659">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2659">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-2660">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-2660">Interactive</span></span>

* <span data-ttu-id="4567b-2661">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2661">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2662">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2662">Network</span></span>

* <span data-ttu-id="4567b-2663">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2663">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="4567b-2664">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2664">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="4567b-2665">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2665">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="4567b-2666">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2666">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="4567b-2667">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2667">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="4567b-2668">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2668">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="4567b-2669">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2669">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="4567b-2670">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2670">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="4567b-2671">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2671">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="4567b-2672">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2672">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-2673">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-2673">Profile</span></span>

* <span data-ttu-id="4567b-2674">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2674">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2675">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2675">Resource</span></span>

* <span data-ttu-id="4567b-2676">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2676">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2677">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2677">Storage</span></span>

* <span data-ttu-id="4567b-2678">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2678">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="4567b-2679">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2679">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="4567b-2680">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2680">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="4567b-2681">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2681">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="4567b-2682">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2682">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2683">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2683">VM</span></span>

* <span data-ttu-id="4567b-2684">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2684">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="4567b-2685">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2685">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="4567b-2686">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2686">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="4567b-2687">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2687">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="4567b-2688">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2688">January 17, 2018</span></span>

<span data-ttu-id="4567b-2689">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="4567b-2689">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-2690">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-2690">ACR</span></span>

* <span data-ttu-id="4567b-2691">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2691">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="4567b-2692">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2692">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2693">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2693">ACS</span></span>

* <span data-ttu-id="4567b-2694">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2694">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="4567b-2695">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2695">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2696">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2696">Appservice</span></span>

* <span data-ttu-id="4567b-2697">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2697">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="4567b-2698">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2698">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="4567b-2699">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2699">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-2700">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-2700">Backup</span></span>

* <span data-ttu-id="4567b-2701">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2701">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="4567b-2702">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2702">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="4567b-2703">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2703">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="4567b-2704">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2704">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="4567b-2705">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2705">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-2706">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-2706">Batch</span></span>

* <span data-ttu-id="4567b-2707">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2707">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="4567b-2708">クラウド</span><span class="sxs-lookup"><span data-stu-id="4567b-2708">Cloud</span></span>

* <span data-ttu-id="4567b-2709">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2709">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="4567b-2710">従量課金</span><span class="sxs-lookup"><span data-stu-id="4567b-2710">Consumption</span></span>

* <span data-ttu-id="4567b-2711">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2711">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="4567b-2712">Event Grid</span><span class="sxs-lookup"><span data-stu-id="4567b-2712">Event Grid</span></span>

* <span data-ttu-id="4567b-2713">[重大な変更]`az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2713">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="4567b-2714">[重大な変更]`az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2714">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="4567b-2715">[重大な変更]`eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2715">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="4567b-2716">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="4567b-2716">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="4567b-2717">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2717">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="4567b-2718">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2718">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="4567b-2719">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2719">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="4567b-2720">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2720">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-2721">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-2721">Interactive</span></span>

* <span data-ttu-id="4567b-2722">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2722">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="4567b-2723">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2723">Fixed errors on startup</span></span>
* <span data-ttu-id="4567b-2724">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2724">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-2725">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-2725">IoT</span></span>

* <span data-ttu-id="4567b-2726">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2726">Added support for device provisioning service</span></span>
* <span data-ttu-id="4567b-2727">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2727">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="4567b-2728">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2728">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-2729">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-2729">Monitor</span></span>

* <span data-ttu-id="4567b-2730">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2730">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="4567b-2731">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="4567b-2731">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="4567b-2732">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2732">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2733">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2733">Network</span></span>

* <span data-ttu-id="4567b-2734">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2734">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="4567b-2735">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2735">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-2736">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-2736">Profile</span></span>

* <span data-ttu-id="4567b-2737">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2737">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="4567b-2738">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-2738">Role</span></span>

* <span data-ttu-id="4567b-2739">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2739">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="4567b-2740">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4567b-2740">Service Fabric</span></span>

* <span data-ttu-id="4567b-2741">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2741">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="4567b-2742">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2742">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2743">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2743">VM</span></span>

* <span data-ttu-id="4567b-2744">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-2744">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="4567b-2745">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2745">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="4567b-2746">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2746">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="4567b-2747">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2747">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="4567b-2748">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2748">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="4567b-2749">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2749">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="4567b-2750">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2750">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="4567b-2751">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2751">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="4567b-2752">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2752">December 19, 2017</span></span>

<span data-ttu-id="4567b-2753">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="4567b-2753">Version 2.0.23</span></span>

* <span data-ttu-id="4567b-2754">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2754">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2755">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2755">Container</span></span>

* <span data-ttu-id="4567b-2756">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2756">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2757">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2757">Network</span></span>

* <span data-ttu-id="4567b-2758">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2758">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="4567b-2759">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2759">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2760">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2760">Storage</span></span>

* <span data-ttu-id="4567b-2761">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2761">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2762">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2762">VM</span></span>

* <span data-ttu-id="4567b-2763">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2763">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="4567b-2764">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2764">December 5, 2017</span></span>

<span data-ttu-id="4567b-2765">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="4567b-2765">Version 2.0.22</span></span>

* <span data-ttu-id="4567b-2766">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2766">Removed `az component` commands.</span></span> <span data-ttu-id="4567b-2767">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="4567b-2767">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2768">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2768">Core</span></span>
* <span data-ttu-id="4567b-2769">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2769">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="4567b-2770">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2770">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2771">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2771">ACS</span></span>

* <span data-ttu-id="4567b-2772">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2772">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="4567b-2773">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2773">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="4567b-2774">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2774">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="4567b-2775">Advisor</span><span class="sxs-lookup"><span data-stu-id="4567b-2775">Advisor</span></span>

* <span data-ttu-id="4567b-2776">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-2776">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2777">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2777">Appservice</span></span>

* <span data-ttu-id="4567b-2778">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2778">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="4567b-2779">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2779">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="4567b-2780">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2780">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="4567b-2781">従量課金</span><span class="sxs-lookup"><span data-stu-id="4567b-2781">Consumption</span></span>

* <span data-ttu-id="4567b-2782">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2782">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2783">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2783">Container</span></span>

* <span data-ttu-id="4567b-2784">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2784">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-2785">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-2785">Monitor</span></span>

* <span data-ttu-id="4567b-2786">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2786">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2787">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2787">Resource</span></span>

* <span data-ttu-id="4567b-2788">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2788">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="4567b-2789">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-2789">Role</span></span>

* <span data-ttu-id="4567b-2790">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2790">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="4567b-2791">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2791">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="4567b-2792">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2792">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2793">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2793">SQL</span></span>

* <span data-ttu-id="4567b-2794">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2794">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="4567b-2795">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2795">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2796">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2796">VM</span></span>

* <span data-ttu-id="4567b-2797">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2797">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="4567b-2798">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2798">November 14, 2017</span></span>

<span data-ttu-id="4567b-2799">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="4567b-2799">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-2800">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-2800">ACR</span></span>

* <span data-ttu-id="4567b-2801">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2801">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="4567b-2802">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2802">ACS</span></span>

* <span data-ttu-id="4567b-2803">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2803">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="4567b-2804">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2804">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="4567b-2805">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2805">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="4567b-2806">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2806">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="4567b-2807">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2807">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2808">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2808">Appservice</span></span>

* <span data-ttu-id="4567b-2809">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2809">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="4567b-2810">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2810">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="4567b-2811">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2811">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="4567b-2812">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2812">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="4567b-2813">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2813">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="4567b-2814">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="4567b-2814">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-2815">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-2815">Batch</span></span>

* <span data-ttu-id="4567b-2816">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2816">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="4567b-2817">Batchai</span><span class="sxs-lookup"><span data-stu-id="4567b-2817">Batchai</span></span>

* <span data-ttu-id="4567b-2818">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2818">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="4567b-2819">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2819">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="4567b-2820">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2820">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="4567b-2821">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2821">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="4567b-2822">クラウド</span><span class="sxs-lookup"><span data-stu-id="4567b-2822">Cloud</span></span>

* <span data-ttu-id="4567b-2823">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2823">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="4567b-2824">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-2824">Container</span></span>

* <span data-ttu-id="4567b-2825">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2825">Added support to open multiple ports</span></span>
* <span data-ttu-id="4567b-2826">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2826">Added container group restart policy</span></span>
* <span data-ttu-id="4567b-2827">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2827">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="4567b-2828">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2828">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="4567b-2829">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="4567b-2829">Data Lake Analytics</span></span>

* <span data-ttu-id="4567b-2830">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2830">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="4567b-2831">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4567b-2831">Data Lake Store</span></span>

* <span data-ttu-id="4567b-2832">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2832">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="4567b-2833">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-2833">Extension</span></span>

* <span data-ttu-id="4567b-2834">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2834">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="4567b-2835">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2835">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-2836">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-2836">IoT</span></span>

* <span data-ttu-id="4567b-2837">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2837">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-2838">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-2838">Monitor</span></span>

* <span data-ttu-id="4567b-2839">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2839">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2840">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2840">Network</span></span>

* <span data-ttu-id="4567b-2841">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2841">Added support for CAA DNS records</span></span>
* <span data-ttu-id="4567b-2842">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2842">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="4567b-2843">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2843">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="4567b-2844">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2844">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="4567b-2845">Reservations</span><span class="sxs-lookup"><span data-stu-id="4567b-2845">Reservations</span></span>

* <span data-ttu-id="4567b-2846">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="4567b-2846">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2847">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2847">Resource</span></span>

* <span data-ttu-id="4567b-2848">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2848">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2849">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2849">SQL</span></span>

* <span data-ttu-id="4567b-2850">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2850">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2851">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2851">Storage</span></span>

* <span data-ttu-id="4567b-2852">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2852">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="4567b-2853">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2853">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="4567b-2854">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2854">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="4567b-2855">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2855">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="4567b-2856">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2856">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="4567b-2857">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2857">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="4567b-2858">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2858">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2859">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2859">VM</span></span>

* <span data-ttu-id="4567b-2860">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2860">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="4567b-2861">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2861">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="4567b-2862">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2862">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="4567b-2863">`vm format-secret` から `vm secret format` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-2863">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="4567b-2864">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2864">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="4567b-2865">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2865">October 24, 2017</span></span>

<span data-ttu-id="4567b-2866">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="4567b-2866">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2867">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2867">Core</span></span>

* <span data-ttu-id="4567b-2868">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2868">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-2869">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-2869">ACR</span></span>

* <span data-ttu-id="4567b-2870">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2870">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="4567b-2871">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2871">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="4567b-2872">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2872">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2873">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2873">ACS</span></span>

* <span data-ttu-id="4567b-2874">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2874">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="4567b-2875">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2875">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2876">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2876">Appservice</span></span>

* <span data-ttu-id="4567b-2877">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2877">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="4567b-2878">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="4567b-2878">Component</span></span>

* <span data-ttu-id="4567b-2879">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2879">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-2880">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-2880">Monitor</span></span>

* <span data-ttu-id="4567b-2881">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2881">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2882">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2882">Resource</span></span>

* <span data-ttu-id="4567b-2883">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2883">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="4567b-2884">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2884">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2885">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2885">VM</span></span>

* <span data-ttu-id="4567b-2886">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2886">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="4567b-2887">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2887">October 9, 2017</span></span>

<span data-ttu-id="4567b-2888">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="4567b-2888">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2889">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2889">Core</span></span>

* <span data-ttu-id="4567b-2890">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2890">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2891">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2891">Appservice</span></span>

* <span data-ttu-id="4567b-2892">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2892">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-2893">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-2893">Batch</span></span>

* <span data-ttu-id="4567b-2894">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2894">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="4567b-2895">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2895">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="4567b-2896">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2896">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="4567b-2897">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2897">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="4567b-2898">Batchai</span><span class="sxs-lookup"><span data-stu-id="4567b-2898">Batchai</span></span>

* <span data-ttu-id="4567b-2899">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-2899">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-2900">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-2900">Keyvault</span></span>

* <span data-ttu-id="4567b-2901">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2901">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="4567b-2902">(#4448)</span><span class="sxs-lookup"><span data-stu-id="4567b-2902">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="4567b-2903">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2903">Network</span></span>

* <span data-ttu-id="4567b-2904">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2904">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="4567b-2905">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2905">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2906">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2906">Resource</span></span>

* <span data-ttu-id="4567b-2907">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2907">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="4567b-2908">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2908">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="4567b-2909">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2909">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="4567b-2910">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2910">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2911">Sql</span><span class="sxs-lookup"><span data-stu-id="4567b-2911">Sql</span></span>

* <span data-ttu-id="4567b-2912">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2912">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="4567b-2913">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2913">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="4567b-2914">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2914">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2915">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2915">Storage</span></span>

* <span data-ttu-id="4567b-2916">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2916">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2917">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2917">Vm</span></span>

* <span data-ttu-id="4567b-2918">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2918">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="4567b-2919">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2919">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="4567b-2920">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2920">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="4567b-2921">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2921">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="4567b-2922">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2922">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="4567b-2923">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2923">September 22, 2017</span></span>

<span data-ttu-id="4567b-2924">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="4567b-2924">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2925">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2925">Resource</span></span>

* <span data-ttu-id="4567b-2926">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2926">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="4567b-2927">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2927">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="4567b-2928">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2928">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="4567b-2929">[重大な変更]`managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2929">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2930">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2930">Network</span></span>

* <span data-ttu-id="4567b-2931">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2931">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="4567b-2932">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2932">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="4567b-2933">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2933">Added `asg` application security group commands</span></span>
* <span data-ttu-id="4567b-2934">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2934">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="4567b-2935">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2935">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="4567b-2936">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2936">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="4567b-2937">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2937">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-2938">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-2938">Storage</span></span>

* <span data-ttu-id="4567b-2939">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2939">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="4567b-2940">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="4567b-2940">Eventgrid</span></span>

* <span data-ttu-id="4567b-2941">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2941">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2942">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2942">SQL</span></span>

* <span data-ttu-id="4567b-2943">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-2943">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="4567b-2944">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="4567b-2944">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="4567b-2945">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2945">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-2946">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-2946">Keyvault</span></span>

* <span data-ttu-id="4567b-2947">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2947">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2948">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2948">VM</span></span>

* <span data-ttu-id="4567b-2949">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2949">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="4567b-2950">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2950">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="4567b-2951">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2951">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="4567b-2952">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2952">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="4567b-2953">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2953">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="4567b-2954">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2954">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2955">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2955">ACS</span></span>

* <span data-ttu-id="4567b-2956">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2956">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2957">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2957">Appservice</span></span>

* <span data-ttu-id="4567b-2958">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2958">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="4567b-2959">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4567b-2959">Backup</span></span>

* <span data-ttu-id="4567b-2960">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="4567b-2960">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="4567b-2961">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2961">September 11, 2017</span></span>

<span data-ttu-id="4567b-2962">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="4567b-2962">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="4567b-2963">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-2963">Core</span></span>

* <span data-ttu-id="4567b-2964">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2964">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="4567b-2965">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2965">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-2966">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-2966">Acs</span></span>

* <span data-ttu-id="4567b-2967">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2967">Added `acs list-locations` command</span></span>
* <span data-ttu-id="4567b-2968">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2968">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-2969">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-2969">Appservice</span></span>

* <span data-ttu-id="4567b-2970">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2970">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="4567b-2971">CDN</span><span class="sxs-lookup"><span data-stu-id="4567b-2971">CDN</span></span>

* <span data-ttu-id="4567b-2972">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2972">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="4567b-2973">拡張機能</span><span class="sxs-lookup"><span data-stu-id="4567b-2973">Extension</span></span>

* <span data-ttu-id="4567b-2974">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-2974">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-2975">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-2975">Keyvault</span></span>

* <span data-ttu-id="4567b-2976">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2976">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-2977">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-2977">Network</span></span>

* <span data-ttu-id="4567b-2978">`vnet list-private-access-services` から `vnet list-endpoint-services` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-2978">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="4567b-2979">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2979">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="4567b-2980">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2980">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="4567b-2981">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2981">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="4567b-2982">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2982">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-2983">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-2983">Resource</span></span>

* <span data-ttu-id="4567b-2984">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="4567b-2984">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="4567b-2985">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="4567b-2985">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="4567b-2986">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="4567b-2986">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="4567b-2987">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="4567b-2987">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-2988">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-2988">SQL</span></span>

* <span data-ttu-id="4567b-2989">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2989">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-2990">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-2990">VM</span></span>

* <span data-ttu-id="4567b-2991">固定:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="4567b-2991">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="4567b-2992">固定:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="4567b-2992">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="4567b-2993">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2993">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="4567b-2994">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="4567b-2994">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="4567b-2995">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="4567b-2995">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="4567b-2996">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4567b-2996">August 31, 2017</span></span>

<span data-ttu-id="4567b-2997">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="4567b-2997">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-2998">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-2998">Keyvault</span></span>

* <span data-ttu-id="4567b-2999">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-2999">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="4567b-3000">SF</span><span class="sxs-lookup"><span data-stu-id="4567b-3000">Sf</span></span>

* <span data-ttu-id="4567b-3001">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="4567b-3001">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-3002">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-3002">Storage</span></span>

* <span data-ttu-id="4567b-3003">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3003">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="4567b-3004">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="4567b-3004">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="4567b-3005">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="4567b-3005">August 28, 2017</span></span>

<span data-ttu-id="4567b-3006">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="4567b-3006">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="4567b-3007">CLI</span><span class="sxs-lookup"><span data-stu-id="4567b-3007">CLI</span></span>

* <span data-ttu-id="4567b-3008">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3008">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-3009">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-3009">ACS</span></span>

* <span data-ttu-id="4567b-3010">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3010">Corrected preview regions</span></span>
* <span data-ttu-id="4567b-3011">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-3011">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="4567b-3012">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3012">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-3013">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-3013">Appservice</span></span>

* <span data-ttu-id="4567b-3014">[重大な変更]`az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3014">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="4567b-3015">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3015">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="4567b-3016">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3016">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="4567b-3017">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3017">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="4567b-3018">固定:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="4567b-3018">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-3019">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-3019">IoT</span></span>

* <span data-ttu-id="4567b-3020">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3020">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="4567b-3021">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-3021">Network</span></span>

* <span data-ttu-id="4567b-3022">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3022">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="4567b-3023">[重大な変更]`vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3023">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="4567b-3024">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3024">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="4567b-3025">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3025">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="4567b-3026">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3026">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-3027">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-3027">Profile</span></span>

* <span data-ttu-id="4567b-3028">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3028">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="4567b-3029">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4567b-3029">Service Fabric</span></span>

* <span data-ttu-id="4567b-3030">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="4567b-3030">Preview release</span></span>
* <span data-ttu-id="4567b-3031">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3031">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="4567b-3032">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3032">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="4567b-3033">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3033">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-3034">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-3034">Storage</span></span>

* <span data-ttu-id="4567b-3035">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-3035">Enabled setting blob tier</span></span>
* <span data-ttu-id="4567b-3036">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3036">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="4567b-3037">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3037">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="4567b-3038">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-3038">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="4567b-3039">[重大な変更]`az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3039">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="4567b-3040">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="4567b-3040">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-3041">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-3041">VM</span></span>

* <span data-ttu-id="4567b-3042">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3042">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="4567b-3043">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-3043">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="4567b-3044">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3044">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="4567b-3045">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3045">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="4567b-3046">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3046">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="4567b-3047">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3047">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="4567b-3048">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="4567b-3048">August 15, 2017</span></span>

<span data-ttu-id="4567b-3049">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="4567b-3049">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-3050">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-3050">ACS</span></span>

* <span data-ttu-id="4567b-3051">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3051">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-3052">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-3052">Appservice</span></span>

* <span data-ttu-id="4567b-3053">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3053">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="4567b-3054">Event Grid</span><span class="sxs-lookup"><span data-stu-id="4567b-3054">Event Grid</span></span>

* <span data-ttu-id="4567b-3055">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3055">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="4567b-3056">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="4567b-3056">August 11, 2017</span></span>

<span data-ttu-id="4567b-3057">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="4567b-3057">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-3058">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-3058">ACS</span></span>

* <span data-ttu-id="4567b-3059">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3059">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-3060">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-3060">Batch</span></span>

* <span data-ttu-id="4567b-3061">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3061">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="4567b-3062">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3062">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="4567b-3063">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3063">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="4567b-3064">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3064">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="4567b-3065">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3065">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="4567b-3066">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3066">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="4567b-3067">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="4567b-3067">Component</span></span>

* <span data-ttu-id="4567b-3068">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3068">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="4567b-3069">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4567b-3069">Container</span></span>

* <span data-ttu-id="4567b-3070">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3070">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="4567b-3071">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4567b-3071">Data Lake Store</span></span>

* <span data-ttu-id="4567b-3072">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-3072">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="4567b-3073">Event Grid</span><span class="sxs-lookup"><span data-stu-id="4567b-3073">Event Grid</span></span>

* <span data-ttu-id="4567b-3074">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-3074">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="4567b-3075">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-3075">Network</span></span>

* <span data-ttu-id="4567b-3076">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3076">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="4567b-3077">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3077">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="4567b-3078">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3078">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="4567b-3079">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3079">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-3080">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-3080">Profile</span></span>

* <span data-ttu-id="4567b-3081">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3081">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-3082">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-3082">Storage</span></span>

* <span data-ttu-id="4567b-3083">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="4567b-3083">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-3084">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-3084">VM</span></span>

* <span data-ttu-id="4567b-3085">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3085">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="4567b-3086">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3086">Exposed `list-skus` command</span></span>
* <span data-ttu-id="4567b-3087">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3087">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="4567b-3088">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="4567b-3088">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="4567b-3089">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3089">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="4567b-3090">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="4567b-3090">July 28, 2017</span></span>

<span data-ttu-id="4567b-3091">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="4567b-3091">Version 2.0.12</span></span>

* <span data-ttu-id="4567b-3092">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3092">Added container commands</span></span>
* <span data-ttu-id="4567b-3093">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3093">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="4567b-3094">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-3094">Core</span></span>

* <span data-ttu-id="4567b-3095">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="4567b-3095">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="4567b-3096">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3096">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="4567b-3097">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="4567b-3097">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="4567b-3098">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="4567b-3098">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="4567b-3099">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="4567b-3099">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="4567b-3100">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="4567b-3100">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="4567b-3101">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="4567b-3101">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="4567b-3102">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="4567b-3102">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="4567b-3103">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="4567b-3103">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="4567b-3104">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="4567b-3104">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="4567b-3105">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="4567b-3105">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="4567b-3106">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="4567b-3106">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="4567b-3107">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3107">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="4567b-3108">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3108">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="4567b-3109">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3109">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="4567b-3110">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="4567b-3110">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="4567b-3111">ACR</span><span class="sxs-lookup"><span data-stu-id="4567b-3111">ACR</span></span>

* <span data-ttu-id="4567b-3112">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3112">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="4567b-3113">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3113">Support SKU update for managed registries</span></span>
* <span data-ttu-id="4567b-3114">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3114">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="4567b-3115">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3115">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="4567b-3116">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3116">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="4567b-3117">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3117">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-3118">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-3118">ACS</span></span>

* <span data-ttu-id="4567b-3119">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3119">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-3120">Appservice</span><span class="sxs-lookup"><span data-stu-id="4567b-3120">Appservice</span></span>

* <span data-ttu-id="4567b-3121">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3121">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="4567b-3122">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3122">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="4567b-3123">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="4567b-3123">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="4567b-3124">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="4567b-3124">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="4567b-3125">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="4567b-3125">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="4567b-3126">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="4567b-3126">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="4567b-3127">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="4567b-3127">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="4567b-3128">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="4567b-3128">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="4567b-3129">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-3129">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="4567b-3130">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="4567b-3130">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="4567b-3131">Batch</span><span class="sxs-lookup"><span data-stu-id="4567b-3131">Batch</span></span>

* <span data-ttu-id="4567b-3132">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="4567b-3132">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="4567b-3133">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3133">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="4567b-3134">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3134">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="4567b-3135">CDN</span><span class="sxs-lookup"><span data-stu-id="4567b-3135">CDN</span></span>

* <span data-ttu-id="4567b-3136">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3136">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="4567b-3137">クラウド</span><span class="sxs-lookup"><span data-stu-id="4567b-3137">Cloud</span></span>

* <span data-ttu-id="4567b-3138">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3138">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="4567b-3139">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="4567b-3139">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="4567b-3140">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3140">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="4567b-3141">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3141">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="4567b-3142">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3142">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-3143">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-3143">CosmosDB</span></span>

* <span data-ttu-id="4567b-3144">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3144">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="4567b-3145">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3145">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="4567b-3146">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="4567b-3146">Data Lake Analytics</span></span>

* <span data-ttu-id="4567b-3147">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3147">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="4567b-3148">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3148">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="4567b-3149">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3149">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="4567b-3150">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4567b-3150">Data Lake Store</span></span>

* <span data-ttu-id="4567b-3151">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3151">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="4567b-3152">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3152">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="4567b-3153">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-3153">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="4567b-3154">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="4567b-3154">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="4567b-3155">Interactive</span><span class="sxs-lookup"><span data-stu-id="4567b-3155">Interactive</span></span>

* <span data-ttu-id="4567b-3156">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3156">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="4567b-3157">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="4567b-3157">Increased test coverage</span></span>
* <span data-ttu-id="4567b-3158">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3158">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="4567b-3159">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="4567b-3159">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="4567b-3160">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="4567b-3160">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="4567b-3161">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="4567b-3161">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="4567b-3162">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="4567b-3162">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="4567b-3163">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3163">Added `--progress` flag</span></span>
* <span data-ttu-id="4567b-3164">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3164">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="4567b-3165">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="4567b-3165">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="4567b-3166">IoT</span><span class="sxs-lookup"><span data-stu-id="4567b-3166">IoT</span></span>

* <span data-ttu-id="4567b-3167">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-3167">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="4567b-3168">(#3934)</span><span class="sxs-lookup"><span data-stu-id="4567b-3168">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="4567b-3169">Key Vault</span><span class="sxs-lookup"><span data-stu-id="4567b-3169">Key vault</span></span>

* <span data-ttu-id="4567b-3170">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-3170">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="4567b-3171">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4567b-3171">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="4567b-3172">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4567b-3172">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="4567b-3173">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4567b-3173">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="4567b-3174">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4567b-3174">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="4567b-3175">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="4567b-3175">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="4567b-3176">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-3176">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="4567b-3177">(#3307)</span><span class="sxs-lookup"><span data-stu-id="4567b-3177">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="4567b-3178">ラボ</span><span class="sxs-lookup"><span data-stu-id="4567b-3178">Lab</span></span>

* <span data-ttu-id="4567b-3179">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3179">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="4567b-3180">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3180">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-3181">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-3181">Monitor</span></span>

* <span data-ttu-id="4567b-3182">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="4567b-3182">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="4567b-3183">`monitor alert-rule-incidents list` から `monitor alert list-incidents` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-3183">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="4567b-3184">`monitor alert-rule-incidents show` から `monitor alert show-incident` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-3184">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="4567b-3185">`monitor metric-defintions list` から `monitor metrics list-definitions` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-3185">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="4567b-3186">`monitor alert-rules` から `monitor alert` への名称変更</span><span class="sxs-lookup"><span data-stu-id="4567b-3186">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="4567b-3187">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="4567b-3187">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="4567b-3188">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3188">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="4567b-3189">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-3189">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="4567b-3190">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3190">`location` no longer required</span></span>
  * <span data-ttu-id="4567b-3191">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-3191">Add name and ID support for target</span></span>
  * <span data-ttu-id="4567b-3192">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="4567b-3192">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="4567b-3193">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-3193">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="4567b-3194">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3194">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="4567b-3195">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="4567b-3195">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="4567b-3196">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3196">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="4567b-3197">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3197">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="4567b-3198">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-3198">Network</span></span>

* <span data-ttu-id="4567b-3199">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3199">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="4567b-3200">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3200">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="4567b-3201">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3201">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="4567b-3202">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3202">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="4567b-3203">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3203">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="4567b-3204">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3204">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="4567b-3205">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3205">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="4567b-3206">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3206">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="4567b-3207">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3207">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="4567b-3208">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3208">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="4567b-3209">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3209">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="4567b-3210">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3210">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="4567b-3211">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3211">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="4567b-3212">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3212">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="4567b-3213">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3213">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="4567b-3214">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3214">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="4567b-3215">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3215">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="4567b-3216">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3216">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="4567b-3217">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3217">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="4567b-3218">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3218">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="4567b-3219">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3219">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="4567b-3220">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3220">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="4567b-3221">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3221">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="4567b-3222">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="4567b-3222">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="4567b-3223">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="4567b-3223">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="4567b-3224">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="4567b-3224">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="4567b-3225">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="4567b-3225">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-3226">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-3226">Profile</span></span>

* <span data-ttu-id="4567b-3227">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3227">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="4567b-3228">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3228">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="4567b-3229">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="4567b-3229">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="4567b-3230">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3230">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="4567b-3231">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3231">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="4567b-3232">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4567b-3232">RDBMS</span></span>

* <span data-ttu-id="4567b-3233">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="4567b-3233">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="4567b-3234">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="4567b-3234">Fixed `%s` not processed because of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="4567b-3235">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="4567b-3235">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="4567b-3236">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="4567b-3236">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-3237">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-3237">Resource</span></span>

* <span data-ttu-id="4567b-3238">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3238">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="4567b-3239">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3239">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="4567b-3240">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3240">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="4567b-3241">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3241">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="4567b-3242">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="4567b-3242">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="4567b-3243">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3243">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="4567b-3244">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="4567b-3244">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="4567b-3245">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3245">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="4567b-3246">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-3246">Role</span></span>

* <span data-ttu-id="4567b-3247">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3247">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="4567b-3248">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="4567b-3248">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="4567b-3249">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="4567b-3249">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="4567b-3250">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="4567b-3250">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="4567b-3251">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3251">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="4567b-3252">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4567b-3252">Service Fabric</span></span>
* <span data-ttu-id="4567b-3253">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="4567b-3253">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="4567b-3254">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="4567b-3254">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="4567b-3255">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="4567b-3255">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-3256">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-3256">SQL</span></span>

* <span data-ttu-id="4567b-3257">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3257">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="4567b-3258">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3258">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="4567b-3259">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3259">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-3260">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-3260">Storage</span></span>

* <span data-ttu-id="4567b-3261">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="4567b-3261">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="4567b-3262">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-3262">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="4567b-3263">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="4567b-3263">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="4567b-3264">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="4567b-3264">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="4567b-3265">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="4567b-3265">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="4567b-3266">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="4567b-3266">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-3267">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-3267">VM</span></span>

* <span data-ttu-id="4567b-3268">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3268">Support configuring nsg</span></span>
* <span data-ttu-id="4567b-3269">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3269">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="4567b-3270">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="4567b-3270">Support managed service identities</span></span>
* <span data-ttu-id="4567b-3271">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3271">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="4567b-3272">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="4567b-3272">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="4567b-3273">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="4567b-3273">May 10, 2017</span></span>

<span data-ttu-id="4567b-3274">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="4567b-3274">Version 2.0.6</span></span>

* <span data-ttu-id="4567b-3275">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3275">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="4567b-3276">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3276">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="4567b-3277">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3277">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="4567b-3278">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3278">Include Cognitive Services module</span></span>
* <span data-ttu-id="4567b-3279">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3279">Include Service Fabric module</span></span>
* <span data-ttu-id="4567b-3280">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="4567b-3280">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="4567b-3281">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3281">Add support for CDN commands</span></span>
* <span data-ttu-id="4567b-3282">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3282">Remove Container module</span></span>
* <span data-ttu-id="4567b-3283">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="4567b-3283">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="4567b-3284">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="4567b-3284">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="4567b-3285">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-3285">Core</span></span>

* <span data-ttu-id="4567b-3286">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="4567b-3286">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="4567b-3287">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="4567b-3287">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="4567b-3288">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="4567b-3288">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="4567b-3289">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="4567b-3289">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="4567b-3290">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="4567b-3290">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="4567b-3291">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="4567b-3291">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="4567b-3292">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="4567b-3292">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="4567b-3293">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="4567b-3293">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="4567b-3294">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="4567b-3294">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="4567b-3295">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="4567b-3295">core: Improved performance</span></span>
* <span data-ttu-id="4567b-3296">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="4567b-3296">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="4567b-3297">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="4567b-3297">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-3298">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-3298">ACS</span></span>

* <span data-ttu-id="4567b-3299">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3299">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="4567b-3300">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3300">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="4567b-3301">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3301">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="4567b-3302">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="4567b-3302">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-3303">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-3303">AppService</span></span>

* <span data-ttu-id="4567b-3304">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3304">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="4567b-3305">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3305">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="4567b-3306">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="4567b-3306">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="4567b-3307">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3307">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="4567b-3308">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3308">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="4567b-3309">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="4567b-3309">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="4567b-3310">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="4567b-3310">support slot swap with preview</span></span>
* <span data-ttu-id="4567b-3311">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="4567b-3311">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="4567b-3312">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="4567b-3312">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4567b-3313">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4567b-3313">CosmosDB</span></span>

* <span data-ttu-id="4567b-3314">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3314">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="4567b-3315">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3315">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="4567b-3316">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3316">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="4567b-3317">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3317">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="4567b-3318">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="4567b-3318">Data Lake Analytics</span></span>

* <span data-ttu-id="4567b-3319">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3319">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="4567b-3320">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="4567b-3320">Add support for new catalog item type: package.</span></span> <span data-ttu-id="4567b-3321">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="4567b-3321">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="4567b-3322">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="4567b-3322">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="4567b-3323">テーブル</span><span class="sxs-lookup"><span data-stu-id="4567b-3323">Table</span></span>
  * <span data-ttu-id="4567b-3324">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="4567b-3324">Table valued function</span></span>
  * <span data-ttu-id="4567b-3325">表示</span><span class="sxs-lookup"><span data-stu-id="4567b-3325">View</span></span>
  * <span data-ttu-id="4567b-3326">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="4567b-3326">Table Statistics.</span></span> <span data-ttu-id="4567b-3327">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="4567b-3327">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="4567b-3328">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4567b-3328">Data Lake Store</span></span>

* <span data-ttu-id="4567b-3329">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3329">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="4567b-3330">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="4567b-3330">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="4567b-3331">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="4567b-3331">missed help for access show.</span></span> <span data-ttu-id="4567b-3332">追加しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3332">adding it.</span></span> <span data-ttu-id="4567b-3333">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="4567b-3333">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="4567b-3334">Find</span><span class="sxs-lookup"><span data-stu-id="4567b-3334">Find</span></span>

* <span data-ttu-id="4567b-3335">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="4567b-3335">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="4567b-3336">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4567b-3336">KeyVault</span></span>

* <span data-ttu-id="4567b-3337">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3337">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="4567b-3338">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3338">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="4567b-3339">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="4567b-3339">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="4567b-3340">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3340">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="4567b-3341">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="4567b-3341">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="4567b-3342">ラボ</span><span class="sxs-lookup"><span data-stu-id="4567b-3342">Lab</span></span>

* <span data-ttu-id="4567b-3343">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3343">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="4567b-3344">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3344">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="4567b-3345">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3345">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="4567b-3346">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3346">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="4567b-3347">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3347">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="4567b-3348">モニター</span><span class="sxs-lookup"><span data-stu-id="4567b-3348">Monitor</span></span>

* <span data-ttu-id="4567b-3349">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="4567b-3349">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="4567b-3350">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="4567b-3350">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="4567b-3351">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-3351">Network</span></span>

* <span data-ttu-id="4567b-3352">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3352">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="4567b-3353">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3353">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="4567b-3354">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3354">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="4567b-3355">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3355">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="4567b-3356">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3356">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="4567b-3357">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3357">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="4567b-3358">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3358">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="4567b-3359">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3359">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="4567b-3360">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3360">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="4567b-3361">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3361">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="4567b-3362">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3362">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="4567b-3363">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3363">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="4567b-3364">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3364">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="4567b-3365">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3365">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="4567b-3366">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4567b-3366">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="4567b-3367">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3367">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="4567b-3368">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4567b-3368">Profile</span></span>

* <span data-ttu-id="4567b-3369">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="4567b-3369">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="4567b-3370">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="4567b-3370">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="4567b-3371">Redis</span><span class="sxs-lookup"><span data-stu-id="4567b-3371">Redis</span></span>

* <span data-ttu-id="4567b-3372">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3372">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="4567b-3373">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3373">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="4567b-3374">リソース</span><span class="sxs-lookup"><span data-stu-id="4567b-3374">Resource</span></span>

* <span data-ttu-id="4567b-3375">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="4567b-3375">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="4567b-3376">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="4567b-3376">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="4567b-3377">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="4567b-3377">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="4567b-3378">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3378">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="4567b-3379">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="4567b-3379">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="4567b-3380">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3380">Add docs for az lock update.</span></span> <span data-ttu-id="4567b-3381">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="4567b-3381">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="4567b-3382">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="4567b-3382">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="4567b-3383">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="4567b-3383">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="4567b-3384">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="4567b-3384">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="4567b-3385">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="4567b-3385">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="4567b-3386">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="4567b-3386">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="4567b-3387">Role</span><span class="sxs-lookup"><span data-stu-id="4567b-3387">Role</span></span>

* <span data-ttu-id="4567b-3388">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="4567b-3388">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="4567b-3389">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="4567b-3389">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="4567b-3390">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="4567b-3390">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="4567b-3391">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="4567b-3391">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="4567b-3392">SQL</span><span class="sxs-lookup"><span data-stu-id="4567b-3392">SQL</span></span>

* <span data-ttu-id="4567b-3393">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4567b-3393">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="4567b-3394">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="4567b-3394">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="4567b-3395">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-3395">Storage</span></span>

* <span data-ttu-id="4567b-3396">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="4567b-3396">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="4567b-3397">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3397">Add support for incremental blob copy</span></span>
* <span data-ttu-id="4567b-3398">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3398">Add support for large block blob upload</span></span>
* <span data-ttu-id="4567b-3399">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="4567b-3399">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-3400">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-3400">VM</span></span>

* <span data-ttu-id="4567b-3401">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="4567b-3401">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="4567b-3402">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="4567b-3402">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="4567b-3403">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="4567b-3403">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="4567b-3404">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="4567b-3404">az vm/vmss disk</span></span>
  3. <span data-ttu-id="4567b-3405">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="4567b-3405">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="4567b-3406">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="4567b-3406">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="4567b-3407">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="4567b-3407">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="4567b-3408">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4567b-3408">April 3, 2017</span></span>

<span data-ttu-id="4567b-3409">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="4567b-3409">Version 2.0.2</span></span>

<span data-ttu-id="4567b-3410">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="4567b-3410">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="4567b-3411">コア</span><span class="sxs-lookup"><span data-stu-id="4567b-3411">Core</span></span>

* <span data-ttu-id="4567b-3412">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-3412">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="4567b-3413">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="4567b-3413">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="4567b-3414">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="4567b-3414">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="4567b-3415">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="4567b-3415">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="4567b-3416">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="4567b-3416">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="4567b-3417">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-3417">Add prompting for missing template parameters.</span></span> <span data-ttu-id="4567b-3418">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="4567b-3418">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="4567b-3419">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-3419">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="4567b-3420">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="4567b-3420">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="4567b-3421">ACS</span><span class="sxs-lookup"><span data-stu-id="4567b-3421">ACS</span></span>

* <span data-ttu-id="4567b-3422">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="4567b-3422">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="4567b-3423">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-3423">Add support for ssh key password prompting.</span></span> <span data-ttu-id="4567b-3424">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="4567b-3424">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="4567b-3425">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="4567b-3425">Add support for windows clusters.</span></span> <span data-ttu-id="4567b-3426">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="4567b-3426">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="4567b-3427">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="4567b-3427">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="4567b-3428">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="4567b-3428">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="4567b-3429">AppService</span><span class="sxs-lookup"><span data-stu-id="4567b-3429">AppService</span></span>

* <span data-ttu-id="4567b-3430">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="4567b-3430">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="4567b-3431">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="4567b-3431">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="4567b-3432">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="4567b-3432">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="4567b-3433">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="4567b-3433">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="4567b-3434">DataLake</span><span class="sxs-lookup"><span data-stu-id="4567b-3434">DataLake</span></span>

* <span data-ttu-id="4567b-3435">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-3435">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="4567b-3436">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4567b-3436">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="4567b-3437">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="4567b-3437">DocuemntDB</span></span>

* <span data-ttu-id="4567b-3438">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="4567b-3438">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="4567b-3439">VM</span><span class="sxs-lookup"><span data-stu-id="4567b-3439">VM</span></span>

* <span data-ttu-id="4567b-3440">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="4567b-3440">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="4567b-3441">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="4567b-3441">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="4567b-3442">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="4567b-3442">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="4567b-3443">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="4567b-3443">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="4567b-3444">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="4567b-3444">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="4567b-3445">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="4567b-3445">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="4567b-3446">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="4567b-3446">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="4567b-3447">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="4567b-3447">February 27, 2017</span></span>

<span data-ttu-id="4567b-3448">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="4567b-3448">Version 2.0.0</span></span>

<span data-ttu-id="4567b-3449">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="4567b-3449">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="4567b-3450">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="4567b-3450">Container Service (acs)</span></span>
- <span data-ttu-id="4567b-3451">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="4567b-3451">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="4567b-3452">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4567b-3452">Networking</span></span>
- <span data-ttu-id="4567b-3453">ストレージ</span><span class="sxs-lookup"><span data-stu-id="4567b-3453">Storage</span></span>

<span data-ttu-id="4567b-3454">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="4567b-3454">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="4567b-3455">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="4567b-3455">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="4567b-3456">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="4567b-3456">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="4567b-3457">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="4567b-3457">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="4567b-3458">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="4567b-3458">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="4567b-3459">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="4567b-3459">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="4567b-3460">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="4567b-3460">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="4567b-3461">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="4567b-3461">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="4567b-3462">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="4567b-3462">Provide feedback from the command line with the `az feedback` command</span></span>
