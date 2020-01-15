---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 01/13/2020
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 3ecb6fb41ee0ae60af58a02c934f2c295133f998
ms.sourcegitcommit: 18973ac471bbd12af2c8f8fa32a233b0abe5b020
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/13/2020
ms.locfileid: "75913721"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="f60c8-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="f60c8-103">Azure CLI release notes</span></span>

## <a name="january-13-2020"></a><span data-ttu-id="f60c8-104">2020 年 1 月 13 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-104">January 13, 2020</span></span>

<span data-ttu-id="f60c8-105">バージョン 2.0.80</span><span class="sxs-lookup"><span data-stu-id="f60c8-105">Version 2.0.80</span></span>

### <a name="compute"></a><span data-ttu-id="f60c8-106">Compute</span><span class="sxs-lookup"><span data-stu-id="f60c8-106">Compute</span></span>

* <span data-ttu-id="f60c8-107">disk update:--disk-encryption-set と --encryption-type を追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-107">disk update: Add --disk-encryption-set and --encryption-type</span></span>
* <span data-ttu-id="f60c8-108">snapshot create/update:--disk-encryption-set と --encryption-type を追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-108">snapshot create/update: Add --disk-encryption-set and --encryption-type</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-109">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-109">Storage</span></span>

* <span data-ttu-id="f60c8-110">azure-mgmt-storage のバージョンを 7.1.0 にアップグレードします</span><span class="sxs-lookup"><span data-stu-id="f60c8-110">Upgrade azure-mgmt-storage version to 7.1.0</span></span>
* <span data-ttu-id="f60c8-111">`az storage account create`:テーブルとキューの暗号化サービスをサポートするための `--encryption-key-type-for-table` と `--encryption-key-type-for-queue` を追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-111">`az storage account create`: Add `--encryption-key-type-for-table` and `--encryption-key-type-for-queue` to support Table and Queue Encryption Service</span></span>

## <a name="january-07-2020"></a><span data-ttu-id="f60c8-112">2020 年 1 月 7 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-112">January 07, 2020</span></span>

<span data-ttu-id="f60c8-113">バージョン 2.0.79</span><span class="sxs-lookup"><span data-stu-id="f60c8-113">Version 2.0.79</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-114">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-114">ACR</span></span>

* <span data-ttu-id="f60c8-115">[重大な変更] 'acr build'、'acr task create/update'、'acr run'、および 'acr pack' の '--os' パラメーターを削除します。</span><span class="sxs-lookup"><span data-stu-id="f60c8-115">[BREAKING CHANGE] Remove '--os' parameter for 'acr build', 'acr task create/update', 'acr run', and 'acr pack'.</span></span> <span data-ttu-id="f60c8-116">代わりに、'--platform' を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f60c8-116">Use '--platform' instead.</span></span>

### <a name="appconfig"></a><span data-ttu-id="f60c8-117">AppConfig</span><span class="sxs-lookup"><span data-stu-id="f60c8-117">AppConfig</span></span>

* <span data-ttu-id="f60c8-118">機能フラグのインポート/エクスポートのサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-118">Add support for importing/exporting feature flags</span></span>
* <span data-ttu-id="f60c8-119">keyvault 参照を作成するための新しいコマンド 'az appconfig kv set-keyvault' を追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-119">Add new command 'az appconfig kv set-keyvault' for creating keyvault reference</span></span>
* <span data-ttu-id="f60c8-120">機能フラグをファイルにエクスポートするときに、さまざまな名前付け規則をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-120">Support various naming conventions when exporting feature flags to file</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-121">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-121">AppService</span></span>

* <span data-ttu-id="f60c8-122">問題 #7154 を修正:単一引用符ではなく、アクサン グラーブを使用するように、コマンド < > のドキュメントを更新しています</span><span class="sxs-lookup"><span data-stu-id="f60c8-122">Fix issue #7154: Updating documentation for command <> to use back ticks instead of single quotes</span></span>
* <span data-ttu-id="f60c8-123">問題 #11287 を修正: webapp up:既定で、up を使用して作成されたアプリを 'SSL 有効' にする必要がある</span><span class="sxs-lookup"><span data-stu-id="f60c8-123">Fix issue #11287: webapp up: By default make the app created using up 'should be 'SSL enabled'</span></span>
* <span data-ttu-id="f60c8-124">問題 #11592 を修正:HTML 静的サイトに az webapp up フラグを追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-124">Fix issue #11592: Add az webapp up flag for html static sites</span></span>

### <a name="arm"></a><span data-ttu-id="f60c8-125">ARM</span><span class="sxs-lookup"><span data-stu-id="f60c8-125">ARM</span></span>

* <span data-ttu-id="f60c8-126">`az resource tag` を修正:Recovery Services コンテナー タグを更新できない</span><span class="sxs-lookup"><span data-stu-id="f60c8-126">Fix `az resource tag`: Recovery Services Vault tags cannot be updated</span></span>

### <a name="backup"></a><span data-ttu-id="f60c8-127">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-127">Backup</span></span>

* <span data-ttu-id="f60c8-128">IaasVM ワークロードの論理的な削除機能を有効にするための新しいコマンド 'backup protection undelete' を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-128">Added new command 'backup protection undelete' to enable soft-delete feature for IaasVM workload</span></span>
* <span data-ttu-id="f60c8-129">backup-properties コマンドを設定するための新しいパラメーター '--soft-delete-feature-state' を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-129">Added new parameter '--soft-delete-feature-state' to set backup-properties command</span></span>
* <span data-ttu-id="f60c8-130">IaasVM ワークロードのディスク除外のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-130">Added disk exclusion support for IaasVM workload</span></span>

### <a name="compute"></a><span data-ttu-id="f60c8-131">Compute</span><span class="sxs-lookup"><span data-stu-id="f60c8-131">Compute</span></span>

* <span data-ttu-id="f60c8-132">Azure Stack プロファイルの `vm create` エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="f60c8-132">Fix `vm create` failure in Azure Stack profile.</span></span>
* <span data-ttu-id="f60c8-133">vm monitor metrics tail/list-definitions: VM のクエリ メトリックとリスト定義をサポートします。</span><span class="sxs-lookup"><span data-stu-id="f60c8-133">vm monitor metrics tail/list-definitions: support query metric and list definitions for a vm.</span></span>
* <span data-ttu-id="f60c8-134">az vm の新しい再適用コマンド アクションを追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-134">Add new reapply command action for az vm</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f60c8-135">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f60c8-135">HDInsight</span></span>

* <span data-ttu-id="f60c8-136">Kafka REST プロキシを使用する Kafka クラスターの作成のサポート</span><span class="sxs-lookup"><span data-stu-id="f60c8-136">Support for creating a Kafka cluster with Kafka Rest Proxy</span></span>
* <span data-ttu-id="f60c8-137">azure-mgmt-hdinsight を 1.3.0 にアップグレード</span><span class="sxs-lookup"><span data-stu-id="f60c8-137">Upgrade azure-mgmt-hdinsight to 1.3.0</span></span>

### <a name="misc"></a><span data-ttu-id="f60c8-138">その他</span><span class="sxs-lookup"><span data-stu-id="f60c8-138">Misc.</span></span>

* <span data-ttu-id="f60c8-139">既定の JSON 形式 または --output によって構成された形式で Azure CLI モジュールと拡張機能のバージョンを表示するプレビュー コマンド `az version show` を追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-139">Add preview command `az version show` to show the versions of Azure CLI modules and extensions in JSON format by default or format configured by --output</span></span>

### <a name="event-hubs"></a><span data-ttu-id="f60c8-140">Event Hubs</span><span class="sxs-lookup"><span data-stu-id="f60c8-140">Event Hubs</span></span>

* <span data-ttu-id="f60c8-141">[重大な変更] コマンド 'az eventhubs eventhub update' と 'az eventhubs eventhub create' から 'ReceiveDisabled' status オプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="f60c8-141">[BREAKING CHANGE] Remove 'ReceiveDisabled' status option from command 'az eventhubs eventhub update' and 'az eventhubs eventhub create'.</span></span> <span data-ttu-id="f60c8-142">このオプションは、イベント ハブ エンティティに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="f60c8-142">This option is not valid for Event Hub entities.</span></span>

### <a name="service-bus"></a><span data-ttu-id="f60c8-143">Service Bus</span><span class="sxs-lookup"><span data-stu-id="f60c8-143">Service Bus</span></span>

* <span data-ttu-id="f60c8-144">[重大な変更] コマンド 'az servicebus topic create'、'az servicebus topic update'、'az servicebus queue create'、および 'az servicebus queue update' から 'ReceiveDisabled' status オプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="f60c8-144">[BREAKING CHANGE] Remove 'ReceiveDisabled' status option from command 'az servicebus topic create', 'az servicebus topic update', 'az servicebus queue create', and 'az servicebus queue update'.</span></span> <span data-ttu-id="f60c8-145">このオプションは、Service Bus のトピックとキューに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="f60c8-145">This option is not valid for Service Bus topics and queues.</span></span>

### <a name="rbac"></a><span data-ttu-id="f60c8-146">RBAC</span><span class="sxs-lookup"><span data-stu-id="f60c8-146">RBAC</span></span>

* <span data-ttu-id="f60c8-147">#11712 を修正: アプリケーションまたはサービス プリンシパルが存在しない場合に `az ad app/sp show` で終了コード 3 が返されない</span><span class="sxs-lookup"><span data-stu-id="f60c8-147">Fix #11712: `az ad app/sp show` does not return exit code 3 when the application or service principal does not exist</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-148">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-148">Storage</span></span>

* <span data-ttu-id="f60c8-149">`az storage account create`:--enable-hierarchical-namespace パラメーターのプレビュー フラグを削除します</span><span class="sxs-lookup"><span data-stu-id="f60c8-149">`az storage account create`: Remove preview flag for --enable-hierarchical-namespace parameter</span></span>
* <span data-ttu-id="f60c8-150">API バージョン 2019-06-01 を使用するために azure-mgmt-storage バージョンを 7.0.0 に更新します</span><span class="sxs-lookup"><span data-stu-id="f60c8-150">Update azure-mgmt-storage version to 7.0.0 to use api version 2019-06-01</span></span>
* <span data-ttu-id="f60c8-151">ストレージ アカウント blob-service-properties の削除の保持ポリシーの管理をサポートするために、新しいパラメーター `--enable-delete-retention` と `--delete-retention-days` を追加します。</span><span class="sxs-lookup"><span data-stu-id="f60c8-151">Add new parameters `--enable-delete-retention` and `--delete-retention-days` to support managing delete retention policy for storage account blob-service-properties.</span></span>

## <a name="december-17-2019"></a><span data-ttu-id="f60c8-152">2019 年 12 月 17 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-152">December 17, 2019</span></span>

<span data-ttu-id="f60c8-153">2.0.78</span><span class="sxs-lookup"><span data-stu-id="f60c8-153">2.0.78</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-154">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-154">ACR</span></span>

* <span data-ttu-id="f60c8-155">acr task run でのローカル コンテキストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-155">Added support Local context in acr task run</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-156">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-156">ACS</span></span>

* <span data-ttu-id="f60c8-157">[重大な変更] az openshift create: `--workspace-resource-id` の名前を `--workspace-id` に変更します。</span><span class="sxs-lookup"><span data-stu-id="f60c8-157">[BREAKING CHANGE]az openshift create: rename `--workspace-resource-id` to `--workspace-id`.</span></span>

### <a name="ams"></a><span data-ttu-id="f60c8-158">AMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-158">AMS</span></span>

* <span data-ttu-id="f60c8-159">リソースが見つからない場合に 3 を返すように表示コマンドを更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-159">Updated show commands to return 3 when resource not found</span></span>

### <a name="appconfig"></a><span data-ttu-id="f60c8-160">AppConfig</span><span class="sxs-lookup"><span data-stu-id="f60c8-160">AppConfig</span></span>

* <span data-ttu-id="f60c8-161">要求 URL に api-version を追加するときのバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-161">Fixed bug when appending api-version to request url.</span></span> <span data-ttu-id="f60c8-162">既存のソリューションは、改ページ位置の自動修正で機能しません。</span><span class="sxs-lookup"><span data-stu-id="f60c8-162">The existing solution doesn't work with pagination.</span></span>
* <span data-ttu-id="f60c8-163">英語以外の言語を表示するためのサポートを追加しました。これは、Microsoft のバックエンド サービスがグローバリゼーション向けに unicode をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="f60c8-163">Added support for showing languages besides English as our backend service support unicode for globalization.</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-164">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-164">AppService</span></span>

* <span data-ttu-id="f60c8-165">問題 #11217 を修正: webapp: az webapp config ssl upload はスロット パラメーターをサポートする必要がある</span><span class="sxs-lookup"><span data-stu-id="f60c8-165">Fixed issue #11217: webapp: az webapp config ssl upload should support slot parameter</span></span>
* <span data-ttu-id="f60c8-166">問題 #10965 を修正:エラー:名前を空にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="f60c8-166">Fixed issue #10965: Error: Name cannot be empty.</span></span> <span data-ttu-id="f60c8-167">ip_address とサブネットによる削除を許可します</span><span class="sxs-lookup"><span data-stu-id="f60c8-167">Allow remove by ip_address and subnet</span></span>
* <span data-ttu-id="f60c8-168">Key Vault `az webapp config ssl import` からの証明書のインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-168">Added support for importing certificates from Key Vault `az webapp config ssl import`</span></span>

### <a name="arm"></a><span data-ttu-id="f60c8-169">ARM</span><span class="sxs-lookup"><span data-stu-id="f60c8-169">ARM</span></span>

* <span data-ttu-id="f60c8-170">6\.0.0 を使用するように azure-mgmt-resource パッケージを更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-170">Updated azure-mgmt-resource package to use 6.0.0</span></span>
* <span data-ttu-id="f60c8-171">新しいパラメーター `--aux-subs` の追加による `az group deployment create` コマンドのクロス テナントのサポート</span><span class="sxs-lookup"><span data-stu-id="f60c8-171">Cross Tenant Support for `az group deployment create` command by adding new parameter `--aux-subs`</span></span>
* <span data-ttu-id="f60c8-172">ポリシー セット定義へのメタデータ情報の追加をサポートするために、新しいパラメーター `--metadata` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-172">Added new parameter `--metadata` to support adding metadata information for policy set definitions.</span></span>

### <a name="backup"></a><span data-ttu-id="f60c8-173">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-173">Backup</span></span>

* <span data-ttu-id="f60c8-174">SQL および SAP Hana ワークロードのバックアップ サポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-174">Added Backup support for SQL and SAP Hana workload.</span></span>

### <a name="botservice"></a><span data-ttu-id="f60c8-175">BotService</span><span class="sxs-lookup"><span data-stu-id="f60c8-175">BotService</span></span>

* <span data-ttu-id="f60c8-176">[重大な変更] プレビューコマンド 'az bot create' から '--version' フラグを削除します。</span><span class="sxs-lookup"><span data-stu-id="f60c8-176">[Breaking change] Remove '--version' flag from preview command 'az bot create'.</span></span> <span data-ttu-id="f60c8-177">v4 SDK ボットのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-177">Only v4 SDK bots are supported.</span></span>
* <span data-ttu-id="f60c8-178">名前を使用できるかどうかのチェックを 'sz bot create' に追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-178">Added name availability check for 'az bot create'.</span></span>
* <span data-ttu-id="f60c8-179">'az bot update' を使用してボットのアイコン URL を更新するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-179">Added support for updating the icon URL for a bot via 'az bot update'.</span></span>
* <span data-ttu-id="f60c8-180">'az bot directline update' を使用して Direct Line チャネルを更新するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-180">Added support for updating a Direct Line channel via 'az bot directline update'.</span></span>
* <span data-ttu-id="f60c8-181">'az bot directline create' に '--enable-enhanced-auth' フラグのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-181">Added '--enable-enhanced-auth' flag support to 'az bot directline create'.</span></span>
* <span data-ttu-id="f60c8-182">コマンド グループ 'az bot authsetting' は、プレビュー段階ではなく、GA です。</span><span class="sxs-lookup"><span data-stu-id="f60c8-182">The following command groups are GA and not in preview: 'az bot authsetting'.</span></span>
* <span data-ttu-id="f60c8-183">'az bot' の次のコマンドは、プレビュー段階ではなく、GA です: 'create'、'prepare-deploy'、'show'、'delete'、'update'。</span><span class="sxs-lookup"><span data-stu-id="f60c8-183">The following commands in 'az bot' are GA and not in preview: 'create', 'prepare-deploy', 'show', 'delete', 'update'.</span></span>
* <span data-ttu-id="f60c8-184">'az bot prepare-deploy' が修正され、 '--proj-file-path' 値が小文字に変更されます (例: "Test.csproj" の場合、"test.csproj")。</span><span class="sxs-lookup"><span data-stu-id="f60c8-184">Fixed 'az bot prepare-deploy' changing '--proj-file-path' value to lower case (e.g. "Test.csproj" to "test.csproj").</span></span>

### <a name="compute"></a><span data-ttu-id="f60c8-185">Compute</span><span class="sxs-lookup"><span data-stu-id="f60c8-185">Compute</span></span>

* <span data-ttu-id="f60c8-186">vmss create/update:--scale-in-policy を追加しました。これは、VMSS がスケールインされるときに削除対象として選択される仮想マシンを決定します。</span><span class="sxs-lookup"><span data-stu-id="f60c8-186">vmss create/update: Added --scale-in-policy, which decides which virtual machines are chosen for removal when a VMSS is scaled-in.</span></span>
* <span data-ttu-id="f60c8-187">vm/vmss update:--priority を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-187">vm/vmss update: Added --priority.</span></span>
* <span data-ttu-id="f60c8-188">vm/vmss update:--max-price を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-188">vm/vmss update: Added --max-price.</span></span>
* <span data-ttu-id="f60c8-189">disk-encryption-set コマンド グループ (create、show、update、delete、list) を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-189">Added disk-encryption-set command group (create, show, update, delete, list).</span></span>
* <span data-ttu-id="f60c8-190">disk create:--encryption-type と --disk-encryption-set を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-190">disk create: Added --encryption-type and --disk-encryption-set.</span></span>
* <span data-ttu-id="f60c8-191">vm/vmss create: --os-disk-encryption-set と --data-disk-encryption-sets を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-191">vm/vmss create: Added --os-disk-encryption-set and --data-disk-encryption-sets.</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-192">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-192">Core</span></span>

* <span data-ttu-id="f60c8-193">Python 3.4 のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-193">Removed support for Python 3.4</span></span>
* <span data-ttu-id="f60c8-194">複数のコマンドでの HaTS 調査のプラグイン</span><span class="sxs-lookup"><span data-stu-id="f60c8-194">Plug in HaTS survey in multiple commands</span></span>

### <a name="dls"></a><span data-ttu-id="f60c8-195">DLS</span><span class="sxs-lookup"><span data-stu-id="f60c8-195">DLS</span></span>

* <span data-ttu-id="f60c8-196">ADLS SDK バージョンを更新しました (0.0.48)。</span><span class="sxs-lookup"><span data-stu-id="f60c8-196">Updated ADLS sdk version (0.0.48).</span></span>

### <a name="install"></a><span data-ttu-id="f60c8-197">インストール</span><span class="sxs-lookup"><span data-stu-id="f60c8-197">Install</span></span>

* <span data-ttu-id="f60c8-198">インストール スクリプトで python 3.8 がサポートされます</span><span class="sxs-lookup"><span data-stu-id="f60c8-198">Install script support python 3.8</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-199">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-199">IOT</span></span>

* <span data-ttu-id="f60c8-200">[重大な変更] manual-failover から --failover-region パラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-200">[BREAKING CHANGE] Removed --failover-region parameter from manual-failover.</span></span> <span data-ttu-id="f60c8-201">これで、割り当てられた geo ペアのセカンダリ リージョンにフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="f60c8-201">Now it will failover to assigned geo-paired secondary region.</span></span>

### <a name="key-vault"></a><span data-ttu-id="f60c8-202">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f60c8-202">Key Vault</span></span>

* <span data-ttu-id="f60c8-203">#8095 を修正: `az keyvault storage remove`: ヘルプ メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="f60c8-203">Fixed #8095: `az keyvault storage remove`: improve the help message</span></span>
* <span data-ttu-id="f60c8-204">#8921 を修正: `az keyvault key/secret/certificate list/list-deleted/list-versions`: パラメーター `--maxresults` の検証のバグを修正します</span><span class="sxs-lookup"><span data-stu-id="f60c8-204">Fixed #8921: `az keyvault key/secret/certificate list/list-deleted/list-versions`: fix the validation bug on parameter `--maxresults`</span></span>
* <span data-ttu-id="f60c8-205">#10512 を修正: `az keyvault set-policy`: `--object-id`、`--spn`、`--upn` のいずれも指定されていない場合のエラー メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="f60c8-205">Fixed #10512: `az keyvault set-policy`: improve the error message when none of `--object-id`, `--spn` or `--upn` is specified</span></span>
* <span data-ttu-id="f60c8-206">#10846 を修正: `az keyvault secret show-deleted`: `--id` を指定した場合、`--name/-n` は必要ありません</span><span class="sxs-lookup"><span data-stu-id="f60c8-206">Fixed #10846: `az keyvault secret show-deleted`: when `--id` is specified, `--name/-n` is not required</span></span>
* <span data-ttu-id="f60c8-207">#11084 を修正: `az keyvault secret download`: パラメーター `--encoding` のヘルプ メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="f60c8-207">Fixed #11084: `az keyvault secret download`: improve the help message of parameter `--encoding`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-208">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-208">Network</span></span>

* <span data-ttu-id="f60c8-209">az network application-gateway probe:作成および更新時にバックエンド サーバーをプローブするためのポートを指定する --port オプションのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-209">az network application-gateway probe: Added support --port option to specify a port for probing backend servers when create and update</span></span>
* <span data-ttu-id="f60c8-210">az network application-gateway url-path-map create/update: `--waf-policy` のバグ修正</span><span class="sxs-lookup"><span data-stu-id="f60c8-210">az network application-gateway url-path-map create/update: bug fix for `--waf-policy`</span></span>
* <span data-ttu-id="f60c8-211">az network application-gateway:`--rewrite-rule-set` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-211">az network application-gateway: Added support `--rewrite-rule-set`</span></span>
* <span data-ttu-id="f60c8-212">az network list-service-aliases:サービス エンドポイント ポリシーに使用できるサービス別名を一覧表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-212">az network list-service-aliases: Added support list service aliases which can be used for Service Endpoint Policies</span></span>
* <span data-ttu-id="f60c8-213">az network dns zone import:レコード名での .@ のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-213">az network dns zone import: Added support .@ in record name</span></span>

### <a name="packaging"></a><span data-ttu-id="f60c8-214">梱包</span><span class="sxs-lookup"><span data-stu-id="f60c8-214">Packaging</span></span>

* <span data-ttu-id="f60c8-215">pip インストール用のバック エッジ ビルドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-215">Added back edge builds for pip install</span></span>
* <span data-ttu-id="f60c8-216">Ubuntu eoan パッケージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-216">Added Ubuntu eoan package</span></span>

### <a name="policy"></a><span data-ttu-id="f60c8-217">ポリシー</span><span class="sxs-lookup"><span data-stu-id="f60c8-217">Policy</span></span>

* <span data-ttu-id="f60c8-218">ポリシー API バージョン 2019-09-01 のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-218">Added support for Policy API version 2019-09-01.</span></span>
* <span data-ttu-id="f60c8-219">az policy set-definition:`--definition-groups` パラメーターを使用したポリシー セット定義内のグループ化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-219">az policy set-definition: Added support grouping within policy set definitions with `--definition-groups` parameter</span></span>

### <a name="redis"></a><span data-ttu-id="f60c8-220">Redis</span><span class="sxs-lookup"><span data-stu-id="f60c8-220">Redis</span></span>

* <span data-ttu-id="f60c8-221">`az redis create` コマンドにプレビュー パラメーター `--replicas-per-master` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-221">Added preview param `--replicas-per-master` to `az redis create` command</span></span>
* <span data-ttu-id="f60c8-222">azure-mgmt-redis を 6.0.0 から 7.0.0rc1 に更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-222">Updated azure-mgmt-redis from 6.0.0 to 7.0.0rc1</span></span>

### <a name="servicefabric"></a><span data-ttu-id="f60c8-223">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f60c8-223">ServiceFabric</span></span>

* <span data-ttu-id="f60c8-224">#10963 を含む node-type 追加ロジックを修正:持続性レベル Gold で新しいノード タイプを追加すると、常に CLI エラーがスローされる</span><span class="sxs-lookup"><span data-stu-id="f60c8-224">Fixed in node-type add logic including #10963: Adding new node type with durability level Gold will always throw CLI error</span></span>
* <span data-ttu-id="f60c8-225">作成テンプレートの ServiceFabricNodeVmExt バージョンを 1.1 に更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-225">Updated ServiceFabricNodeVmExt version to 1.1 in creation template</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-226">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-226">SQL</span></span>

* <span data-ttu-id="f60c8-227">読み取りスケール管理をサポートするために、sql db create および update コマンドに "--read-scale" と "--read-replicas" パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-227">Added "--read-scale" and "--read-replicas" parameters to sql db create and update commands, to support read scale management.</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-228">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-228">Storage</span></span>

* <span data-ttu-id="f60c8-229">GA リリースでの storage account create および update コマンド用の大きいファイルの共有プロパティ</span><span class="sxs-lookup"><span data-stu-id="f60c8-229">GA Release Large File Shares property for storage account create and update command</span></span>
* <span data-ttu-id="f60c8-230">GA リリースでのユーザー委任 SAS トークンのサポート</span><span class="sxs-lookup"><span data-stu-id="f60c8-230">GA Release User Delegation SAS token Support</span></span>
* <span data-ttu-id="f60c8-231">ストレージ アカウントの Blob service のプロパティを管理するための新しいコマンド `az storage account blob-service-properties show` と `az storage account blob-service-properties update --enable-change-feed` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-231">Added new commands `az storage account blob-service-properties show` and `az storage account blob-service-properties update --enable-change-feed` to manage blob service properties for storage account.</span></span>
* <span data-ttu-id="f60c8-232">[今後の破壊的変更] `az storage copy`: `*` 文字は URL 内のワイルドカードとしてサポートされなくなりましたが、新しいパラメーターの --include-pattern と --exclude-pattern が `*` ワイルドカードをサポートして追加されます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-232">[COMING BREAKING CHANGE] `az storage copy`: `*` character is no longer supported as a wildcard in URL, but new parameters --include-pattern and --exclude-pattern will be added with `*` wildcard support.</span></span>
* <span data-ttu-id="f60c8-233">問題 #11043 を修正:`az storage remove` コマンドでコンテナー/共有全体を削除するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-233">Fixed issue #11043: Added support to remove whole container/share in `az storage remove` command</span></span>

## <a name="november-26-2019"></a><span data-ttu-id="f60c8-234">2019 年 11 月 26 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-234">November 26, 2019</span></span>

<span data-ttu-id="f60c8-235">バージョン 2.0.77</span><span class="sxs-lookup"><span data-stu-id="f60c8-235">Version 2.0.77</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-236">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-236">ACR</span></span>

* <span data-ttu-id="f60c8-237">acr task create/update からパラメーター `--branch` が非推奨になりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-237">Deprecated parameter `--branch` from acr task create/update</span></span>

### <a name="azure-red-hat-openshift"></a><span data-ttu-id="f60c8-238">Azure Red Hat OpenShift</span><span class="sxs-lookup"><span data-stu-id="f60c8-238">Azure Red Hat OpenShift</span></span>

* <span data-ttu-id="f60c8-239">監視を使用して Azure Red Hat Openshift クラスターを作成できるように、`--workspace-resource-id` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-239">Added `--workspace-resource-id` flag to allow creation of Azure Red Hat Openshift cluster with monitoring</span></span>
* <span data-ttu-id="f60c8-240">監視を使用して Azure Red Hat OpenShift クラスターを作成するために `monitor_profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-240">Added `monitor_profile` to create Azure Red Hat OpenShift cluster with monitoring</span></span>

### <a name="aks"></a><span data-ttu-id="f60c8-241">AKS</span><span class="sxs-lookup"><span data-stu-id="f60c8-241">AKS</span></span>

* <span data-ttu-id="f60c8-242">"az aks rotate-certs" を使用したクラスター証明書ローテーション操作のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-242">Added support cluster certificate rotation operation using "az aks rotate-certs".</span></span>

### <a name="appconfig"></a><span data-ttu-id="f60c8-243">AppConfig</span><span class="sxs-lookup"><span data-stu-id="f60c8-243">AppConfig</span></span>

* <span data-ttu-id="f60c8-244">`as az appconfig kv import` の区切り文字に ":" を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-244">Added support for using ":" for `as az appconfig kv import` separator</span></span>
* <span data-ttu-id="f60c8-245">null ラベルを含む複数のラベルを持つキー値の一覧表示に関する問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-245">Fixed issue for listing key values with multiple labels including null label.</span></span> 
* <span data-ttu-id="f60c8-246">管理プレーン SKD である azure-mgmt-appconfiguration を バージョン 0.3.0 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-246">Updated management plane sdk, azure-mgmt-appconfiguration, to version 0.3.0.</span></span> 

### <a name="appservice"></a><span data-ttu-id="f60c8-247">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-247">AppService</span></span>

* <span data-ttu-id="f60c8-248">問題 #11100 を修正:サービス プランの作成時の az webapp up の AttributeError</span><span class="sxs-lookup"><span data-stu-id="f60c8-248">Fixed issue #11100: AttributeError for az webapp up when create service plan</span></span>
* <span data-ttu-id="f60c8-249">az webapp up:サポートされている言語のサイトに作成またはデプロイを強制します。既定値は使用されません。</span><span class="sxs-lookup"><span data-stu-id="f60c8-249">az webapp up: Forcing the creation or deployment to a site for supported languages, no defaults used.</span></span>
* <span data-ttu-id="f60c8-250">App Service Environment のサポートを追加しました: az appservice ase show | list | list-addresses | list-plans | create | update | delete</span><span class="sxs-lookup"><span data-stu-id="f60c8-250">Added support for App Service Environment: az appservice ase show | list | list-addresses | list-plans | create | update | delete</span></span>

### <a name="backup"></a><span data-ttu-id="f60c8-251">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-251">Backup</span></span>

* <span data-ttu-id="f60c8-252">az backup policy list-associated-items の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-252">Fixed issue in az backup policy list-associated-items.</span></span> <span data-ttu-id="f60c8-253">省略可能な BackupManagementType パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-253">Added optional BackupManagementType parameter.</span></span>

### <a name="compute"></a><span data-ttu-id="f60c8-254">Compute</span><span class="sxs-lookup"><span data-stu-id="f60c8-254">Compute</span></span>

* <span data-ttu-id="f60c8-255">コンピューティング、ディスク、スナップショットの API バージョンを 2019-07-01 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-255">Upgraded API version of compute, disks, snapshots to 2019-07-01</span></span>
* <span data-ttu-id="f60c8-256">vmss create: --orchestration-mode の改善</span><span class="sxs-lookup"><span data-stu-id="f60c8-256">vmss create: Improvement for --orchestration-mode</span></span>
* <span data-ttu-id="f60c8-257">sig image-definition create: --os-state を追加して、このイメージの下に作成された仮想マシンを "一般化" するか、または "特殊化" するかを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-257">sig image-definition create: Added --os-state to allow specifying whether the virtual machines created under this image are 'Generalized' or 'Specialized'</span></span>
* <span data-ttu-id="f60c8-258">sig image-definition create: --hyper-v-generation を追加して、ハイパーバイザーの生成を指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-258">sig image-definition create: Added --hyper-v-generation to allow specifying the hypervisor generation</span></span>
* <span data-ttu-id="f60c8-259">sig image-version create: --os-snapshot と --data-snapshots のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-259">sig image-version create: Added support --os-snapshot and --data-snapshots</span></span>
* <span data-ttu-id="f60c8-260">image create: --data-disk-caching を追加して、データ ディスクのキャッシュ設定を指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-260">image create: Added --data-disk-caching to allow specifying caching setting of data disks</span></span>
* <span data-ttu-id="f60c8-261">Python Compute SDK を 10.0.0 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-261">Upgraded Python Compute SDK to 10.0.0</span></span>
* <span data-ttu-id="f60c8-262">vm/vmss create: 'Priority' 列挙型プロパティに 'Spot' を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-262">vm/vmss create: Added 'Spot' to 'Priority' enum property</span></span>
* <span data-ttu-id="f60c8-263">[重大な変更] Swagger と Powershell のコマンドレットとの一貫性を維持するために、VM と VMSS の両方で '--max-billing' パラメーターを '--max-price' に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-263">[Breaking change] Renamed '--max-billing' parameter to '--max-price', for both VM and VMSS, to be consistent with Swagger and Powershell cmdlets</span></span>
* <span data-ttu-id="f60c8-264">vm monitor log show: リンクされた Log Analytics ワークスペースに対してログのクエリを実行するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-264">vm monitor log show: Added support for querying log over linked log analytics workspace.</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-265">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-265">IOT</span></span>

* <span data-ttu-id="f60c8-266">#2531 の修正: ハブの更新に便利な引数を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-266">Fix #2531: Added convenience arguments for hub update.</span></span>
* <span data-ttu-id="f60c8-267">#8323 の修正: ストレージ カスタム エンドポイントを作成するために不足しているパラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-267">Fix #8323: Added missing parameters to create storage custom endpoint.</span></span>
* <span data-ttu-id="f60c8-268">回帰バグの修正: 既定のストレージ エンドポイントをオーバーライドする変更を元に戻しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-268">Fix regression bug: Reverted the changes which overrides the default storage endpoint.</span></span>

### <a name="key-vault"></a><span data-ttu-id="f60c8-269">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f60c8-269">Key Vault</span></span>

* <span data-ttu-id="f60c8-270">#11121 を修正しました: `az keyvault certificate list` を使用する場合、`--include-pending` を渡すときに `true` または `false` の値が必須ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-270">Fixed #11121: When using `az keyvault certificate list`, passing `--include-pending` now doesn't require a value of `true` or `false`</span></span>

### <a name="netappfiles"></a><span data-ttu-id="f60c8-271">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="f60c8-271">NetAppFiles</span></span>

* <span data-ttu-id="f60c8-272">azure-mgmt-netapp を 0.7.0 にアップグレードしました。これには、今後のレプリケーション操作に関連した追加のボリューム プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f60c8-272">Upgraded azure-mgmt-netapp to 0.7.0 which includes some additional volume properties associated with upcoming replication operations</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-273">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-273">Network</span></span>

* <span data-ttu-id="f60c8-274">application-gateway waf-config: 非推奨になりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-274">application-gateway waf-config: deprecated</span></span>
* <span data-ttu-id="f60c8-275">application-gateway waf-policy: 管理されているルール セットと除外ルールを管理するために、サブグループ managed-rules を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-275">application-gateway waf-policy: Added subgroup managed-rules to manage managed rule sets and exclusion rules</span></span>
* <span data-ttu-id="f60c8-276">application-gateway waf-policy: waf-policy のグローバル構成を管理するために、サブグループ policy-setting を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-276">application-gateway waf-policy: Added subgroup policy-setting to manage global configuration of a waf-policy</span></span>
* <span data-ttu-id="f60c8-277">[重大な変更] application-gateway waf-policy: subgroup rule を custom-rule に名前変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-277">[BREAKING CHANGE] application-gateway waf-policy: Renamed subgroup rule to custom-rule</span></span>
* <span data-ttu-id="f60c8-278">application-gateway http-listener: 作成時の --firewall-policy を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-278">application-gateway http-listener: Added --firewall-policy when create</span></span>
* <span data-ttu-id="f60c8-279">application-gateway url-path-map rule: 作成時の --firewall-policy を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-279">application-gateway url-path-map rule: Added --firewall-policy when create</span></span>

### <a name="packaging"></a><span data-ttu-id="f60c8-280">梱包</span><span class="sxs-lookup"><span data-stu-id="f60c8-280">Packaging</span></span>

* <span data-ttu-id="f60c8-281">az ラッパーを Python で書き直しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-281">Rewrote the az wrapper in Python</span></span>
* <span data-ttu-id="f60c8-282">Python 3.8 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-282">Added support for Python 3.8</span></span>
* <span data-ttu-id="f60c8-283">RPM パッケージで Python 3 に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-283">Changed to Python 3 for RPM package</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-284">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-284">Profile</span></span>

* <span data-ttu-id="f60c8-285">Microsoft アカウントで `az login -u {} -p {}` を実行するときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-285">Polished error when running `az login -u {} -p {}` with Microsoft account</span></span>
* <span data-ttu-id="f60c8-286">自己署名ルート証明書使用してプロキシの背後で `az login` を実行するときの `SSLError` を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-286">Polished `SSLError` when running `az login` behind a proxy with self-signed root certificate</span></span>
* <span data-ttu-id="f60c8-287">#10578 を修正: Windows または WSL で同時に複数のインスタンスを起動すると `az login` がハングする</span><span class="sxs-lookup"><span data-stu-id="f60c8-287">Fixed #10578: `az login` hangs when more than one instances are launched at the same time on Windows or WSL</span></span>
* <span data-ttu-id="f60c8-288">#11059 を修正: テナントにサブスクリプションがあると `az login --allow-no-subscriptions` が失敗する</span><span class="sxs-lookup"><span data-stu-id="f60c8-288">Fixed #11059: `az login --allow-no-subscriptions` fails if there are subscriptions in the tenant</span></span>
* <span data-ttu-id="f60c8-289">#11238 を修正: サブスクリプションの名前を変更した後、MSI を使用してログインすると、同じサブスクリプションが 2 回表示される</span><span class="sxs-lookup"><span data-stu-id="f60c8-289">Fixed #11238: After renaming a subscription, logging in with MSI will result in the same subscription appearing twice</span></span>

### <a name="rbac"></a><span data-ttu-id="f60c8-290">RBAC</span><span class="sxs-lookup"><span data-stu-id="f60c8-290">RBAC</span></span>

* <span data-ttu-id="f60c8-291">#10996 を修正: `--password` が指定されていないときの `az ad user update` での `--force-change-password-next-login` のエラーを改善</span><span class="sxs-lookup"><span data-stu-id="f60c8-291">Fixed #10996: Polish error for `--force-change-password-next-login` in `az ad user update` when `--password` is not specified</span></span>

### <a name="redis"></a><span data-ttu-id="f60c8-292">Redis</span><span class="sxs-lookup"><span data-stu-id="f60c8-292">Redis</span></span>

* <span data-ttu-id="f60c8-293">#2902 を修正: Basic SKU キャッシュの更新中、メモリ構成を設定しない</span><span class="sxs-lookup"><span data-stu-id="f60c8-293">Fixed #2902: Avoid setting memory configs while updating Basic SKU cache</span></span>

### <a name="reservations"></a><span data-ttu-id="f60c8-294">Reservations</span><span class="sxs-lookup"><span data-stu-id="f60c8-294">Reservations</span></span>

* <span data-ttu-id="f60c8-295">SDK バージョンを 0.6.0 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-295">Upgraded SDK Version to 0.6.0</span></span>
* <span data-ttu-id="f60c8-296">Gat-Gatalogs を呼び出した後の billingplan の詳細情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-296">Added billingplan details info after calling Get-Gatalogs</span></span>
* <span data-ttu-id="f60c8-297">予約の価格を計算するための新しいコマンド `az reservations reservation-order calculate` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-297">Added new command `az reservations reservation-order calculate` to calculate the price for a reservation</span></span>
* <span data-ttu-id="f60c8-298">新しい予約を購入するための新しいコマンド `az reservations reservation-order purchase` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-298">Added new command `az reservations reservation-order purchase` to purchase a new reservation</span></span>

### <a name="rest"></a><span data-ttu-id="f60c8-299">REST</span><span class="sxs-lookup"><span data-stu-id="f60c8-299">Rest</span></span>
* <span data-ttu-id="f60c8-300">`az rest` を GA に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-300">Changed `az rest` to GA</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-301">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-301">SQL</span></span>

* <span data-ttu-id="f60c8-302">azure-mgmt-sql をバージョン 0.15.0 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-302">Updated azure-mgmt-sql to version 0.15.0.</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-303">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-303">Storage</span></span>

* <span data-ttu-id="f60c8-304">storage account create: Blob service でのファイルシステムのセマンティクスをサポートするために、--enable-hierarchical-namespace を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-304">storage account create: Added --enable-hierarchical-namespace to support filesystem semantics in blob service.</span></span>
* <span data-ttu-id="f60c8-305">エラー メッセージから関連性のない例外を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-305">Removed unrelated exception from error message</span></span>
* <span data-ttu-id="f60c8-306">"この操作を実行するのに必要なアクセス許可がありません" という誤ったエラー メッセージが</span><span class="sxs-lookup"><span data-stu-id="f60c8-306">Fixed issues with incorrect error message "You do not have the required permissions needed to perform this operation."</span></span> <span data-ttu-id="f60c8-307">ネットワーク ルールまたは AuthenticationFailed によってブロックされた場合に表示される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-307">when blocked by network rules or AuthenticationFailed.</span></span>

## <a name="november-4-2019"></a><span data-ttu-id="f60c8-308">2019 年 11 月 4 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-308">November 4, 2019</span></span>

<span data-ttu-id="f60c8-309">バージョン 2.0.76</span><span class="sxs-lookup"><span data-stu-id="f60c8-309">Version 2.0.76</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-310">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-310">ACR</span></span>

* <span data-ttu-id="f60c8-311">コマンド `az acr pack build` にプレビュー パラメーター `--pack-image-tag` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-311">Added a preview parameter `--pack-image-tag` to command `az acr pack build`.</span></span>
* <span data-ttu-id="f60c8-312">レジストリ作成時の監査を有効にするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-312">Added support for enabling auditing on creating a registry</span></span>
* <span data-ttu-id="f60c8-313">レジストリ スコープが設定された RBAC のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-313">Added support for Repository-scoped RBAC</span></span>

### <a name="aks"></a><span data-ttu-id="f60c8-314">AKS</span><span class="sxs-lookup"><span data-stu-id="f60c8-314">AKS</span></span>

* <span data-ttu-id="f60c8-315">`az aks create` コマンドに `--enable-cluster-autoscaler`、`--min-count`、および `--max-count` を追加しました。これにより、ノード プールのクラスター オートスケーラーが有効になります。</span><span class="sxs-lookup"><span data-stu-id="f60c8-315">Added `--enable-cluster-autoscaler`, `--min-count` and `--max-count` to the `az aks create` command, which enables cluster autoscaler for the node pool.</span></span>
* <span data-ttu-id="f60c8-316">上記のフラグに加えて、`--update-cluster-autoscaler` および `--disable-cluster-autoscaler` を `az aks update` コマンドに追加し、クラスター オートスケーラーを更新できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-316">Added the above flags as well as `--update-cluster-autoscaler` and `--disable-cluster-autoscaler` to the `az aks update` command, allowing updates to cluster autoscaler.</span></span>

### <a name="appconfig"></a><span data-ttu-id="f60c8-317">AppConfig</span><span class="sxs-lookup"><span data-stu-id="f60c8-317">AppConfig</span></span>

* <span data-ttu-id="f60c8-318">App Configuration に格納される機能フラグを管理するために、appconfig feature コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-318">Added appconfig feature command group to manage feature flags stored in an App Configuration.</span></span>
* <span data-ttu-id="f60c8-319">ファイルに対する appconfig kv export コマンドの軽微なバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-319">Fixed minor bug for appconfig kv export to file command.</span></span> <span data-ttu-id="f60c8-320">エクスポート中に宛先ファイルの内容を読み取らないようにしました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-320">Stop reading dest file contents during export.</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-321">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-321">AppService</span></span>

* <span data-ttu-id="f60c8-322">`az appservice plan create`:appservice plan create に "persitescaling" を設定するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-322">`az appservice plan create`: Added support to set 'persitescaling' on appservice plan create.</span></span>
* <span data-ttu-id="f60c8-323">webapp config ssl bind 操作がリソースから既存のタグを削除する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-323">Fixed an issue where webapp config ssl bind operation was removing existing tags from the resource</span></span>
* <span data-ttu-id="f60c8-324">関数アプリのデプロイ時にリモート ビルド アクションをサポートするために、`az functionapp deployment source config-zip` に `--build-remote` フラグを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-324">Added `--build-remote` flag for `az functionapp deployment source config-zip` to support remote build action during function app deployment.</span></span>
* <span data-ttu-id="f60c8-325">Windows 向けの関数アプリの既定のノードバージョンを 10 に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-325">Changed default node version on function apps to ~10 for Windows</span></span>
* <span data-ttu-id="f60c8-326">`az functionapp create` に `--runtime-version` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-326">Added `--runtime-version` property to `az functionapp create`</span></span>

### <a name="arm"></a><span data-ttu-id="f60c8-327">ARM</span><span class="sxs-lookup"><span data-stu-id="f60c8-327">ARM</span></span>

* <span data-ttu-id="f60c8-328">`az deployment/group deployment validate`:デプロイ時に、json テンプレートで複数行とコメントをサポートするために `--handle-extended-json-format` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-328">`az deployment/group deployment validate`: Added `--handle-extended-json-format` parameter to support multiline and comments in json template when deployment.</span></span>
* <span data-ttu-id="f60c8-329">azure-mgmt-resource を 2019-07-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="f60c8-329">Bumped azure-mgmt-resource to 2019-07-01</span></span>

### <a name="backup"></a><span data-ttu-id="f60c8-330">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-330">Backup</span></span>

* <span data-ttu-id="f60c8-331">AzureFiles のバックアップ サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-331">Added AzureFiles backup support</span></span>

### <a name="compute"></a><span data-ttu-id="f60c8-332">Compute</span><span class="sxs-lookup"><span data-stu-id="f60c8-332">Compute</span></span>

* <span data-ttu-id="f60c8-333">`az vm create`:高速ネットワークと既存の NIC を一緒に指定した場合の警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-333">`az vm create`: Added warning when specifying accelerated networking and an existing NIC together.</span></span>
* <span data-ttu-id="f60c8-334">`az vm create`:仮想マシンを割り当てる必要がある既存の仮想マシン スケール セットを指定するための `--vmss` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-334">`az vm create`: Added `--vmss` to specify an existing virtual machine scale set that the virtual machine should be assigned to.</span></span>
* <span data-ttu-id="f60c8-335">`az vm/vmss create`:イメージ エイリアス ファイルのローカル コピーを追加し、制限付きネットワーク環境でそれにアクセスできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-335">`az vm/vmss create`: Added a local copy of image alias file so that it can be accessed in a restricted network environment.</span></span>
* <span data-ttu-id="f60c8-336">`az vmss create`:スケール セットによる仮想マシンの管理方法を指定するための `--orchestration-mode` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-336">`az vmss create`: Added `--orchestration-mode` to specify how virtual machines are managed by the scale set.</span></span>
* <span data-ttu-id="f60c8-337">`az vm/vmss update`:Ultra SSD 設定を更新できるように `--ultra-ssd-enabled` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-337">`az vm/vmss update`: Added `--ultra-ssd-enabled` to allow updating ultra SSD setting.</span></span>
* <span data-ttu-id="f60c8-338">[破壊的変更] `az vm extension set`:ユーザーが `--ids` を使用して、VM に拡張機能を設定できないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-338">[BREAKING CHANGE] `az vm extension set`: Fixed bug where users could not set an extension on a VM with `--ids`.</span></span>
* <span data-ttu-id="f60c8-339">Azure Marketplace イメージの使用条件を管理するための新しいコマンド `az vm image terms accept/cancel/show` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-339">Added new commands `az vm image terms accept/cancel/show` to manage Azure Marketplace image terms.</span></span>
* <span data-ttu-id="f60c8-340">VMAccessForLinux をバージョン 1.5 に更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-340">Updated VMAccessForLinux to version 1.5</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-341">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-341">CosmosDB</span></span>

* <span data-ttu-id="f60c8-342">[破壊的変更] `az sql container create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-342">[BREAKING CHANGE] `az sql container create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="f60c8-343">[破壊的変更] `az gremlin graph create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-343">[BREAKING CHANGE] `az gremlin graph create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="f60c8-344">`az sql container create`:`--unique-key-policy` および `--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-344">`az sql container create`: Added `--unique-key-policy` and `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="f60c8-345">`az sql container create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-345">`az sql container create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="f60c8-346">`gremlin graph create`:`--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-346">`gremlin graph create`: Added `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="f60c8-347">`gremlin graph create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-347">`gremlin graph create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="f60c8-348">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-348">Fixed typo in help message</span></span>
* <span data-ttu-id="f60c8-349">データベース:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-349">database: Added deprecation infomation</span></span>
* <span data-ttu-id="f60c8-350">コレクション:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-350">collection: Added deprecation infomation</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-351">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-351">IoT</span></span>

* <span data-ttu-id="f60c8-352">新しいルーティング ソースの種類を追加しました: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="f60c8-352">Added new routing source type: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="f60c8-353">`az iot hub create` の不十分な機能を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-353">Fixed missing features in `az iot hub create`</span></span>

### <a name="key-vault"></a><span data-ttu-id="f60c8-354">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f60c8-354">Key Vault</span></span>

* <span data-ttu-id="f60c8-355">証明書ファイルが存在しない場合の予期しないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-355">Fixed an unexpected error when certificate file does not exist</span></span>
* <span data-ttu-id="f60c8-356">`az keyvault recover/purge` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-356">Fixed `az keyvault recover/purge` not working</span></span>

### <a name="netappfiles"></a><span data-ttu-id="f60c8-357">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="f60c8-357">NetAppFiles</span></span>

* <span data-ttu-id="f60c8-358">API バージョン 2019-07-01 を使用するために azure-mgmt-netapp を 0.6.0 にアップグレードしました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-358">Upgraded azure-mgmt-netapp to 0.6.0 to use API version 2019-07-01.</span></span> <span data-ttu-id="f60c8-359">この新しい API バージョンには以下の変更内容が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-359">This new API version includes:</span></span>

    - <span data-ttu-id="f60c8-360">ボリューム作成の `--protocol-types` が "NFSv4" ではなく "NFSv 4.1" を受け入れるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-360">Volume creation `--protocol-types` accepts now "NFSv4.1" not "NFSv4"</span></span>
    - <span data-ttu-id="f60c8-361">ボリューム エクスポート ポリシー プロパティの名前が "nfsv4" ではなく "nfsv41" に変更されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-361">Volume export policy property now named 'nfsv41' not 'nfsv4'</span></span>
    - <span data-ttu-id="f60c8-362">ボリュームの `--creation-token` の名前が `--file-path` に変更されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-362">Volume `--creation-token` renamed to `--file-path`</span></span>
    - <span data-ttu-id="f60c8-363">スナップショット作成日の名前が単に "created" に変更されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-363">Snapshot creation date now named just 'created'</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-364">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-364">Network</span></span>

* <span data-ttu-id="f60c8-365">`az network private-dns link vnet create/update`:テナント間の仮想ネットワーク リンクがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f60c8-365">`az network private-dns link vnet create/update`: Support cross-tenant virtual network linking.</span></span>
* <span data-ttu-id="f60c8-366">[破壊的変更] `az network vnet subnet list`:`--resource-group` と `--vnet-name` を必須に変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-366">[BREAKING CHANGE] `az network vnet subnet list`: Changed `--resource-group` and `--vnet-name` to be required now.</span></span>
* <span data-ttu-id="f60c8-367">`az network public-ip prefix create`:作成時に IP アドレスのバージョン (IPv4、IPv6) を指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-367">`az network public-ip prefix create`: Added support to specify IP address version (IPv4, IPv6) when creation</span></span>
* <span data-ttu-id="f60c8-368">azure-mgmt-network を 7.0.0 に、api-version を 2019-09-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="f60c8-368">Bumped azure-mgmt-network to 7.0.0 and api-version to 2019-09-01</span></span>
* <span data-ttu-id="f60c8-369">`az network vrouter`:新しいサービスの仮想ルーターと仮想ルーター ピアリングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-369">`az network vrouter`: Added support for new service virtual router and virtual router peering</span></span>
* <span data-ttu-id="f60c8-370">`az network express-route gateway connection`:`--internet-security` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-370">`az network express-route gateway connection`: Added support for `--internet-security`</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-371">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-371">Profile</span></span>

* <span data-ttu-id="f60c8-372">`az account get-access-token --resource-type ms-graph` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-372">Fixed `az account get-access-token --resource-type ms-graph` not working</span></span>
* <span data-ttu-id="f60c8-373">`az login` からの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-373">Removed warning from `az login`</span></span>

### <a name="rbac"></a><span data-ttu-id="f60c8-374">RBAC</span><span class="sxs-lookup"><span data-stu-id="f60c8-374">RBAC</span></span>

* <span data-ttu-id="f60c8-375">`az ad app update --id {} --display-name {}` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-375">Fixed `az ad app update --id {} --display-name {}` doesn't work</span></span>

### <a name="servicefabric"></a><span data-ttu-id="f60c8-376">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f60c8-376">ServiceFabric</span></span>

* <span data-ttu-id="f60c8-377">`az sf cluster create`:Service Fabric の Linux と Windows の template.json コンピューティング vmss を標準からマネージド ディスクに変更することによって問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-377">`az sf cluster create`: Fixed an issue by modifying service fabric linux and windows template.json compute vmss from standard to managed disks</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-378">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-378">SQL</span></span>

* <span data-ttu-id="f60c8-379">新しい SQL Database オファリングであるサーバーレス コンピューティング モデルの CRUD 操作をサポートするために、`--compute-model`、`--auto-pause-delay`、および `--min-capacity` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-379">Added `--compute-model`, `--auto-pause-delay`, and `--min-capacity` parameters to support CRUD operations for new SQL Database offering: Serverless compute model.</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-380">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-380">Storage</span></span>

* <span data-ttu-id="f60c8-381">`az storage account create/update`:Azure Files Active Directory Domain Services 認証をサポートするために、--enable-files-adds パラメーターと Azure Active Directory プロパティ引数グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-381">`az storage account create/update`: Added --enable-files-adds parameter and Azure Active Directory Properties Argument group to support Azure Files Active Directory Domain Service Authentication</span></span>
* <span data-ttu-id="f60c8-382">ストレージ アカウントの Kerberos キーの一覧表示または再生成をサポートするために、`az storage account keys list/renew` を拡張しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-382">Expanded `az storage account keys list/renew` to support listing or regenerating Kerberos keys of storage account.</span></span>

## <a name="october-15-2019"></a><span data-ttu-id="f60c8-383">2019 年 10 月 15 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-383">October 15, 2019</span></span>

<span data-ttu-id="f60c8-384">バージョン 2.0.75</span><span class="sxs-lookup"><span data-stu-id="f60c8-384">Version 2.0.75</span></span>

### <a name="aks"></a><span data-ttu-id="f60c8-385">AKS</span><span class="sxs-lookup"><span data-stu-id="f60c8-385">AKS</span></span>

* <span data-ttu-id="f60c8-386">Kubernetes のバージョンでサポートされている場合、`--load-balancer-sku` の既定値を `standard` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-386">Changed `--load-balancer-sku` default value to `standard` if supported by the kubernetes version</span></span>
* <span data-ttu-id="f60c8-387">Kubernetes のバージョンでサポートされている場合、`--vm-set-type` の既定値を `virtualmachinescalesets` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-387">Changed `--vm-set-type` default value to `virtualmachinescalesets` if supported by the kubernetes version</span></span>

### <a name="ams"></a><span data-ttu-id="f60c8-388">AMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-388">AMS</span></span>

* <span data-ttu-id="f60c8-389">[重大な変更]`job start` の名前を `job create` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-389">[BREAKING CHANGE] Changed the name of `job start` to `job create`</span></span>
* <span data-ttu-id="f60c8-390">[重大な変更]`content-key-policy create` の `--ask` パラメーターが UTF8 ではなく 32 文字の 16 進文字列を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-390">[BREAKING CHANGE] Changed the `--ask` parameter of `content-key-policy create` to use a 32-character hex string instead of UTF8</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-391">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-391">AppService</span></span>

* <span data-ttu-id="f60c8-392">コマンド `webapp config access-restriction show|set|add|remove` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-392">Added commands `webapp config access-restriction show|set|add|remove`</span></span>
* <span data-ttu-id="f60c8-393">より優れたエラー処理を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-393">Added better error handling to `webapp up`</span></span>
* <span data-ttu-id="f60c8-394">`Isolated` SKU のサポートを `appservice plan update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-394">Added support for `Isolated` SKU to `appservice plan update`</span></span>

### <a name="arm"></a><span data-ttu-id="f60c8-395">ARM</span><span class="sxs-lookup"><span data-stu-id="f60c8-395">ARM</span></span>

* <span data-ttu-id="f60c8-396">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `deployment create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-396">Added `--handle-extended-json-format` parameter `deployment create` to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="f60c8-397">Compute</span><span class="sxs-lookup"><span data-stu-id="f60c8-397">Compute</span></span>

* <span data-ttu-id="f60c8-398">`--enable-agent` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-398">Added `--enable-agent` parameter to `vm create`</span></span>
* <span data-ttu-id="f60c8-399">ゾーンを使用するときに標準のパブリック IP SKU を自動的に使用するように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-399">Changed `vm create` to use standard public IP SKU automatically when using zones</span></span>
* <span data-ttu-id="f60c8-400">VM の有効なコンピューター名が指定されていない場合に自動的に作成されるように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-400">Changed `vm create` to automatically create a valid computer name for a VM if none is provided</span></span>
* <span data-ttu-id="f60c8-401">VMSS 内の仮想マシンのカスタム コンピューター名プレフィックスをサポートするために `--computer-name-prefix` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-401">Added `--computer-name-prefix` parameter to `vmss create` to support custom computer name prefix of virtual machines in the VMSS</span></span>
* <span data-ttu-id="f60c8-402">ログ分析ワークスペースを自動的に有効にする `--workspace` パラメーターを `vm create` に追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-402">Add `--workspace` parameter to `vm create` to enable log analytics workspace automatically</span></span>
* <span data-ttu-id="f60c8-403">ギャラリーの API バージョンが 2019-07-01 に更新されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-403">Updated galleries API version to 2019-07-01</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-404">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-404">Core</span></span>

* <span data-ttu-id="f60c8-405">汎用の update コマンドで `--set` パラメーターの構文チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-405">Added syntax check for `--set` parameter in generic update command</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-406">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-406">IoT</span></span>

* <span data-ttu-id="f60c8-407">`iot hub show` で "リソースが見つかりません" のエラーが誤って発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-407">Fixed an issue where `iot hub show` would incorrectly error with "resource not found"</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-408">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-408">Monitor</span></span>

* <span data-ttu-id="f60c8-409">CRUD のサポートを `monitor log-analytics workspace` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-409">Added support for CRUD to `monitor log-analytics workspace`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-410">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-410">Network</span></span>

* <span data-ttu-id="f60c8-411">クロステナントの仮想リンクのサポートを `network private-dns link vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-411">Added support for cross-tenant virtual linking to `network private-dns link vnet [create|update]`</span></span>
* <span data-ttu-id="f60c8-412">[重大な変更]`network vnet subnet list` で `--resource-group` および `--vnet-name` パラメーターが必須に変更になりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-412">[BREAKING CHANGE] Changed `network vnet subnet list` to require `--resource-group` and `--vnet-name` parameters</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-413">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-413">SQL</span></span>

* <span data-ttu-id="f60c8-414">マネージ インスタンスの AAD 管理者の設定をサポートするコマンドを `sql mi ad-admin` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-414">Added commands to `sql mi ad-admin` that support setting an AAD administrator on managed instances</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-415">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-415">Storage</span></span>

* <span data-ttu-id="f60c8-416">サービス間のコピー中にアクセス層を保持する `--preserve-s2s-access-tier` パラメーターを `storage copy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-416">Added `--preserve-s2s-access-tier` parameter `storage copy` to preserve access tier during service to service copy</span></span>
* <span data-ttu-id="f60c8-417">ストレージ アカウントで大容量ファイルの共有をサポートするために `--enable-large-file-share` パラメーターを `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-417">Added `--enable-large-file-share` parameter to `storage account [create|update]` to support large file shares for storage account</span></span>

## <a name="september-24-2019"></a><span data-ttu-id="f60c8-418">2019 年 9 月 24 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-418">September 24, 2019</span></span>

<span data-ttu-id="f60c8-419">バージョン 2.0.74</span><span class="sxs-lookup"><span data-stu-id="f60c8-419">Version 2.0.74</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-420">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-420">ACR</span></span>

* <span data-ttu-id="f60c8-421">必須の `--type` パラメーターを `acr config retention update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-421">Added a required `--type` parameter to `acr config retention update`</span></span>
* <span data-ttu-id="f60c8-422">[破壊的変更] `acr config` コマンド グループでパラメーター `--name -n` の名前が `--registry -r ` に変更されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-422">[BREAKING CHNAGE] Renamed parameter `--name -n` changed to `--registry -r ` for `acr config` command group</span></span>

### <a name="aks"></a><span data-ttu-id="f60c8-423">AKS</span><span class="sxs-lookup"><span data-stu-id="f60c8-423">AKS</span></span>

* <span data-ttu-id="f60c8-424">`--load-balancer-sku` パラメーターを `aks create` コマンドに追加しました。これにより、SLB を使用する AKS クラスターを作成できます</span><span class="sxs-lookup"><span data-stu-id="f60c8-424">Added `--load-balancer-sku` parameter to `aks create` command, which allows for creating AKS cluster with SLB</span></span>
* <span data-ttu-id="f60c8-425">`--load-balancer-managed-outbound-ip-count`、`--load-balancer-outbound-ips`、`--load-balancer-outbound-ip-prefixes` パラメーターを `aks [create|update]` コマンドに追加しました。これにより、SLB を使用する AKS クラスターのロード バランサー プロファイルを更新できます</span><span class="sxs-lookup"><span data-stu-id="f60c8-425">Added `--load-balancer-managed-outbound-ip-count`, `--load-balancer-outbound-ips` and `--load-balancer-outbound-ip-prefixes` parameters to `aks [create|update]` commands, which allow for updating load balancer profile of an AKS cluster with SLB</span></span>
* <span data-ttu-id="f60c8-426">`--vm-set-type` パラメーターを `aks create` コマンドに追加しました。これにより、AKS クラスターの VM の種類 (vmas または vmss) を指定できます</span><span class="sxs-lookup"><span data-stu-id="f60c8-426">Added `--vm-set-type` parameter to `aks create` command, which allows to specify vm types of an AKS Cluster (vmas or vmss)</span></span>

### <a name="arm"></a><span data-ttu-id="f60c8-427">ARM</span><span class="sxs-lookup"><span data-stu-id="f60c8-427">ARM</span></span>

* <span data-ttu-id="f60c8-428">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `group deployment create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-428">Added `--handle-extended-json-format` parameter to `group deployment create` command to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="f60c8-429">Compute</span><span class="sxs-lookup"><span data-stu-id="f60c8-429">Compute</span></span>

* <span data-ttu-id="f60c8-430">終了のスケジュール化されたイベントを構成しやすくするために `--terminate-notification-time` パラメーターを `vmss [create|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-430">Added `--terminate-notification-time` parameter to `vmss [create|update]` commands to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="f60c8-431">終了のスケジュール化されたイベントを構成しやすくするために `--enable-terminate-notification` パラメーターを `vmss update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-431">Added `--enable-terminate-notification` parameter to `vmss update` command to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="f60c8-432">`--priority,` `--eviction-policy,` `--max-billing` パラメーターを `[vm|vmss] create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-432">Added `--priority,` `--eviction-policy,` `--max-billing` parameters to `[vm|vmss] create` commands</span></span>
* <span data-ttu-id="f60c8-433">`disk create` を変更し、ディスク アップロードの正確なサイズを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-433">Changed `disk create` to allow specifying the exact size of the disk upload</span></span>
* <span data-ttu-id="f60c8-434">マネージド ディスクの増分スナップショットのサポートを `snapshot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-434">Added support for incremental snapshots for managed disks to `snapshot create`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="f60c8-435">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-435">Cosmos DB</span></span>

* <span data-ttu-id="f60c8-436">キー、読み取り専用キー、または接続文字列を表示する `--type <key-type>` パラメーターを `cosmosdb keys list` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-436">Added `--type <key-type>` parameter to `cosmosdb keys list` command to show key, read only keys or connection strings</span></span>
* <span data-ttu-id="f60c8-437">`cosmosdb keys regenerate` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-437">Added `cosmosdb keys regenerate` command</span></span>
* <span data-ttu-id="f60c8-438">[非推奨]`cosmosdb list-connection-strings`、`cosmosdb regenerate-key`、`cosmosdb list-read-only-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-438">[DEPRECATED] Deprecated `cosmosdb list-connection-strings`, `cosmosdb regenerate-key` and `cosmosdb list-read-only-keys` commands</span></span>

### <a name="eventgrid"></a><span data-ttu-id="f60c8-439">EventGrid</span><span class="sxs-lookup"><span data-stu-id="f60c8-439">EventGrid</span></span>

* <span data-ttu-id="f60c8-440">正しいパラメーターを参照するようにエンドポイントのヘルプ テキストを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-440">Fixed the endpoint help text to refer to the right parameter</span></span>

### <a name="key-vault"></a><span data-ttu-id="f60c8-441">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f60c8-441">Key Vault</span></span>

* <span data-ttu-id="f60c8-442">テナントを使用してログインすると (`login -t`)、`keyvault create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-442">Fixed issue where logging in with a tenant (`login -t`) could cause `keyvault create` to fail</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-443">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-443">Monitor</span></span>

* <span data-ttu-id="f60c8-444">`monitor metrics alert create` の `--condition` 引数で `:` 文字を使用できないという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-444">Fixed issue where `:` character was not allowed in `--condition` argument to `monitor metrics alert create`</span></span>

### <a name="policy"></a><span data-ttu-id="f60c8-445">ポリシー</span><span class="sxs-lookup"><span data-stu-id="f60c8-445">Policy</span></span>

* <span data-ttu-id="f60c8-446">Policy API バージョン 2019-06-01 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-446">Added support for Policy API version 2019-06-01</span></span>
* <span data-ttu-id="f60c8-447">`policy assignment create` コマンドに `--enforcement-mode` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-447">Added `--enforcement-mode` parameter to `policy assignment create` command</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-448">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-448">Storage</span></span>

* <span data-ttu-id="f60c8-449">`az storage copy` コマンドに `--blob-type` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-449">Added `--blob-type` parameter to `az storage copy` command</span></span>

## <a name="september-10-2019"></a><span data-ttu-id="f60c8-450">2019 年 9 月 10 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-450">September 10, 2019</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-451">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-451">ACR</span></span>

* <span data-ttu-id="f60c8-452">アイテム保持ポリシーを構成するためのコマンド グループ `acr config retention` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-452">Added command group `acr config retention` to configure retention policy</span></span>

### <a name="aks"></a><span data-ttu-id="f60c8-453">AKS</span><span class="sxs-lookup"><span data-stu-id="f60c8-453">AKS</span></span>

* <span data-ttu-id="f60c8-454">次のコマンドを使用した ACR 統合のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-454">Added support for ACR integration with the following commands:</span></span>
  * <span data-ttu-id="f60c8-455">AKS クラスターに ACR をアタッチするための `--attach-acr` パラメーターを `aks [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-455">Added `--attach-acr` parameter to `aks [create|update]` to attach an ACR to an AKS cluster</span></span>
  * <span data-ttu-id="f60c8-456">AKS クラスターから ACR をデタッチするための `--detach-acr` パラメーターを `aks update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-456">Added `--detach-acr` parameter to `aks update` to detach the ACR from an AKS cluster</span></span>

### <a name="arm"></a><span data-ttu-id="f60c8-457">ARM</span><span class="sxs-lookup"><span data-stu-id="f60c8-457">ARM</span></span>

* <span data-ttu-id="f60c8-458">API バージョン 2019-05-10 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-458">Updated to use API version 2019-05-10</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-459">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-459">Batch</span></span>

* <span data-ttu-id="f60c8-460">`batch pool create` の `--json-file` に新しい JSON 構成設定を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-460">Added new JSON configuration settings to `--json-file` for `batch pool create`:</span></span>
  * <span data-ttu-id="f60c8-461">ファイル システム マウント用の `MountConfigurations` を追加しました (詳細については https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="f60c8-461">Added `MountConfigurations` for file system mounts (see https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body for details)</span></span>
  * <span data-ttu-id="f60c8-462">プール上のパブリック IP 用に、`NetworkConfiguration` にオプションのプロパティ `publicIPs` を追加しました (詳細については https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="f60c8-462">Added optional property `publicIPs` on `NetworkConfiguration` for public IPs on pools (see https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body for details)</span></span>
* <span data-ttu-id="f60c8-463">共有イメージ ギャラリーのサポートを `--image` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-463">Added support for shared image galleries to `--image`</span></span>
* <span data-ttu-id="f60c8-464">[重大な変更]`batch pool create` の `--start-task-wait-for-success` の既定値を `true` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-464">[BREAKING CHANGE] Changed default value of `--start-task-wait-for-success` on `batch pool create` to be `true`</span></span>
* <span data-ttu-id="f60c8-465">[重大な変更]`AutoUserSpecification` の `Scope` の既定値が常に Pool になるように変更しました (以前は Windows ノードでは `Task`、Linux ノードでは `Pool` でした)</span><span class="sxs-lookup"><span data-stu-id="f60c8-465">[BREAKING CHANGE] Changed default value for `Scope` on `AutoUserSpecification` to always be Pool (was `Task` on Windows nodes, `Pool` on Linux nodes)</span></span>
  * <span data-ttu-id="f60c8-466">この引数は、`--json-file` を使用して JSON 構成からのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-466">This argument can only be set from a JSON configuration with `--json-file`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f60c8-467">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f60c8-467">HDInsight</span></span>

* <span data-ttu-id="f60c8-468">GA リリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-468">GA release</span></span>
* <span data-ttu-id="f60c8-469">[重大な変更]`az hdinsight resize` のパラメーター `--workernode-count/-c` が必須に変更されました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-469">[BREAKING CHANGE] Changed parameter `--workernode-count/-c` of `az hdinsight resize` to be required.</span></span>

### <a name="key-vault"></a><span data-ttu-id="f60c8-470">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f60c8-470">Key Vault</span></span>

* <span data-ttu-id="f60c8-471">ネットワーク ルールからサブネットを削除できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-471">Fixed issue where subnets couldn't be deleted from network rules</span></span>
* <span data-ttu-id="f60c8-472">重複したサブネットと IP アドレスをネットワーク ルールに追加できる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-472">Fixed issue where duplicated subnets and IP addresses could be added to network rules</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-473">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-473">Network</span></span>

* <span data-ttu-id="f60c8-474">トラフィック分析間隔の値を設定する `--interval` パラメーターを `network watcher flow-log` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-474">Added `--interval` parameter to `network watcher flow-log` to set traffic analysis interval value</span></span>
* <span data-ttu-id="f60c8-475">ゲートウェイ ID を管理するための `network application-gateway identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-475">Added `network application-gateway identity` to manage gateway identity</span></span>
* <span data-ttu-id="f60c8-476">Key Vault ID を設定するためのサポートを `network application-gateway ssl-cert` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-476">Added support for setting Key Vault ID to `network application-gateway ssl-cert`</span></span>
* <span data-ttu-id="f60c8-477">`network express-route peering peer-connection [show|list]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-477">Added `network express-route peering peer-connection [show|list]`</span></span>

### <a name="policy"></a><span data-ttu-id="f60c8-478">ポリシー</span><span class="sxs-lookup"><span data-stu-id="f60c8-478">Policy</span></span>

* <span data-ttu-id="f60c8-479">API バージョン 2019-01-01 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-479">Updated to use API version 2019-01-01</span></span>

## <a name="august-27-2019"></a><span data-ttu-id="f60c8-480">2019 年 8 月 27 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-480">August 27, 2019</span></span>

<span data-ttu-id="f60c8-481">バージョン 2.0.72</span><span class="sxs-lookup"><span data-stu-id="f60c8-481">Version 2.0.72</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-482">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-482">ACR</span></span>

* <span data-ttu-id="f60c8-483">[重大な変更]`classic` SKU のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-483">[BREAKING CHANGE] Removed support for the `classic` SKU</span></span>

### <a name="api-management"></a><span data-ttu-id="f60c8-484">API Management</span><span class="sxs-lookup"><span data-stu-id="f60c8-484">API Management</span></span>

* <span data-ttu-id="f60c8-485">[プレビュー] `apim` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-485">[PREVIEW] Added `apim` command group</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-486">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-486">AppService</span></span>

* <span data-ttu-id="f60c8-487">スロットを指定したときの `webapp webjob continuous start` コマンドに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-487">Fixed issue with `webapp webjob continuous start` command when specifying a slot</span></span>
* <span data-ttu-id="f60c8-488">`env` フォルダーを検出してデプロイに使用されているファイルから削除するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-488">Changed `webapp up` to detect `env` folder and remove it from the file used for deployment</span></span>

### <a name="keyvault"></a><span data-ttu-id="f60c8-489">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f60c8-489">Keyvault</span></span>

* <span data-ttu-id="f60c8-490">`--expires` 引数を無視する `keyvault secret set` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-490">Fixed a bug in `keyvault secret set` that igored the `--expires` argument</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-491">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-491">Network</span></span>

* <span data-ttu-id="f60c8-492">`--private-ip-address-version` 引数に IPv6 アドレスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-492">Added support for IPv6 addresses to `--private-ip-address-version` arguments</span></span>
* <span data-ttu-id="f60c8-493">プライベート エンドポイントの管理用に新しいコマンド `network private-endpoint [create|update|list-types]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-493">Added new commands `network private-endpoint [create|update|list-types]` for private endpoint management</span></span>
* <span data-ttu-id="f60c8-494">コマンド グループ `network private-link-service` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-494">Added command group `network private-link-service`</span></span>
* <span data-ttu-id="f60c8-495">`--private-endpoint-network-policies` 引数と `--private-link-service-network-policies` 引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-495">Added `--private-endpoint-network-policies` and `--private-link-service-network-policies` arguments to `network vnet subnet update`</span></span>

### <a name="rbac"></a><span data-ttu-id="f60c8-496">RBAC</span><span class="sxs-lookup"><span data-stu-id="f60c8-496">RBAC</span></span>

* <span data-ttu-id="f60c8-497">ホームページが更新されない `ad app update --homepage` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-497">Fixed issue with `ad app update --homepage` where homepage would not be updated</span></span>

### <a name="servicefabric"></a><span data-ttu-id="f60c8-498">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f60c8-498">ServiceFabric</span></span>

* <span data-ttu-id="f60c8-499">キー コンテナーの大文字と小文字が混在する名前のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-499">Added support for mixed-case Key Vault names</span></span>
* <span data-ttu-id="f60c8-500">Key Vault で証明書を使用したときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-500">Fixed issue when using certificates in Key Vault</span></span>
* <span data-ttu-id="f60c8-501">PFX 証明書ファイルの使用に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-501">Fixed issue with using PFX certificate files</span></span>
* <span data-ttu-id="f60c8-502">Key Vault リソースグループが指定されていなかったときの `sf cluster certificate add` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-502">Fixed issue with `sf cluster certificate add` when Key Vault resource group wasn't specified</span></span>
* <span data-ttu-id="f60c8-503">`sf cluster set` が動作しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-503">Fixed issue with `sf cluster set` not working</span></span>

### <a name="signalr"></a><span data-ttu-id="f60c8-504">SignalR</span><span class="sxs-lookup"><span data-stu-id="f60c8-504">SignalR</span></span>

* <span data-ttu-id="f60c8-505">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-505">Added new commands:</span></span>
  * <span data-ttu-id="f60c8-506">`signalr cors`:SignalR CORS の管理</span><span class="sxs-lookup"><span data-stu-id="f60c8-506">`signalr cors`: Manage SignalR CORS</span></span>
  * <span data-ttu-id="f60c8-507">`signalr restart`:SignalR Service の再起動</span><span class="sxs-lookup"><span data-stu-id="f60c8-507">`signalr restart`: Restart a SignalR service</span></span>
  * <span data-ttu-id="f60c8-508">`signalr update`:SignalR Service の更新</span><span class="sxs-lookup"><span data-stu-id="f60c8-508">`signalr update`: Update a SignalR service</span></span>
* <span data-ttu-id="f60c8-509">`--service-mode` 引数を `signalr create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-509">Added `--service-mode` argument to `signalr create`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-510">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-510">Storage</span></span>

* <span data-ttu-id="f60c8-511">`storage account revoke-delegation-keys` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-511">Added `storage account revoke-delegation-keys` command</span></span>

## <a name="august-13-2019"></a><span data-ttu-id="f60c8-512">2019 年 8 月 13 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-512">August 13, 2019</span></span>

<span data-ttu-id="f60c8-513">バージョン 2.0.71</span><span class="sxs-lookup"><span data-stu-id="f60c8-513">Version 2.0.71</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-514">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-514">AppService</span></span>

* <span data-ttu-id="f60c8-515">`webapp webjob continuous` コマンドがスロットで失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-515">Fixed issue where `webapp webjob continuous` commands were failing for slots</span></span>

### <a name="botservice"></a><span data-ttu-id="f60c8-516">BotService</span><span class="sxs-lookup"><span data-stu-id="f60c8-516">BotService</span></span>

* <span data-ttu-id="f60c8-517">[重大な変更] v3 SDK ボットの作成のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-517">[BREAKING CHANGE] Removed support for creating v3 SDK bots</span></span>

### <a name="cognitiveservices"></a><span data-ttu-id="f60c8-518">CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f60c8-518">CognitiveServices</span></span>

* <span data-ttu-id="f60c8-519">`cognitiveservices account network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-519">Added `cognitiveservices account network-rule` commands</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="f60c8-520">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-520">Cosmos DB</span></span>

* <span data-ttu-id="f60c8-521">複数の書き込み場所を更新するときの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-521">Removed warning when updating multiple write locations</span></span>
* <span data-ttu-id="f60c8-522">CosmosDB SQL、MongoDB、Cassandra、Gremlin、およびテーブル リソースとリソースのスループットのための CRUD コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-522">Added CRUD commands for CosmosDB SQL, MongoDB, Cassandra, Gremlin and Table resources and resource's throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f60c8-523">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f60c8-523">HDInsight</span></span>

<span data-ttu-id="f60c8-524">このリリースには、多数の破壊的変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f60c8-524">This release contains a large number of breaking changes.</span></span>

* <span data-ttu-id="f60c8-525">[重大な変更]`hdinsight create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-525">[BREAKING CHANGE] Renamed parameters for `hdinsight create`:</span></span>
  * <span data-ttu-id="f60c8-526">`--storage-default-container` から `--storage-container` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-526">Renamed `--storage-default-container` to `--storage-container`</span></span>
  * <span data-ttu-id="f60c8-527">`--storage-default-filesystem` から `--storage-filesystem` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-527">Renamed `--storage-default-filesystem` to `--storage-filesystem`</span></span>
* <span data-ttu-id="f60c8-528">[重大な変更]`application create` の `--name` 引数が、クラスター名の代わりにアプリケーション名を表すように変更されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-528">[BREAKING CHANGE] Changed the `--name` argument of `application create` to represent the application name instead of the cluster name</span></span>
* <span data-ttu-id="f60c8-529">`--cluster-name` 引数が `application create` に追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-529">Added `--cluster-name` argument to `application create` to replace old `--name` functionality</span></span>
* <span data-ttu-id="f60c8-530">[重大な変更]`application create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-530">[BREAKING CHANGE] Renamed parameters for `application create`:</span></span>
  * <span data-ttu-id="f60c8-531">`--application-type` から `--type` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-531">Renamed `--application-type` to `--type`</span></span>
  * <span data-ttu-id="f60c8-532">`--marketplace-identifier` から `--marketplace-id` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-532">Renamed `--marketplace-identifier` to `--marketplace-id`</span></span>
  * <span data-ttu-id="f60c8-533">`--https-endpoint-access-mode` から `--access-mode` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-533">Renamed `--https-endpoint-access-mode` to `--access-mode`</span></span>
  * <span data-ttu-id="f60c8-534">`--https-endpoint-destination-port` の名前を `--destination-port` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-534">Renamed  `--https-endpoint-destination-port` to `--destination-port`</span></span>
* <span data-ttu-id="f60c8-535">[重大な変更]`application create` のパラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-535">[BREAKING CHANGE] Removed parameters for `application create`:</span></span>
  * `--https-endpoint-location`
  * `--https-endpoint-public-port`
  * `--ssh-endpoint-destination-port`
  * `--ssh-endpoint-location`
  * `--ssh-endpoint-public-port`
* <span data-ttu-id="f60c8-536">[破壊的変更] `hdinsight resize`の `--target-instance-count` の名前を `--workernode-count` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-536">[BREAKING CHNAGE] Renamed `--target-instance-count` to `--workernode-count` for `hdinsight resize`</span></span>
* <span data-ttu-id="f60c8-537">[重大な変更]`hdinsight script-action` グループのすべてのコマンドが、スクリプト アクションの名前として `--name` パラメーターを使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-537">[BREAKING CHANGE] Changed all commands in the `hdinsight script-action` group to use the `--name` parameter as the name of the script action.</span></span>
* <span data-ttu-id="f60c8-538">`--cluster-name` 引数がすべての `hdinsight script-action` コマンドに追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-538">Added `--cluster-name` argument to all `hdinsight script-action` commands to replace old `--name` functionality</span></span>
* <span data-ttu-id="f60c8-539">[重大な変更] すべての `hdinsight script-action` コマンドで `--script-execution-id` の名前を `--execution-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-539">[BREAKING CHANGE] Renamed `--script-execution-id` to `--execution-id` for all `hdinsight script-action` commands</span></span>
* <span data-ttu-id="f60c8-540">[重大な変更] 名前を `hdinsight script-action show` から `hdinsight script-action show-execution-details` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-540">[BREAKING CHANGE] Renamed `hdinsight script-action show` to `hdinsight script-action show-execution-details`</span></span>
* <span data-ttu-id="f60c8-541">[破壊的変更] `hdinsight script-action execute --roles` に対するパラメーターを、コンマ区切りではなくスペース区切りにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-541">[BREAKING CHNAGE] Changed parameters to `hdinsight script-action execute --roles` to be space-separated instead of comma-separated</span></span>
* <span data-ttu-id="f60c8-542">[重大な変更]`hdinsight script-action list`の `--persisted` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-542">[BREAKING CHANGE] Removed the `--persisted` parameter of `hdinsight script-action list`</span></span>
* <span data-ttu-id="f60c8-543">ローカル JSON ファイルへのパスまたは JSON 文字列を受け入れるように `hdinsight create --cluster-configurations` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-543">Changed the `hdinsight create --cluster-configurations` parameter to accept a path to a local JSON file or a JSON string</span></span>
* <span data-ttu-id="f60c8-544">`hdinsight script-action list-execution-history` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-544">Added command `hdinsight script-action list-execution-history`</span></span>
* <span data-ttu-id="f60c8-545">Log Analytics ワークスペース ID またはワークスペース名を受け入れるように `hdinsight monitor enable --workspace` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-545">Changed `hdinsight monitor enable --workspace` to accept a Log Analytics workspace ID or workspace name</span></span>
* <span data-ttu-id="f60c8-546">`hdinsight monitor enable --primary-key` 引数を追加しました。これは、ワークスペース ID がパラメーターとして指定されている場合に必要です</span><span class="sxs-lookup"><span data-stu-id="f60c8-546">Added the `hdinsight monitor enable --primary-key` argument, which is needed if a workspace ID is provided as the parameter</span></span>
* <span data-ttu-id="f60c8-547">例をさらに追加し、ヘルプ メッセージの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-547">Added more examples and updated descriptions for help messages</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-548">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-548">Interactive</span></span>

* <span data-ttu-id="f60c8-549">読み込みエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-549">Fixed a loading error</span></span>

### <a name="kubernetes"></a><span data-ttu-id="f60c8-550">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="f60c8-550">Kubernetes</span></span>

* <span data-ttu-id="f60c8-551">ダッシュボードのコンテナー ポートで `https` が使用されている場合に `https` を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-551">Changed to use `https` if dashboard container port is using `https`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-552">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-552">Network</span></span>

* <span data-ttu-id="f60c8-553">`--yes` 引数を `network dns record-set cname delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-553">Added `--yes` argument `network dns record-set cname delete`</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-554">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-554">Profile</span></span>

* <span data-ttu-id="f60c8-555">リソースのアクセス トークンを取得するための `account get-access-token` に `--resource-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-555">Added `--resource-type` argument to `account get-access-token` to get resource access tokens</span></span>

### <a name="servicefabric"></a><span data-ttu-id="f60c8-556">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f60c8-556">ServiceFabric</span></span>

* <span data-ttu-id="f60c8-557">sf cluster create でサポートされているすべての OS バージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-557">Added all supported os version for sf cluster create</span></span>
* <span data-ttu-id="f60c8-558">プライマリ証明書の検証のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-558">Fixed primary certificate validation bug</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-559">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-559">Storage</span></span>

* <span data-ttu-id="f60c8-560">`storage copy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-560">Added command `storage copy`</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="f60c8-561">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-561">July 30, 2019</span></span>

<span data-ttu-id="f60c8-562">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="f60c8-562">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-563">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-563">ACR</span></span>

* <span data-ttu-id="f60c8-564">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-564">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="f60c8-565">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-565">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-566">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-566">Appservice</span></span>

* <span data-ttu-id="f60c8-567">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-567">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="f60c8-568">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-568">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="f60c8-569">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-569">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-570">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-570">Network</span></span>

* <span data-ttu-id="f60c8-571">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="f60c8-571">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="f60c8-572">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-572">Fixes #9604.</span></span> <span data-ttu-id="f60c8-573">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-573">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="f60c8-574">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="f60c8-574">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="f60c8-575">RBAC</span><span class="sxs-lookup"><span data-stu-id="f60c8-575">RBAC</span></span>

* <span data-ttu-id="f60c8-576">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-576">Added `user update` command</span></span>
* <span data-ttu-id="f60c8-577">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-577">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="f60c8-578">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="f60c8-578">Use replacement argument `--id`</span></span>
* <span data-ttu-id="f60c8-579">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-579">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-580">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-580">SQL</span></span>

* <span data-ttu-id="f60c8-581">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-581">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-582">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-582">Storage</span></span>

* <span data-ttu-id="f60c8-583">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-583">Added `storage remove` command</span></span>
* <span data-ttu-id="f60c8-584">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-584">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-585">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-585">VM</span></span>

* <span data-ttu-id="f60c8-586">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-586">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="f60c8-587">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-587">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="f60c8-588">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-588">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="f60c8-589">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-589">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="f60c8-590">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-590">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="f60c8-591">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-591">July 16, 2019</span></span>

<span data-ttu-id="f60c8-592">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="f60c8-592">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-593">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-593">Appservice</span></span>

* <span data-ttu-id="f60c8-594">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-594">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="f60c8-595">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-595">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="f60c8-596">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-596">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-597">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-597">Core</span></span>

* <span data-ttu-id="f60c8-598">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-598">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-599">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-599">Batch</span></span>

* <span data-ttu-id="f60c8-600">[重大な変更]`batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="f60c8-600">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="f60c8-601">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-601">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="f60c8-602">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-602">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="f60c8-603">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-603">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="f60c8-604">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="f60c8-604">Eventhubs</span></span>

* <span data-ttu-id="f60c8-605">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-605">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-606">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-606">RDBMS</span></span>

* <span data-ttu-id="f60c8-607">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-607">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="f60c8-608">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-608">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="f60c8-609">リレー</span><span class="sxs-lookup"><span data-stu-id="f60c8-609">Relay</span></span>

* <span data-ttu-id="f60c8-610">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="f60c8-610">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="f60c8-611">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-611">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="f60c8-612">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f60c8-612">Servicebus</span></span>

* <span data-ttu-id="f60c8-613">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-613">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-614">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-614">Storage</span></span>

* <span data-ttu-id="f60c8-615">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="f60c8-615">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="f60c8-616">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="f60c8-616">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="f60c8-617">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-617">July 2, 2019</span></span>

<span data-ttu-id="f60c8-618">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="f60c8-618">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-619">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-619">Core</span></span>

* <span data-ttu-id="f60c8-620">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-620">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="f60c8-621">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-621">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="f60c8-622">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-622">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-623">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-623">ACR</span></span>

* <span data-ttu-id="f60c8-624">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-624">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-625">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-625">Appservice</span></span>

* <span data-ttu-id="f60c8-626">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-626">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="f60c8-627">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-627">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="f60c8-628">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="f60c8-628">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="f60c8-629">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-629">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="f60c8-630">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-630">Cosmos DB</span></span>

* <span data-ttu-id="f60c8-631">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-631">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="f60c8-632">DLS</span><span class="sxs-lookup"><span data-stu-id="f60c8-632">DLS</span></span>

* <span data-ttu-id="f60c8-633">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="f60c8-633">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="f60c8-634">フィードバック</span><span class="sxs-lookup"><span data-stu-id="f60c8-634">Feedback</span></span>

* <span data-ttu-id="f60c8-635">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-635">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f60c8-636">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f60c8-636">HDInsight</span></span>

* <span data-ttu-id="f60c8-637">[重大な変更]`oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-637">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="f60c8-638">[重大な変更]`--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-638">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="f60c8-639">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-639">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="f60c8-640">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-640">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="f60c8-641">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-641">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="f60c8-642">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-642">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="f60c8-643">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-643">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="f60c8-644">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-644">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="f60c8-645">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-645">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="f60c8-646">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="f60c8-646">Managed Services</span></span>

* <span data-ttu-id="f60c8-647">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="f60c8-647">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-648">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-648">Profile</span></span>
* <span data-ttu-id="f60c8-649">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="f60c8-649">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="f60c8-650">RBAC</span><span class="sxs-lookup"><span data-stu-id="f60c8-650">RBAC</span></span>

* <span data-ttu-id="f60c8-651">[重大な変更]`create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-651">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="f60c8-652">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-652">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="f60c8-653">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-653">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="f60c8-654">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-654">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-655">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-655">RDBMS</span></span>

* <span data-ttu-id="f60c8-656">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-656">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-657">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-657">SQL</span></span>

* <span data-ttu-id="f60c8-658">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-658">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-659">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-659">Storage</span></span>

* <span data-ttu-id="f60c8-660">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-660">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="f60c8-661">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-661">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="f60c8-662">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-662">VM</span></span>

* <span data-ttu-id="f60c8-663">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-663">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="f60c8-664">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-664">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="f60c8-665">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-665">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="f60c8-666">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-666">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="f60c8-667">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-667">June 18, 2019</span></span>

<span data-ttu-id="f60c8-668">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="f60c8-668">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-669">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-669">Core</span></span>

<span data-ttu-id="f60c8-670">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-670">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="f60c8-671">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-671">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="f60c8-672">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="f60c8-672">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="f60c8-673">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="f60c8-673">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="f60c8-674">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-674">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="f60c8-675">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="f60c8-675">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="f60c8-676">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="f60c8-676">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-677">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-677">ACR</span></span>
* <span data-ttu-id="f60c8-678">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-678">Added 'acr check-health' command</span></span>
* <span data-ttu-id="f60c8-679">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-679">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-680">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-680">ACS</span></span>
* <span data-ttu-id="f60c8-681">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-681">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="f60c8-682">AMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-682">AMS</span></span>
* <span data-ttu-id="f60c8-683">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-683">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-684">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-684">AppService</span></span>
* <span data-ttu-id="f60c8-685">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-685">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="f60c8-686">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-686">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="f60c8-687">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-687">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="f60c8-688">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-688">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="f60c8-689">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-689">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="f60c8-690">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-690">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-691">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-691">Batch</span></span>
* <span data-ttu-id="f60c8-692">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-692">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="f60c8-693">BatchAI</span><span class="sxs-lookup"><span data-stu-id="f60c8-693">BatchAI</span></span>
* <span data-ttu-id="f60c8-694">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-694">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="f60c8-695">BotService</span><span class="sxs-lookup"><span data-stu-id="f60c8-695">BotService</span></span>
* <span data-ttu-id="f60c8-696">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-696">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-697">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-697">CosmosDB</span></span>
* <span data-ttu-id="f60c8-698">[非推奨]`cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-698">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="f60c8-699">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="f60c8-699">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="f60c8-700">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-700">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="f60c8-701">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-701">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="f60c8-702">EventGrid</span><span class="sxs-lookup"><span data-stu-id="f60c8-702">EventGrid</span></span>
* <span data-ttu-id="f60c8-703">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-703">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="f60c8-704">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-704">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="f60c8-705">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-705">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="f60c8-706">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-706">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="f60c8-707">[重大な変更]`eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-707">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f60c8-708">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f60c8-708">HDInsight</span></span>
* <span data-ttu-id="f60c8-709">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-709">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-710">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-710">IoT</span></span>
* <span data-ttu-id="f60c8-711">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-711">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="f60c8-712">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-712">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-713">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-713">Network</span></span>
* <span data-ttu-id="f60c8-714">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-714">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="f60c8-715">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-715">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="f60c8-716">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-716">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="f60c8-717">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-717">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-718">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-718">Resource</span></span>
* <span data-ttu-id="f60c8-719">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-719">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="f60c8-720">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-720">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="f60c8-721">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f60c8-721">ServiceBus</span></span>
* <span data-ttu-id="f60c8-722">`servicebus topic create --max-size` での問題 [#9319](https://github.com/azure/azure-cli/issues/9319) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-722">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-723">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-723">SQL</span></span>
* <span data-ttu-id="f60c8-724">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-724">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="f60c8-725">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-725">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="f60c8-726">SQLVm</span><span class="sxs-lookup"><span data-stu-id="f60c8-726">SQLVm</span></span>
* <span data-ttu-id="f60c8-727">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-727">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="f60c8-728">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-728">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-729">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-729">Storage</span></span>
* <span data-ttu-id="f60c8-730">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-730">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="f60c8-731">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-731">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-732">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-732">VM</span></span>
* <span data-ttu-id="f60c8-733">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-733">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="f60c8-734">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-734">June 4, 2019</span></span>

<span data-ttu-id="f60c8-735">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="f60c8-735">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-736">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-736">Core</span></span>
* <span data-ttu-id="f60c8-737">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-737">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-738">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-738">ACR</span></span>
* <span data-ttu-id="f60c8-739">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-739">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-740">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-740">ACS</span></span>
* <span data-ttu-id="f60c8-741">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-741">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="f60c8-742">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-742">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-743">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-743">Batch</span></span>
* <span data-ttu-id="f60c8-744">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-744">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-745">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-745">IoT</span></span>
* <span data-ttu-id="f60c8-746">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-746">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-747">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-747">Network</span></span>
* <span data-ttu-id="f60c8-748">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-748">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="f60c8-749">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-749">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="f60c8-750">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-750">Resource</span></span>
* <span data-ttu-id="f60c8-751">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-751">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-752">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-752">Role</span></span>
* <span data-ttu-id="f60c8-753">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-753">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="f60c8-754">Compute</span><span class="sxs-lookup"><span data-stu-id="f60c8-754">Compute</span></span>
* <span data-ttu-id="f60c8-755">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-755">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="f60c8-756">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-756">May 21, 2019</span></span>

<span data-ttu-id="f60c8-757">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="f60c8-757">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-758">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-758">Core</span></span>
* <span data-ttu-id="f60c8-759">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-759">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="f60c8-760">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-760">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="f60c8-761">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-761">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-762">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-762">ACR</span></span>
* <span data-ttu-id="f60c8-763">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-763">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-764">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-764">ACS</span></span>
* <span data-ttu-id="f60c8-765">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-765">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-766">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-766">AppService</span></span>
* <span data-ttu-id="f60c8-767">[非推奨]`functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-767">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="f60c8-768">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-768">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="f60c8-769">[重大な変更]`--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="f60c8-769">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="f60c8-770">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-770">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="f60c8-771">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-771">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="f60c8-772">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-772">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="f60c8-773">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-773">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="f60c8-774">BotService</span><span class="sxs-lookup"><span data-stu-id="f60c8-774">BotService</span></span>
* <span data-ttu-id="f60c8-775">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-775">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="f60c8-776">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-776">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="f60c8-777">従量課金</span><span class="sxs-lookup"><span data-stu-id="f60c8-777">Consumption</span></span>
* <span data-ttu-id="f60c8-778">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-778">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-779">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-779">IoT</span></span>
* <span data-ttu-id="f60c8-780">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-780">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-781">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-781">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="f60c8-783">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-783">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="f60c8-784">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-784">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-785">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-785">RDBMS</span></span>
* <span data-ttu-id="f60c8-786">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-786">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="f60c8-787">RBAC</span><span class="sxs-lookup"><span data-stu-id="f60c8-787">RBAC</span></span>
* <span data-ttu-id="f60c8-788">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-788">Added support for management group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-789">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-789">Storage</span></span>
* <span data-ttu-id="f60c8-790">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="f60c8-790">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="f60c8-791">Compute</span><span class="sxs-lookup"><span data-stu-id="f60c8-791">Compute</span></span>
* <span data-ttu-id="f60c8-792">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-792">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="f60c8-793">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-793">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="f60c8-794">__注__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-794">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="f60c8-795">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-795">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="f60c8-796">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-796">May 6, 2019</span></span>

<span data-ttu-id="f60c8-797">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="f60c8-797">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-798">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-798">ACS</span></span>
* <span data-ttu-id="f60c8-799">[重大な変更]`--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-799">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="f60c8-800">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-800">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="f60c8-801">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-801">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="f60c8-802">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-802">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-803">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-803">Appservice</span></span>
* <span data-ttu-id="f60c8-804">[非推奨]`functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-804">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="f60c8-805">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-805">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="f60c8-806">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-806">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="f60c8-807">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-807">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="f60c8-808">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-808">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="f60c8-809">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-809">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="f60c8-810">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-810">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="f60c8-811">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-811">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="f60c8-812">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-812">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="f60c8-813">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-813">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-814">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-814">Batch</span></span>
* <span data-ttu-id="f60c8-815">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-815">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="f60c8-816">Botservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-816">Botservice</span></span>
* <span data-ttu-id="f60c8-817">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="f60c8-817">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="f60c8-818">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-818">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="f60c8-819">[重大な変更]`--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-819">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="f60c8-820">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-820">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="f60c8-821">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-821">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="f60c8-822">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-822">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="f60c8-823">[重大な変更]`bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-823">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="f60c8-824">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-824">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="f60c8-825">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-825">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="f60c8-826">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-826">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="f60c8-827">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-827">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="f60c8-828">[重大な変更]`Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-828">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="f60c8-829">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-829">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="f60c8-830">[重大な変更]`SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-830">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="f60c8-831">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="f60c8-831">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="f60c8-832">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-832">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="f60c8-833">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-833">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="f60c8-834">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-834">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="f60c8-835">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-835">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="f60c8-836">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-836">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="f60c8-837">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-837">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="f60c8-838">[構成]</span><span class="sxs-lookup"><span data-stu-id="f60c8-838">Configure</span></span>
* <span data-ttu-id="f60c8-839">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-839">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="f60c8-840">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="f60c8-840">Eventhubs</span></span>
* <span data-ttu-id="f60c8-841">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-841">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="f60c8-842">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-842">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-843">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-843">Network</span></span>
* <span data-ttu-id="f60c8-844">[重大な変更]`vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="f60c8-844">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="f60c8-845">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="f60c8-845">Policy Insights</span></span>
* <span data-ttu-id="f60c8-846">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-846">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-847">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-847">Role</span></span>
* <span data-ttu-id="f60c8-848">[非推奨]`create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-848">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="f60c8-849">Service Bus</span><span class="sxs-lookup"><span data-stu-id="f60c8-849">Service Bus</span></span>
* <span data-ttu-id="f60c8-850">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-850">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="f60c8-851">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-851">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="f60c8-852">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-852">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-853">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-853">SQL</span></span>
* <span data-ttu-id="f60c8-854">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-854">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-855">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-855">VM</span></span>
* <span data-ttu-id="f60c8-856">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-856">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="f60c8-857">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-857">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="f60c8-858">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-858">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="f60c8-859">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-859">Added new `ppg` command group for managing Proximity Placement Groups</span></span>
* <span data-ttu-id="f60c8-860">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-860">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="f60c8-861">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-861">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="f60c8-862">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-862">April 23, 2019</span></span>

<span data-ttu-id="f60c8-863">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="f60c8-863">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-864">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-864">ACS</span></span>
* <span data-ttu-id="f60c8-865">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-865">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="f60c8-866">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-866">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="f60c8-867">AMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-867">AMS</span></span>
* <span data-ttu-id="f60c8-868">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-868">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-869">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-869">AppService</span></span>
* <span data-ttu-id="f60c8-870">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-870">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="f60c8-871">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-871">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="f60c8-872">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-872">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="f60c8-873">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-873">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="f60c8-874">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-874">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="f60c8-875">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-875">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="f60c8-876">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-876">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="f60c8-877">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-877">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="f60c8-878">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-878">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="f60c8-879">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="f60c8-879">Deployment Manager</span></span>
* <span data-ttu-id="f60c8-880">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="f60c8-880">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="f60c8-881">ラボ</span><span class="sxs-lookup"><span data-stu-id="f60c8-881">Lab</span></span>
* <span data-ttu-id="f60c8-882">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-882">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-883">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-883">Network</span></span>
* <span data-ttu-id="f60c8-884">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-884">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-885">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-885">Resource</span></span>
* <span data-ttu-id="f60c8-886">[非推奨]`resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-886">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="f60c8-887">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-887">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="f60c8-888">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-888">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="f60c8-889">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-889">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-890">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-890">SQL</span></span>
* <span data-ttu-id="f60c8-891">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-891">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="f60c8-892">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-892">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="f60c8-893">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-893">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="f60c8-894">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-894">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-895">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-895">Storage</span></span>
* <span data-ttu-id="f60c8-896">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-896">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-897">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-897">VM</span></span>
* <span data-ttu-id="f60c8-898">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-898">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="f60c8-899">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-899">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="f60c8-900">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-900">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="f60c8-901">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-901">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-902">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-902">Core</span></span>
* <span data-ttu-id="f60c8-903">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-903">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-904">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-904">ACR</span></span>
* <span data-ttu-id="f60c8-905">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-905">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="f60c8-906">AMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-906">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="f60c8-909">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-909">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="f60c8-910">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-910">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-911">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-911">AppService</span></span>
* <span data-ttu-id="f60c8-912">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-912">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="f60c8-913">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-913">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="f60c8-914">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-914">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="f60c8-915">[重大な変更]`devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-915">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="f60c8-916">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-916">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="f60c8-917">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-917">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="f60c8-918">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-918">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="f60c8-919">CDN</span><span class="sxs-lookup"><span data-stu-id="f60c8-919">CDN</span></span>
* <span data-ttu-id="f60c8-920">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-920">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="f60c8-921">フィードバック</span><span class="sxs-lookup"><span data-stu-id="f60c8-921">Feedback</span></span>
* <span data-ttu-id="f60c8-922">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-922">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="f60c8-923">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-923">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="f60c8-924">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-924">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-925">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-925">Monitor</span></span>
* <span data-ttu-id="f60c8-926">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-926">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="f60c8-927">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-927">Network</span></span>
* <span data-ttu-id="f60c8-928">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-928">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="f60c8-929">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-929">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="f60c8-930">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-930">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="f60c8-931">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-931">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="f60c8-932">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="f60c8-932">PrivateDNS</span></span>
* <span data-ttu-id="f60c8-933">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-933">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-934">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-934">Resource</span></span>
* <span data-ttu-id="f60c8-935">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-935">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-936">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-936">Role</span></span>
* <span data-ttu-id="f60c8-937">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-937">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="f60c8-938">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-938">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-939">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-939">SQL</span></span>
* <span data-ttu-id="f60c8-940">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-940">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-941">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-941">Storage</span></span>
* <span data-ttu-id="f60c8-942">[重大な変更]`storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-942">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="f60c8-943">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-943">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="f60c8-944">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-944">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="f60c8-945">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-945">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="f60c8-946">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-946">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="f60c8-947">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-947">Core</span></span>
* <span data-ttu-id="f60c8-948">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-948">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="f60c8-949">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-949">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="f60c8-950">クラウド</span><span class="sxs-lookup"><span data-stu-id="f60c8-950">Cloud</span></span>
* <span data-ttu-id="f60c8-951">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-951">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-952">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-952">ACR</span></span>
* <span data-ttu-id="f60c8-953">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-953">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="f60c8-954">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-954">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="f60c8-955">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-955">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="f60c8-956">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-956">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-957">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-957">AppService</span></span>
* <span data-ttu-id="f60c8-958">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-958">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="f60c8-959">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-959">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="f60c8-960">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="f60c8-960">BOT Service</span></span>
* <span data-ttu-id="f60c8-961">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-961">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="f60c8-962">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-962">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="f60c8-963">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-963">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="f60c8-964">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-964">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="f60c8-965">CDN</span><span class="sxs-lookup"><span data-stu-id="f60c8-965">CDN</span></span>
* <span data-ttu-id="f60c8-966">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-966">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="f60c8-968">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-968">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="f60c8-969">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-969">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-970">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="f60c8-970">Cosmosdb</span></span>
* <span data-ttu-id="f60c8-971">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-971">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="f60c8-972">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-972">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-973">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-973">Interactive</span></span>
* <span data-ttu-id="f60c8-974">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-974">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-975">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-975">Monitor</span></span>
* <span data-ttu-id="f60c8-976">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-976">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-977">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-977">Network</span></span>
* <span data-ttu-id="f60c8-978">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-978">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-979">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-979">Profile</span></span>
* <span data-ttu-id="f60c8-980">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-980">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="f60c8-981">Postgres</span><span class="sxs-lookup"><span data-stu-id="f60c8-981">Postgres</span></span> 
* <span data-ttu-id="f60c8-982">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-982">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="f60c8-983">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="f60c8-983">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-984">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-984">Resource</span></span>
* <span data-ttu-id="f60c8-985">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-985">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="f60c8-986">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-986">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="f60c8-987">グラフ</span><span class="sxs-lookup"><span data-stu-id="f60c8-987">Graph</span></span>
* <span data-ttu-id="f60c8-988">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-988">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="f60c8-989">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-989">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="f60c8-990">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-990">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="f60c8-991">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-991">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="f60c8-992">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-992">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-993">storage</span><span class="sxs-lookup"><span data-stu-id="f60c8-993">storage</span></span>
* <span data-ttu-id="f60c8-994">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-994">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="f60c8-995">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-995">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="f60c8-996">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-996">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="f60c8-997">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-997">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-998">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-998">VM</span></span>
* <span data-ttu-id="f60c8-999">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-999">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="f60c8-1000">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1000">March 12, 2019</span></span>

<span data-ttu-id="f60c8-1001">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="f60c8-1001">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1002">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1002">Core</span></span>

* <span data-ttu-id="f60c8-1003">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1003">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1004">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1004">ACR</span></span>

* <span data-ttu-id="f60c8-1005">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1005">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1006">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1006">ACS</span></span>

* <span data-ttu-id="f60c8-1007">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1007">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="f60c8-1008">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1008">AppService</span></span>

* <span data-ttu-id="f60c8-1009">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1009">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="f60c8-1010">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1010">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="f60c8-1011">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1011">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="f60c8-1012">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1012">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="f60c8-1013">Botservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1013">Botservice</span></span>

* <span data-ttu-id="f60c8-1014">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1014">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="f60c8-1015">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1015">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="f60c8-1016">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1016">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="f60c8-1017">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1017">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-1018">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1018">Container</span></span>

* <span data-ttu-id="f60c8-1019">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1019">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="f60c8-1020">EventHub</span><span class="sxs-lookup"><span data-stu-id="f60c8-1020">EventHub</span></span>

* <span data-ttu-id="f60c8-1021">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1021">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="f60c8-1022">Find</span><span class="sxs-lookup"><span data-stu-id="f60c8-1022">Find</span></span>

* <span data-ttu-id="f60c8-1023">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="f60c8-1023">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f60c8-1024">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f60c8-1024">HDInsight</span></span>

* <span data-ttu-id="f60c8-1025">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1025">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1026">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1026">Network</span></span>

* <span data-ttu-id="f60c8-1027">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1027">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-1028">Rdbms</span><span class="sxs-lookup"><span data-stu-id="f60c8-1028">Rdbms</span></span>

* <span data-ttu-id="f60c8-1029">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1029">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1030">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1030">Role</span></span>

* <span data-ttu-id="f60c8-1031">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1031">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="f60c8-1032">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1032">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="f60c8-1033">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f60c8-1033">Service Fabric</span></span>

* <span data-ttu-id="f60c8-1034">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1034">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="f60c8-1035">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1035">February 26, 2019</span></span>

<span data-ttu-id="f60c8-1036">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="f60c8-1036">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1037">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1037">Core</span></span>

* <span data-ttu-id="f60c8-1038">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1038">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1039">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1039">ACR</span></span>

* <span data-ttu-id="f60c8-1040">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1040">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="f60c8-1041">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1041">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1042">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1042">ACS</span></span>

* <span data-ttu-id="f60c8-1043">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1043">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1044">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1044">AppService</span></span>

* <span data-ttu-id="f60c8-1045">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1045">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-1046">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-1046">Batch</span></span>
* <span data-ttu-id="f60c8-1047">[重大な変更]`batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1047">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="f60c8-1048">[重大な変更]`Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1048">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="f60c8-1049">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1049">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="f60c8-1050">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1050">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="f60c8-1051">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1051">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="f60c8-1052">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="f60c8-1052">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-1053">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-1053">CosmosDB</span></span>

* <span data-ttu-id="f60c8-1054">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1054">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="f60c8-1055">Kusto</span><span class="sxs-lookup"><span data-stu-id="f60c8-1055">Kusto</span></span>

* <span data-ttu-id="f60c8-1056">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1056">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1057">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1057">Network</span></span>

* <span data-ttu-id="f60c8-1058">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1058">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="f60c8-1059">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1059">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="f60c8-1060">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1060">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="f60c8-1061">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1061">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="f60c8-1062">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1062">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="f60c8-1063">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1063">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="f60c8-1064">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1064">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-1065">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1065">Resource</span></span>

* <span data-ttu-id="f60c8-1066">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1066">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="f60c8-1067">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1067">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="f60c8-1068">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1068">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="f60c8-1069">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1069">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="f60c8-1070">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1070">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1071">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1071">Role</span></span>

* <span data-ttu-id="f60c8-1072">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1072">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1073">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1073">VM</span></span>

* <span data-ttu-id="f60c8-1074">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1074">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="f60c8-1075">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1075">February 12, 2019</span></span>

<span data-ttu-id="f60c8-1076">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="f60c8-1076">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1077">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1077">Core</span></span>

* <span data-ttu-id="f60c8-1078">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1078">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="f60c8-1079">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1079">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1080">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1080">ACR</span></span>
* <span data-ttu-id="f60c8-1081">[重大な変更]`acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1081">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="f60c8-1082">[重大な変更]`acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1082">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1083">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1083">ACS</span></span>
* <span data-ttu-id="f60c8-1084">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1084">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="f60c8-1085">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1085">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="f60c8-1086">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1086">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="f60c8-1087">AMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1087">AMS</span></span>
* <span data-ttu-id="f60c8-1088">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1088">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="f60c8-1089">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1089">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1090">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1090">Appservice</span></span>
* <span data-ttu-id="f60c8-1091">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1091">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="f60c8-1092">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1092">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="f60c8-1093">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1093">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="f60c8-1094">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1094">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="f60c8-1095">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1095">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="f60c8-1096">Botservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1096">Botservice</span></span>
* <span data-ttu-id="f60c8-1097">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1097">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="f60c8-1098">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1098">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="f60c8-1099">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1099">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="f60c8-1100">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1100">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="f60c8-1101">[非推奨]`--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1101">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="f60c8-1102">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1102">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="f60c8-1103">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1103">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="f60c8-1104">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1104">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="f60c8-1105">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="f60c8-1105">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="f60c8-1106">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1106">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="f60c8-1107">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f60c8-1107">Key Vault</span></span>
* <span data-ttu-id="f60c8-1108">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1108">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-1109">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-1109">Monitor</span></span>
* <span data-ttu-id="f60c8-1110">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1110">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1111">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1111">Network</span></span>
* <span data-ttu-id="f60c8-1112">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1112">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="f60c8-1113">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1113">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="f60c8-1114">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1114">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="f60c8-1115">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1115">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="f60c8-1116">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="f60c8-1116">Policy Insights</span></span>
* <span data-ttu-id="f60c8-1117">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1117">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-1118">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1118">RDBMS</span></span>
* <span data-ttu-id="f60c8-1119">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1119">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="f60c8-1120">Redis</span><span class="sxs-lookup"><span data-stu-id="f60c8-1120">Redis</span></span>
* <span data-ttu-id="f60c8-1121">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1121">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="f60c8-1122">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1122">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="f60c8-1123">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1123">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="f60c8-1124">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1124">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="f60c8-1125">[重大な変更]`redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1125">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="f60c8-1126">[重大な変更]`redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1126">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="f60c8-1127">[非推奨]`redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1127">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1128">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1128">Role</span></span>
* <span data-ttu-id="f60c8-1129">[重大な変更]`az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1129">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="f60c8-1130">SQL VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1130">SQL VM</span></span>
* <span data-ttu-id="f60c8-1131">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1131">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1132">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1132">VM</span></span>
* <span data-ttu-id="f60c8-1133">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1133">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="f60c8-1134">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1134">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="f60c8-1135">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1135">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="f60c8-1136">[重大な変更]`az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1136">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="f60c8-1137">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1137">January 31, 2019</span></span>

<span data-ttu-id="f60c8-1138">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="f60c8-1138">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1139">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1139">Core</span></span>

* <span data-ttu-id="f60c8-1140">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1140">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="f60c8-1141">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1141">January 28, 2019</span></span>

<span data-ttu-id="f60c8-1142">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="f60c8-1142">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1143">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1143">ACR</span></span>
* <span data-ttu-id="f60c8-1144">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1144">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1145">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1145">ACS</span></span>
* <span data-ttu-id="f60c8-1146">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1146">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="f60c8-1147">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1147">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="f60c8-1148">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1148">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="f60c8-1149">AMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1149">AMS</span></span>
* <span data-ttu-id="f60c8-1150">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1150">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="f60c8-1151">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1151">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1152">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1152">Appservice</span></span>
* <span data-ttu-id="f60c8-1153">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1153">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="f60c8-1154">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1154">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="f60c8-1155">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1155">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-1156">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1156">Container</span></span>
* <span data-ttu-id="f60c8-1157">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1157">Added `container start` command</span></span>
* <span data-ttu-id="f60c8-1158">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1158">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="f60c8-1159">EventGrid</span><span class="sxs-lookup"><span data-stu-id="f60c8-1159">EventGrid</span></span>
* <span data-ttu-id="f60c8-1160">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1160">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="f60c8-1161">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1161">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="f60c8-1162">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1162">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="f60c8-1163">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1163">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="f60c8-1164">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1164">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f60c8-1165">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f60c8-1165">HDInsight</span></span>
* <span data-ttu-id="f60c8-1166">[重大な変更]`hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1166">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="f60c8-1167">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1167">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="f60c8-1168">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1168">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="f60c8-1169">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1169">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="f60c8-1170">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1170">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="f60c8-1171">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1171">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-1172">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-1172">IoT</span></span>
* <span data-ttu-id="f60c8-1173">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1173">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="f60c8-1174">Kusto</span><span class="sxs-lookup"><span data-stu-id="f60c8-1174">Kusto</span></span>
* <span data-ttu-id="f60c8-1175">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1175">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-1176">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-1176">Monitor</span></span>
* <span data-ttu-id="f60c8-1177">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1177">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-1178">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-1178">Profile</span></span>
* <span data-ttu-id="f60c8-1179">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1179">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1180">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1180">Network</span></span>
* <span data-ttu-id="f60c8-1181">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1181">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="f60c8-1182">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1182">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-1183">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1183">Resource</span></span>
* <span data-ttu-id="f60c8-1184">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1184">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="f60c8-1185">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1185">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="f60c8-1186">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="f60c8-1186">SQL Virtual Machine</span></span>
* <span data-ttu-id="f60c8-1187">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1187">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1188">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1188">Storage</span></span>
* <span data-ttu-id="f60c8-1189">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1189">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="f60c8-1190">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="f60c8-1190">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1191">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1191">VM</span></span>
* <span data-ttu-id="f60c8-1192">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1192">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="f60c8-1193">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1193">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="f60c8-1194">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1194">January 15, 2019</span></span>

<span data-ttu-id="f60c8-1195">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="f60c8-1195">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1196">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1196">ACR</span></span>
* <span data-ttu-id="f60c8-1197">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1197">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="f60c8-1198">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1198">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="f60c8-1199">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1199">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="f60c8-1200">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1200">ACS</span></span>
* <span data-ttu-id="f60c8-1201">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1201">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1202">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1202">Appservice</span></span>
* <span data-ttu-id="f60c8-1203">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1203">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="f60c8-1204">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1204">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="f60c8-1205">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1205">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="f60c8-1206">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1206">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="f60c8-1207">Botservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1207">Botservice</span></span>
* <span data-ttu-id="f60c8-1208">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1208">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="f60c8-1209">[構成]</span><span class="sxs-lookup"><span data-stu-id="f60c8-1209">Configure</span></span>
* <span data-ttu-id="f60c8-1210">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1210">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-1211">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-1211">CosmosDB</span></span>
* <span data-ttu-id="f60c8-1212">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1212">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f60c8-1213">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f60c8-1213">HDInsight</span></span>
* <span data-ttu-id="f60c8-1214">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1214">Added commands for managing applications</span></span>
* <span data-ttu-id="f60c8-1215">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1215">Added commands for managing script actions</span></span>
* <span data-ttu-id="f60c8-1216">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1216">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="f60c8-1217">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1217">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="f60c8-1218">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1218">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1219">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1219">Network</span></span>
* <span data-ttu-id="f60c8-1220">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1220">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="f60c8-1221">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1221">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="f60c8-1222">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1222">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="f60c8-1223">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1223">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1224">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1224">Role</span></span>
* <span data-ttu-id="f60c8-1225">[非推奨]`create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1225">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="f60c8-1226">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="f60c8-1226">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="f60c8-1227">Security</span><span class="sxs-lookup"><span data-stu-id="f60c8-1227">Security</span></span>
* <span data-ttu-id="f60c8-1228">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1228">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1229">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1229">Storage</span></span>
* <span data-ttu-id="f60c8-1230">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1230">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="f60c8-1231">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="f60c8-1231">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="f60c8-1232">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1232">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="f60c8-1233">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1233">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="f60c8-1234">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1234">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1235">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1235">VM</span></span>
* <span data-ttu-id="f60c8-1236">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1236">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="f60c8-1237">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1237">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="f60c8-1238">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1238">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="f60c8-1239">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1239">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="f60c8-1240">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1240">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="f60c8-1241">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1241">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="f60c8-1242">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1242">December 20, 2018</span></span>

<span data-ttu-id="f60c8-1243">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="f60c8-1243">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="f60c8-1244">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1244">Appservice</span></span>
* <span data-ttu-id="f60c8-1245">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1245">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="f60c8-1246">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1246">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="f60c8-1247">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1247">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="f60c8-1248">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="f60c8-1248">IoTCentral</span></span>
* <span data-ttu-id="f60c8-1249">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1249">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1250">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1250">Role</span></span>
* <span data-ttu-id="f60c8-1251">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1251">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-1252">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-1252">SQL</span></span>
* <span data-ttu-id="f60c8-1253">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1253">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1254">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1254">VM</span></span>
* <span data-ttu-id="f60c8-1255">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1255">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="f60c8-1256">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1256">December 18, 2018</span></span>

<span data-ttu-id="f60c8-1257">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="f60c8-1257">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="f60c8-1258">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1258">ACR</span></span>
* <span data-ttu-id="f60c8-1259">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1259">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="f60c8-1260">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1260">Condensed the table layout for task list</span></span>
* <span data-ttu-id="f60c8-1261">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1261">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1262">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1262">ACS</span></span>
* <span data-ttu-id="f60c8-1263">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1263">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="f60c8-1264">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1264">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="f60c8-1265">[非推奨]`az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1265">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="f60c8-1266">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="f60c8-1266">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="f60c8-1267">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1267">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="f60c8-1268">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1268">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1269">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1269">Appservice</span></span>
* <span data-ttu-id="f60c8-1270">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1270">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="f60c8-1271">Botservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1271">Botservice</span></span>
* <span data-ttu-id="f60c8-1272">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1272">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="f60c8-1273">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1273">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="f60c8-1274">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1274">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="f60c8-1275">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1275">Reduced Kudu network calls</span></span>
* <span data-ttu-id="f60c8-1276">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1276">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="f60c8-1277">従量課金</span><span class="sxs-lookup"><span data-stu-id="f60c8-1277">Consumption</span></span>
* <span data-ttu-id="f60c8-1278">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1278">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-1279">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-1279">CosmosDB</span></span>
* <span data-ttu-id="f60c8-1280">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1280">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="f60c8-1281">マップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1281">Maps</span></span>
* <span data-ttu-id="f60c8-1282">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1282">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1283">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1283">Network</span></span>
* <span data-ttu-id="f60c8-1284">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1284">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="f60c8-1285">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1285">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-1286">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1286">Resource</span></span>
* <span data-ttu-id="f60c8-1287">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1287">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="f60c8-1288">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1288">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1289">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1289">Storage</span></span>
*  <span data-ttu-id="f60c8-1290">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1290">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1291">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1291">VM</span></span>
* <span data-ttu-id="f60c8-1292">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1292">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="f60c8-1293">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1293">December 4, 2018</span></span>

<span data-ttu-id="f60c8-1294">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="f60c8-1294">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="f60c8-1295">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1295">Core</span></span>
* <span data-ttu-id="f60c8-1296">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1296">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="f60c8-1297">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1297">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1298">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1298">Appservice</span></span>
* <span data-ttu-id="f60c8-1299">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1299">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="f60c8-1300">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1300">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1301">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1301">Network</span></span>
* <span data-ttu-id="f60c8-1302">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1302">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1303">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1303">Role</span></span>
* <span data-ttu-id="f60c8-1304">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1304">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="f60c8-1305">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1305">VM</span></span>
* <span data-ttu-id="f60c8-1306">[非推奨]`vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1306">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="f60c8-1307">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1307">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="f60c8-1308">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1308">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="f60c8-1309">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1309">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="f60c8-1310">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1310">November 20, 2018</span></span>

<span data-ttu-id="f60c8-1311">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="f60c8-1311">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="f60c8-1312">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1312">Core</span></span>
* <span data-ttu-id="f60c8-1313">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1313">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1314">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1314">ACR</span></span>
* <span data-ttu-id="f60c8-1315">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1315">Added context token to task step</span></span>
* <span data-ttu-id="f60c8-1316">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1316">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="f60c8-1317">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1317">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1318">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1318">Appservice</span></span>
* <span data-ttu-id="f60c8-1319">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1319">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="f60c8-1320">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1320">Updated the default `node_version`.</span></span> <span data-ttu-id="f60c8-1321">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-1321">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="f60c8-1322">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1322">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="f60c8-1323">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1323">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="f60c8-1324">IotCentral</span><span class="sxs-lookup"><span data-stu-id="f60c8-1324">IotCentral</span></span>
* <span data-ttu-id="f60c8-1325">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1325">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="f60c8-1326">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f60c8-1326">KeyVault</span></span>
* <span data-ttu-id="f60c8-1327">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1327">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1328">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1328">Network</span></span>
* <span data-ttu-id="f60c8-1329">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1329">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="f60c8-1330">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1330">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="f60c8-1331">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1331">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="f60c8-1332">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1332">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-1333">Rdbms</span><span class="sxs-lookup"><span data-stu-id="f60c8-1333">Rdbms</span></span>
* <span data-ttu-id="f60c8-1334">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1334">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="f60c8-1335">Rbac</span><span class="sxs-lookup"><span data-stu-id="f60c8-1335">Rbac</span></span>
* <span data-ttu-id="f60c8-1336">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1336">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="f60c8-1337">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1337">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="f60c8-1338">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1338">Storage</span></span>
* <span data-ttu-id="f60c8-1339">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1339">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="f60c8-1340">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1340">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="f60c8-1341">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1341">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="f60c8-1342">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-1342">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1343">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1343">VM</span></span>
* <span data-ttu-id="f60c8-1344">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1344">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="f60c8-1345">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1345">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="f60c8-1346">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1346">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="f60c8-1347">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1347">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="f60c8-1348">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1348">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="f60c8-1349">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1349">Added `snapshot wait` command</span></span>
* <span data-ttu-id="f60c8-1350">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1350">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="f60c8-1351">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1351">November 6, 2018</span></span>

<span data-ttu-id="f60c8-1352">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="f60c8-1352">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1353">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1353">Core</span></span>
* <span data-ttu-id="f60c8-1354">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1354">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1355">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1355">ACR</span></span>
* <span data-ttu-id="f60c8-1356">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1356">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="f60c8-1357">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1357">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1358">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1358">ACS</span></span>
* <span data-ttu-id="f60c8-1359">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1359">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="f60c8-1360">Advisor</span><span class="sxs-lookup"><span data-stu-id="f60c8-1360">Advisor</span></span>
* <span data-ttu-id="f60c8-1361">GA リリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1361">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="f60c8-1362">AMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1362">AMS</span></span>
* <span data-ttu-id="f60c8-1363">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1363">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="f60c8-1364">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1364">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="f60c8-1365">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1365">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="f60c8-1366">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1366">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="f60c8-1367">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1367">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="f60c8-1368">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1368">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="f60c8-1369">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1369">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="f60c8-1370">[重大な変更]`ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1370">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="f60c8-1371">[重大な変更]`ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1371">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="f60c8-1372">[重大な変更]`ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1372">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="f60c8-1373">[重大な変更]`ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1373">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="f60c8-1374">[重大な変更]`ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1374">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="f60c8-1375">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1375">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="f60c8-1376">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="f60c8-1376">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="f60c8-1377">[重大な変更]`ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1377">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="f60c8-1378">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1378">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="f60c8-1379">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="f60c8-1379">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1380">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1380">AppService</span></span>
* <span data-ttu-id="f60c8-1381">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1381">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="f60c8-1382">[構成]</span><span class="sxs-lookup"><span data-stu-id="f60c8-1382">Configure</span></span>
* <span data-ttu-id="f60c8-1383">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1383">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-1384">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1384">Container</span></span>
* <span data-ttu-id="f60c8-1385">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1385">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="f60c8-1386">EventHub</span><span class="sxs-lookup"><span data-stu-id="f60c8-1386">EventHub</span></span>
* <span data-ttu-id="f60c8-1387">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1387">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-1388">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-1388">Interactive</span></span>
* <span data-ttu-id="f60c8-1389">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="f60c8-1389">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-1390">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-1390">Monitor</span></span>
* <span data-ttu-id="f60c8-1391">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1391">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1392">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1392">Network</span></span>
* <span data-ttu-id="f60c8-1393">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1393">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="f60c8-1394">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1394">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="f60c8-1395">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1395">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="f60c8-1396">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-1396">Profile</span></span>
* <span data-ttu-id="f60c8-1397">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1397">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-1398">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1398">RDBMS</span></span>
* <span data-ttu-id="f60c8-1399">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1399">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-1400">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1400">Resource</span></span>
* <span data-ttu-id="f60c8-1401">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1401">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1402">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1402">Role</span></span>
* <span data-ttu-id="f60c8-1403">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1403">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="f60c8-1404">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1404">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="f60c8-1405">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1405">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1406">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1406">Storage</span></span>
* <span data-ttu-id="f60c8-1407">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="f60c8-1407">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1408">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1408">VM</span></span>
* <span data-ttu-id="f60c8-1409">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1409">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="f60c8-1410">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1410">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="f60c8-1411">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1411">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="f60c8-1412">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1412">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="f60c8-1413">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="f60c8-1413">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="f60c8-1414">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1414">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="f60c8-1415">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1415">October 23, 2018</span></span>

<span data-ttu-id="f60c8-1416">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="f60c8-1416">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1417">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1417">Core</span></span>
* <span data-ttu-id="f60c8-1418">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1418">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="f60c8-1419">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1419">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1420">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1420">ACR</span></span>
* <span data-ttu-id="f60c8-1421">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1421">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="f60c8-1422">CDN</span><span class="sxs-lookup"><span data-stu-id="f60c8-1422">CDN</span></span>
* <span data-ttu-id="f60c8-1423">[重大な変更]`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1423">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="f60c8-1424">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1424">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-1425">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1425">Container</span></span>
* <span data-ttu-id="f60c8-1426">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1426">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="f60c8-1427">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1427">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="f60c8-1428">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1428">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="f60c8-1429">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1429">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="f60c8-1430">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1430">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="f60c8-1431">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1431">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="f60c8-1432">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1432">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-1433">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-1433">CosmosDB</span></span>
* <span data-ttu-id="f60c8-1434">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1434">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-1435">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-1435">Interactive</span></span>
* <span data-ttu-id="f60c8-1436">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1436">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="f60c8-1437">IoT Central</span><span class="sxs-lookup"><span data-stu-id="f60c8-1437">IoT Central</span></span>
* <span data-ttu-id="f60c8-1438">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1438">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="f60c8-1439">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1439">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-1440">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-1440">Monitor</span></span>
* <span data-ttu-id="f60c8-1441">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="f60c8-1441">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="f60c8-1442">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1442">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="f60c8-1443">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1443">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="f60c8-1444">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1444">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="f60c8-1445">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1445">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="f60c8-1446">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1446">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="f60c8-1447">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="f60c8-1447">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="f60c8-1448">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1448">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="f60c8-1449">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1449">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="f60c8-1450">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1450">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1451">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1451">Network</span></span>
* <span data-ttu-id="f60c8-1452">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1452">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="f60c8-1453">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1453">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="f60c8-1454">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f60c8-1454">ServiceBus</span></span>
* <span data-ttu-id="f60c8-1455">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1455">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-1456">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-1456">SQL</span></span>
* <span data-ttu-id="f60c8-1457">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1457">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1458">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1458">Storage</span></span>
* <span data-ttu-id="f60c8-1459">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1459">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="f60c8-1460">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1460">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1461">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1461">VM</span></span>
* <span data-ttu-id="f60c8-1462">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-1462">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="f60c8-1463">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1463">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="f60c8-1464">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1464">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="f60c8-1465">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1465">October 16, 2018</span></span>

<span data-ttu-id="f60c8-1466">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="f60c8-1466">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1467">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1467">VM</span></span>
* <span data-ttu-id="f60c8-1468">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1468">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="f60c8-1469">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1469">October 9, 2018</span></span>

<span data-ttu-id="f60c8-1470">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="f60c8-1470">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1471">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1471">Core</span></span>
* <span data-ttu-id="f60c8-1472">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1472">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1473">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1473">ACR</span></span>
* <span data-ttu-id="f60c8-1474">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1474">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1475">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1475">ACS</span></span>
* <span data-ttu-id="f60c8-1476">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="f60c8-1476">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="f60c8-1477">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1477">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="f60c8-1478">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1478">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="f60c8-1479">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1479">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-1480">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1480">Container</span></span>
* <span data-ttu-id="f60c8-1481">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1481">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="f60c8-1482">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1482">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="f60c8-1483">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1483">Event Hub</span></span>
* <span data-ttu-id="f60c8-1484">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1484">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="f60c8-1485">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1485">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="f60c8-1486">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f60c8-1486">Extensions</span></span>
* <span data-ttu-id="f60c8-1487">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1487">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f60c8-1488">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f60c8-1488">HDInsight</span></span>
* <span data-ttu-id="f60c8-1489">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1489">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-1490">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-1490">IoT</span></span>
* <span data-ttu-id="f60c8-1491">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1491">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="f60c8-1492">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f60c8-1492">KeyVault</span></span>
* <span data-ttu-id="f60c8-1493">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1493">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1494">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1494">Network</span></span>
* <span data-ttu-id="f60c8-1495">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1495">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="f60c8-1496">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="f60c8-1496">See #6052</span></span>
* <span data-ttu-id="f60c8-1497">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1497">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="f60c8-1498">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="f60c8-1498">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="f60c8-1499">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1499">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="f60c8-1500">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1500">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="f60c8-1501">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1501">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="f60c8-1502">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1502">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1503">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1503">Role</span></span>
* <span data-ttu-id="f60c8-1504">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1504">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="f60c8-1505">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1505">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="f60c8-1506">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1506">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="f60c8-1507">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1507">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="f60c8-1508">Service Bus</span><span class="sxs-lookup"><span data-stu-id="f60c8-1508">Service Bus</span></span>
* <span data-ttu-id="f60c8-1509">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1509">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1510">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1510">VM</span></span>
* <span data-ttu-id="f60c8-1511">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1511">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="f60c8-1512">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1512">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="f60c8-1513">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1513">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="f60c8-1514">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1514">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="f60c8-1515">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1515">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="f60c8-1516">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1516">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="f60c8-1517">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1517">September 21, 2018</span></span>

<span data-ttu-id="f60c8-1518">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="f60c8-1518">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1519">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1519">ACR</span></span>
* <span data-ttu-id="f60c8-1520">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1520">Added ACR Task commands</span></span>
* <span data-ttu-id="f60c8-1521">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1521">Added quick run command</span></span>
* <span data-ttu-id="f60c8-1522">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1522">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="f60c8-1523">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1523">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="f60c8-1524">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1524">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="f60c8-1525">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1525">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1526">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1526">ACS</span></span>
* <span data-ttu-id="f60c8-1527">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1527">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="f60c8-1528">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1528">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1529">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1529">AppService</span></span>

* <span data-ttu-id="f60c8-1530">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1530">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="f60c8-1531">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1531">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="f60c8-1532">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1532">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="f60c8-1533">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1533">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-1534">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-1534">Batch</span></span>
* <span data-ttu-id="f60c8-1535">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1535">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="f60c8-1536">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1536">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="f60c8-1537">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1537">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="f60c8-1538">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1538">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="f60c8-1539">Batch AI</span><span class="sxs-lookup"><span data-stu-id="f60c8-1539">Batch AI</span></span> 
* <span data-ttu-id="f60c8-1540">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1540">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="f60c8-1541">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="f60c8-1541">Cognitive Services</span></span>
* <span data-ttu-id="f60c8-1542">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1542">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="f60c8-1543">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1543">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="f60c8-1544">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1544">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="f60c8-1545">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1545">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="f60c8-1546">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1546">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="f60c8-1547">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1547">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-1548">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1548">Container</span></span>
* <span data-ttu-id="f60c8-1549">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1549">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="f60c8-1550">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1550">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="f60c8-1551">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1551">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="f60c8-1552">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1552">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="f60c8-1553">DataLake</span><span class="sxs-lookup"><span data-stu-id="f60c8-1553">Datalake</span></span>
* <span data-ttu-id="f60c8-1554">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1554">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="f60c8-1555">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="f60c8-1555">Interactive Shell</span></span>
* <span data-ttu-id="f60c8-1556">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1556">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="f60c8-1557">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1557">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-1558">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-1558">IoT</span></span>
* <span data-ttu-id="f60c8-1559">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1559">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="f60c8-1560">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f60c8-1560">Key Vault</span></span>
* <span data-ttu-id="f60c8-1561">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1561">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1562">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1562">Network</span></span>
* <span data-ttu-id="f60c8-1563">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1563">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="f60c8-1564">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1564">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="f60c8-1565">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1565">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="f60c8-1566">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1566">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="f60c8-1567">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1567">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="f60c8-1568">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1568">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="f60c8-1569">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1569">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="f60c8-1570">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1570">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="f60c8-1571">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1571">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="f60c8-1572">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1572">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="f60c8-1573">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1573">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="f60c8-1574">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1574">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="f60c8-1575">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1575">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="f60c8-1576">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1576">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="f60c8-1577">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1577">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="f60c8-1578">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1578">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="f60c8-1579">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1579">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="f60c8-1580">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1580">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-1581">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1581">RDBMS</span></span>
* <span data-ttu-id="f60c8-1582">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1582">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="f60c8-1583">予約</span><span class="sxs-lookup"><span data-stu-id="f60c8-1583">Reservation</span></span>
* <span data-ttu-id="f60c8-1584">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1584">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="f60c8-1585">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1585">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="f60c8-1586">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="f60c8-1586">Manage App</span></span>
* <span data-ttu-id="f60c8-1587">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1587">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="f60c8-1588">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1588">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1589">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1589">Role</span></span>
* <span data-ttu-id="f60c8-1590">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1590">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="f60c8-1591">SignalR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1591">SignalR</span></span>
* <span data-ttu-id="f60c8-1592">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1592">First release</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1593">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1593">Storage</span></span>
* <span data-ttu-id="f60c8-1594">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1594">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="f60c8-1595">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1595">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1596">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1596">VM</span></span>
* <span data-ttu-id="f60c8-1597">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="f60c8-1597">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="f60c8-1598">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1598">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="f60c8-1599">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1599">August 28, 2018</span></span>

<span data-ttu-id="f60c8-1600">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="f60c8-1600">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1601">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1601">Core</span></span>

* <span data-ttu-id="f60c8-1602">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1602">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="f60c8-1603">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1603">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1604">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1604">ACR</span></span>

* <span data-ttu-id="f60c8-1605">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1605">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="f60c8-1606">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1606">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1607">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1607">ACS</span></span>

* <span data-ttu-id="f60c8-1608">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1608">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="f60c8-1609">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1609">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1610">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1610">AppService</span></span>

* <span data-ttu-id="f60c8-1611">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1611">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="f60c8-1612">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1612">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="f60c8-1613">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1613">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="f60c8-1614">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1614">Backup</span></span>

* <span data-ttu-id="f60c8-1615">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1615">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="f60c8-1616">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="f60c8-1616">Bot Service</span></span>

* <span data-ttu-id="f60c8-1617">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1617">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="f60c8-1618">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="f60c8-1618">Cognitive Services</span></span>

* <span data-ttu-id="f60c8-1619">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1619">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-1620">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-1620">IoT</span></span>

* <span data-ttu-id="f60c8-1621">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1621">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-1622">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-1622">Monitor</span></span>

* <span data-ttu-id="f60c8-1623">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1623">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="f60c8-1624">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1624">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1625">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1625">Network</span></span>

* <span data-ttu-id="f60c8-1626">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1626">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-1627">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1627">Resource</span></span>

* <span data-ttu-id="f60c8-1628">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1628">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1629">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1629">Storage</span></span>

* <span data-ttu-id="f60c8-1630">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1630">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1631">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1631">VM</span></span>

* <span data-ttu-id="f60c8-1632">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1632">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="f60c8-1633">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1633">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="f60c8-1634">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1634">Auguest 14, 2018</span></span>

<span data-ttu-id="f60c8-1635">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="f60c8-1635">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1636">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1636">Core</span></span>

* <span data-ttu-id="f60c8-1637">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1637">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="f60c8-1638">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1638">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="f60c8-1639">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1639">Telemetry</span></span>

* <span data-ttu-id="f60c8-1640">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1640">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1641">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1641">ACR</span></span>

* <span data-ttu-id="f60c8-1642">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1642">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="f60c8-1643">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1643">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1644">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1644">ACS</span></span>

* <span data-ttu-id="f60c8-1645">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1645">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="f60c8-1646">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1646">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="f60c8-1647">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1647">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="f60c8-1648">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1648">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="f60c8-1649">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1649">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="f60c8-1650">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1650">AppService</span></span>

* <span data-ttu-id="f60c8-1651">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1651">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="f60c8-1652">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1652">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="f60c8-1653">BatchAI</span><span class="sxs-lookup"><span data-stu-id="f60c8-1653">BatchAI</span></span>

* <span data-ttu-id="f60c8-1654">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1654">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="f60c8-1655">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1655">Container</span></span>

* <span data-ttu-id="f60c8-1656">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1656">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="f60c8-1657">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-1657">IoT</span></span>

* <span data-ttu-id="f60c8-1658">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1658">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="f60c8-1659">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1659">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="f60c8-1660">Iot Central</span><span class="sxs-lookup"><span data-stu-id="f60c8-1660">Iot Central</span></span>

* <span data-ttu-id="f60c8-1661">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1661">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="f60c8-1662">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f60c8-1662">KeyVault</span></span>


* <span data-ttu-id="f60c8-1663">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1663">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="f60c8-1664">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1664">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="f60c8-1665">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1665">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="f60c8-1666">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1666">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="f60c8-1667">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1667">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="f60c8-1668">リレー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1668">Relay</span></span>

* <span data-ttu-id="f60c8-1669">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1669">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-1670">Sql</span><span class="sxs-lookup"><span data-stu-id="f60c8-1670">Sql</span></span>

* <span data-ttu-id="f60c8-1671">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1671">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1672">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1672">Storage</span></span>

* <span data-ttu-id="f60c8-1673">[重大な変更]`--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-1673">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="f60c8-1674">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1674">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="f60c8-1675">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1675">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="f60c8-1676">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1676">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="f60c8-1677">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1677">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1678">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1678">VM</span></span>

* <span data-ttu-id="f60c8-1679">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1679">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="f60c8-1680">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1680">July 31, 2018</span></span>

<span data-ttu-id="f60c8-1681">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="f60c8-1681">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1682">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1682">ACR</span></span>

* <span data-ttu-id="f60c8-1683">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1683">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="f60c8-1684">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1684">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1685">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1685">ACS</span></span>

* <span data-ttu-id="f60c8-1686">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1686">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-1687">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-1687">Batch</span></span>

* <span data-ttu-id="f60c8-1688">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1688">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-1689">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1689">Container</span></span>

* <span data-ttu-id="f60c8-1690">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1690">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1691">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1691">Network</span></span>

* <span data-ttu-id="f60c8-1692">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1692">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="f60c8-1693">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1693">Resource</span></span>

* <span data-ttu-id="f60c8-1694">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1694">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="f60c8-1695">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1695">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1696">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1696">Role</span></span>

* <span data-ttu-id="f60c8-1697">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1697">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="f60c8-1698">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1698">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="f60c8-1699">検索</span><span class="sxs-lookup"><span data-stu-id="f60c8-1699">Search</span></span>

* <span data-ttu-id="f60c8-1700">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1700">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="f60c8-1701">Service Bus</span><span class="sxs-lookup"><span data-stu-id="f60c8-1701">Service Bus</span></span>

* <span data-ttu-id="f60c8-1702">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1702">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="f60c8-1703">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1703">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="f60c8-1704">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="f60c8-1704">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="f60c8-1705">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="f60c8-1705">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1706">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1706">Storage</span></span>

* <span data-ttu-id="f60c8-1707">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1707">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="f60c8-1708">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1708">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1709">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1709">VM</span></span>

* <span data-ttu-id="f60c8-1710">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1710">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="f60c8-1711">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1711">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="f60c8-1712">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1712">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="f60c8-1713">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1713">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="f60c8-1714">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1714">July 18, 2018</span></span>

<span data-ttu-id="f60c8-1715">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="f60c8-1715">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1716">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1716">Core</span></span>

* <span data-ttu-id="f60c8-1717">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1717">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="f60c8-1718">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1718">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="f60c8-1719">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1719">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1720">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1720">ACR</span></span>

* <span data-ttu-id="f60c8-1721">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1721">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="f60c8-1722">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1722">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="f60c8-1723">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1723">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="f60c8-1724">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1724">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1725">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1725">ACS</span></span>

* <span data-ttu-id="f60c8-1726">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1726">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1727">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1727">AppService</span></span>

* <span data-ttu-id="f60c8-1728">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1728">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-1729">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-1729">Batch</span></span>

* <span data-ttu-id="f60c8-1730">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1730">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="f60c8-1731">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1731">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="f60c8-1732">Batch AI</span><span class="sxs-lookup"><span data-stu-id="f60c8-1732">Batch AI</span></span>

* <span data-ttu-id="f60c8-1733">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1733">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-1734">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1734">Container</span></span>

* <span data-ttu-id="f60c8-1735">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1735">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="f60c8-1736">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1736">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1737">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1737">Network</span></span>

* <span data-ttu-id="f60c8-1738">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1738">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="f60c8-1739">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1739">Added `network nic wait`</span></span>
* <span data-ttu-id="f60c8-1740">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1740">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="f60c8-1741">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1741">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="f60c8-1742">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1742">Resource</span></span>

* <span data-ttu-id="f60c8-1743">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1743">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="f60c8-1744">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1744">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="f60c8-1745">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1745">Added `deployment wait` command</span></span>
* <span data-ttu-id="f60c8-1746">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1746">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-1747">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-1747">SQL</span></span>

* <span data-ttu-id="f60c8-1748">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1748">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="f60c8-1749">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1749">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="f60c8-1750">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1750">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1751">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1751">Storage</span></span>

* <span data-ttu-id="f60c8-1752">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1752">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1753">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1753">VM</span></span>

* <span data-ttu-id="f60c8-1754">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1754">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="f60c8-1755">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1755">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="f60c8-1756">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1756">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="f60c8-1757">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1757">July 3, 2018</span></span>

<span data-ttu-id="f60c8-1758">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="f60c8-1758">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="f60c8-1759">AKS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1759">AKS</span></span>

* <span data-ttu-id="f60c8-1760">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1760">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="f60c8-1761">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1761">July 3, 2018</span></span>

<span data-ttu-id="f60c8-1762">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="f60c8-1762">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1763">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1763">Core</span></span>

* <span data-ttu-id="f60c8-1764">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1764">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1765">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1765">ACR</span></span>

* <span data-ttu-id="f60c8-1766">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1766">Added polling build status</span></span>
* <span data-ttu-id="f60c8-1767">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1767">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="f60c8-1768">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1768">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1769">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1769">ACS</span></span>

* <span data-ttu-id="f60c8-1770">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1770">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="f60c8-1771">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1771">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="f60c8-1772">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1772">Updated options for `aks browse` command.</span></span> <span data-ttu-id="f60c8-1773">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1773">Added `--listen-port` support</span></span>
* <span data-ttu-id="f60c8-1774">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1774">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="f60c8-1775">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1775">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="f60c8-1776">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1776">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1777">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1777">AppService</span></span>

* <span data-ttu-id="f60c8-1778">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1778">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="f60c8-1779">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1779">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="f60c8-1780">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1780">Backup</span></span>

* <span data-ttu-id="f60c8-1781">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1781">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="f60c8-1782">BatchAI</span><span class="sxs-lookup"><span data-stu-id="f60c8-1782">BatchAI</span></span>

* <span data-ttu-id="f60c8-1783">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1783">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="f60c8-1784">クラウド</span><span class="sxs-lookup"><span data-stu-id="f60c8-1784">Cloud</span></span>

* <span data-ttu-id="f60c8-1785">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1785">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-1786">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1786">Container</span></span>

* <span data-ttu-id="f60c8-1787">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1787">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="f60c8-1788">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1788">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="f60c8-1789">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1789">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="f60c8-1790">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f60c8-1790">Extension</span></span>

* <span data-ttu-id="f60c8-1791">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1791">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1792">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1792">Network</span></span>

* <span data-ttu-id="f60c8-1793">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1793">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-1794">Rdbms</span><span class="sxs-lookup"><span data-stu-id="f60c8-1794">Rdbms</span></span>

* <span data-ttu-id="f60c8-1795">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1795">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-1796">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1796">Resource</span></span>

* <span data-ttu-id="f60c8-1797">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1797">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1798">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1798">VM</span></span>

* <span data-ttu-id="f60c8-1799">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1799">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="f60c8-1800">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1800">June 25, 2018</span></span>

<span data-ttu-id="f60c8-1801">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="f60c8-1801">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="f60c8-1802">CLI</span><span class="sxs-lookup"><span data-stu-id="f60c8-1802">CLI</span></span>

* <span data-ttu-id="f60c8-1803">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1803">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="f60c8-1804">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1804">June 19, 2018</span></span>

<span data-ttu-id="f60c8-1805">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="f60c8-1805">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1806">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1806">Core</span></span>

* <span data-ttu-id="f60c8-1807">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1807">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1808">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1808">ACR</span></span>

* <span data-ttu-id="f60c8-1809">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1809">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="f60c8-1810">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1810">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1811">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1811">ACS</span></span>

* <span data-ttu-id="f60c8-1812">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1812">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="f60c8-1813">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1813">Added `--update` support</span></span>
* <span data-ttu-id="f60c8-1814">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1814">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="f60c8-1815">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1815">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="f60c8-1816">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1816">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="f60c8-1817">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1817">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="f60c8-1818">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1818">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="f60c8-1819">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1819">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1820">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1820">AppService</span></span>

* <span data-ttu-id="f60c8-1821">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1821">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="f60c8-1822">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1822">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-1823">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-1823">Batch</span></span>

* <span data-ttu-id="f60c8-1824">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1824">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="f60c8-1825">Batch AI</span><span class="sxs-lookup"><span data-stu-id="f60c8-1825">Batch AI</span></span>

* <span data-ttu-id="f60c8-1826">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1826">Added support for workspaces.</span></span> <span data-ttu-id="f60c8-1827">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="f60c8-1827">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="f60c8-1828">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1828">Added support for experiments.</span></span> <span data-ttu-id="f60c8-1829">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="f60c8-1829">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="f60c8-1830">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1830">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="f60c8-1831">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1831">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="f60c8-1832">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1832">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="f60c8-1833">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1833">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="f60c8-1834">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="f60c8-1834">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="f60c8-1835">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="f60c8-1835">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="f60c8-1836">[重大な変更]`--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1836">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="f60c8-1837">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1837">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="f60c8-1838">[重大な変更]`--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1838">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="f60c8-1839">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1839">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="f60c8-1840">[重大な変更]`location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1840">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="f60c8-1841">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1841">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="f60c8-1842">[重大な変更]`--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1842">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="f60c8-1843">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1843">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="f60c8-1844">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1844">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="f60c8-1845">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1845">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="f60c8-1846">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1846">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="f60c8-1847">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1847">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="f60c8-1848">マップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1848">Maps</span></span>

* <span data-ttu-id="f60c8-1849">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1849">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1850">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1850">Network</span></span>

* <span data-ttu-id="f60c8-1851">`https` のサポートを `network lb probe create` に追加しました ([#6571](https://github.com/Azure/azure-cli/issues/6571))</span><span class="sxs-lookup"><span data-stu-id="f60c8-1851">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="f60c8-1852">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1852">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="f60c8-1853">#6502</span><span class="sxs-lookup"><span data-stu-id="f60c8-1853">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="f60c8-1854">Reservations</span><span class="sxs-lookup"><span data-stu-id="f60c8-1854">Reservations</span></span>

* <span data-ttu-id="f60c8-1855">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1855">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="f60c8-1856">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1856">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="f60c8-1857">[重大な変更]`kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1857">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="f60c8-1858">[重大な変更]`Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1858">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="f60c8-1859">[重大な変更]`Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1859">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="f60c8-1860">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1860">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-1861">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-1861">Role</span></span>

* <span data-ttu-id="f60c8-1862">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1862">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-1863">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-1863">SQL</span></span>

* <span data-ttu-id="f60c8-1864">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1864">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1865">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1865">Storage</span></span>

* <span data-ttu-id="f60c8-1866">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1866">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1867">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1867">VM</span></span>

* <span data-ttu-id="f60c8-1868">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1868">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="f60c8-1869">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1869">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="f60c8-1870">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1870">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="f60c8-1871">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1871">June 13, 2018</span></span>

<span data-ttu-id="f60c8-1872">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="f60c8-1872">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1873">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1873">Core</span></span>

* <span data-ttu-id="f60c8-1874">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1874">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="f60c8-1875">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1875">June 13, 2018</span></span>

<span data-ttu-id="f60c8-1876">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="f60c8-1876">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="f60c8-1877">AKS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1877">AKS</span></span>

* <span data-ttu-id="f60c8-1878">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1878">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="f60c8-1879">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1879">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="f60c8-1880">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1880">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="f60c8-1881">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1881">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="f60c8-1882">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1882">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1883">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1883">AppService</span></span>

* <span data-ttu-id="f60c8-1884">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1884">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="f60c8-1885">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1885">June 5, 2018</span></span>

<span data-ttu-id="f60c8-1886">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="f60c8-1886">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-1887">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-1887">Interactive</span></span>

* <span data-ttu-id="f60c8-1888">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1888">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="f60c8-1889">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1889">June 5, 2018</span></span>

<span data-ttu-id="f60c8-1890">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="f60c8-1890">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1891">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1891">Core</span></span>

* <span data-ttu-id="f60c8-1892">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1892">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="f60c8-1893">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1893">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1894">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1894">ACR</span></span>

* <span data-ttu-id="f60c8-1895">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1895">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="f60c8-1896">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1896">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="f60c8-1897">AKS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1897">AKS</span></span>

* <span data-ttu-id="f60c8-1898">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1898">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-1899">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-1899">Batch</span></span>

* <span data-ttu-id="f60c8-1900">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1900">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-1901">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-1901">IOT</span></span>

* <span data-ttu-id="f60c8-1902">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1902">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1903">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1903">Network</span></span>

* <span data-ttu-id="f60c8-1904">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1904">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="f60c8-1905">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="f60c8-1905">Policy Insights</span></span>

* <span data-ttu-id="f60c8-1906">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-1906">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="f60c8-1907">ARM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1907">ARM</span></span>

* <span data-ttu-id="f60c8-1908">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1908">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-1909">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-1909">SQL</span></span>

* <span data-ttu-id="f60c8-1910">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1910">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="f60c8-1911">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1911">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="f60c8-1912">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1912">Storage</span></span>

* <span data-ttu-id="f60c8-1913">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1913">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1914">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1914">VM</span></span>

* <span data-ttu-id="f60c8-1915">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1915">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="f60c8-1916">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1916">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="f60c8-1917">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1917">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="f60c8-1918">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1918">May 22, 2018</span></span>

<span data-ttu-id="f60c8-1919">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="f60c8-1919">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1920">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1920">Core</span></span>

* <span data-ttu-id="f60c8-1921">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1921">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1922">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1922">ACS</span></span>

* <span data-ttu-id="f60c8-1923">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1923">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="f60c8-1924">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1924">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1925">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-1925">AppService</span></span>

* <span data-ttu-id="f60c8-1926">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1926">Improved generic update commands</span></span>
* <span data-ttu-id="f60c8-1927">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1927">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-1928">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-1928">Container</span></span>

* <span data-ttu-id="f60c8-1929">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1929">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="f60c8-1930">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1930">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="f60c8-1931">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f60c8-1931">Extension</span></span>

* <span data-ttu-id="f60c8-1932">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1932">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-1933">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-1933">Interactive</span></span>

* <span data-ttu-id="f60c8-1934">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1934">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="f60c8-1935">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1935">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="f60c8-1936">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f60c8-1936">KeyVault</span></span>

* <span data-ttu-id="f60c8-1937">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1937">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-1938">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-1938">Network</span></span>

* <span data-ttu-id="f60c8-1939">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1939">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="f60c8-1940">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1940">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-1941">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-1941">SQL</span></span>

* <span data-ttu-id="f60c8-1942">[重大な変更]`db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1942">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="f60c8-1943">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1943">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="f60c8-1944">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1944">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="f60c8-1945">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1945">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="f60c8-1946">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1946">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="f60c8-1947">`requestedServiceObjectiveName`.</span><span class="sxs-lookup"><span data-stu-id="f60c8-1947">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="f60c8-1948">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1948">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="f60c8-1949">`edition`.</span><span class="sxs-lookup"><span data-stu-id="f60c8-1949">`edition`.</span></span> <span data-ttu-id="f60c8-1950">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1950">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="f60c8-1951">`elasticPoolName`.</span><span class="sxs-lookup"><span data-stu-id="f60c8-1951">`elasticPoolName`.</span></span> <span data-ttu-id="f60c8-1952">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1952">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="f60c8-1953">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1953">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="f60c8-1954">`edition`.</span><span class="sxs-lookup"><span data-stu-id="f60c8-1954">`edition`.</span></span> <span data-ttu-id="f60c8-1955">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1955">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="f60c8-1956">`dtu`.</span><span class="sxs-lookup"><span data-stu-id="f60c8-1956">`dtu`.</span></span> <span data-ttu-id="f60c8-1957">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1957">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="f60c8-1958">`databaseDtuMin`.</span><span class="sxs-lookup"><span data-stu-id="f60c8-1958">`databaseDtuMin`.</span></span> <span data-ttu-id="f60c8-1959">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1959">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="f60c8-1960">`databaseDtuMax`.</span><span class="sxs-lookup"><span data-stu-id="f60c8-1960">`databaseDtuMax`.</span></span> <span data-ttu-id="f60c8-1961">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-1961">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="f60c8-1962">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1962">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="f60c8-1963">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1963">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-1964">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-1964">Storage</span></span>

* <span data-ttu-id="f60c8-1965">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1965">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="f60c8-1966">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1966">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-1967">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-1967">VM</span></span>

* <span data-ttu-id="f60c8-1968">[重大な変更]`--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1968">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="f60c8-1969">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="f60c8-1969">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="f60c8-1970">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1970">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="f60c8-1971">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1971">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="f60c8-1972">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1972">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="f60c8-1973">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-1973">May 7, 2018</span></span>

<span data-ttu-id="f60c8-1974">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="f60c8-1974">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-1975">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-1975">Core</span></span>

* <span data-ttu-id="f60c8-1976">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1976">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="f60c8-1977">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1977">Added limited support for positional arguments</span></span>
* <span data-ttu-id="f60c8-1978">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1978">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="f60c8-1979">#5591</span><span class="sxs-lookup"><span data-stu-id="f60c8-1979">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="f60c8-1980">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-1980">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="f60c8-1981">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="f60c8-1981">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="f60c8-1982">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1982">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="f60c8-1983">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1983">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="f60c8-1984">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1984">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-1985">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-1985">ACR</span></span>

* <span data-ttu-id="f60c8-1986">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1986">Added ACR Build commands</span></span>
* <span data-ttu-id="f60c8-1987">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1987">Improved resource not found error messages</span></span>
* <span data-ttu-id="f60c8-1988">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1988">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="f60c8-1989">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1989">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="f60c8-1990">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1990">Improved repository commands error messages</span></span>
* <span data-ttu-id="f60c8-1991">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1991">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-1992">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1992">ACS</span></span>

* <span data-ttu-id="f60c8-1993">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1993">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="f60c8-1994">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1994">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="f60c8-1995">AMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-1995">AMS</span></span>

* <span data-ttu-id="f60c8-1996">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="f60c8-1996">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-1997">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-1997">Appservice</span></span>

* <span data-ttu-id="f60c8-1998">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1998">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="f60c8-1999">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-1999">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="f60c8-2000">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2000">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="f60c8-2001">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2001">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="f60c8-2002">Batch AI</span><span class="sxs-lookup"><span data-stu-id="f60c8-2002">Batch AI</span></span>

* <span data-ttu-id="f60c8-2003">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2003">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="f60c8-2004">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="f60c8-2004">Cognitive Services</span></span>

* <span data-ttu-id="f60c8-2005">`cognitiveservices account create` の例の誤りを修正しました ([#5603](https://github.com/Azure/azure-cli/issues/5603))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2005">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="f60c8-2006">従量課金</span><span class="sxs-lookup"><span data-stu-id="f60c8-2006">Consumption</span></span>

* <span data-ttu-id="f60c8-2007">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2007">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-2008">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-2008">Container</span></span>

* <span data-ttu-id="f60c8-2009">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2009">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="f60c8-2010">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-2010">Cosmos DB</span></span>

* <span data-ttu-id="f60c8-2011">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2011">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="f60c8-2012">DMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2012">DMS</span></span>

* <span data-ttu-id="f60c8-2013">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2013">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="f60c8-2014">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f60c8-2014">Extension</span></span>

* <span data-ttu-id="f60c8-2015">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2015">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-2016">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-2016">Interactive</span></span>

* <span data-ttu-id="f60c8-2017">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2017">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="f60c8-2018">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2018">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="f60c8-2019">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2019">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="f60c8-2020">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2020">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="f60c8-2021">ラボ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2021">Lab</span></span>

* <span data-ttu-id="f60c8-2022">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2022">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2023">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2023">Network</span></span>

* <span data-ttu-id="f60c8-2024">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2024">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="f60c8-2025">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-2025">Profile</span></span>

* <span data-ttu-id="f60c8-2026">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2026">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="f60c8-2027">[重大な変更]`--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2027">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="f60c8-2028">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2028">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="f60c8-2029">Redis</span><span class="sxs-lookup"><span data-stu-id="f60c8-2029">Redis</span></span>

* <span data-ttu-id="f60c8-2030">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2030">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="f60c8-2031">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2031">Deprecated `redis list-all`.</span></span> <span data-ttu-id="f60c8-2032">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2032">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="f60c8-2033">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2033">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="f60c8-2034">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2034">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-2035">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-2035">Role</span></span>

* <span data-ttu-id="f60c8-2036">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2036">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2037">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2037">Storage</span></span>

* <span data-ttu-id="f60c8-2038">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2038">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="f60c8-2039">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2039">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="f60c8-2040">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="f60c8-2040">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="f60c8-2041">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2041">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="f60c8-2042">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2042">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2043">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2043">VM</span></span>

* <span data-ttu-id="f60c8-2044">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2044">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="f60c8-2045">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2045">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="f60c8-2046">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="f60c8-2046">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="f60c8-2047">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2047">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="f60c8-2048">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2048">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="f60c8-2049">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2049">Added write accelerator support</span></span>
* <span data-ttu-id="f60c8-2050">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2050">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="f60c8-2051">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2051">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="f60c8-2052">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2052">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="f60c8-2053">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2053">April 10, 2018</span></span>

<span data-ttu-id="f60c8-2054">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="f60c8-2054">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-2055">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-2055">ACR</span></span>

* <span data-ttu-id="f60c8-2056">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2056">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2057">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2057">ACS</span></span>

* <span data-ttu-id="f60c8-2058">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2058">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2059">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2059">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="f60c8-2061">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2061">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="f60c8-2062">BatchAI</span><span class="sxs-lookup"><span data-stu-id="f60c8-2062">BatchAI</span></span>

* <span data-ttu-id="f60c8-2063">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2063">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="f60c8-2064">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="f60c8-2064">Job level mounting</span></span>
  - <span data-ttu-id="f60c8-2065">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="f60c8-2065">Environment variables with secret values</span></span>
  - <span data-ttu-id="f60c8-2066">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="f60c8-2066">Performance counters settings</span></span>
  - <span data-ttu-id="f60c8-2067">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="f60c8-2067">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="f60c8-2068">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="f60c8-2068">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="f60c8-2069">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="f60c8-2069">Usage and limits reporting</span></span>
  - <span data-ttu-id="f60c8-2070">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="f60c8-2070">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="f60c8-2071">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="f60c8-2071">Support for custom images</span></span>
  - <span data-ttu-id="f60c8-2072">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2072">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="f60c8-2073">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2073">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="f60c8-2074">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2074">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="f60c8-2075">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="f60c8-2075">National clouds are supported</span></span>
* <span data-ttu-id="f60c8-2076">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2076">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="f60c8-2077">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2077">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="f60c8-2078">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2078">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="f60c8-2079">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2079">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="f60c8-2080">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2080">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="f60c8-2081">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2081">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="f60c8-2082">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2082">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="f60c8-2083">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2083">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="f60c8-2084">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="f60c8-2084">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="f60c8-2085">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2085">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="f60c8-2086">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2086">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="f60c8-2087">[重大な変更]`job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2087">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="f60c8-2088">[重大な変更]`cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2088">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="f60c8-2089">課金</span><span class="sxs-lookup"><span data-stu-id="f60c8-2089">Billing</span></span>

* <span data-ttu-id="f60c8-2090">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2090">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="f60c8-2091">従量課金</span><span class="sxs-lookup"><span data-stu-id="f60c8-2091">Consumption</span></span>

* <span data-ttu-id="f60c8-2092">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2092">Added `marketplace` commands</span></span>
* <span data-ttu-id="f60c8-2093">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2093">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="f60c8-2094">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2094">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="f60c8-2095">[重大な変更]`reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2095">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="f60c8-2096">[重大な変更]`reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2096">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="f60c8-2097">[重大な変更]`pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2097">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-2098">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-2098">Container</span></span>

* <span data-ttu-id="f60c8-2099">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2099">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="f60c8-2100">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2100">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="f60c8-2101">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f60c8-2101">Extension</span></span>

* <span data-ttu-id="f60c8-2102">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2102">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-2103">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-2103">Interactive</span></span>

* <span data-ttu-id="f60c8-2104">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2104">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="f60c8-2105">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2105">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="f60c8-2106">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2106">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2107">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2107">Network</span></span>

* <span data-ttu-id="f60c8-2108">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2108">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="f60c8-2109">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2109">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="f60c8-2110">#4910</span><span class="sxs-lookup"><span data-stu-id="f60c8-2110">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="f60c8-2111">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2111">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="f60c8-2112">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2112">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="f60c8-2113">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2113">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="f60c8-2114">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2114">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="f60c8-2115">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2115">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-2116">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-2116">Profile</span></span>

* <span data-ttu-id="f60c8-2117">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2117">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="f60c8-2118">[重大な変更]`--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2118">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-2119">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2119">RDBMS</span></span>

* <span data-ttu-id="f60c8-2120">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2120">Added `georestore` command</span></span>
* <span data-ttu-id="f60c8-2121">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2121">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2122">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2122">Resource</span></span>

* <span data-ttu-id="f60c8-2123">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2123">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="f60c8-2124">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2124">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-2125">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-2125">SQL</span></span>

* <span data-ttu-id="f60c8-2126">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2126">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2127">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2127">Storage</span></span>

* <span data-ttu-id="f60c8-2128">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2128">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2129">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2129">VM</span></span>

* <span data-ttu-id="f60c8-2130">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2130">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="f60c8-2131">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2131">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="f60c8-2133">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2133">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="f60c8-2134">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2134">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="f60c8-2135">#5718</span><span class="sxs-lookup"><span data-stu-id="f60c8-2135">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="f60c8-2136">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2136">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="f60c8-2137">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2137">March 27, 2018</span></span>

<span data-ttu-id="f60c8-2138">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="f60c8-2138">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-2139">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-2139">Core</span></span>

* <span data-ttu-id="f60c8-2140">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2140">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2141">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2141">ACS</span></span>

* <span data-ttu-id="f60c8-2142">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2142">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2143">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2143">Appservice</span></span>

* <span data-ttu-id="f60c8-2144">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2144">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="f60c8-2145">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2145">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="f60c8-2146">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2146">Backup</span></span>

* <span data-ttu-id="f60c8-2147">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2147">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="f60c8-2148">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2148">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="f60c8-2149">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2149">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="f60c8-2150">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2150">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-2151">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-2151">Container</span></span>

* <span data-ttu-id="f60c8-2152">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2152">Added `container exec` command.</span></span> <span data-ttu-id="f60c8-2153">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2153">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="f60c8-2154">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2154">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="f60c8-2155">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f60c8-2155">Extension</span></span>

* <span data-ttu-id="f60c8-2156">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2156">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="f60c8-2157">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2157">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="f60c8-2158">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2158">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-2159">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-2159">Interactive</span></span>

* <span data-ttu-id="f60c8-2160">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2160">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="f60c8-2161">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2161">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="f60c8-2162">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2162">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="f60c8-2163">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2163">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="f60c8-2164">ラボ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2164">Lab</span></span>

* <span data-ttu-id="f60c8-2165">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2165">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-2166">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-2166">Monitor</span></span>

* <span data-ttu-id="f60c8-2167">`--top`、`--orderby`、および `--namespace` のサポートを `metrics list` に追加しました ([#5785](https://github.com/Azure/azure-cli/issues/5785))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2167">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="f60c8-2168">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2168">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="f60c8-2169">`--namespace` のサポートを `metrics list-definitions` に追加しました ([#5785](https://github.com/Azure/azure-cli/issues/5785))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2169">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2170">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2170">Network</span></span>

* <span data-ttu-id="f60c8-2171">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2171">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-2172">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-2172">Profile</span></span>

* <span data-ttu-id="f60c8-2173">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2173">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-2174">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2174">RDBMS</span></span>

* <span data-ttu-id="f60c8-2175">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2175">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2176">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2176">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="f60c8-2178">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-2178">Role</span></span>

* <span data-ttu-id="f60c8-2179">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2179">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="f60c8-2180">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2180">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="f60c8-2181">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2181">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="f60c8-2182">[重大な変更]`az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2182">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="f60c8-2183">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2183">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2184">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2184">Storage</span></span>

* <span data-ttu-id="f60c8-2185">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2185">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="f60c8-2186">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="f60c8-2186">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2187">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2187">VM</span></span>

* <span data-ttu-id="f60c8-2188">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2188">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="f60c8-2189">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2189">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="f60c8-2190">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2190">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="f60c8-2191">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2191">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="f60c8-2192">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2192">March 13, 2018</span></span>

<span data-ttu-id="f60c8-2193">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="f60c8-2193">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-2194">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-2194">ACR</span></span>

* <span data-ttu-id="f60c8-2195">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2195">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="f60c8-2196">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2196">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="f60c8-2197">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2197">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2198">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2198">ACS</span></span>

* <span data-ttu-id="f60c8-2199">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2199">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="f60c8-2200">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2200">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="f60c8-2201">Advisor</span><span class="sxs-lookup"><span data-stu-id="f60c8-2201">Advisor</span></span>

* <span data-ttu-id="f60c8-2202">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2202">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="f60c8-2203">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2203">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="f60c8-2204">[重大な変更]`advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2204">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="f60c8-2205">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2205">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="f60c8-2206">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2206">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2207">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2207">Appservice</span></span>

* <span data-ttu-id="f60c8-2208">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2208">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="f60c8-2209">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2209">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="f60c8-2210">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2210">Eventhubs</span></span>

* <span data-ttu-id="f60c8-2211">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2211">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="f60c8-2212">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f60c8-2212">Extension</span></span>

* <span data-ttu-id="f60c8-2213">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2213">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-2214">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-2214">Interactive</span></span>

* <span data-ttu-id="f60c8-2215">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2215">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="f60c8-2216">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="f60c8-2216">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="f60c8-2217">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="f60c8-2217">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="f60c8-2218">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2218">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-2219">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-2219">Monitor</span></span>

* <span data-ttu-id="f60c8-2220">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2220">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="f60c8-2221">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2221">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="f60c8-2222">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2222">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="f60c8-2223">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2223">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2224">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2224">Network</span></span>

* <span data-ttu-id="f60c8-2225">[重大な変更]`route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2225">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="f60c8-2226">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2226">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="f60c8-2227">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2227">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="f60c8-2228">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2228">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-2229">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-2229">Profile</span></span>

* <span data-ttu-id="f60c8-2230">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2230">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="f60c8-2231">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2231">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-2232">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2232">RDBMS</span></span>

* <span data-ttu-id="f60c8-2233">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2233">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="f60c8-2234">Service Bus</span><span class="sxs-lookup"><span data-stu-id="f60c8-2234">Service Bus</span></span>

* <span data-ttu-id="f60c8-2235">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2235">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2236">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2236">Storage</span></span>

* <span data-ttu-id="f60c8-2237">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2237">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="f60c8-2238">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2238">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2239">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2239">VM</span></span>

* <span data-ttu-id="f60c8-2240">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2240">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="f60c8-2241">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2241">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="f60c8-2242">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2242">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="f60c8-2243">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2243">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="f60c8-2244">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2244">February 27, 2018</span></span>

<span data-ttu-id="f60c8-2245">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="f60c8-2245">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-2246">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-2246">Core</span></span>

* <span data-ttu-id="f60c8-2247">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="f60c8-2247">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="f60c8-2248">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2248">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="f60c8-2249">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2249">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2250">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2250">ACS</span></span>

* <span data-ttu-id="f60c8-2251">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2251">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="f60c8-2252">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="f60c8-2252">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="f60c8-2253">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2253">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="f60c8-2254">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2254">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2255">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2255">Appservice</span></span>

* <span data-ttu-id="f60c8-2256">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="f60c8-2256">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="f60c8-2257">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="f60c8-2257">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="f60c8-2258">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="f60c8-2258">Cognitive Services</span></span>

* <span data-ttu-id="f60c8-2259">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2259">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="f60c8-2260">従量課金</span><span class="sxs-lookup"><span data-stu-id="f60c8-2260">Consumption</span></span>

* <span data-ttu-id="f60c8-2261">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2261">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="f60c8-2262">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2262">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-2263">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-2263">Container</span></span>

* <span data-ttu-id="f60c8-2264">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2264">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2265">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2265">Network</span></span>

* <span data-ttu-id="f60c8-2266">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="f60c8-2266">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2267">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2267">Resource</span></span>

* <span data-ttu-id="f60c8-2268">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2268">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-2269">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-2269">Role</span></span>

* <span data-ttu-id="f60c8-2270">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2270">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-2271">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-2271">SQL</span></span>

* <span data-ttu-id="f60c8-2272">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2272">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2273">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2273">Storage</span></span>

* <span data-ttu-id="f60c8-2274">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2274">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2275">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2275">VM</span></span>

* <span data-ttu-id="f60c8-2276">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2276">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="f60c8-2277">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2277">February 13, 2018</span></span>

<span data-ttu-id="f60c8-2278">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="f60c8-2278">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-2279">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-2279">Core</span></span>

* <span data-ttu-id="f60c8-2280">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2280">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2281">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2281">ACS</span></span>

* <span data-ttu-id="f60c8-2282">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2282">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="f60c8-2283">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2283">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="f60c8-2284">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2284">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="f60c8-2285">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2285">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="f60c8-2286">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2286">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="f60c8-2287">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2287">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="f60c8-2288">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2288">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="f60c8-2289">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2289">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2290">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2290">Appservice</span></span>

* <span data-ttu-id="f60c8-2291">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2291">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="f60c8-2292">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2292">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="f60c8-2293">CDN</span><span class="sxs-lookup"><span data-stu-id="f60c8-2293">CDN</span></span>

* <span data-ttu-id="f60c8-2294">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2294">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-2295">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-2295">Container</span></span>

* <span data-ttu-id="f60c8-2296">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2296">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="f60c8-2297">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2297">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-2298">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-2298">CosmosDB</span></span>

* <span data-ttu-id="f60c8-2299">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2299">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="f60c8-2300">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f60c8-2300">Extension</span></span>

* <span data-ttu-id="f60c8-2301">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2301">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="f60c8-2302">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2302">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="f60c8-2303">フィードバック</span><span class="sxs-lookup"><span data-stu-id="f60c8-2303">Feedback</span></span>

* <span data-ttu-id="f60c8-2304">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2304">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-2305">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-2305">Interactive</span></span>

* <span data-ttu-id="f60c8-2306">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2306">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="f60c8-2307">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2307">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-2308">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-2308">IoT</span></span>

* <span data-ttu-id="f60c8-2309">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2309">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="f60c8-2310">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2310">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="f60c8-2311">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2311">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="f60c8-2312">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2312">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-2313">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-2313">Monitor</span></span>

* <span data-ttu-id="f60c8-2314">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2314">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2315">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2315">Network</span></span>

* <span data-ttu-id="f60c8-2316">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2316">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="f60c8-2317">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-2317">Profile</span></span>

* <span data-ttu-id="f60c8-2318">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2318">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2319">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2319">Resource</span></span>

* <span data-ttu-id="f60c8-2320">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2320">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-2321">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-2321">Role</span></span>

* <span data-ttu-id="f60c8-2322">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2322">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-2323">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-2323">SQL</span></span>

* <span data-ttu-id="f60c8-2324">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2324">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="f60c8-2325">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2325">Added `sql db rename`</span></span>
* <span data-ttu-id="f60c8-2326">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2326">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2327">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2327">Storage</span></span>

* <span data-ttu-id="f60c8-2328">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2328">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2329">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2329">VM</span></span>

* <span data-ttu-id="f60c8-2330">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2330">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="f60c8-2331">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2331">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="f60c8-2332">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2332">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="f60c8-2333">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2333">January 31, 2018</span></span>

<span data-ttu-id="f60c8-2334">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="f60c8-2334">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-2335">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-2335">Core</span></span>

* <span data-ttu-id="f60c8-2336">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2336">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="f60c8-2337">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2337">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="f60c8-2338">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2338">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="f60c8-2339">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2339">Use `--verbose` to see</span></span>
* <span data-ttu-id="f60c8-2340">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2340">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2341">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2341">ACS</span></span>

* <span data-ttu-id="f60c8-2342">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2342">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="f60c8-2343">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2343">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2344">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2344">Appservice</span></span>

* <span data-ttu-id="f60c8-2345">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2345">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="f60c8-2346">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2346">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="f60c8-2347">CDN</span><span class="sxs-lookup"><span data-stu-id="f60c8-2347">CDN</span></span>

* <span data-ttu-id="f60c8-2348">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2348">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-2349">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-2349">CosmosDB</span></span>

* <span data-ttu-id="f60c8-2350">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2350">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-2351">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-2351">Interactive</span></span>

* <span data-ttu-id="f60c8-2352">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2352">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2353">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2353">Network</span></span>

* <span data-ttu-id="f60c8-2354">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2354">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="f60c8-2355">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2355">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="f60c8-2356">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2356">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="f60c8-2357">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2357">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="f60c8-2358">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2358">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="f60c8-2359">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2359">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="f60c8-2360">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2360">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="f60c8-2361">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2361">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="f60c8-2362">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2362">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="f60c8-2363">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2363">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-2364">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-2364">Profile</span></span>

* <span data-ttu-id="f60c8-2365">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2365">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2366">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2366">Resource</span></span>

* <span data-ttu-id="f60c8-2367">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2367">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2368">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2368">Storage</span></span>

* <span data-ttu-id="f60c8-2369">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2369">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="f60c8-2370">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2370">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="f60c8-2371">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2371">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="f60c8-2372">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2372">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="f60c8-2373">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2373">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2374">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2374">VM</span></span>

* <span data-ttu-id="f60c8-2375">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2375">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="f60c8-2376">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2376">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="f60c8-2377">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2377">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="f60c8-2378">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2378">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="f60c8-2379">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2379">January 17, 2018</span></span>

<span data-ttu-id="f60c8-2380">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="f60c8-2380">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-2381">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-2381">ACR</span></span>

* <span data-ttu-id="f60c8-2382">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2382">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="f60c8-2383">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2383">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2384">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2384">ACS</span></span>

* <span data-ttu-id="f60c8-2385">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2385">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="f60c8-2386">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2386">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2387">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2387">Appservice</span></span>

* <span data-ttu-id="f60c8-2388">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2388">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="f60c8-2389">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2389">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="f60c8-2390">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2390">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="f60c8-2391">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2391">Backup</span></span>

* <span data-ttu-id="f60c8-2392">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2392">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="f60c8-2393">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2393">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="f60c8-2394">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2394">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="f60c8-2395">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2395">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="f60c8-2396">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2396">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-2397">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-2397">Batch</span></span>

* <span data-ttu-id="f60c8-2398">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2398">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="f60c8-2399">クラウド</span><span class="sxs-lookup"><span data-stu-id="f60c8-2399">Cloud</span></span>

* <span data-ttu-id="f60c8-2400">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2400">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="f60c8-2401">従量課金</span><span class="sxs-lookup"><span data-stu-id="f60c8-2401">Consumption</span></span>

* <span data-ttu-id="f60c8-2402">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2402">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="f60c8-2403">Event Grid</span><span class="sxs-lookup"><span data-stu-id="f60c8-2403">Event Grid</span></span>

* <span data-ttu-id="f60c8-2404">[重大な変更]`az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2404">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="f60c8-2405">[重大な変更]`az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2405">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="f60c8-2406">[重大な変更]`eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2406">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="f60c8-2407">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="f60c8-2407">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="f60c8-2408">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2408">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="f60c8-2409">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2409">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="f60c8-2410">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2410">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="f60c8-2411">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2411">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-2412">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-2412">Interactive</span></span>

* <span data-ttu-id="f60c8-2413">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2413">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="f60c8-2414">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2414">Fixed errors on startup</span></span>
* <span data-ttu-id="f60c8-2415">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2415">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-2416">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-2416">IoT</span></span>

* <span data-ttu-id="f60c8-2417">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2417">Added support for device provisioning service</span></span>
* <span data-ttu-id="f60c8-2418">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2418">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="f60c8-2419">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2419">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-2420">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-2420">Monitor</span></span>

* <span data-ttu-id="f60c8-2421">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2421">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="f60c8-2422">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2422">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="f60c8-2423">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2423">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2424">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2424">Network</span></span>

* <span data-ttu-id="f60c8-2425">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2425">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="f60c8-2426">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2426">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-2427">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-2427">Profile</span></span>

* <span data-ttu-id="f60c8-2428">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2428">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-2429">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-2429">Role</span></span>

* <span data-ttu-id="f60c8-2430">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2430">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="f60c8-2431">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f60c8-2431">Service Fabric</span></span>

* <span data-ttu-id="f60c8-2432">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2432">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="f60c8-2433">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2433">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2434">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2434">VM</span></span>

* <span data-ttu-id="f60c8-2435">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="f60c8-2435">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="f60c8-2436">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2436">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="f60c8-2437">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2437">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="f60c8-2438">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2438">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="f60c8-2439">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2439">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="f60c8-2440">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2440">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="f60c8-2441">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2441">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="f60c8-2442">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2442">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="f60c8-2443">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2443">December 19, 2017</span></span>

<span data-ttu-id="f60c8-2444">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="f60c8-2444">Version 2.0.23</span></span>

* <span data-ttu-id="f60c8-2445">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2445">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-2446">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-2446">Container</span></span>

* <span data-ttu-id="f60c8-2447">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2447">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2448">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2448">Network</span></span>

* <span data-ttu-id="f60c8-2449">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2449">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="f60c8-2450">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2450">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2451">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2451">Storage</span></span>

* <span data-ttu-id="f60c8-2452">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2452">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2453">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2453">VM</span></span>

* <span data-ttu-id="f60c8-2454">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2454">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="f60c8-2455">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2455">December 5, 2017</span></span>

<span data-ttu-id="f60c8-2456">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="f60c8-2456">Version 2.0.22</span></span>

* <span data-ttu-id="f60c8-2457">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2457">Removed `az component` commands.</span></span> <span data-ttu-id="f60c8-2458">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="f60c8-2458">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-2459">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-2459">Core</span></span>
* <span data-ttu-id="f60c8-2460">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2460">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="f60c8-2461">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2461">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2462">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2462">ACS</span></span>

* <span data-ttu-id="f60c8-2463">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2463">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="f60c8-2464">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2464">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="f60c8-2465">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2465">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="f60c8-2466">Advisor</span><span class="sxs-lookup"><span data-stu-id="f60c8-2466">Advisor</span></span>

* <span data-ttu-id="f60c8-2467">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2467">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2468">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2468">Appservice</span></span>

* <span data-ttu-id="f60c8-2469">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2469">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="f60c8-2470">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2470">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="f60c8-2471">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2471">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="f60c8-2472">従量課金</span><span class="sxs-lookup"><span data-stu-id="f60c8-2472">Consumption</span></span>

* <span data-ttu-id="f60c8-2473">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2473">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-2474">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-2474">Container</span></span>

* <span data-ttu-id="f60c8-2475">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2475">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-2476">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-2476">Monitor</span></span>

* <span data-ttu-id="f60c8-2477">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2477">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2478">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2478">Resource</span></span>

* <span data-ttu-id="f60c8-2479">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2479">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-2480">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-2480">Role</span></span>

* <span data-ttu-id="f60c8-2481">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2481">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="f60c8-2482">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2482">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="f60c8-2483">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2483">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-2484">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-2484">SQL</span></span>

* <span data-ttu-id="f60c8-2485">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2485">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="f60c8-2486">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2486">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2487">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2487">VM</span></span>

* <span data-ttu-id="f60c8-2488">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2488">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="f60c8-2489">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2489">November 14, 2017</span></span>

<span data-ttu-id="f60c8-2490">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="f60c8-2490">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-2491">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-2491">ACR</span></span>

* <span data-ttu-id="f60c8-2492">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2492">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="f60c8-2493">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2493">ACS</span></span>

* <span data-ttu-id="f60c8-2494">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2494">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="f60c8-2495">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2495">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="f60c8-2496">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2496">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="f60c8-2497">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2497">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="f60c8-2498">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2498">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2499">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2499">Appservice</span></span>

* <span data-ttu-id="f60c8-2500">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2500">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="f60c8-2501">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2501">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="f60c8-2502">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2502">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="f60c8-2503">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2503">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="f60c8-2504">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2504">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="f60c8-2505">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2505">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-2506">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-2506">Batch</span></span>

* <span data-ttu-id="f60c8-2507">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2507">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="f60c8-2508">Batchai</span><span class="sxs-lookup"><span data-stu-id="f60c8-2508">Batchai</span></span>

* <span data-ttu-id="f60c8-2509">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2509">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="f60c8-2510">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2510">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="f60c8-2511">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2511">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="f60c8-2512">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2512">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="f60c8-2513">クラウド</span><span class="sxs-lookup"><span data-stu-id="f60c8-2513">Cloud</span></span>

* <span data-ttu-id="f60c8-2514">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2514">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-2515">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-2515">Container</span></span>

* <span data-ttu-id="f60c8-2516">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2516">Added support to open multiple ports</span></span>
* <span data-ttu-id="f60c8-2517">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2517">Added container group restart policy</span></span>
* <span data-ttu-id="f60c8-2518">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2518">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="f60c8-2519">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2519">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="f60c8-2520">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f60c8-2520">Data Lake Analytics</span></span>

* <span data-ttu-id="f60c8-2521">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2521">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="f60c8-2522">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f60c8-2522">Data Lake Store</span></span>

* <span data-ttu-id="f60c8-2523">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2523">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="f60c8-2524">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f60c8-2524">Extension</span></span>

* <span data-ttu-id="f60c8-2525">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2525">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="f60c8-2526">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2526">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-2527">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-2527">IoT</span></span>

* <span data-ttu-id="f60c8-2528">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2528">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-2529">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-2529">Monitor</span></span>

* <span data-ttu-id="f60c8-2530">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2530">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2531">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2531">Network</span></span>

* <span data-ttu-id="f60c8-2532">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2532">Added support for CAA DNS records</span></span>
* <span data-ttu-id="f60c8-2533">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2533">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="f60c8-2534">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2534">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="f60c8-2535">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2535">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="f60c8-2536">Reservations</span><span class="sxs-lookup"><span data-stu-id="f60c8-2536">Reservations</span></span>

* <span data-ttu-id="f60c8-2537">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2537">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2538">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2538">Resource</span></span>

* <span data-ttu-id="f60c8-2539">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2539">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-2540">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-2540">SQL</span></span>

* <span data-ttu-id="f60c8-2541">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2541">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2542">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2542">Storage</span></span>

* <span data-ttu-id="f60c8-2543">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2543">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="f60c8-2544">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2544">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="f60c8-2545">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2545">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="f60c8-2546">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2546">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="f60c8-2547">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2547">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="f60c8-2548">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2548">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="f60c8-2549">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2549">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2550">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2550">VM</span></span>

* <span data-ttu-id="f60c8-2551">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2551">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="f60c8-2552">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2552">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="f60c8-2553">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2553">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="f60c8-2554">`vm format-secret` から `vm secret format` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-2554">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="f60c8-2555">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2555">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="f60c8-2556">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2556">October 24, 2017</span></span>

<span data-ttu-id="f60c8-2557">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="f60c8-2557">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-2558">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-2558">Core</span></span>

* <span data-ttu-id="f60c8-2559">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2559">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-2560">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-2560">ACR</span></span>

* <span data-ttu-id="f60c8-2561">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2561">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="f60c8-2562">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2562">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="f60c8-2563">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2563">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2564">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2564">ACS</span></span>

* <span data-ttu-id="f60c8-2565">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2565">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="f60c8-2566">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2566">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2567">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2567">Appservice</span></span>

* <span data-ttu-id="f60c8-2568">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2568">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="f60c8-2569">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f60c8-2569">Component</span></span>

* <span data-ttu-id="f60c8-2570">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2570">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-2571">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-2571">Monitor</span></span>

* <span data-ttu-id="f60c8-2572">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2572">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2573">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2573">Resource</span></span>

* <span data-ttu-id="f60c8-2574">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2574">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="f60c8-2575">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2575">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2576">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2576">VM</span></span>

* <span data-ttu-id="f60c8-2577">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2577">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="f60c8-2578">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2578">October 9, 2017</span></span>

<span data-ttu-id="f60c8-2579">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="f60c8-2579">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-2580">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-2580">Core</span></span>

* <span data-ttu-id="f60c8-2581">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2581">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2582">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2582">Appservice</span></span>

* <span data-ttu-id="f60c8-2583">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2583">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-2584">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-2584">Batch</span></span>

* <span data-ttu-id="f60c8-2585">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2585">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="f60c8-2586">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2586">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="f60c8-2587">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2587">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="f60c8-2588">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2588">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="f60c8-2589">Batchai</span><span class="sxs-lookup"><span data-stu-id="f60c8-2589">Batchai</span></span>

* <span data-ttu-id="f60c8-2590">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2590">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="f60c8-2591">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f60c8-2591">Keyvault</span></span>

* <span data-ttu-id="f60c8-2592">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2592">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="f60c8-2593">(#4448)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2593">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="f60c8-2594">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2594">Network</span></span>

* <span data-ttu-id="f60c8-2595">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2595">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="f60c8-2596">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2596">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2597">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2597">Resource</span></span>

* <span data-ttu-id="f60c8-2598">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2598">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="f60c8-2599">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2599">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="f60c8-2600">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2600">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="f60c8-2601">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2601">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-2602">Sql</span><span class="sxs-lookup"><span data-stu-id="f60c8-2602">Sql</span></span>

* <span data-ttu-id="f60c8-2603">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2603">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="f60c8-2604">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2604">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="f60c8-2605">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2605">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2606">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2606">Storage</span></span>

* <span data-ttu-id="f60c8-2607">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2607">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2608">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2608">Vm</span></span>

* <span data-ttu-id="f60c8-2609">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2609">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="f60c8-2610">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2610">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="f60c8-2611">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2611">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="f60c8-2612">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2612">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="f60c8-2613">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2613">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="f60c8-2614">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2614">September 22, 2017</span></span>

<span data-ttu-id="f60c8-2615">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="f60c8-2615">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2616">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2616">Resource</span></span>

* <span data-ttu-id="f60c8-2617">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2617">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="f60c8-2618">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2618">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="f60c8-2619">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2619">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="f60c8-2620">[重大な変更]`managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2620">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2621">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2621">Network</span></span>

* <span data-ttu-id="f60c8-2622">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2622">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="f60c8-2623">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2623">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="f60c8-2624">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2624">Added `asg` application security group commands</span></span>
* <span data-ttu-id="f60c8-2625">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2625">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="f60c8-2626">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2626">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="f60c8-2627">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2627">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="f60c8-2628">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2628">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2629">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2629">Storage</span></span>

* <span data-ttu-id="f60c8-2630">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2630">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="f60c8-2631">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="f60c8-2631">Eventgrid</span></span>

* <span data-ttu-id="f60c8-2632">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2632">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-2633">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-2633">SQL</span></span>

* <span data-ttu-id="f60c8-2634">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2634">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="f60c8-2635">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2635">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="f60c8-2636">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2636">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="f60c8-2637">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f60c8-2637">Keyvault</span></span>

* <span data-ttu-id="f60c8-2638">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2638">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2639">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2639">VM</span></span>

* <span data-ttu-id="f60c8-2640">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2640">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="f60c8-2641">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2641">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="f60c8-2642">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2642">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="f60c8-2643">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2643">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="f60c8-2644">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2644">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="f60c8-2645">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2645">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2646">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2646">ACS</span></span>

* <span data-ttu-id="f60c8-2647">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2647">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2648">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2648">Appservice</span></span>

* <span data-ttu-id="f60c8-2649">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2649">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="f60c8-2650">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2650">Backup</span></span>

* <span data-ttu-id="f60c8-2651">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2651">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="f60c8-2652">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2652">September 11, 2017</span></span>

<span data-ttu-id="f60c8-2653">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="f60c8-2653">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="f60c8-2654">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-2654">Core</span></span>

* <span data-ttu-id="f60c8-2655">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2655">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="f60c8-2656">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2656">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2657">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2657">Acs</span></span>

* <span data-ttu-id="f60c8-2658">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2658">Added `acs list-locations` command</span></span>
* <span data-ttu-id="f60c8-2659">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2659">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2660">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2660">Appservice</span></span>

* <span data-ttu-id="f60c8-2661">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2661">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="f60c8-2662">CDN</span><span class="sxs-lookup"><span data-stu-id="f60c8-2662">CDN</span></span>

* <span data-ttu-id="f60c8-2663">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2663">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="f60c8-2664">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f60c8-2664">Extension</span></span>

* <span data-ttu-id="f60c8-2665">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2665">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="f60c8-2666">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f60c8-2666">Keyvault</span></span>

* <span data-ttu-id="f60c8-2667">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2667">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2668">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2668">Network</span></span>

* <span data-ttu-id="f60c8-2669">`vnet list-private-access-services` から `vnet list-endpoint-services` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-2669">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="f60c8-2670">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2670">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="f60c8-2671">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2671">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="f60c8-2672">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2672">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="f60c8-2673">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2673">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2674">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2674">Resource</span></span>

* <span data-ttu-id="f60c8-2675">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2675">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="f60c8-2676">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2676">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="f60c8-2677">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2677">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="f60c8-2678">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2678">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-2679">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-2679">SQL</span></span>

* <span data-ttu-id="f60c8-2680">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2680">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2681">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2681">VM</span></span>

* <span data-ttu-id="f60c8-2682">固定:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="f60c8-2682">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="f60c8-2683">固定:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="f60c8-2683">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="f60c8-2684">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2684">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="f60c8-2685">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="f60c8-2685">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="f60c8-2686">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="f60c8-2686">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="f60c8-2687">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2687">August 31, 2017</span></span>

<span data-ttu-id="f60c8-2688">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="f60c8-2688">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="f60c8-2689">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f60c8-2689">Keyvault</span></span>

* <span data-ttu-id="f60c8-2690">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2690">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="f60c8-2691">SF</span><span class="sxs-lookup"><span data-stu-id="f60c8-2691">Sf</span></span>

* <span data-ttu-id="f60c8-2692">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2692">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2693">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2693">Storage</span></span>

* <span data-ttu-id="f60c8-2694">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2694">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="f60c8-2695">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2695">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="f60c8-2696">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2696">August 28, 2017</span></span>

<span data-ttu-id="f60c8-2697">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="f60c8-2697">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="f60c8-2698">CLI</span><span class="sxs-lookup"><span data-stu-id="f60c8-2698">CLI</span></span>

* <span data-ttu-id="f60c8-2699">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2699">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2700">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2700">ACS</span></span>

* <span data-ttu-id="f60c8-2701">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2701">Corrected preview regions</span></span>
* <span data-ttu-id="f60c8-2702">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2702">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="f60c8-2703">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2703">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2704">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2704">Appservice</span></span>

* <span data-ttu-id="f60c8-2705">[重大な変更]`az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2705">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="f60c8-2706">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2706">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="f60c8-2707">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2707">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="f60c8-2708">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2708">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="f60c8-2709">固定:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="f60c8-2709">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-2710">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-2710">IoT</span></span>

* <span data-ttu-id="f60c8-2711">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2711">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2712">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2712">Network</span></span>

* <span data-ttu-id="f60c8-2713">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2713">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="f60c8-2714">[重大な変更]`vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2714">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="f60c8-2715">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2715">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="f60c8-2716">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2716">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="f60c8-2717">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2717">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-2718">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-2718">Profile</span></span>

* <span data-ttu-id="f60c8-2719">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2719">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="f60c8-2720">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f60c8-2720">Service Fabric</span></span>

* <span data-ttu-id="f60c8-2721">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2721">Preview release</span></span>
* <span data-ttu-id="f60c8-2722">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2722">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="f60c8-2723">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2723">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="f60c8-2724">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2724">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2725">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2725">Storage</span></span>

* <span data-ttu-id="f60c8-2726">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2726">Enabled setting blob tier</span></span>
* <span data-ttu-id="f60c8-2727">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2727">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="f60c8-2728">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2728">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="f60c8-2729">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2729">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="f60c8-2730">[重大な変更]`az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2730">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="f60c8-2731">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="f60c8-2731">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2732">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2732">VM</span></span>

* <span data-ttu-id="f60c8-2733">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2733">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="f60c8-2734">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2734">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="f60c8-2735">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2735">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="f60c8-2736">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2736">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="f60c8-2737">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2737">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="f60c8-2738">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2738">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="f60c8-2739">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2739">August 15, 2017</span></span>

<span data-ttu-id="f60c8-2740">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="f60c8-2740">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2741">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2741">ACS</span></span>

* <span data-ttu-id="f60c8-2742">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2742">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2743">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2743">Appservice</span></span>

* <span data-ttu-id="f60c8-2744">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2744">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="f60c8-2745">Event Grid</span><span class="sxs-lookup"><span data-stu-id="f60c8-2745">Event Grid</span></span>

* <span data-ttu-id="f60c8-2746">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2746">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="f60c8-2747">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2747">August 11, 2017</span></span>

<span data-ttu-id="f60c8-2748">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="f60c8-2748">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2749">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2749">ACS</span></span>

* <span data-ttu-id="f60c8-2750">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2750">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-2751">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-2751">Batch</span></span>

* <span data-ttu-id="f60c8-2752">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2752">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="f60c8-2753">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2753">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="f60c8-2754">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2754">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="f60c8-2755">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2755">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="f60c8-2756">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2756">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="f60c8-2757">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2757">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="f60c8-2758">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f60c8-2758">Component</span></span>

* <span data-ttu-id="f60c8-2759">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2759">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="f60c8-2760">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f60c8-2760">Container</span></span>

* <span data-ttu-id="f60c8-2761">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2761">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="f60c8-2762">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f60c8-2762">Data Lake Store</span></span>

* <span data-ttu-id="f60c8-2763">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2763">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="f60c8-2764">Event Grid</span><span class="sxs-lookup"><span data-stu-id="f60c8-2764">Event Grid</span></span>

* <span data-ttu-id="f60c8-2765">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2765">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2766">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2766">Network</span></span>

* <span data-ttu-id="f60c8-2767">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2767">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="f60c8-2768">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2768">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="f60c8-2769">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2769">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="f60c8-2770">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2770">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-2771">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-2771">Profile</span></span>

* <span data-ttu-id="f60c8-2772">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2772">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2773">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2773">Storage</span></span>

* <span data-ttu-id="f60c8-2774">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2774">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2775">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2775">VM</span></span>

* <span data-ttu-id="f60c8-2776">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2776">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="f60c8-2777">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2777">Exposed `list-skus` command</span></span>
* <span data-ttu-id="f60c8-2778">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2778">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="f60c8-2779">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2779">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="f60c8-2780">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2780">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="f60c8-2781">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2781">July 28, 2017</span></span>

<span data-ttu-id="f60c8-2782">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="f60c8-2782">Version 2.0.12</span></span>

* <span data-ttu-id="f60c8-2783">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2783">Added container commands</span></span>
* <span data-ttu-id="f60c8-2784">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2784">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="f60c8-2785">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-2785">Core</span></span>

* <span data-ttu-id="f60c8-2786">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2786">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="f60c8-2787">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2787">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="f60c8-2788">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2788">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="f60c8-2789">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2789">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="f60c8-2790">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2790">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="f60c8-2791">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2791">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="f60c8-2792">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2792">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="f60c8-2793">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2793">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="f60c8-2794">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2794">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="f60c8-2795">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2795">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="f60c8-2796">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2796">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="f60c8-2797">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2797">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="f60c8-2798">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2798">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="f60c8-2799">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2799">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="f60c8-2800">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2800">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="f60c8-2801">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2801">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="f60c8-2802">ACR</span><span class="sxs-lookup"><span data-stu-id="f60c8-2802">ACR</span></span>

* <span data-ttu-id="f60c8-2803">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2803">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="f60c8-2804">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2804">Support SKU update for managed registries</span></span>
* <span data-ttu-id="f60c8-2805">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2805">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="f60c8-2806">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2806">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="f60c8-2807">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2807">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="f60c8-2808">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2808">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2809">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2809">ACS</span></span>

* <span data-ttu-id="f60c8-2810">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2810">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2811">Appservice</span><span class="sxs-lookup"><span data-stu-id="f60c8-2811">Appservice</span></span>

* <span data-ttu-id="f60c8-2812">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2812">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="f60c8-2813">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2813">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="f60c8-2814">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2814">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="f60c8-2815">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2815">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="f60c8-2816">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2816">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="f60c8-2817">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2817">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="f60c8-2818">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2818">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="f60c8-2819">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2819">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="f60c8-2820">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2820">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="f60c8-2821">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="f60c8-2821">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="f60c8-2822">Batch</span><span class="sxs-lookup"><span data-stu-id="f60c8-2822">Batch</span></span>

* <span data-ttu-id="f60c8-2823">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2823">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="f60c8-2824">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2824">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="f60c8-2825">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2825">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="f60c8-2826">CDN</span><span class="sxs-lookup"><span data-stu-id="f60c8-2826">CDN</span></span>

* <span data-ttu-id="f60c8-2827">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2827">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="f60c8-2828">クラウド</span><span class="sxs-lookup"><span data-stu-id="f60c8-2828">Cloud</span></span>

* <span data-ttu-id="f60c8-2829">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2829">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="f60c8-2830">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="f60c8-2830">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="f60c8-2831">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2831">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="f60c8-2832">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2832">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="f60c8-2833">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2833">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-2834">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-2834">CosmosDB</span></span>

* <span data-ttu-id="f60c8-2835">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2835">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="f60c8-2836">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2836">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="f60c8-2837">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f60c8-2837">Data Lake Analytics</span></span>

* <span data-ttu-id="f60c8-2838">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2838">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="f60c8-2839">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2839">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="f60c8-2840">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2840">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="f60c8-2841">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f60c8-2841">Data Lake Store</span></span>

* <span data-ttu-id="f60c8-2842">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2842">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="f60c8-2843">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2843">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="f60c8-2844">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2844">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="f60c8-2845">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2845">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="f60c8-2846">Interactive</span><span class="sxs-lookup"><span data-stu-id="f60c8-2846">Interactive</span></span>

* <span data-ttu-id="f60c8-2847">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2847">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="f60c8-2848">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2848">Increased test coverage</span></span>
* <span data-ttu-id="f60c8-2849">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2849">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="f60c8-2850">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2850">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="f60c8-2851">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2851">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="f60c8-2852">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2852">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="f60c8-2853">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2853">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="f60c8-2854">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2854">Added `--progress` flag</span></span>
* <span data-ttu-id="f60c8-2855">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2855">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="f60c8-2856">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2856">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="f60c8-2857">IoT</span><span class="sxs-lookup"><span data-stu-id="f60c8-2857">IoT</span></span>

* <span data-ttu-id="f60c8-2858">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2858">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="f60c8-2859">(#3934)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2859">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="f60c8-2860">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f60c8-2860">Key vault</span></span>

* <span data-ttu-id="f60c8-2861">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2861">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="f60c8-2862">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="f60c8-2862">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="f60c8-2863">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="f60c8-2863">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="f60c8-2864">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="f60c8-2864">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="f60c8-2865">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="f60c8-2865">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="f60c8-2866">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2866">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="f60c8-2867">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2867">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="f60c8-2868">(#3307)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2868">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="f60c8-2869">ラボ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2869">Lab</span></span>

* <span data-ttu-id="f60c8-2870">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2870">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="f60c8-2871">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2871">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-2872">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-2872">Monitor</span></span>

* <span data-ttu-id="f60c8-2873">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2873">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="f60c8-2874">`monitor alert-rule-incidents list` から `monitor alert list-incidents` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-2874">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="f60c8-2875">`monitor alert-rule-incidents show` から `monitor alert show-incident` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-2875">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="f60c8-2876">`monitor metric-defintions list` から `monitor metrics list-definitions` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-2876">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="f60c8-2877">`monitor alert-rules` から `monitor alert` への名称変更</span><span class="sxs-lookup"><span data-stu-id="f60c8-2877">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="f60c8-2878">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-2878">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="f60c8-2879">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2879">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="f60c8-2880">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2880">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="f60c8-2881">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2881">`location` no longer required</span></span>
  * <span data-ttu-id="f60c8-2882">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2882">Add name and ID support for target</span></span>
  * <span data-ttu-id="f60c8-2883">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2883">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="f60c8-2884">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2884">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="f60c8-2885">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2885">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="f60c8-2886">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2886">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="f60c8-2887">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2887">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="f60c8-2888">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2888">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-2889">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-2889">Network</span></span>

* <span data-ttu-id="f60c8-2890">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2890">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="f60c8-2891">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2891">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="f60c8-2892">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2892">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="f60c8-2893">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2893">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="f60c8-2894">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2894">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="f60c8-2895">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2895">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="f60c8-2896">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2896">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="f60c8-2897">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2897">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="f60c8-2898">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2898">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="f60c8-2899">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2899">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="f60c8-2900">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2900">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="f60c8-2901">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2901">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="f60c8-2902">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2902">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="f60c8-2903">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2903">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="f60c8-2904">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2904">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="f60c8-2905">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2905">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="f60c8-2906">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2906">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="f60c8-2907">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2907">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="f60c8-2908">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2908">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="f60c8-2909">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2909">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="f60c8-2910">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2910">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="f60c8-2911">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2911">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="f60c8-2912">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2912">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="f60c8-2913">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2913">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="f60c8-2914">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2914">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="f60c8-2915">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2915">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="f60c8-2916">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2916">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-2917">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-2917">Profile</span></span>

* <span data-ttu-id="f60c8-2918">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2918">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="f60c8-2919">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2919">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="f60c8-2920">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2920">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="f60c8-2921">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2921">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="f60c8-2922">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2922">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="f60c8-2923">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2923">RDBMS</span></span>

* <span data-ttu-id="f60c8-2924">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2924">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="f60c8-2925">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2925">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="f60c8-2926">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2926">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="f60c8-2927">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2927">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-2928">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-2928">Resource</span></span>

* <span data-ttu-id="f60c8-2929">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2929">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="f60c8-2930">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2930">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="f60c8-2931">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2931">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="f60c8-2932">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2932">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="f60c8-2933">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2933">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="f60c8-2934">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2934">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="f60c8-2935">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2935">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="f60c8-2936">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2936">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-2937">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-2937">Role</span></span>

* <span data-ttu-id="f60c8-2938">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2938">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="f60c8-2939">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2939">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="f60c8-2940">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2940">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="f60c8-2941">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2941">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="f60c8-2942">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2942">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="f60c8-2943">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f60c8-2943">Service Fabric</span></span>
* <span data-ttu-id="f60c8-2944">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2944">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="f60c8-2945">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2945">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="f60c8-2946">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2946">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-2947">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-2947">SQL</span></span>

* <span data-ttu-id="f60c8-2948">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2948">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="f60c8-2949">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2949">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="f60c8-2950">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2950">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-2951">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-2951">Storage</span></span>

* <span data-ttu-id="f60c8-2952">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2952">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="f60c8-2953">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2953">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="f60c8-2954">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2954">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="f60c8-2955">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2955">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="f60c8-2956">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2956">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="f60c8-2957">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2957">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-2958">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-2958">VM</span></span>

* <span data-ttu-id="f60c8-2959">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2959">Support configuring nsg</span></span>
* <span data-ttu-id="f60c8-2960">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2960">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="f60c8-2961">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="f60c8-2961">Support managed service identities</span></span>
* <span data-ttu-id="f60c8-2962">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2962">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="f60c8-2963">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="f60c8-2963">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="f60c8-2964">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-2964">May 10, 2017</span></span>

<span data-ttu-id="f60c8-2965">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="f60c8-2965">Version 2.0.6</span></span>

* <span data-ttu-id="f60c8-2966">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2966">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="f60c8-2967">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2967">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="f60c8-2968">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2968">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="f60c8-2969">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2969">Include Cognitive Services module</span></span>
* <span data-ttu-id="f60c8-2970">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2970">Include Service Fabric module</span></span>
* <span data-ttu-id="f60c8-2971">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2971">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="f60c8-2972">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2972">Add support for CDN commands</span></span>
* <span data-ttu-id="f60c8-2973">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2973">Remove Container module</span></span>
* <span data-ttu-id="f60c8-2974">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2974">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="f60c8-2975">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2975">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="f60c8-2976">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-2976">Core</span></span>

* <span data-ttu-id="f60c8-2977">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2977">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="f60c8-2978">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2978">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="f60c8-2979">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2979">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="f60c8-2980">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2980">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="f60c8-2981">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2981">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="f60c8-2982">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2982">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="f60c8-2983">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2983">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="f60c8-2984">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2984">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="f60c8-2985">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2985">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="f60c8-2986">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="f60c8-2986">core: Improved performance</span></span>
* <span data-ttu-id="f60c8-2987">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2987">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="f60c8-2988">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-2988">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-2989">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-2989">ACS</span></span>

* <span data-ttu-id="f60c8-2990">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2990">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="f60c8-2991">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2991">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="f60c8-2992">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2992">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="f60c8-2993">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="f60c8-2993">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-2994">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-2994">AppService</span></span>

* <span data-ttu-id="f60c8-2995">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2995">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="f60c8-2996">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2996">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="f60c8-2997">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="f60c8-2997">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="f60c8-2998">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2998">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="f60c8-2999">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-2999">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="f60c8-3000">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3000">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="f60c8-3001">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="f60c8-3001">support slot swap with preview</span></span>
* <span data-ttu-id="f60c8-3002">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3002">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="f60c8-3003">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3003">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f60c8-3004">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f60c8-3004">CosmosDB</span></span>

* <span data-ttu-id="f60c8-3005">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3005">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="f60c8-3006">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3006">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="f60c8-3007">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3007">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="f60c8-3008">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3008">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="f60c8-3009">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f60c8-3009">Data Lake Analytics</span></span>

* <span data-ttu-id="f60c8-3010">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3010">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="f60c8-3011">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-3011">Add support for new catalog item type: package.</span></span> <span data-ttu-id="f60c8-3012">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="f60c8-3012">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="f60c8-3013">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="f60c8-3013">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="f60c8-3014">テーブル</span><span class="sxs-lookup"><span data-stu-id="f60c8-3014">Table</span></span>
  * <span data-ttu-id="f60c8-3015">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="f60c8-3015">Table valued function</span></span>
  * <span data-ttu-id="f60c8-3016">表示</span><span class="sxs-lookup"><span data-stu-id="f60c8-3016">View</span></span>
  * <span data-ttu-id="f60c8-3017">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="f60c8-3017">Table Statistics.</span></span> <span data-ttu-id="f60c8-3018">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="f60c8-3018">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="f60c8-3019">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f60c8-3019">Data Lake Store</span></span>

* <span data-ttu-id="f60c8-3020">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3020">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="f60c8-3021">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3021">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="f60c8-3022">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="f60c8-3022">missed help for access show.</span></span> <span data-ttu-id="f60c8-3023">追加しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3023">adding it.</span></span> <span data-ttu-id="f60c8-3024">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3024">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="f60c8-3025">Find</span><span class="sxs-lookup"><span data-stu-id="f60c8-3025">Find</span></span>

* <span data-ttu-id="f60c8-3026">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3026">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="f60c8-3027">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f60c8-3027">KeyVault</span></span>

* <span data-ttu-id="f60c8-3028">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3028">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="f60c8-3029">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3029">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="f60c8-3030">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="f60c8-3030">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="f60c8-3031">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3031">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="f60c8-3032">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3032">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="f60c8-3033">ラボ</span><span class="sxs-lookup"><span data-stu-id="f60c8-3033">Lab</span></span>

* <span data-ttu-id="f60c8-3034">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3034">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="f60c8-3035">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3035">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="f60c8-3036">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3036">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="f60c8-3037">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3037">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="f60c8-3038">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3038">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="f60c8-3039">モニター</span><span class="sxs-lookup"><span data-stu-id="f60c8-3039">Monitor</span></span>

* <span data-ttu-id="f60c8-3040">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3040">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="f60c8-3041">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3041">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="f60c8-3042">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-3042">Network</span></span>

* <span data-ttu-id="f60c8-3043">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3043">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="f60c8-3044">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3044">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="f60c8-3045">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3045">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="f60c8-3046">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3046">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="f60c8-3047">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3047">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="f60c8-3048">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3048">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="f60c8-3049">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3049">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="f60c8-3050">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3050">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="f60c8-3051">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3051">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="f60c8-3052">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3052">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="f60c8-3053">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3053">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="f60c8-3054">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3054">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="f60c8-3055">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3055">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="f60c8-3056">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3056">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="f60c8-3057">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3057">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="f60c8-3058">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3058">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="f60c8-3059">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f60c8-3059">Profile</span></span>

* <span data-ttu-id="f60c8-3060">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3060">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="f60c8-3061">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3061">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="f60c8-3062">Redis</span><span class="sxs-lookup"><span data-stu-id="f60c8-3062">Redis</span></span>

* <span data-ttu-id="f60c8-3063">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3063">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="f60c8-3064">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3064">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="f60c8-3065">リソース</span><span class="sxs-lookup"><span data-stu-id="f60c8-3065">Resource</span></span>

* <span data-ttu-id="f60c8-3066">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3066">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="f60c8-3067">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3067">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="f60c8-3068">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3068">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="f60c8-3069">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3069">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="f60c8-3070">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3070">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="f60c8-3071">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3071">Add docs for az lock update.</span></span> <span data-ttu-id="f60c8-3072">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3072">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="f60c8-3073">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-3073">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="f60c8-3074">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3074">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="f60c8-3075">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="f60c8-3075">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="f60c8-3076">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3076">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="f60c8-3077">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3077">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="f60c8-3078">Role</span><span class="sxs-lookup"><span data-stu-id="f60c8-3078">Role</span></span>

* <span data-ttu-id="f60c8-3079">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3079">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="f60c8-3080">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3080">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="f60c8-3081">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3081">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="f60c8-3082">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-3082">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="f60c8-3083">SQL</span><span class="sxs-lookup"><span data-stu-id="f60c8-3083">SQL</span></span>

* <span data-ttu-id="f60c8-3084">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3084">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="f60c8-3085">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3085">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="f60c8-3086">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-3086">Storage</span></span>

* <span data-ttu-id="f60c8-3087">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="f60c8-3087">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="f60c8-3088">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3088">Add support for incremental blob copy</span></span>
* <span data-ttu-id="f60c8-3089">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3089">Add support for large block blob upload</span></span>
* <span data-ttu-id="f60c8-3090">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="f60c8-3090">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-3091">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-3091">VM</span></span>

* <span data-ttu-id="f60c8-3092">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3092">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="f60c8-3093">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="f60c8-3093">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="f60c8-3094">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="f60c8-3094">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="f60c8-3095">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="f60c8-3095">az vm/vmss disk</span></span>
  3. <span data-ttu-id="f60c8-3096">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="f60c8-3096">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="f60c8-3097">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="f60c8-3097">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="f60c8-3098">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3098">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="f60c8-3099">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-3099">April 3, 2017</span></span>

<span data-ttu-id="f60c8-3100">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="f60c8-3100">Version 2.0.2</span></span>

<span data-ttu-id="f60c8-3101">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="f60c8-3101">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="f60c8-3102">コア</span><span class="sxs-lookup"><span data-stu-id="f60c8-3102">Core</span></span>

* <span data-ttu-id="f60c8-3103">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="f60c8-3103">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="f60c8-3104">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3104">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="f60c8-3105">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3105">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="f60c8-3106">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3106">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="f60c8-3107">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3107">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="f60c8-3108">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="f60c8-3108">Add prompting for missing template parameters.</span></span> <span data-ttu-id="f60c8-3109">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3109">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="f60c8-3110">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="f60c8-3110">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="f60c8-3111">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="f60c8-3111">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="f60c8-3112">ACS</span><span class="sxs-lookup"><span data-stu-id="f60c8-3112">ACS</span></span>

* <span data-ttu-id="f60c8-3113">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3113">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="f60c8-3114">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="f60c8-3114">Add support for ssh key password prompting.</span></span> <span data-ttu-id="f60c8-3115">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3115">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="f60c8-3116">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="f60c8-3116">Add support for windows clusters.</span></span> <span data-ttu-id="f60c8-3117">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3117">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="f60c8-3118">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="f60c8-3118">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="f60c8-3119">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3119">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="f60c8-3120">AppService</span><span class="sxs-lookup"><span data-stu-id="f60c8-3120">AppService</span></span>

* <span data-ttu-id="f60c8-3121">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3121">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="f60c8-3122">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3122">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="f60c8-3123">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3123">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="f60c8-3124">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3124">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="f60c8-3125">DataLake</span><span class="sxs-lookup"><span data-stu-id="f60c8-3125">DataLake</span></span>

* <span data-ttu-id="f60c8-3126">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-3126">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="f60c8-3127">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f60c8-3127">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="f60c8-3128">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="f60c8-3128">DocuemntDB</span></span>

* <span data-ttu-id="f60c8-3129">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3129">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="f60c8-3130">VM</span><span class="sxs-lookup"><span data-stu-id="f60c8-3130">VM</span></span>

* <span data-ttu-id="f60c8-3131">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3131">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="f60c8-3132">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3132">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="f60c8-3133">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3133">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="f60c8-3134">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3134">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="f60c8-3135">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3135">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="f60c8-3136">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3136">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="f60c8-3137">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="f60c8-3137">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="f60c8-3138">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="f60c8-3138">February 27, 2017</span></span>

<span data-ttu-id="f60c8-3139">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="f60c8-3139">Version 2.0.0</span></span>

<span data-ttu-id="f60c8-3140">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="f60c8-3140">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="f60c8-3141">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="f60c8-3141">Container Service (acs)</span></span>
- <span data-ttu-id="f60c8-3142">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="f60c8-3142">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="f60c8-3143">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f60c8-3143">Networking</span></span>
- <span data-ttu-id="f60c8-3144">ストレージ</span><span class="sxs-lookup"><span data-stu-id="f60c8-3144">Storage</span></span>

<span data-ttu-id="f60c8-3145">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-3145">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="f60c8-3146">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="f60c8-3146">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="f60c8-3147">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-3147">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="f60c8-3148">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="f60c8-3148">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="f60c8-3149">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="f60c8-3149">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="f60c8-3150">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="f60c8-3150">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="f60c8-3151">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="f60c8-3151">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="f60c8-3152">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="f60c8-3152">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="f60c8-3153">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="f60c8-3153">Provide feedback from the command line with the `az feedback` command</span></span>

