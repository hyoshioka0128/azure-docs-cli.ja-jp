---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 01/07/2020
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 9fc54add3bfb2a75d1912c47f0a2571d9d065ec0
ms.sourcegitcommit: 5646008e7a521dd9a8a627418f57bd92ee180352
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/07/2020
ms.locfileid: "75694276"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="61bea-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="61bea-103">Azure CLI release notes</span></span>

## <a name="january-07-2020"></a><span data-ttu-id="61bea-104">2020 年 1 月 7 日</span><span class="sxs-lookup"><span data-stu-id="61bea-104">January 07, 2020</span></span>

<span data-ttu-id="61bea-105">バージョン 2.0.79</span><span class="sxs-lookup"><span data-stu-id="61bea-105">Version 2.0.79</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-106">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-106">ACR</span></span>

* <span data-ttu-id="61bea-107">[重大な変更] 'acr build'、'acr task create/update'、'acr run'、および 'acr pack' の '--os' パラメーターを削除します。</span><span class="sxs-lookup"><span data-stu-id="61bea-107">[BREAKING CHANGE] Remove '--os' parameter for 'acr build', 'acr task create/update', 'acr run', and 'acr pack'.</span></span> <span data-ttu-id="61bea-108">代わりに、'--platform' を使用してください。</span><span class="sxs-lookup"><span data-stu-id="61bea-108">Use '--platform' instead.</span></span>

### <a name="appconfig"></a><span data-ttu-id="61bea-109">AppConfig</span><span class="sxs-lookup"><span data-stu-id="61bea-109">AppConfig</span></span>

* <span data-ttu-id="61bea-110">機能フラグのインポート/エクスポートのサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="61bea-110">Add support for importing/exporting feature flags</span></span>
* <span data-ttu-id="61bea-111">keyvault 参照を作成するための新しいコマンド 'az appconfig kv set-keyvault' を追加します</span><span class="sxs-lookup"><span data-stu-id="61bea-111">Add new command 'az appconfig kv set-keyvault' for creating keyvault reference</span></span>
* <span data-ttu-id="61bea-112">機能フラグをファイルにエクスポートするときに、さまざまな名前付け規則をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-112">Support various naming conventions when exporting feature flags to file</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-113">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-113">AppService</span></span>

* <span data-ttu-id="61bea-114">問題 #7154 を修正:単一引用符ではなく、アクサン グラーブを使用するように、コマンド < > のドキュメントを更新しています</span><span class="sxs-lookup"><span data-stu-id="61bea-114">Fix issue #7154: Updating documentation for command <> to use back ticks instead of single quotes</span></span>
* <span data-ttu-id="61bea-115">問題 #11287 を修正: webapp up:既定で、up を使用して作成されたアプリを 'SSL 有効' にする必要がある</span><span class="sxs-lookup"><span data-stu-id="61bea-115">Fix issue #11287: webapp up: By default make the app created using up 'should be 'SSL enabled'</span></span>
* <span data-ttu-id="61bea-116">問題 #11592 を修正:HTML 静的サイトに az webapp up フラグを追加します</span><span class="sxs-lookup"><span data-stu-id="61bea-116">Fix issue #11592: Add az webapp up flag for html static sites</span></span>

### <a name="arm"></a><span data-ttu-id="61bea-117">ARM</span><span class="sxs-lookup"><span data-stu-id="61bea-117">ARM</span></span>

* <span data-ttu-id="61bea-118">`az resource tag` を修正:Recovery Services コンテナー タグを更新できない</span><span class="sxs-lookup"><span data-stu-id="61bea-118">Fix `az resource tag`: Recovery Services Vault tags cannot be updated</span></span>

### <a name="backup"></a><span data-ttu-id="61bea-119">バックアップ</span><span class="sxs-lookup"><span data-stu-id="61bea-119">Backup</span></span>

* <span data-ttu-id="61bea-120">IaasVM ワークロードの論理的な削除機能を有効にするための新しいコマンド 'backup protection undelete' を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-120">Added new command 'backup protection undelete' to enable soft-delete feature for IaasVM workload</span></span>
* <span data-ttu-id="61bea-121">backup-properties コマンドを設定するための新しいパラメーター '--soft-delete-feature-state' を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-121">Added new parameter '--soft-delete-feature-state' to set backup-properties command</span></span>
* <span data-ttu-id="61bea-122">IaasVM ワークロードのディスク除外のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-122">Added disk exclusion support for IaasVM workload</span></span>

### <a name="compute"></a><span data-ttu-id="61bea-123">Compute</span><span class="sxs-lookup"><span data-stu-id="61bea-123">Compute</span></span>

* <span data-ttu-id="61bea-124">Azure Stack プロファイルの `vm create` エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="61bea-124">Fix `vm create` failure in Azure Stack profile.</span></span>
* <span data-ttu-id="61bea-125">vm monitor metrics tail/list-definitions: VM のクエリ メトリックとリスト定義をサポートします。</span><span class="sxs-lookup"><span data-stu-id="61bea-125">vm monitor metrics tail/list-definitions: support query metric and list definitions for a vm.</span></span>
* <span data-ttu-id="61bea-126">az vm の新しい再適用コマンド アクションを追加します</span><span class="sxs-lookup"><span data-stu-id="61bea-126">Add new reapply command action for az vm</span></span>

### <a name="misc"></a><span data-ttu-id="61bea-127">その他</span><span class="sxs-lookup"><span data-stu-id="61bea-127">Misc.</span></span>

* <span data-ttu-id="61bea-128">既定の JSON 形式 または --output によって構成された形式で Azure CLI モジュールと拡張機能のバージョンを表示するプレビュー コマンド `az version show` を追加します</span><span class="sxs-lookup"><span data-stu-id="61bea-128">Add preview command `az version show` to show the versions of Azure CLI modules and extensions in JSON format by default or format configured by --output</span></span>

### <a name="event-hubs"></a><span data-ttu-id="61bea-129">Event Hubs</span><span class="sxs-lookup"><span data-stu-id="61bea-129">Event Hubs</span></span>

* <span data-ttu-id="61bea-130">[重大な変更] コマンド 'az eventhubs eventhub update' と 'az eventhubs eventhub create' から 'ReceiveDisabled' status オプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="61bea-130">[BREAKING CHANGE] Remove 'ReceiveDisabled' status option from command 'az eventhubs eventhub update' and 'az eventhubs eventhub create'.</span></span> <span data-ttu-id="61bea-131">このオプションは、イベント ハブ エンティティに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="61bea-131">This option is not valid for Event Hub entities.</span></span>

### <a name="service-bus"></a><span data-ttu-id="61bea-132">Service Bus</span><span class="sxs-lookup"><span data-stu-id="61bea-132">Service Bus</span></span>

* <span data-ttu-id="61bea-133">[重大な変更] コマンド 'az servicebus topic create'、'az servicebus topic update'、'az servicebus queue create'、および 'az servicebus queue update' から 'ReceiveDisabled' status オプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="61bea-133">[BREAKING CHANGE] Remove 'ReceiveDisabled' status option from command 'az servicebus topic create', 'az servicebus topic update', 'az servicebus queue create', and 'az servicebus queue update'.</span></span> <span data-ttu-id="61bea-134">このオプションは、Service Bus のトピックとキューに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="61bea-134">This option is not valid for Service Bus topics and queues.</span></span>

### <a name="rbac"></a><span data-ttu-id="61bea-135">RBAC</span><span class="sxs-lookup"><span data-stu-id="61bea-135">RBAC</span></span>

* <span data-ttu-id="61bea-136">#11712 を修正: アプリケーションまたはサービス プリンシパルが存在しない場合に `az ad app/sp show` で終了コード 3 が返されない</span><span class="sxs-lookup"><span data-stu-id="61bea-136">Fix #11712: `az ad app/sp show` does not return exit code 3 when the application or service principal does not exist</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-137">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-137">Storage</span></span>

* <span data-ttu-id="61bea-138">`az storage account create`:--enable-hierarchical-namespace パラメーターのプレビュー フラグを削除します</span><span class="sxs-lookup"><span data-stu-id="61bea-138">`az storage account create`: Remove preview flag for --enable-hierarchical-namespace parameter</span></span>
* <span data-ttu-id="61bea-139">API バージョン 2019-06-01 を使用するために azure-mgmt-storage バージョンを 7.0.0 に更新します</span><span class="sxs-lookup"><span data-stu-id="61bea-139">Update azure-mgmt-storage version to 7.0.0 to use api version 2019-06-01</span></span>
* <span data-ttu-id="61bea-140">ストレージ アカウント blob-service-properties の削除の保持ポリシーの管理をサポートするために、新しいパラメーター `--enable-delete-retention` と `--delete-retention-days` を追加します。</span><span class="sxs-lookup"><span data-stu-id="61bea-140">Add new parameters `--enable-delete-retention` and `--delete-retention-days` to support managing delete retention policy for storage account blob-service-properties.</span></span>

## <a name="december-17-2019"></a><span data-ttu-id="61bea-141">2019 年 12 月 17 日</span><span class="sxs-lookup"><span data-stu-id="61bea-141">December 17, 2019</span></span>

<span data-ttu-id="61bea-142">2.0.78</span><span class="sxs-lookup"><span data-stu-id="61bea-142">2.0.78</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-143">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-143">ACR</span></span>

* <span data-ttu-id="61bea-144">acr task run でのローカル コンテキストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-144">Added support Local context in acr task run</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-145">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-145">ACS</span></span>

* <span data-ttu-id="61bea-146">[重大な変更] az openshift create: `--workspace-resource-id` の名前を `--workspace-id` に変更します。</span><span class="sxs-lookup"><span data-stu-id="61bea-146">[BREAKING CHANGE]az openshift create: rename `--workspace-resource-id` to `--workspace-id`.</span></span>

### <a name="ams"></a><span data-ttu-id="61bea-147">AMS</span><span class="sxs-lookup"><span data-stu-id="61bea-147">AMS</span></span>

* <span data-ttu-id="61bea-148">リソースが見つからない場合に 3 を返すように表示コマンドを更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-148">Updated show commands to return 3 when resource not found</span></span>

### <a name="appconfig"></a><span data-ttu-id="61bea-149">AppConfig</span><span class="sxs-lookup"><span data-stu-id="61bea-149">AppConfig</span></span>

* <span data-ttu-id="61bea-150">要求 URL に api-version を追加するときのバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-150">Fixed bug when appending api-version to request url.</span></span> <span data-ttu-id="61bea-151">既存のソリューションは、改ページ位置の自動修正で機能しません。</span><span class="sxs-lookup"><span data-stu-id="61bea-151">The existing solution doesn't work with pagination.</span></span>
* <span data-ttu-id="61bea-152">英語以外の言語を表示するためのサポートを追加しました。これは、Microsoft のバックエンド サービスがグローバリゼーション向けに unicode をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="61bea-152">Added support for showing languages besides English as our backend service support unicode for globalization.</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-153">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-153">AppService</span></span>

* <span data-ttu-id="61bea-154">問題 #11217 を修正: webapp: az webapp config ssl upload はスロット パラメーターをサポートする必要がある</span><span class="sxs-lookup"><span data-stu-id="61bea-154">Fixed issue #11217: webapp: az webapp config ssl upload should support slot parameter</span></span>
* <span data-ttu-id="61bea-155">問題 #10965 を修正:エラー:名前を空にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="61bea-155">Fixed issue #10965: Error: Name cannot be empty.</span></span> <span data-ttu-id="61bea-156">ip_address とサブネットによる削除を許可します</span><span class="sxs-lookup"><span data-stu-id="61bea-156">Allow remove by ip_address and subnet</span></span>
* <span data-ttu-id="61bea-157">Key Vault `az webapp config ssl import` からの証明書のインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-157">Added support for importing certificates from Key Vault `az webapp config ssl import`</span></span>

### <a name="arm"></a><span data-ttu-id="61bea-158">ARM</span><span class="sxs-lookup"><span data-stu-id="61bea-158">ARM</span></span>

* <span data-ttu-id="61bea-159">6\.0.0 を使用するように azure-mgmt-resource パッケージを更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-159">Updated azure-mgmt-resource package to use 6.0.0</span></span>
* <span data-ttu-id="61bea-160">新しいパラメーター `--aux-subs` の追加による `az group deployment create` コマンドのクロス テナントのサポート</span><span class="sxs-lookup"><span data-stu-id="61bea-160">Cross Tenant Support for `az group deployment create` command by adding new parameter `--aux-subs`</span></span>
* <span data-ttu-id="61bea-161">ポリシー セット定義へのメタデータ情報の追加をサポートするために、新しいパラメーター `--metadata` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-161">Added new parameter `--metadata` to support adding metadata information for policy set definitions.</span></span>

### <a name="backup"></a><span data-ttu-id="61bea-162">バックアップ</span><span class="sxs-lookup"><span data-stu-id="61bea-162">Backup</span></span>

* <span data-ttu-id="61bea-163">SQL および SAP Hana ワークロードのバックアップ サポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-163">Added Backup support for SQL and SAP Hana workload.</span></span>

### <a name="botservice"></a><span data-ttu-id="61bea-164">BotService</span><span class="sxs-lookup"><span data-stu-id="61bea-164">BotService</span></span>

* <span data-ttu-id="61bea-165">[重大な変更] プレビューコマンド 'az bot create' から '--version' フラグを削除します。</span><span class="sxs-lookup"><span data-stu-id="61bea-165">[Breaking change] Remove '--version' flag from preview command 'az bot create'.</span></span> <span data-ttu-id="61bea-166">v4 SDK ボットのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="61bea-166">Only v4 SDK bots are supported.</span></span>
* <span data-ttu-id="61bea-167">名前を使用できるかどうかのチェックを 'sz bot create' に追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-167">Added name availability check for 'az bot create'.</span></span>
* <span data-ttu-id="61bea-168">'az bot update' を使用してボットのアイコン URL を更新するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-168">Added support for updating the icon URL for a bot via 'az bot update'.</span></span>
* <span data-ttu-id="61bea-169">'az bot directline update' を使用して Direct Line チャネルを更新するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-169">Added support for updating a Direct Line channel via 'az bot directline update'.</span></span>
* <span data-ttu-id="61bea-170">'az bot directline create' に '--enable-enhanced-auth' フラグのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-170">Added '--enable-enhanced-auth' flag support to 'az bot directline create'.</span></span>
* <span data-ttu-id="61bea-171">コマンド グループ 'az bot authsetting' は、プレビュー段階ではなく、GA です。</span><span class="sxs-lookup"><span data-stu-id="61bea-171">The following command groups are GA and not in preview: 'az bot authsetting'.</span></span>
* <span data-ttu-id="61bea-172">'az bot' の次のコマンドは、プレビュー段階ではなく、GA です: 'create'、'prepare-deploy'、'show'、'delete'、'update'。</span><span class="sxs-lookup"><span data-stu-id="61bea-172">The following commands in 'az bot' are GA and not in preview: 'create', 'prepare-deploy', 'show', 'delete', 'update'.</span></span>
* <span data-ttu-id="61bea-173">'az bot prepare-deploy' が修正され、 '--proj-file-path' 値が小文字に変更されます (例: "Test.csproj" の場合、"test.csproj")。</span><span class="sxs-lookup"><span data-stu-id="61bea-173">Fixed 'az bot prepare-deploy' changing '--proj-file-path' value to lower case (e.g. "Test.csproj" to "test.csproj").</span></span>

### <a name="compute"></a><span data-ttu-id="61bea-174">Compute</span><span class="sxs-lookup"><span data-stu-id="61bea-174">Compute</span></span>

* <span data-ttu-id="61bea-175">vmss create/update:--scale-in-policy を追加しました。これは、VMSS がスケールインされるときに削除対象として選択される仮想マシンを決定します。</span><span class="sxs-lookup"><span data-stu-id="61bea-175">vmss create/update: Added --scale-in-policy, which decides which virtual machines are chosen for removal when a VMSS is scaled-in.</span></span>
* <span data-ttu-id="61bea-176">vm/vmss update:--priority を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-176">vm/vmss update: Added --priority.</span></span>
* <span data-ttu-id="61bea-177">vm/vmss update:--max-price を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-177">vm/vmss update: Added --max-price.</span></span>
* <span data-ttu-id="61bea-178">disk-encryption-set コマンド グループ (create、show、update、delete、list) を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-178">Added disk-encryption-set command group (create, show, update, delete, list).</span></span>
* <span data-ttu-id="61bea-179">disk create:--encryption-type と --disk-encryption-set を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-179">disk create: Added --encryption-type and --disk-encryption-set.</span></span>
* <span data-ttu-id="61bea-180">vm/vmss create: --os-disk-encryption-set と --data-disk-encryption-sets を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-180">vm/vmss create: Added --os-disk-encryption-set and --data-disk-encryption-sets.</span></span>

### <a name="core"></a><span data-ttu-id="61bea-181">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-181">Core</span></span>

* <span data-ttu-id="61bea-182">Python 3.4 のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-182">Removed support for Python 3.4</span></span>
* <span data-ttu-id="61bea-183">複数のコマンドでの HaTS 調査のプラグイン</span><span class="sxs-lookup"><span data-stu-id="61bea-183">Plug in HaTS survey in multiple commands</span></span>

### <a name="dls"></a><span data-ttu-id="61bea-184">DLS</span><span class="sxs-lookup"><span data-stu-id="61bea-184">DLS</span></span>

* <span data-ttu-id="61bea-185">ADLS SDK バージョンを更新しました (0.0.48)。</span><span class="sxs-lookup"><span data-stu-id="61bea-185">Updated ADLS sdk version (0.0.48).</span></span>

### <a name="install"></a><span data-ttu-id="61bea-186">インストール</span><span class="sxs-lookup"><span data-stu-id="61bea-186">Install</span></span>

* <span data-ttu-id="61bea-187">インストール スクリプトで python 3.8 がサポートされます</span><span class="sxs-lookup"><span data-stu-id="61bea-187">Install script support python 3.8</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-188">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-188">IOT</span></span>

* <span data-ttu-id="61bea-189">[重大な変更] manual-failover から --failover-region パラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-189">[BREAKING CHANGE] Removed --failover-region parameter from manual-failover.</span></span> <span data-ttu-id="61bea-190">これで、割り当てられた geo ペアのセカンダリ リージョンにフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="61bea-190">Now it will failover to assigned geo-paired secondary region.</span></span>

### <a name="key-vault"></a><span data-ttu-id="61bea-191">Key Vault</span><span class="sxs-lookup"><span data-stu-id="61bea-191">Key Vault</span></span>

* <span data-ttu-id="61bea-192">#8095 を修正: `az keyvault storage remove`: ヘルプ メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="61bea-192">Fixed #8095: `az keyvault storage remove`: improve the help message</span></span>
* <span data-ttu-id="61bea-193">#8921 を修正: `az keyvault key/secret/certificate list/list-deleted/list-versions`: パラメーター `--maxresults` の検証のバグを修正します</span><span class="sxs-lookup"><span data-stu-id="61bea-193">Fixed #8921: `az keyvault key/secret/certificate list/list-deleted/list-versions`: fix the validation bug on parameter `--maxresults`</span></span>
* <span data-ttu-id="61bea-194">#10512 を修正: `az keyvault set-policy`: `--object-id`、`--spn`、`--upn` のいずれも指定されていない場合のエラー メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="61bea-194">Fixed #10512: `az keyvault set-policy`: improve the error message when none of `--object-id`, `--spn` or `--upn` is specified</span></span>
* <span data-ttu-id="61bea-195">#10846 を修正: `az keyvault secret show-deleted`: `--id` を指定した場合、`--name/-n` は必要ありません</span><span class="sxs-lookup"><span data-stu-id="61bea-195">Fixed #10846: `az keyvault secret show-deleted`: when `--id` is specified, `--name/-n` is not required</span></span>
* <span data-ttu-id="61bea-196">#11084 を修正: `az keyvault secret download`: パラメーター `--encoding` のヘルプ メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="61bea-196">Fixed #11084: `az keyvault secret download`: improve the help message of parameter `--encoding`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-197">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-197">Network</span></span>

* <span data-ttu-id="61bea-198">az network application-gateway probe:作成および更新時にバックエンド サーバーをプローブするためのポートを指定する --port オプションのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-198">az network application-gateway probe: Added support --port option to specify a port for probing backend servers when create and update</span></span>
* <span data-ttu-id="61bea-199">az network application-gateway url-path-map create/update: `--waf-policy` のバグ修正</span><span class="sxs-lookup"><span data-stu-id="61bea-199">az network application-gateway url-path-map create/update: bug fix for `--waf-policy`</span></span>
* <span data-ttu-id="61bea-200">az network application-gateway:`--rewrite-rule-set` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-200">az network application-gateway: Added support `--rewrite-rule-set`</span></span>
* <span data-ttu-id="61bea-201">az network list-service-aliases:サービス エンドポイント ポリシーに使用できるサービス別名を一覧表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-201">az network list-service-aliases: Added support list service aliases which can be used for Service Endpoint Policies</span></span>
* <span data-ttu-id="61bea-202">az network dns zone import:レコード名での .@ のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-202">az network dns zone import: Added support .@ in record name</span></span>

### <a name="packaging"></a><span data-ttu-id="61bea-203">梱包</span><span class="sxs-lookup"><span data-stu-id="61bea-203">Packaging</span></span>

* <span data-ttu-id="61bea-204">pip インストール用のバック エッジ ビルドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-204">Added back edge builds for pip install</span></span>
* <span data-ttu-id="61bea-205">Ubuntu eoan パッケージを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-205">Added Ubuntu eoan package</span></span>

### <a name="policy"></a><span data-ttu-id="61bea-206">ポリシー</span><span class="sxs-lookup"><span data-stu-id="61bea-206">Policy</span></span>

* <span data-ttu-id="61bea-207">ポリシー API バージョン 2019-09-01 のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-207">Added support for Policy API version 2019-09-01.</span></span>
* <span data-ttu-id="61bea-208">az policy set-definition:`--definition-groups` パラメーターを使用したポリシー セット定義内のグループ化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-208">az policy set-definition: Added support grouping within policy set definitions with `--definition-groups` parameter</span></span>

### <a name="redis"></a><span data-ttu-id="61bea-209">Redis</span><span class="sxs-lookup"><span data-stu-id="61bea-209">Redis</span></span>

* <span data-ttu-id="61bea-210">`az redis create` コマンドにプレビュー パラメーター `--replicas-per-master` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-210">Added preview param `--replicas-per-master` to `az redis create` command</span></span>
* <span data-ttu-id="61bea-211">azure-mgmt-redis を 6.0.0 から 7.0.0rc1 に更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-211">Updated azure-mgmt-redis from 6.0.0 to 7.0.0rc1</span></span>

### <a name="servicefabric"></a><span data-ttu-id="61bea-212">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="61bea-212">ServiceFabric</span></span>

* <span data-ttu-id="61bea-213">#10963 を含む node-type 追加ロジックを修正:持続性レベル Gold で新しいノード タイプを追加すると、常に CLI エラーがスローされる</span><span class="sxs-lookup"><span data-stu-id="61bea-213">Fixed in node-type add logic including #10963: Adding new node type with durability level Gold will always throw CLI error</span></span>
* <span data-ttu-id="61bea-214">作成テンプレートの ServiceFabricNodeVmExt バージョンを 1.1 に更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-214">Updated ServiceFabricNodeVmExt version to 1.1 in creation template</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-215">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-215">SQL</span></span>

* <span data-ttu-id="61bea-216">読み取りスケール管理をサポートするために、sql db create および update コマンドに "--read-scale" と "--read-replicas" パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-216">Added "--read-scale" and "--read-replicas" parameters to sql db create and update commands, to support read scale management.</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-217">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-217">Storage</span></span>

* <span data-ttu-id="61bea-218">GA リリースでの storage account create および update コマンド用の大きいファイルの共有プロパティ</span><span class="sxs-lookup"><span data-stu-id="61bea-218">GA Release Large File Shares property for storage account create and update command</span></span>
* <span data-ttu-id="61bea-219">GA リリースでのユーザー委任 SAS トークンのサポート</span><span class="sxs-lookup"><span data-stu-id="61bea-219">GA Release User Delegation SAS token Support</span></span>
* <span data-ttu-id="61bea-220">ストレージ アカウントの Blob service のプロパティを管理するための新しいコマンド `az storage account blob-service-properties show` と `az storage account blob-service-properties update --enable-change-feed` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="61bea-220">Added new commands `az storage account blob-service-properties show` and `az storage account blob-service-properties update --enable-change-feed` to manage blob service properties for storage account.</span></span>
* <span data-ttu-id="61bea-221">[今後の破壊的変更] `az storage copy`: `*` 文字は URL 内のワイルドカードとしてサポートされなくなりましたが、新しいパラメーターの --include-pattern と --exclude-pattern が `*` ワイルドカードをサポートして追加されます。</span><span class="sxs-lookup"><span data-stu-id="61bea-221">[COMING BREAKING CHANGE] `az storage copy`: `*` character is no longer supported as a wildcard in URL, but new parameters --include-pattern and --exclude-pattern will be added with `*` wildcard support.</span></span>
* <span data-ttu-id="61bea-222">問題 #11043 を修正:`az storage remove` コマンドでコンテナー/共有全体を削除するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-222">Fixed issue #11043: Added support to remove whole container/share in `az storage remove` command</span></span>

## <a name="november-26-2019"></a><span data-ttu-id="61bea-223">2019 年 11 月 26 日</span><span class="sxs-lookup"><span data-stu-id="61bea-223">November 26, 2019</span></span>

<span data-ttu-id="61bea-224">バージョン 2.0.77</span><span class="sxs-lookup"><span data-stu-id="61bea-224">Version 2.0.77</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-225">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-225">ACR</span></span>

* <span data-ttu-id="61bea-226">acr task create/update からパラメーター `--branch` が非推奨になりました</span><span class="sxs-lookup"><span data-stu-id="61bea-226">Deprecated parameter `--branch` from acr task create/update</span></span>

### <a name="azure-red-hat-openshift"></a><span data-ttu-id="61bea-227">Azure Red Hat OpenShift</span><span class="sxs-lookup"><span data-stu-id="61bea-227">Azure Red Hat OpenShift</span></span>

* <span data-ttu-id="61bea-228">監視を使用して Azure Red Hat Openshift クラスターを作成できるように、`--workspace-resource-id` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-228">Added `--workspace-resource-id` flag to allow creation of Azure Red Hat Openshift cluster with monitoring</span></span>
* <span data-ttu-id="61bea-229">監視を使用して Azure Red Hat OpenShift クラスターを作成するために `monitor_profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-229">Added `monitor_profile` to create Azure Red Hat OpenShift cluster with monitoring</span></span>

### <a name="aks"></a><span data-ttu-id="61bea-230">AKS</span><span class="sxs-lookup"><span data-stu-id="61bea-230">AKS</span></span>

* <span data-ttu-id="61bea-231">"az aks rotate-certs" を使用したクラスター証明書ローテーション操作のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-231">Added support cluster certificate rotation operation using "az aks rotate-certs".</span></span>

### <a name="appconfig"></a><span data-ttu-id="61bea-232">AppConfig</span><span class="sxs-lookup"><span data-stu-id="61bea-232">AppConfig</span></span>

* <span data-ttu-id="61bea-233">`as az appconfig kv import` の区切り文字に ":" を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-233">Added support for using ":" for `as az appconfig kv import` separator</span></span>
* <span data-ttu-id="61bea-234">null ラベルを含む複数のラベルを持つキー値の一覧表示に関する問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-234">Fixed issue for listing key values with multiple labels including null label.</span></span> 
* <span data-ttu-id="61bea-235">管理プレーン SKD である azure-mgmt-appconfiguration を バージョン 0.3.0 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-235">Updated management plane sdk, azure-mgmt-appconfiguration, to version 0.3.0.</span></span> 

### <a name="appservice"></a><span data-ttu-id="61bea-236">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-236">AppService</span></span>

* <span data-ttu-id="61bea-237">問題 #11100 を修正:サービス プランの作成時の az webapp up の AttributeError</span><span class="sxs-lookup"><span data-stu-id="61bea-237">Fixed issue #11100: AttributeError for az webapp up when create service plan</span></span>
* <span data-ttu-id="61bea-238">az webapp up:サポートされている言語のサイトに作成またはデプロイを強制します。既定値は使用されません。</span><span class="sxs-lookup"><span data-stu-id="61bea-238">az webapp up: Forcing the creation or deployment to a site for supported languages, no defaults used.</span></span>
* <span data-ttu-id="61bea-239">App Service Environment のサポートを追加しました: az appservice ase show | list | list-addresses | list-plans | create | update | delete</span><span class="sxs-lookup"><span data-stu-id="61bea-239">Added support for App Service Environment: az appservice ase show | list | list-addresses | list-plans | create | update | delete</span></span>

### <a name="backup"></a><span data-ttu-id="61bea-240">バックアップ</span><span class="sxs-lookup"><span data-stu-id="61bea-240">Backup</span></span>

* <span data-ttu-id="61bea-241">az backup policy list-associated-items の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-241">Fixed issue in az backup policy list-associated-items.</span></span> <span data-ttu-id="61bea-242">省略可能な BackupManagementType パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-242">Added optional BackupManagementType parameter.</span></span>

### <a name="compute"></a><span data-ttu-id="61bea-243">Compute</span><span class="sxs-lookup"><span data-stu-id="61bea-243">Compute</span></span>

* <span data-ttu-id="61bea-244">コンピューティング、ディスク、スナップショットの API バージョンを 2019-07-01 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="61bea-244">Upgraded API version of compute, disks, snapshots to 2019-07-01</span></span>
* <span data-ttu-id="61bea-245">vmss create: --orchestration-mode の改善</span><span class="sxs-lookup"><span data-stu-id="61bea-245">vmss create: Improvement for --orchestration-mode</span></span>
* <span data-ttu-id="61bea-246">sig image-definition create: --os-state を追加して、このイメージの下に作成された仮想マシンを "一般化" するか、または "特殊化" するかを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-246">sig image-definition create: Added --os-state to allow specifying whether the virtual machines created under this image are 'Generalized' or 'Specialized'</span></span>
* <span data-ttu-id="61bea-247">sig image-definition create: --hyper-v-generation を追加して、ハイパーバイザーの生成を指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-247">sig image-definition create: Added --hyper-v-generation to allow specifying the hypervisor generation</span></span>
* <span data-ttu-id="61bea-248">sig image-version create: --os-snapshot と --data-snapshots のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-248">sig image-version create: Added support --os-snapshot and --data-snapshots</span></span>
* <span data-ttu-id="61bea-249">image create: --data-disk-caching を追加して、データ ディスクのキャッシュ設定を指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-249">image create: Added --data-disk-caching to allow specifying caching setting of data disks</span></span>
* <span data-ttu-id="61bea-250">Python Compute SDK を 10.0.0 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="61bea-250">Upgraded Python Compute SDK to 10.0.0</span></span>
* <span data-ttu-id="61bea-251">vm/vmss create: 'Priority' 列挙型プロパティに 'Spot' を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-251">vm/vmss create: Added 'Spot' to 'Priority' enum property</span></span>
* <span data-ttu-id="61bea-252">[重大な変更] Swagger と Powershell のコマンドレットとの一貫性を維持するために、VM と VMSS の両方で '--max-billing' パラメーターを '--max-price' に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-252">[Breaking change] Renamed '--max-billing' parameter to '--max-price', for both VM and VMSS, to be consistent with Swagger and Powershell cmdlets</span></span>
* <span data-ttu-id="61bea-253">vm monitor log show: リンクされた Log Analytics ワークスペースに対してログのクエリを実行するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-253">vm monitor log show: Added support for querying log over linked log analytics workspace.</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-254">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-254">IOT</span></span>

* <span data-ttu-id="61bea-255">#2531 の修正: ハブの更新に便利な引数を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-255">Fix #2531: Added convenience arguments for hub update.</span></span>
* <span data-ttu-id="61bea-256">#8323 の修正: ストレージ カスタム エンドポイントを作成するために不足しているパラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-256">Fix #8323: Added missing parameters to create storage custom endpoint.</span></span>
* <span data-ttu-id="61bea-257">回帰バグの修正: 既定のストレージ エンドポイントをオーバーライドする変更を元に戻しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-257">Fix regression bug: Reverted the changes which overrides the default storage endpoint.</span></span>

### <a name="key-vault"></a><span data-ttu-id="61bea-258">Key Vault</span><span class="sxs-lookup"><span data-stu-id="61bea-258">Key Vault</span></span>

* <span data-ttu-id="61bea-259">#11121 を修正しました: `az keyvault certificate list` を使用する場合、`--include-pending` を渡すときに `true` または `false` の値が必須ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="61bea-259">Fixed #11121: When using `az keyvault certificate list`, passing `--include-pending` now doesn't require a value of `true` or `false`</span></span>

### <a name="netappfiles"></a><span data-ttu-id="61bea-260">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="61bea-260">NetAppFiles</span></span>

* <span data-ttu-id="61bea-261">azure-mgmt-netapp を 0.7.0 にアップグレードしました。これには、今後のレプリケーション操作に関連した追加のボリューム プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="61bea-261">Upgraded azure-mgmt-netapp to 0.7.0 which includes some additional volume properties associated with upcoming replication operations</span></span>

### <a name="network"></a><span data-ttu-id="61bea-262">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-262">Network</span></span>

* <span data-ttu-id="61bea-263">application-gateway waf-config: 非推奨になりました</span><span class="sxs-lookup"><span data-stu-id="61bea-263">application-gateway waf-config: deprecated</span></span>
* <span data-ttu-id="61bea-264">application-gateway waf-policy: 管理されているルール セットと除外ルールを管理するために、サブグループ managed-rules を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-264">application-gateway waf-policy: Added subgroup managed-rules to manage managed rule sets and exclusion rules</span></span>
* <span data-ttu-id="61bea-265">application-gateway waf-policy: waf-policy のグローバル構成を管理するために、サブグループ policy-setting を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-265">application-gateway waf-policy: Added subgroup policy-setting to manage global configuration of a waf-policy</span></span>
* <span data-ttu-id="61bea-266">[重大な変更] application-gateway waf-policy: subgroup rule を custom-rule に名前変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-266">[BREAKING CHANGE] application-gateway waf-policy: Renamed subgroup rule to custom-rule</span></span>
* <span data-ttu-id="61bea-267">application-gateway http-listener: 作成時の --firewall-policy を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-267">application-gateway http-listener: Added --firewall-policy when create</span></span>
* <span data-ttu-id="61bea-268">application-gateway url-path-map rule: 作成時の --firewall-policy を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-268">application-gateway url-path-map rule: Added --firewall-policy when create</span></span>

### <a name="packaging"></a><span data-ttu-id="61bea-269">梱包</span><span class="sxs-lookup"><span data-stu-id="61bea-269">Packaging</span></span>

* <span data-ttu-id="61bea-270">az ラッパーを Python で書き直しました</span><span class="sxs-lookup"><span data-stu-id="61bea-270">Rewrote the az wrapper in Python</span></span>
* <span data-ttu-id="61bea-271">Python 3.8 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-271">Added support for Python 3.8</span></span>
* <span data-ttu-id="61bea-272">RPM パッケージで Python 3 に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-272">Changed to Python 3 for RPM package</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-273">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-273">Profile</span></span>

* <span data-ttu-id="61bea-274">Microsoft アカウントで `az login -u {} -p {}` を実行するときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-274">Polished error when running `az login -u {} -p {}` with Microsoft account</span></span>
* <span data-ttu-id="61bea-275">自己署名ルート証明書使用してプロキシの背後で `az login` を実行するときの `SSLError` を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-275">Polished `SSLError` when running `az login` behind a proxy with self-signed root certificate</span></span>
* <span data-ttu-id="61bea-276">#10578 を修正: Windows または WSL で同時に複数のインスタンスを起動すると `az login` がハングする</span><span class="sxs-lookup"><span data-stu-id="61bea-276">Fixed #10578: `az login` hangs when more than one instances are launched at the same time on Windows or WSL</span></span>
* <span data-ttu-id="61bea-277">#11059 を修正: テナントにサブスクリプションがあると `az login --allow-no-subscriptions` が失敗する</span><span class="sxs-lookup"><span data-stu-id="61bea-277">Fixed #11059: `az login --allow-no-subscriptions` fails if there are subscriptions in the tenant</span></span>
* <span data-ttu-id="61bea-278">#11238 を修正: サブスクリプションの名前を変更した後、MSI を使用してログインすると、同じサブスクリプションが 2 回表示される</span><span class="sxs-lookup"><span data-stu-id="61bea-278">Fixed #11238: After renaming a subscription, logging in with MSI will result in the same subscription appearing twice</span></span>

### <a name="rbac"></a><span data-ttu-id="61bea-279">RBAC</span><span class="sxs-lookup"><span data-stu-id="61bea-279">RBAC</span></span>

* <span data-ttu-id="61bea-280">#10996 を修正: `--password` が指定されていないときの `az ad user update` での `--force-change-password-next-login` のエラーを改善</span><span class="sxs-lookup"><span data-stu-id="61bea-280">Fixed #10996: Polish error for `--force-change-password-next-login` in `az ad user update` when `--password` is not specified</span></span>

### <a name="redis"></a><span data-ttu-id="61bea-281">Redis</span><span class="sxs-lookup"><span data-stu-id="61bea-281">Redis</span></span>

* <span data-ttu-id="61bea-282">#2902 を修正: Basic SKU キャッシュの更新中、メモリ構成を設定しない</span><span class="sxs-lookup"><span data-stu-id="61bea-282">Fixed #2902: Avoid setting memory configs while updating Basic SKU cache</span></span>

### <a name="reservations"></a><span data-ttu-id="61bea-283">Reservations</span><span class="sxs-lookup"><span data-stu-id="61bea-283">Reservations</span></span>

* <span data-ttu-id="61bea-284">SDK バージョンを 0.6.0 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="61bea-284">Upgraded SDK Version to 0.6.0</span></span>
* <span data-ttu-id="61bea-285">Gat-Gatalogs を呼び出した後の billingplan の詳細情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-285">Added billingplan details info after calling Get-Gatalogs</span></span>
* <span data-ttu-id="61bea-286">予約の価格を計算するための新しいコマンド `az reservations reservation-order calculate` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-286">Added new command `az reservations reservation-order calculate` to calculate the price for a reservation</span></span>
* <span data-ttu-id="61bea-287">新しい予約を購入するための新しいコマンド `az reservations reservation-order purchase` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-287">Added new command `az reservations reservation-order purchase` to purchase a new reservation</span></span>

### <a name="rest"></a><span data-ttu-id="61bea-288">REST</span><span class="sxs-lookup"><span data-stu-id="61bea-288">Rest</span></span>
* <span data-ttu-id="61bea-289">`az rest` を GA に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-289">Changed `az rest` to GA</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-290">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-290">SQL</span></span>

* <span data-ttu-id="61bea-291">azure-mgmt-sql をバージョン 0.15.0 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-291">Updated azure-mgmt-sql to version 0.15.0.</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-292">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-292">Storage</span></span>

* <span data-ttu-id="61bea-293">storage account create: Blob service でのファイルシステムのセマンティクスをサポートするために、--enable-hierarchical-namespace を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-293">storage account create: Added --enable-hierarchical-namespace to support filesystem semantics in blob service.</span></span>
* <span data-ttu-id="61bea-294">エラー メッセージから関連性のない例外を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-294">Removed unrelated exception from error message</span></span>
* <span data-ttu-id="61bea-295">"この操作を実行するのに必要なアクセス許可がありません" という誤ったエラー メッセージが</span><span class="sxs-lookup"><span data-stu-id="61bea-295">Fixed issues with incorrect error message "You do not have the required permissions needed to perform this operation."</span></span> <span data-ttu-id="61bea-296">ネットワーク ルールまたは AuthenticationFailed によってブロックされた場合に表示される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-296">when blocked by network rules or AuthenticationFailed.</span></span>

## <a name="november-4-2019"></a><span data-ttu-id="61bea-297">2019 年 11 月 4 日</span><span class="sxs-lookup"><span data-stu-id="61bea-297">November 4, 2019</span></span>

<span data-ttu-id="61bea-298">バージョン 2.0.76</span><span class="sxs-lookup"><span data-stu-id="61bea-298">Version 2.0.76</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-299">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-299">ACR</span></span>

* <span data-ttu-id="61bea-300">コマンド `az acr pack build` にプレビュー パラメーター `--pack-image-tag` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-300">Added a preview parameter `--pack-image-tag` to command `az acr pack build`.</span></span>
* <span data-ttu-id="61bea-301">レジストリ作成時の監査を有効にするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-301">Added support for enabling auditing on creating a registry</span></span>
* <span data-ttu-id="61bea-302">レジストリ スコープが設定された RBAC のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-302">Added support for Repository-scoped RBAC</span></span>

### <a name="aks"></a><span data-ttu-id="61bea-303">AKS</span><span class="sxs-lookup"><span data-stu-id="61bea-303">AKS</span></span>

* <span data-ttu-id="61bea-304">`az aks create` コマンドに `--enable-cluster-autoscaler`、`--min-count`、および `--max-count` を追加しました。これにより、ノード プールのクラスター オートスケーラーが有効になります。</span><span class="sxs-lookup"><span data-stu-id="61bea-304">Added `--enable-cluster-autoscaler`, `--min-count` and `--max-count` to the `az aks create` command, which enables cluster autoscaler for the node pool.</span></span>
* <span data-ttu-id="61bea-305">上記のフラグに加えて、`--update-cluster-autoscaler` および `--disable-cluster-autoscaler` を `az aks update` コマンドに追加し、クラスター オートスケーラーを更新できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="61bea-305">Added the above flags as well as `--update-cluster-autoscaler` and `--disable-cluster-autoscaler` to the `az aks update` command, allowing updates to cluster autoscaler.</span></span>

### <a name="appconfig"></a><span data-ttu-id="61bea-306">AppConfig</span><span class="sxs-lookup"><span data-stu-id="61bea-306">AppConfig</span></span>

* <span data-ttu-id="61bea-307">App Configuration に格納される機能フラグを管理するために、appconfig feature コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-307">Added appconfig feature command group to manage feature flags stored in an App Configuration.</span></span>
* <span data-ttu-id="61bea-308">ファイルに対する appconfig kv export コマンドの軽微なバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-308">Fixed minor bug for appconfig kv export to file command.</span></span> <span data-ttu-id="61bea-309">エクスポート中に宛先ファイルの内容を読み取らないようにしました。</span><span class="sxs-lookup"><span data-stu-id="61bea-309">Stop reading dest file contents during export.</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-310">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-310">AppService</span></span>

* <span data-ttu-id="61bea-311">`az appservice plan create`:appservice plan create に "persitescaling" を設定するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-311">`az appservice plan create`: Added support to set 'persitescaling' on appservice plan create.</span></span>
* <span data-ttu-id="61bea-312">webapp config ssl bind 操作がリソースから既存のタグを削除する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-312">Fixed an issue where webapp config ssl bind operation was removing existing tags from the resource</span></span>
* <span data-ttu-id="61bea-313">関数アプリのデプロイ時にリモート ビルド アクションをサポートするために、`az functionapp deployment source config-zip` に `--build-remote` フラグを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-313">Added `--build-remote` flag for `az functionapp deployment source config-zip` to support remote build action during function app deployment.</span></span>
* <span data-ttu-id="61bea-314">Windows 向けの関数アプリの既定のノードバージョンを 10 に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-314">Changed default node version on function apps to ~10 for Windows</span></span>
* <span data-ttu-id="61bea-315">`az functionapp create` に `--runtime-version` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-315">Added `--runtime-version` property to `az functionapp create`</span></span>

### <a name="arm"></a><span data-ttu-id="61bea-316">ARM</span><span class="sxs-lookup"><span data-stu-id="61bea-316">ARM</span></span>

* <span data-ttu-id="61bea-317">`az deployment/group deployment validate`:デプロイ時に、json テンプレートで複数行とコメントをサポートするために `--handle-extended-json-format` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-317">`az deployment/group deployment validate`: Added `--handle-extended-json-format` parameter to support multiline and comments in json template when deployment.</span></span>
* <span data-ttu-id="61bea-318">azure-mgmt-resource を 2019-07-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="61bea-318">Bumped azure-mgmt-resource to 2019-07-01</span></span>

### <a name="backup"></a><span data-ttu-id="61bea-319">バックアップ</span><span class="sxs-lookup"><span data-stu-id="61bea-319">Backup</span></span>

* <span data-ttu-id="61bea-320">AzureFiles のバックアップ サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-320">Added AzureFiles backup support</span></span>

### <a name="compute"></a><span data-ttu-id="61bea-321">Compute</span><span class="sxs-lookup"><span data-stu-id="61bea-321">Compute</span></span>

* <span data-ttu-id="61bea-322">`az vm create`:高速ネットワークと既存の NIC を一緒に指定した場合の警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-322">`az vm create`: Added warning when specifying accelerated networking and an existing NIC together.</span></span>
* <span data-ttu-id="61bea-323">`az vm create`:仮想マシンを割り当てる必要がある既存の仮想マシン スケール セットを指定するための `--vmss` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-323">`az vm create`: Added `--vmss` to specify an existing virtual machine scale set that the virtual machine should be assigned to.</span></span>
* <span data-ttu-id="61bea-324">`az vm/vmss create`:イメージ エイリアス ファイルのローカル コピーを追加し、制限付きネットワーク環境でそれにアクセスできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="61bea-324">`az vm/vmss create`: Added a local copy of image alias file so that it can be accessed in a restricted network environment.</span></span>
* <span data-ttu-id="61bea-325">`az vmss create`:スケール セットによる仮想マシンの管理方法を指定するための `--orchestration-mode` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-325">`az vmss create`: Added `--orchestration-mode` to specify how virtual machines are managed by the scale set.</span></span>
* <span data-ttu-id="61bea-326">`az vm/vmss update`:Ultra SSD 設定を更新できるように `--ultra-ssd-enabled` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-326">`az vm/vmss update`: Added `--ultra-ssd-enabled` to allow updating ultra SSD setting.</span></span>
* <span data-ttu-id="61bea-327">[破壊的変更] `az vm extension set`:ユーザーが `--ids` を使用して、VM に拡張機能を設定できないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-327">[BREAKING CHANGE] `az vm extension set`: Fixed bug where users could not set an extension on a VM with `--ids`.</span></span>
* <span data-ttu-id="61bea-328">Azure Marketplace イメージの使用条件を管理するための新しいコマンド `az vm image terms accept/cancel/show` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-328">Added new commands `az vm image terms accept/cancel/show` to manage Azure Marketplace image terms.</span></span>
* <span data-ttu-id="61bea-329">VMAccessForLinux をバージョン 1.5 に更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-329">Updated VMAccessForLinux to version 1.5</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-330">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-330">CosmosDB</span></span>

* <span data-ttu-id="61bea-331">[破壊的変更] `az sql container create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-331">[BREAKING CHANGE] `az sql container create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="61bea-332">[破壊的変更] `az gremlin graph create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-332">[BREAKING CHANGE] `az gremlin graph create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="61bea-333">`az sql container create`:`--unique-key-policy` および `--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-333">`az sql container create`: Added `--unique-key-policy` and `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="61bea-334">`az sql container create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-334">`az sql container create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="61bea-335">`gremlin graph create`:`--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-335">`gremlin graph create`: Added `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="61bea-336">`gremlin graph create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-336">`gremlin graph create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="61bea-337">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-337">Fixed typo in help message</span></span>
* <span data-ttu-id="61bea-338">データベース:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-338">database: Added deprecation infomation</span></span>
* <span data-ttu-id="61bea-339">コレクション:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-339">collection: Added deprecation infomation</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-340">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-340">IoT</span></span>

* <span data-ttu-id="61bea-341">新しいルーティング ソースの種類を追加しました: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="61bea-341">Added new routing source type: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="61bea-342">`az iot hub create` の不十分な機能を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-342">Fixed missing features in `az iot hub create`</span></span>

### <a name="key-vault"></a><span data-ttu-id="61bea-343">Key Vault</span><span class="sxs-lookup"><span data-stu-id="61bea-343">Key Vault</span></span>

* <span data-ttu-id="61bea-344">証明書ファイルが存在しない場合の予期しないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-344">Fixed an unexpected error when certificate file does not exist</span></span>
* <span data-ttu-id="61bea-345">`az keyvault recover/purge` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-345">Fixed `az keyvault recover/purge` not working</span></span>

### <a name="netappfiles"></a><span data-ttu-id="61bea-346">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="61bea-346">NetAppFiles</span></span>

* <span data-ttu-id="61bea-347">API バージョン 2019-07-01 を使用するために azure-mgmt-netapp を 0.6.0 にアップグレードしました。</span><span class="sxs-lookup"><span data-stu-id="61bea-347">Upgraded azure-mgmt-netapp to 0.6.0 to use API version 2019-07-01.</span></span> <span data-ttu-id="61bea-348">この新しい API バージョンには以下の変更内容が含まれます。</span><span class="sxs-lookup"><span data-stu-id="61bea-348">This new API version includes:</span></span>

    - <span data-ttu-id="61bea-349">ボリューム作成の `--protocol-types` が "NFSv4" ではなく "NFSv 4.1" を受け入れるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-349">Volume creation `--protocol-types` accepts now "NFSv4.1" not "NFSv4"</span></span>
    - <span data-ttu-id="61bea-350">ボリューム エクスポート ポリシー プロパティの名前が "nfsv4" ではなく "nfsv41" に変更されました</span><span class="sxs-lookup"><span data-stu-id="61bea-350">Volume export policy property now named 'nfsv41' not 'nfsv4'</span></span>
    - <span data-ttu-id="61bea-351">ボリュームの `--creation-token` の名前が `--file-path` に変更されました</span><span class="sxs-lookup"><span data-stu-id="61bea-351">Volume `--creation-token` renamed to `--file-path`</span></span>
    - <span data-ttu-id="61bea-352">スナップショット作成日の名前が単に "created" に変更されました</span><span class="sxs-lookup"><span data-stu-id="61bea-352">Snapshot creation date now named just 'created'</span></span>

### <a name="network"></a><span data-ttu-id="61bea-353">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-353">Network</span></span>

* <span data-ttu-id="61bea-354">`az network private-dns link vnet create/update`:テナント間の仮想ネットワーク リンクがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="61bea-354">`az network private-dns link vnet create/update`: Support cross-tenant virtual network linking.</span></span>
* <span data-ttu-id="61bea-355">[破壊的変更] `az network vnet subnet list`:`--resource-group` と `--vnet-name` を必須に変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-355">[BREAKING CHANGE] `az network vnet subnet list`: Changed `--resource-group` and `--vnet-name` to be required now.</span></span>
* <span data-ttu-id="61bea-356">`az network public-ip prefix create`:作成時に IP アドレスのバージョン (IPv4、IPv6) を指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-356">`az network public-ip prefix create`: Added support to specify IP address version (IPv4, IPv6) when creation</span></span>
* <span data-ttu-id="61bea-357">azure-mgmt-network を 7.0.0 に、api-version を 2019-09-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="61bea-357">Bumped azure-mgmt-network to 7.0.0 and api-version to 2019-09-01</span></span>
* <span data-ttu-id="61bea-358">`az network vrouter`:新しいサービスの仮想ルーターと仮想ルーター ピアリングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-358">`az network vrouter`: Added support for new service virtual router and virtual router peering</span></span>
* <span data-ttu-id="61bea-359">`az network express-route gateway connection`:`--internet-security` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-359">`az network express-route gateway connection`: Added support for `--internet-security`</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-360">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-360">Profile</span></span>

* <span data-ttu-id="61bea-361">`az account get-access-token --resource-type ms-graph` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-361">Fixed `az account get-access-token --resource-type ms-graph` not working</span></span>
* <span data-ttu-id="61bea-362">`az login` からの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-362">Removed warning from `az login`</span></span>

### <a name="rbac"></a><span data-ttu-id="61bea-363">RBAC</span><span class="sxs-lookup"><span data-stu-id="61bea-363">RBAC</span></span>

* <span data-ttu-id="61bea-364">`az ad app update --id {} --display-name {}` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-364">Fixed `az ad app update --id {} --display-name {}` doesn't work</span></span>

### <a name="servicefabric"></a><span data-ttu-id="61bea-365">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="61bea-365">ServiceFabric</span></span>

* <span data-ttu-id="61bea-366">`az sf cluster create`:Service Fabric の Linux と Windows の template.json コンピューティング vmss を標準からマネージド ディスクに変更することによって問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-366">`az sf cluster create`: Fixed an issue by modifying service fabric linux and windows template.json compute vmss from standard to managed disks</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-367">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-367">SQL</span></span>

* <span data-ttu-id="61bea-368">新しい SQL Database オファリングであるサーバーレス コンピューティング モデルの CRUD 操作をサポートするために、`--compute-model`、`--auto-pause-delay`、および `--min-capacity` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-368">Added `--compute-model`, `--auto-pause-delay`, and `--min-capacity` parameters to support CRUD operations for new SQL Database offering: Serverless compute model.</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-369">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-369">Storage</span></span>

* <span data-ttu-id="61bea-370">`az storage account create/update`:Azure Files Active Directory Domain Services 認証をサポートするために、--enable-files-adds パラメーターと Azure Active Directory プロパティ引数グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-370">`az storage account create/update`: Added --enable-files-adds parameter and Azure Active Directory Properties Argument group to support Azure Files Active Directory Domain Service Authentication</span></span>
* <span data-ttu-id="61bea-371">ストレージ アカウントの Kerberos キーの一覧表示または再生成をサポートするために、`az storage account keys list/renew` を拡張しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-371">Expanded `az storage account keys list/renew` to support listing or regenerating Kerberos keys of storage account.</span></span>

## <a name="october-15-2019"></a><span data-ttu-id="61bea-372">2019 年 10 月 15 日</span><span class="sxs-lookup"><span data-stu-id="61bea-372">October 15, 2019</span></span>

<span data-ttu-id="61bea-373">バージョン 2.0.75</span><span class="sxs-lookup"><span data-stu-id="61bea-373">Version 2.0.75</span></span>

### <a name="aks"></a><span data-ttu-id="61bea-374">AKS</span><span class="sxs-lookup"><span data-stu-id="61bea-374">AKS</span></span>

* <span data-ttu-id="61bea-375">Kubernetes のバージョンでサポートされている場合、`--load-balancer-sku` の既定値を `standard` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-375">Changed `--load-balancer-sku` default value to `standard` if supported by the kubernetes version</span></span>
* <span data-ttu-id="61bea-376">Kubernetes のバージョンでサポートされている場合、`--vm-set-type` の既定値を `virtualmachinescalesets` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-376">Changed `--vm-set-type` default value to `virtualmachinescalesets` if supported by the kubernetes version</span></span>

### <a name="ams"></a><span data-ttu-id="61bea-377">AMS</span><span class="sxs-lookup"><span data-stu-id="61bea-377">AMS</span></span>

* <span data-ttu-id="61bea-378">[重大な変更]`job start` の名前を `job create` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-378">[BREAKING CHANGE] Changed the name of `job start` to `job create`</span></span>
* <span data-ttu-id="61bea-379">[重大な変更]`content-key-policy create` の `--ask` パラメーターが UTF8 ではなく 32 文字の 16 進文字列を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-379">[BREAKING CHANGE] Changed the `--ask` parameter of `content-key-policy create` to use a 32-character hex string instead of UTF8</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-380">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-380">AppService</span></span>

* <span data-ttu-id="61bea-381">コマンド `webapp config access-restriction show|set|add|remove` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-381">Added commands `webapp config access-restriction show|set|add|remove`</span></span>
* <span data-ttu-id="61bea-382">より優れたエラー処理を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-382">Added better error handling to `webapp up`</span></span>
* <span data-ttu-id="61bea-383">`Isolated` SKU のサポートを `appservice plan update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-383">Added support for `Isolated` SKU to `appservice plan update`</span></span>

### <a name="arm"></a><span data-ttu-id="61bea-384">ARM</span><span class="sxs-lookup"><span data-stu-id="61bea-384">ARM</span></span>

* <span data-ttu-id="61bea-385">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `deployment create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-385">Added `--handle-extended-json-format` parameter `deployment create` to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="61bea-386">Compute</span><span class="sxs-lookup"><span data-stu-id="61bea-386">Compute</span></span>

* <span data-ttu-id="61bea-387">`--enable-agent` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-387">Added `--enable-agent` parameter to `vm create`</span></span>
* <span data-ttu-id="61bea-388">ゾーンを使用するときに標準のパブリック IP SKU を自動的に使用するように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-388">Changed `vm create` to use standard public IP SKU automatically when using zones</span></span>
* <span data-ttu-id="61bea-389">VM の有効なコンピューター名が指定されていない場合に自動的に作成されるように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-389">Changed `vm create` to automatically create a valid computer name for a VM if none is provided</span></span>
* <span data-ttu-id="61bea-390">VMSS 内の仮想マシンのカスタム コンピューター名プレフィックスをサポートするために `--computer-name-prefix` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-390">Added `--computer-name-prefix` parameter to `vmss create` to support custom computer name prefix of virtual machines in the VMSS</span></span>
* <span data-ttu-id="61bea-391">ログ分析ワークスペースを自動的に有効にする `--workspace` パラメーターを `vm create` に追加します</span><span class="sxs-lookup"><span data-stu-id="61bea-391">Add `--workspace` parameter to `vm create` to enable log analytics workspace automatically</span></span>
* <span data-ttu-id="61bea-392">ギャラリーの API バージョンが 2019-07-01 に更新されました</span><span class="sxs-lookup"><span data-stu-id="61bea-392">Updated galleries API version to 2019-07-01</span></span>

### <a name="core"></a><span data-ttu-id="61bea-393">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-393">Core</span></span>

* <span data-ttu-id="61bea-394">汎用の update コマンドで `--set` パラメーターの構文チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-394">Added syntax check for `--set` parameter in generic update command</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-395">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-395">IoT</span></span>

* <span data-ttu-id="61bea-396">`iot hub show` で "リソースが見つかりません" のエラーが誤って発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-396">Fixed an issue where `iot hub show` would incorrectly error with "resource not found"</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-397">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-397">Monitor</span></span>

* <span data-ttu-id="61bea-398">CRUD のサポートを `monitor log-analytics workspace` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-398">Added support for CRUD to `monitor log-analytics workspace`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-399">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-399">Network</span></span>

* <span data-ttu-id="61bea-400">クロステナントの仮想リンクのサポートを `network private-dns link vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-400">Added support for cross-tenant virtual linking to `network private-dns link vnet [create|update]`</span></span>
* <span data-ttu-id="61bea-401">[重大な変更]`network vnet subnet list` で `--resource-group` および `--vnet-name` パラメーターが必須に変更になりました</span><span class="sxs-lookup"><span data-stu-id="61bea-401">[BREAKING CHANGE] Changed `network vnet subnet list` to require `--resource-group` and `--vnet-name` parameters</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-402">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-402">SQL</span></span>

* <span data-ttu-id="61bea-403">マネージ インスタンスの AAD 管理者の設定をサポートするコマンドを `sql mi ad-admin` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-403">Added commands to `sql mi ad-admin` that support setting an AAD administrator on managed instances</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-404">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-404">Storage</span></span>

* <span data-ttu-id="61bea-405">サービス間のコピー中にアクセス層を保持する `--preserve-s2s-access-tier` パラメーターを `storage copy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-405">Added `--preserve-s2s-access-tier` parameter `storage copy` to preserve access tier during service to service copy</span></span>
* <span data-ttu-id="61bea-406">ストレージ アカウントで大容量ファイルの共有をサポートするために `--enable-large-file-share` パラメーターを `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-406">Added `--enable-large-file-share` parameter to `storage account [create|update]` to support large file shares for storage account</span></span>

## <a name="september-24-2019"></a><span data-ttu-id="61bea-407">2019 年 9 月 24 日</span><span class="sxs-lookup"><span data-stu-id="61bea-407">September 24, 2019</span></span>

<span data-ttu-id="61bea-408">バージョン 2.0.74</span><span class="sxs-lookup"><span data-stu-id="61bea-408">Version 2.0.74</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-409">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-409">ACR</span></span>

* <span data-ttu-id="61bea-410">必須の `--type` パラメーターを `acr config retention update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-410">Added a required `--type` parameter to `acr config retention update`</span></span>
* <span data-ttu-id="61bea-411">[破壊的変更] `acr config` コマンド グループでパラメーター `--name -n` の名前が `--registry -r ` に変更されました</span><span class="sxs-lookup"><span data-stu-id="61bea-411">[BREAKING CHNAGE] Renamed parameter `--name -n` changed to `--registry -r ` for `acr config` command group</span></span>

### <a name="aks"></a><span data-ttu-id="61bea-412">AKS</span><span class="sxs-lookup"><span data-stu-id="61bea-412">AKS</span></span>

* <span data-ttu-id="61bea-413">`--load-balancer-sku` パラメーターを `aks create` コマンドに追加しました。これにより、SLB を使用する AKS クラスターを作成できます</span><span class="sxs-lookup"><span data-stu-id="61bea-413">Added `--load-balancer-sku` parameter to `aks create` command, which allows for creating AKS cluster with SLB</span></span>
* <span data-ttu-id="61bea-414">`--load-balancer-managed-outbound-ip-count`、`--load-balancer-outbound-ips`、`--load-balancer-outbound-ip-prefixes` パラメーターを `aks [create|update]` コマンドに追加しました。これにより、SLB を使用する AKS クラスターのロード バランサー プロファイルを更新できます</span><span class="sxs-lookup"><span data-stu-id="61bea-414">Added `--load-balancer-managed-outbound-ip-count`, `--load-balancer-outbound-ips` and `--load-balancer-outbound-ip-prefixes` parameters to `aks [create|update]` commands, which allow for updating load balancer profile of an AKS cluster with SLB</span></span>
* <span data-ttu-id="61bea-415">`--vm-set-type` パラメーターを `aks create` コマンドに追加しました。これにより、AKS クラスターの VM の種類 (vmas または vmss) を指定できます</span><span class="sxs-lookup"><span data-stu-id="61bea-415">Added `--vm-set-type` parameter to `aks create` command, which allows to specify vm types of an AKS Cluster (vmas or vmss)</span></span>

### <a name="arm"></a><span data-ttu-id="61bea-416">ARM</span><span class="sxs-lookup"><span data-stu-id="61bea-416">ARM</span></span>

* <span data-ttu-id="61bea-417">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `group deployment create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-417">Added `--handle-extended-json-format` parameter to `group deployment create` command to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="61bea-418">Compute</span><span class="sxs-lookup"><span data-stu-id="61bea-418">Compute</span></span>

* <span data-ttu-id="61bea-419">終了のスケジュール化されたイベントを構成しやすくするために `--terminate-notification-time` パラメーターを `vmss [create|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-419">Added `--terminate-notification-time` parameter to `vmss [create|update]` commands to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="61bea-420">終了のスケジュール化されたイベントを構成しやすくするために `--enable-terminate-notification` パラメーターを `vmss update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-420">Added `--enable-terminate-notification` parameter to `vmss update` command to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="61bea-421">`--priority,` `--eviction-policy,` `--max-billing` パラメーターを `[vm|vmss] create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-421">Added `--priority,` `--eviction-policy,` `--max-billing` parameters to `[vm|vmss] create` commands</span></span>
* <span data-ttu-id="61bea-422">`disk create` を変更し、ディスク アップロードの正確なサイズを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-422">Changed `disk create` to allow specifying the exact size of the disk upload</span></span>
* <span data-ttu-id="61bea-423">マネージド ディスクの増分スナップショットのサポートを `snapshot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-423">Added support for incremental snapshots for managed disks to `snapshot create`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="61bea-424">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-424">Cosmos DB</span></span>

* <span data-ttu-id="61bea-425">キー、読み取り専用キー、または接続文字列を表示する `--type <key-type>` パラメーターを `cosmosdb keys list` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-425">Added `--type <key-type>` parameter to `cosmosdb keys list` command to show key, read only keys or connection strings</span></span>
* <span data-ttu-id="61bea-426">`cosmosdb keys regenerate` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-426">Added `cosmosdb keys regenerate` command</span></span>
* <span data-ttu-id="61bea-427">[非推奨]`cosmosdb list-connection-strings`、`cosmosdb regenerate-key`、`cosmosdb list-read-only-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-427">[DEPRECATED] Deprecated `cosmosdb list-connection-strings`, `cosmosdb regenerate-key` and `cosmosdb list-read-only-keys` commands</span></span>

### <a name="eventgrid"></a><span data-ttu-id="61bea-428">EventGrid</span><span class="sxs-lookup"><span data-stu-id="61bea-428">EventGrid</span></span>

* <span data-ttu-id="61bea-429">正しいパラメーターを参照するようにエンドポイントのヘルプ テキストを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-429">Fixed the endpoint help text to refer to the right parameter</span></span>

### <a name="key-vault"></a><span data-ttu-id="61bea-430">Key Vault</span><span class="sxs-lookup"><span data-stu-id="61bea-430">Key Vault</span></span>

* <span data-ttu-id="61bea-431">テナントを使用してログインすると (`login -t`)、`keyvault create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-431">Fixed issue where logging in with a tenant (`login -t`) could cause `keyvault create` to fail</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-432">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-432">Monitor</span></span>

* <span data-ttu-id="61bea-433">`monitor metrics alert create` の `--condition` 引数で `:` 文字を使用できないという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-433">Fixed issue where `:` character was not allowed in `--condition` argument to `monitor metrics alert create`</span></span>

### <a name="policy"></a><span data-ttu-id="61bea-434">ポリシー</span><span class="sxs-lookup"><span data-stu-id="61bea-434">Policy</span></span>

* <span data-ttu-id="61bea-435">Policy API バージョン 2019-06-01 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-435">Added support for Policy API version 2019-06-01</span></span>
* <span data-ttu-id="61bea-436">`policy assignment create` コマンドに `--enforcement-mode` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-436">Added `--enforcement-mode` parameter to `policy assignment create` command</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-437">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-437">Storage</span></span>

* <span data-ttu-id="61bea-438">`az storage copy` コマンドに `--blob-type` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-438">Added `--blob-type` parameter to `az storage copy` command</span></span>

## <a name="september-10-2019"></a><span data-ttu-id="61bea-439">2019 年 9 月 10 日</span><span class="sxs-lookup"><span data-stu-id="61bea-439">September 10, 2019</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-440">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-440">ACR</span></span>

* <span data-ttu-id="61bea-441">アイテム保持ポリシーを構成するためのコマンド グループ `acr config retention` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-441">Added command group `acr config retention` to configure retention policy</span></span>

### <a name="aks"></a><span data-ttu-id="61bea-442">AKS</span><span class="sxs-lookup"><span data-stu-id="61bea-442">AKS</span></span>

* <span data-ttu-id="61bea-443">次のコマンドを使用した ACR 統合のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="61bea-443">Added support for ACR integration with the following commands:</span></span>
  * <span data-ttu-id="61bea-444">AKS クラスターに ACR をアタッチするための `--attach-acr` パラメーターを `aks [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-444">Added `--attach-acr` parameter to `aks [create|update]` to attach an ACR to an AKS cluster</span></span>
  * <span data-ttu-id="61bea-445">AKS クラスターから ACR をデタッチするための `--detach-acr` パラメーターを `aks update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-445">Added `--detach-acr` parameter to `aks update` to detach the ACR from an AKS cluster</span></span>

### <a name="arm"></a><span data-ttu-id="61bea-446">ARM</span><span class="sxs-lookup"><span data-stu-id="61bea-446">ARM</span></span>

* <span data-ttu-id="61bea-447">API バージョン 2019-05-10 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-447">Updated to use API version 2019-05-10</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-448">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-448">Batch</span></span>

* <span data-ttu-id="61bea-449">`batch pool create` の `--json-file` に新しい JSON 構成設定を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-449">Added new JSON configuration settings to `--json-file` for `batch pool create`:</span></span>
  * <span data-ttu-id="61bea-450">ファイル システム マウント用の `MountConfigurations` を追加しました (詳細については https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="61bea-450">Added `MountConfigurations` for file system mounts (see https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body for details)</span></span>
  * <span data-ttu-id="61bea-451">プール上のパブリック IP 用に、`NetworkConfiguration` にオプションのプロパティ `publicIPs` を追加しました (詳細については https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="61bea-451">Added optional property `publicIPs` on `NetworkConfiguration` for public IPs on pools (see https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body for details)</span></span>
* <span data-ttu-id="61bea-452">共有イメージ ギャラリーのサポートを `--image` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-452">Added support for shared image galleries to `--image`</span></span>
* <span data-ttu-id="61bea-453">[重大な変更]`batch pool create` の `--start-task-wait-for-success` の既定値を `true` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-453">[BREAKING CHANGE] Changed default value of `--start-task-wait-for-success` on `batch pool create` to be `true`</span></span>
* <span data-ttu-id="61bea-454">[重大な変更]`AutoUserSpecification` の `Scope` の既定値が常に Pool になるように変更しました (以前は Windows ノードでは `Task`、Linux ノードでは `Pool` でした)</span><span class="sxs-lookup"><span data-stu-id="61bea-454">[BREAKING CHANGE] Changed default value for `Scope` on `AutoUserSpecification` to always be Pool (was `Task` on Windows nodes, `Pool` on Linux nodes)</span></span>
  * <span data-ttu-id="61bea-455">この引数は、`--json-file` を使用して JSON 構成からのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="61bea-455">This argument can only be set from a JSON configuration with `--json-file`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="61bea-456">HDInsight</span><span class="sxs-lookup"><span data-stu-id="61bea-456">HDInsight</span></span>

* <span data-ttu-id="61bea-457">GA リリース</span><span class="sxs-lookup"><span data-stu-id="61bea-457">GA release</span></span>
* <span data-ttu-id="61bea-458">[重大な変更]`az hdinsight resize` のパラメーター `--workernode-count/-c` が必須に変更されました。</span><span class="sxs-lookup"><span data-stu-id="61bea-458">[BREAKING CHANGE] Changed parameter `--workernode-count/-c` of `az hdinsight resize` to be required.</span></span>

### <a name="key-vault"></a><span data-ttu-id="61bea-459">Key Vault</span><span class="sxs-lookup"><span data-stu-id="61bea-459">Key Vault</span></span>

* <span data-ttu-id="61bea-460">ネットワーク ルールからサブネットを削除できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-460">Fixed issue where subnets couldn't be deleted from network rules</span></span>
* <span data-ttu-id="61bea-461">重複したサブネットと IP アドレスをネットワーク ルールに追加できる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-461">Fixed issue where duplicated subnets and IP addresses could be added to network rules</span></span>

### <a name="network"></a><span data-ttu-id="61bea-462">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-462">Network</span></span>

* <span data-ttu-id="61bea-463">トラフィック分析間隔の値を設定する `--interval` パラメーターを `network watcher flow-log` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-463">Added `--interval` parameter to `network watcher flow-log` to set traffic analysis interval value</span></span>
* <span data-ttu-id="61bea-464">ゲートウェイ ID を管理するための `network application-gateway identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-464">Added `network application-gateway identity` to manage gateway identity</span></span>
* <span data-ttu-id="61bea-465">Key Vault ID を設定するためのサポートを `network application-gateway ssl-cert` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-465">Added support for setting Key Vault ID to `network application-gateway ssl-cert`</span></span>
* <span data-ttu-id="61bea-466">`network express-route peering peer-connection [show|list]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-466">Added `network express-route peering peer-connection [show|list]`</span></span>

### <a name="policy"></a><span data-ttu-id="61bea-467">ポリシー</span><span class="sxs-lookup"><span data-stu-id="61bea-467">Policy</span></span>

* <span data-ttu-id="61bea-468">API バージョン 2019-01-01 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-468">Updated to use API version 2019-01-01</span></span>

## <a name="august-27-2019"></a><span data-ttu-id="61bea-469">2019 年 8 月 27 日</span><span class="sxs-lookup"><span data-stu-id="61bea-469">August 27, 2019</span></span>

<span data-ttu-id="61bea-470">バージョン 2.0.72</span><span class="sxs-lookup"><span data-stu-id="61bea-470">Version 2.0.72</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-471">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-471">ACR</span></span>

* <span data-ttu-id="61bea-472">[重大な変更]`classic` SKU のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-472">[BREAKING CHANGE] Removed support for the `classic` SKU</span></span>

### <a name="api-management"></a><span data-ttu-id="61bea-473">API Management</span><span class="sxs-lookup"><span data-stu-id="61bea-473">API Management</span></span>

* <span data-ttu-id="61bea-474">[プレビュー] `apim` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-474">[PREVIEW] Added `apim` command group</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-475">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-475">AppService</span></span>

* <span data-ttu-id="61bea-476">スロットを指定したときの `webapp webjob continuous start` コマンドに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-476">Fixed issue with `webapp webjob continuous start` command when specifying a slot</span></span>
* <span data-ttu-id="61bea-477">`env` フォルダーを検出してデプロイに使用されているファイルから削除するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-477">Changed `webapp up` to detect `env` folder and remove it from the file used for deployment</span></span>

### <a name="keyvault"></a><span data-ttu-id="61bea-478">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61bea-478">Keyvault</span></span>

* <span data-ttu-id="61bea-479">`--expires` 引数を無視する `keyvault secret set` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-479">Fixed a bug in `keyvault secret set` that igored the `--expires` argument</span></span>

### <a name="network"></a><span data-ttu-id="61bea-480">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-480">Network</span></span>

* <span data-ttu-id="61bea-481">`--private-ip-address-version` 引数に IPv6 アドレスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-481">Added support for IPv6 addresses to `--private-ip-address-version` arguments</span></span>
* <span data-ttu-id="61bea-482">プライベート エンドポイントの管理用に新しいコマンド `network private-endpoint [create|update|list-types]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-482">Added new commands `network private-endpoint [create|update|list-types]` for private endpoint management</span></span>
* <span data-ttu-id="61bea-483">コマンド グループ `network private-link-service` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-483">Added command group `network private-link-service`</span></span>
* <span data-ttu-id="61bea-484">`--private-endpoint-network-policies` 引数と `--private-link-service-network-policies` 引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-484">Added `--private-endpoint-network-policies` and `--private-link-service-network-policies` arguments to `network vnet subnet update`</span></span>

### <a name="rbac"></a><span data-ttu-id="61bea-485">RBAC</span><span class="sxs-lookup"><span data-stu-id="61bea-485">RBAC</span></span>

* <span data-ttu-id="61bea-486">ホームページが更新されない `ad app update --homepage` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-486">Fixed issue with `ad app update --homepage` where homepage would not be updated</span></span>

### <a name="servicefabric"></a><span data-ttu-id="61bea-487">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="61bea-487">ServiceFabric</span></span>

* <span data-ttu-id="61bea-488">キー コンテナーの大文字と小文字が混在する名前のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-488">Added support for mixed-case Key Vault names</span></span>
* <span data-ttu-id="61bea-489">Key Vault で証明書を使用したときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-489">Fixed issue when using certificates in Key Vault</span></span>
* <span data-ttu-id="61bea-490">PFX 証明書ファイルの使用に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-490">Fixed issue with using PFX certificate files</span></span>
* <span data-ttu-id="61bea-491">Key Vault リソースグループが指定されていなかったときの `sf cluster certificate add` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-491">Fixed issue with `sf cluster certificate add` when Key Vault resource group wasn't specified</span></span>
* <span data-ttu-id="61bea-492">`sf cluster set` が動作しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-492">Fixed issue with `sf cluster set` not working</span></span>

### <a name="signalr"></a><span data-ttu-id="61bea-493">SignalR</span><span class="sxs-lookup"><span data-stu-id="61bea-493">SignalR</span></span>

* <span data-ttu-id="61bea-494">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-494">Added new commands:</span></span>
  * <span data-ttu-id="61bea-495">`signalr cors`:SignalR CORS の管理</span><span class="sxs-lookup"><span data-stu-id="61bea-495">`signalr cors`: Manage SignalR CORS</span></span>
  * <span data-ttu-id="61bea-496">`signalr restart`:SignalR Service の再起動</span><span class="sxs-lookup"><span data-stu-id="61bea-496">`signalr restart`: Restart a SignalR service</span></span>
  * <span data-ttu-id="61bea-497">`signalr update`:SignalR Service の更新</span><span class="sxs-lookup"><span data-stu-id="61bea-497">`signalr update`: Update a SignalR service</span></span>
* <span data-ttu-id="61bea-498">`--service-mode` 引数を `signalr create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-498">Added `--service-mode` argument to `signalr create`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-499">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-499">Storage</span></span>

* <span data-ttu-id="61bea-500">`storage account revoke-delegation-keys` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-500">Added `storage account revoke-delegation-keys` command</span></span>

## <a name="august-13-2019"></a><span data-ttu-id="61bea-501">2019 年 8 月 13 日</span><span class="sxs-lookup"><span data-stu-id="61bea-501">August 13, 2019</span></span>

<span data-ttu-id="61bea-502">バージョン 2.0.71</span><span class="sxs-lookup"><span data-stu-id="61bea-502">Version 2.0.71</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-503">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-503">AppService</span></span>

* <span data-ttu-id="61bea-504">`webapp webjob continuous` コマンドがスロットで失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-504">Fixed issue where `webapp webjob continuous` commands were failing for slots</span></span>

### <a name="botservice"></a><span data-ttu-id="61bea-505">BotService</span><span class="sxs-lookup"><span data-stu-id="61bea-505">BotService</span></span>

* <span data-ttu-id="61bea-506">[重大な変更] v3 SDK ボットの作成のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-506">[BREAKING CHANGE] Removed support for creating v3 SDK bots</span></span>

### <a name="cognitiveservices"></a><span data-ttu-id="61bea-507">CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="61bea-507">CognitiveServices</span></span>

* <span data-ttu-id="61bea-508">`cognitiveservices account network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-508">Added `cognitiveservices account network-rule` commands</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="61bea-509">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-509">Cosmos DB</span></span>

* <span data-ttu-id="61bea-510">複数の書き込み場所を更新するときの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-510">Removed warning when updating multiple write locations</span></span>
* <span data-ttu-id="61bea-511">CosmosDB SQL、MongoDB、Cassandra、Gremlin、およびテーブル リソースとリソースのスループットのための CRUD コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-511">Added CRUD commands for CosmosDB SQL, MongoDB, Cassandra, Gremlin and Table resources and resource's throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="61bea-512">HDInsight</span><span class="sxs-lookup"><span data-stu-id="61bea-512">HDInsight</span></span>

<span data-ttu-id="61bea-513">このリリースには、多数の破壊的変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61bea-513">This release contains a large number of breaking changes.</span></span>

* <span data-ttu-id="61bea-514">[重大な変更]`hdinsight create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-514">[BREAKING CHANGE] Renamed parameters for `hdinsight create`:</span></span>
  * <span data-ttu-id="61bea-515">`--storage-default-container` から `--storage-container` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-515">Renamed `--storage-default-container` to `--storage-container`</span></span>
  * <span data-ttu-id="61bea-516">`--storage-default-filesystem` から `--storage-filesystem` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-516">Renamed `--storage-default-filesystem` to `--storage-filesystem`</span></span>
* <span data-ttu-id="61bea-517">[重大な変更]`application create` の `--name` 引数が、クラスター名の代わりにアプリケーション名を表すように変更されました</span><span class="sxs-lookup"><span data-stu-id="61bea-517">[BREAKING CHANGE] Changed the `--name` argument of `application create` to represent the application name instead of the cluster name</span></span>
* <span data-ttu-id="61bea-518">`--cluster-name` 引数が `application create` に追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="61bea-518">Added `--cluster-name` argument to `application create` to replace old `--name` functionality</span></span>
* <span data-ttu-id="61bea-519">[重大な変更]`application create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-519">[BREAKING CHANGE] Renamed parameters for `application create`:</span></span>
  * <span data-ttu-id="61bea-520">`--application-type` から `--type` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-520">Renamed `--application-type` to `--type`</span></span>
  * <span data-ttu-id="61bea-521">`--marketplace-identifier` から `--marketplace-id` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-521">Renamed `--marketplace-identifier` to `--marketplace-id`</span></span>
  * <span data-ttu-id="61bea-522">`--https-endpoint-access-mode` から `--access-mode` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-522">Renamed `--https-endpoint-access-mode` to `--access-mode`</span></span>
  * <span data-ttu-id="61bea-523">`--https-endpoint-destination-port` の名前を `--destination-port` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-523">Renamed  `--https-endpoint-destination-port` to `--destination-port`</span></span>
* <span data-ttu-id="61bea-524">[重大な変更]`application create` のパラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-524">[BREAKING CHANGE] Removed parameters for `application create`:</span></span>
  * `--https-endpoint-location`
  * `--https-endpoint-public-port`
  * `--ssh-endpoint-destination-port`
  * `--ssh-endpoint-location`
  * `--ssh-endpoint-public-port`
* <span data-ttu-id="61bea-525">[破壊的変更] `hdinsight resize`の `--target-instance-count` の名前を `--workernode-count` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-525">[BREAKING CHNAGE] Renamed `--target-instance-count` to `--workernode-count` for `hdinsight resize`</span></span>
* <span data-ttu-id="61bea-526">[重大な変更]`hdinsight script-action` グループのすべてのコマンドが、スクリプト アクションの名前として `--name` パラメーターを使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="61bea-526">[BREAKING CHANGE] Changed all commands in the `hdinsight script-action` group to use the `--name` parameter as the name of the script action.</span></span>
* <span data-ttu-id="61bea-527">`--cluster-name` 引数がすべての `hdinsight script-action` コマンドに追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="61bea-527">Added `--cluster-name` argument to all `hdinsight script-action` commands to replace old `--name` functionality</span></span>
* <span data-ttu-id="61bea-528">[重大な変更] すべての `hdinsight script-action` コマンドで `--script-execution-id` の名前を `--execution-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-528">[BREAKING CHANGE] Renamed `--script-execution-id` to `--execution-id` for all `hdinsight script-action` commands</span></span>
* <span data-ttu-id="61bea-529">[重大な変更] 名前を `hdinsight script-action show` から `hdinsight script-action show-execution-details` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-529">[BREAKING CHANGE] Renamed `hdinsight script-action show` to `hdinsight script-action show-execution-details`</span></span>
* <span data-ttu-id="61bea-530">[破壊的変更] `hdinsight script-action execute --roles` に対するパラメーターを、コンマ区切りではなくスペース区切りにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-530">[BREAKING CHNAGE] Changed parameters to `hdinsight script-action execute --roles` to be space-separated instead of comma-separated</span></span>
* <span data-ttu-id="61bea-531">[重大な変更]`hdinsight script-action list`の `--persisted` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-531">[BREAKING CHANGE] Removed the `--persisted` parameter of `hdinsight script-action list`</span></span>
* <span data-ttu-id="61bea-532">ローカル JSON ファイルへのパスまたは JSON 文字列を受け入れるように `hdinsight create --cluster-configurations` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-532">Changed the `hdinsight create --cluster-configurations` parameter to accept a path to a local JSON file or a JSON string</span></span>
* <span data-ttu-id="61bea-533">`hdinsight script-action list-execution-history` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-533">Added command `hdinsight script-action list-execution-history`</span></span>
* <span data-ttu-id="61bea-534">Log Analytics ワークスペース ID またはワークスペース名を受け入れるように `hdinsight monitor enable --workspace` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-534">Changed `hdinsight monitor enable --workspace` to accept a Log Analytics workspace ID or workspace name</span></span>
* <span data-ttu-id="61bea-535">`hdinsight monitor enable --primary-key` 引数を追加しました。これは、ワークスペース ID がパラメーターとして指定されている場合に必要です</span><span class="sxs-lookup"><span data-stu-id="61bea-535">Added the `hdinsight monitor enable --primary-key` argument, which is needed if a workspace ID is provided as the parameter</span></span>
* <span data-ttu-id="61bea-536">例をさらに追加し、ヘルプ メッセージの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-536">Added more examples and updated descriptions for help messages</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-537">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-537">Interactive</span></span>

* <span data-ttu-id="61bea-538">読み込みエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-538">Fixed a loading error</span></span>

### <a name="kubernetes"></a><span data-ttu-id="61bea-539">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="61bea-539">Kubernetes</span></span>

* <span data-ttu-id="61bea-540">ダッシュボードのコンテナー ポートで `https` が使用されている場合に `https` を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-540">Changed to use `https` if dashboard container port is using `https`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-541">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-541">Network</span></span>

* <span data-ttu-id="61bea-542">`--yes` 引数を `network dns record-set cname delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-542">Added `--yes` argument `network dns record-set cname delete`</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-543">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-543">Profile</span></span>

* <span data-ttu-id="61bea-544">リソースのアクセス トークンを取得するための `account get-access-token` に `--resource-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-544">Added `--resource-type` argument to `account get-access-token` to get resource access tokens</span></span>

### <a name="servicefabric"></a><span data-ttu-id="61bea-545">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="61bea-545">ServiceFabric</span></span>

* <span data-ttu-id="61bea-546">sf cluster create でサポートされているすべての OS バージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-546">Added all supported os version for sf cluster create</span></span>
* <span data-ttu-id="61bea-547">プライマリ証明書の検証のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-547">Fixed primary certificate validation bug</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-548">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-548">Storage</span></span>

* <span data-ttu-id="61bea-549">`storage copy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-549">Added command `storage copy`</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="61bea-550">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="61bea-550">July 30, 2019</span></span>

<span data-ttu-id="61bea-551">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="61bea-551">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-552">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-552">ACR</span></span>

* <span data-ttu-id="61bea-553">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-553">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="61bea-554">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-554">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-555">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-555">Appservice</span></span>

* <span data-ttu-id="61bea-556">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-556">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="61bea-557">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-557">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="61bea-558">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-558">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="61bea-559">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-559">Network</span></span>

* <span data-ttu-id="61bea-560">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="61bea-560">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="61bea-561">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-561">Fixes #9604.</span></span> <span data-ttu-id="61bea-562">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-562">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="61bea-563">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="61bea-563">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="61bea-564">RBAC</span><span class="sxs-lookup"><span data-stu-id="61bea-564">RBAC</span></span>

* <span data-ttu-id="61bea-565">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-565">Added `user update` command</span></span>
* <span data-ttu-id="61bea-566">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-566">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="61bea-567">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="61bea-567">Use replacement argument `--id`</span></span>
* <span data-ttu-id="61bea-568">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-568">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-569">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-569">SQL</span></span>

* <span data-ttu-id="61bea-570">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-570">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-571">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-571">Storage</span></span>

* <span data-ttu-id="61bea-572">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-572">Added `storage remove` command</span></span>
* <span data-ttu-id="61bea-573">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-573">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-574">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-574">VM</span></span>

* <span data-ttu-id="61bea-575">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-575">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="61bea-576">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-576">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="61bea-577">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-577">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="61bea-578">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-578">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="61bea-579">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-579">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="61bea-580">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="61bea-580">July 16, 2019</span></span>

<span data-ttu-id="61bea-581">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="61bea-581">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-582">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-582">Appservice</span></span>

* <span data-ttu-id="61bea-583">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="61bea-583">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="61bea-584">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-584">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="61bea-585">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-585">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="61bea-586">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-586">Core</span></span>

* <span data-ttu-id="61bea-587">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-587">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-588">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-588">Batch</span></span>

* <span data-ttu-id="61bea-589">[重大な変更]`batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="61bea-589">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="61bea-590">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-590">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="61bea-591">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-591">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="61bea-592">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-592">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="61bea-593">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="61bea-593">Eventhubs</span></span>

* <span data-ttu-id="61bea-594">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-594">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-595">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61bea-595">RDBMS</span></span>

* <span data-ttu-id="61bea-596">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-596">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="61bea-597">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-597">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="61bea-598">リレー</span><span class="sxs-lookup"><span data-stu-id="61bea-598">Relay</span></span>

* <span data-ttu-id="61bea-599">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="61bea-599">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="61bea-600">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-600">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="61bea-601">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="61bea-601">Servicebus</span></span>

* <span data-ttu-id="61bea-602">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-602">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-603">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-603">Storage</span></span>

* <span data-ttu-id="61bea-604">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="61bea-604">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="61bea-605">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="61bea-605">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="61bea-606">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="61bea-606">July 2, 2019</span></span>

<span data-ttu-id="61bea-607">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="61bea-607">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="61bea-608">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-608">Core</span></span>

* <span data-ttu-id="61bea-609">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="61bea-609">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="61bea-610">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="61bea-610">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="61bea-611">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="61bea-611">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-612">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-612">ACR</span></span>

* <span data-ttu-id="61bea-613">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-613">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-614">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-614">Appservice</span></span>

* <span data-ttu-id="61bea-615">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-615">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="61bea-616">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-616">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="61bea-617">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="61bea-617">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="61bea-618">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-618">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="61bea-619">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-619">Cosmos DB</span></span>

* <span data-ttu-id="61bea-620">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-620">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="61bea-621">DLS</span><span class="sxs-lookup"><span data-stu-id="61bea-621">DLS</span></span>

* <span data-ttu-id="61bea-622">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="61bea-622">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="61bea-623">フィードバック</span><span class="sxs-lookup"><span data-stu-id="61bea-623">Feedback</span></span>

* <span data-ttu-id="61bea-624">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-624">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="61bea-625">HDInsight</span><span class="sxs-lookup"><span data-stu-id="61bea-625">HDInsight</span></span>

* <span data-ttu-id="61bea-626">[重大な変更]`oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-626">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="61bea-627">[重大な変更]`--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-627">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="61bea-628">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-628">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="61bea-629">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-629">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="61bea-630">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-630">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="61bea-631">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-631">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="61bea-632">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-632">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="61bea-633">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="61bea-633">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="61bea-634">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-634">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="61bea-635">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="61bea-635">Managed Services</span></span>

* <span data-ttu-id="61bea-636">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="61bea-636">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-637">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-637">Profile</span></span>
* <span data-ttu-id="61bea-638">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="61bea-638">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="61bea-639">RBAC</span><span class="sxs-lookup"><span data-stu-id="61bea-639">RBAC</span></span>

* <span data-ttu-id="61bea-640">[重大な変更]`create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-640">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="61bea-641">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-641">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="61bea-642">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-642">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="61bea-643">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-643">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-644">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61bea-644">RDBMS</span></span>

* <span data-ttu-id="61bea-645">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-645">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-646">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-646">SQL</span></span>

* <span data-ttu-id="61bea-647">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-647">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-648">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-648">Storage</span></span>

* <span data-ttu-id="61bea-649">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-649">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="61bea-650">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-650">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="61bea-651">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-651">VM</span></span>

* <span data-ttu-id="61bea-652">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-652">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="61bea-653">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-653">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="61bea-654">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="61bea-654">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="61bea-655">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-655">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="61bea-656">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="61bea-656">June 18, 2019</span></span>

<span data-ttu-id="61bea-657">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="61bea-657">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="61bea-658">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-658">Core</span></span>

<span data-ttu-id="61bea-659">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="61bea-659">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="61bea-660">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="61bea-660">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="61bea-661">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="61bea-661">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="61bea-662">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="61bea-662">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="61bea-663">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="61bea-663">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="61bea-664">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="61bea-664">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="61bea-665">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="61bea-665">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-666">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-666">ACR</span></span>
* <span data-ttu-id="61bea-667">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-667">Added 'acr check-health' command</span></span>
* <span data-ttu-id="61bea-668">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-668">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-669">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-669">ACS</span></span>
* <span data-ttu-id="61bea-670">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="61bea-670">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="61bea-671">AMS</span><span class="sxs-lookup"><span data-stu-id="61bea-671">AMS</span></span>
* <span data-ttu-id="61bea-672">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-672">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-673">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-673">AppService</span></span>
* <span data-ttu-id="61bea-674">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-674">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="61bea-675">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-675">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="61bea-676">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-676">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="61bea-677">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-677">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="61bea-678">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-678">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="61bea-679">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-679">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-680">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-680">Batch</span></span>
* <span data-ttu-id="61bea-681">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-681">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="61bea-682">BatchAI</span><span class="sxs-lookup"><span data-stu-id="61bea-682">BatchAI</span></span>
* <span data-ttu-id="61bea-683">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="61bea-683">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="61bea-684">BotService</span><span class="sxs-lookup"><span data-stu-id="61bea-684">BotService</span></span>
* <span data-ttu-id="61bea-685">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-685">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-686">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-686">CosmosDB</span></span>
* <span data-ttu-id="61bea-687">[非推奨]`cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-687">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="61bea-688">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="61bea-688">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="61bea-689">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-689">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="61bea-690">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-690">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="61bea-691">EventGrid</span><span class="sxs-lookup"><span data-stu-id="61bea-691">EventGrid</span></span>
* <span data-ttu-id="61bea-692">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-692">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="61bea-693">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-693">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="61bea-694">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-694">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="61bea-695">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-695">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="61bea-696">[重大な変更]`eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-696">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="61bea-697">HDInsight</span><span class="sxs-lookup"><span data-stu-id="61bea-697">HDInsight</span></span>
* <span data-ttu-id="61bea-698">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-698">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-699">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-699">IoT</span></span>
* <span data-ttu-id="61bea-700">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-700">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="61bea-701">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-701">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="61bea-702">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-702">Network</span></span>
* <span data-ttu-id="61bea-703">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-703">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="61bea-704">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-704">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="61bea-705">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-705">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="61bea-706">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-706">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-707">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-707">Resource</span></span>
* <span data-ttu-id="61bea-708">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-708">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="61bea-709">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-709">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="61bea-710">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="61bea-710">ServiceBus</span></span>
* <span data-ttu-id="61bea-711">`servicebus topic create --max-size` での問題 [#9319](https://github.com/azure/azure-cli/issues/9319) を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-711">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-712">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-712">SQL</span></span>
* <span data-ttu-id="61bea-713">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-713">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="61bea-714">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-714">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="61bea-715">SQLVm</span><span class="sxs-lookup"><span data-stu-id="61bea-715">SQLVm</span></span>
* <span data-ttu-id="61bea-716">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-716">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="61bea-717">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-717">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-718">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-718">Storage</span></span>
* <span data-ttu-id="61bea-719">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-719">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="61bea-720">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-720">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-721">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-721">VM</span></span>
* <span data-ttu-id="61bea-722">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-722">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="61bea-723">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="61bea-723">June 4, 2019</span></span>

<span data-ttu-id="61bea-724">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="61bea-724">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="61bea-725">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-725">Core</span></span>
* <span data-ttu-id="61bea-726">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-726">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-727">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-727">ACR</span></span>
* <span data-ttu-id="61bea-728">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-728">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-729">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-729">ACS</span></span>
* <span data-ttu-id="61bea-730">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-730">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="61bea-731">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="61bea-731">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-732">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-732">Batch</span></span>
* <span data-ttu-id="61bea-733">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-733">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-734">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-734">IoT</span></span>
* <span data-ttu-id="61bea-735">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-735">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="61bea-736">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-736">Network</span></span>
* <span data-ttu-id="61bea-737">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-737">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="61bea-738">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-738">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="61bea-739">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-739">Resource</span></span>
* <span data-ttu-id="61bea-740">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-740">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="61bea-741">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-741">Role</span></span>
* <span data-ttu-id="61bea-742">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-742">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="61bea-743">Compute</span><span class="sxs-lookup"><span data-stu-id="61bea-743">Compute</span></span>
* <span data-ttu-id="61bea-744">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-744">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="61bea-745">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="61bea-745">May 21, 2019</span></span>

<span data-ttu-id="61bea-746">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="61bea-746">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="61bea-747">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-747">Core</span></span>
* <span data-ttu-id="61bea-748">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-748">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="61bea-749">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-749">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="61bea-750">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-750">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-751">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-751">ACR</span></span>
* <span data-ttu-id="61bea-752">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-752">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-753">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-753">ACS</span></span>
* <span data-ttu-id="61bea-754">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-754">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-755">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-755">AppService</span></span>
* <span data-ttu-id="61bea-756">[非推奨]`functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="61bea-756">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="61bea-757">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-757">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="61bea-758">[重大な変更]`--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="61bea-758">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="61bea-759">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-759">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="61bea-760">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-760">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="61bea-761">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-761">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="61bea-762">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-762">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="61bea-763">BotService</span><span class="sxs-lookup"><span data-stu-id="61bea-763">BotService</span></span>
* <span data-ttu-id="61bea-764">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-764">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="61bea-765">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-765">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="61bea-766">従量課金</span><span class="sxs-lookup"><span data-stu-id="61bea-766">Consumption</span></span>
* <span data-ttu-id="61bea-767">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-767">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-768">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-768">IoT</span></span>
* <span data-ttu-id="61bea-769">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-769">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="61bea-770">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-770">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="61bea-772">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-772">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="61bea-773">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-773">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-774">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61bea-774">RDBMS</span></span>
* <span data-ttu-id="61bea-775">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-775">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="61bea-776">RBAC</span><span class="sxs-lookup"><span data-stu-id="61bea-776">RBAC</span></span>
* <span data-ttu-id="61bea-777">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-777">Added support for management group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-778">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-778">Storage</span></span>
* <span data-ttu-id="61bea-779">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="61bea-779">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="61bea-780">Compute</span><span class="sxs-lookup"><span data-stu-id="61bea-780">Compute</span></span>
* <span data-ttu-id="61bea-781">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-781">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="61bea-782">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-782">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="61bea-783">__注__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="61bea-783">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="61bea-784">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-784">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="61bea-785">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="61bea-785">May 6, 2019</span></span>

<span data-ttu-id="61bea-786">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="61bea-786">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-787">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-787">ACS</span></span>
* <span data-ttu-id="61bea-788">[重大な変更]`--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-788">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="61bea-789">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-789">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="61bea-790">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-790">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="61bea-791">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-791">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-792">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-792">Appservice</span></span>
* <span data-ttu-id="61bea-793">[非推奨]`functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-793">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="61bea-794">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-794">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="61bea-795">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-795">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="61bea-796">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-796">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="61bea-797">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-797">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="61bea-798">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-798">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="61bea-799">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-799">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="61bea-800">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-800">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="61bea-801">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-801">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="61bea-802">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-802">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-803">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-803">Batch</span></span>
* <span data-ttu-id="61bea-804">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-804">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="61bea-805">Botservice</span><span class="sxs-lookup"><span data-stu-id="61bea-805">Botservice</span></span>
* <span data-ttu-id="61bea-806">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="61bea-806">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="61bea-807">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-807">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="61bea-808">[重大な変更]`--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-808">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="61bea-809">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-809">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="61bea-810">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-810">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="61bea-811">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="61bea-811">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="61bea-812">[重大な変更]`bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-812">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="61bea-813">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-813">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="61bea-814">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-814">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="61bea-815">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-815">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="61bea-816">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-816">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="61bea-817">[重大な変更]`Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-817">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="61bea-818">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-818">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="61bea-819">[重大な変更]`SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-819">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="61bea-820">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="61bea-820">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="61bea-821">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-821">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="61bea-822">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-822">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="61bea-823">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-823">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="61bea-824">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-824">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="61bea-825">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-825">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="61bea-826">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-826">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="61bea-827">[構成]</span><span class="sxs-lookup"><span data-stu-id="61bea-827">Configure</span></span>
* <span data-ttu-id="61bea-828">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-828">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="61bea-829">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="61bea-829">Eventhubs</span></span>
* <span data-ttu-id="61bea-830">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-830">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="61bea-831">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-831">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-832">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-832">Network</span></span>
* <span data-ttu-id="61bea-833">[重大な変更]`vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="61bea-833">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="61bea-834">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="61bea-834">Policy Insights</span></span>
* <span data-ttu-id="61bea-835">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-835">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="61bea-836">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-836">Role</span></span>
* <span data-ttu-id="61bea-837">[非推奨]`create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="61bea-837">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="61bea-838">Service Bus</span><span class="sxs-lookup"><span data-stu-id="61bea-838">Service Bus</span></span>
* <span data-ttu-id="61bea-839">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-839">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="61bea-840">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-840">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="61bea-841">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-841">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-842">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-842">SQL</span></span>
* <span data-ttu-id="61bea-843">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-843">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-844">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-844">VM</span></span>
* <span data-ttu-id="61bea-845">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-845">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="61bea-846">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-846">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="61bea-847">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-847">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="61bea-848">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-848">Added new `ppg` command group for managing Proximity Placement Groups</span></span>
* <span data-ttu-id="61bea-849">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-849">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="61bea-850">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-850">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="61bea-851">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="61bea-851">April 23, 2019</span></span>

<span data-ttu-id="61bea-852">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="61bea-852">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-853">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-853">ACS</span></span>
* <span data-ttu-id="61bea-854">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-854">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="61bea-855">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-855">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="61bea-856">AMS</span><span class="sxs-lookup"><span data-stu-id="61bea-856">AMS</span></span>
* <span data-ttu-id="61bea-857">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-857">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-858">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-858">AppService</span></span>
* <span data-ttu-id="61bea-859">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-859">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="61bea-860">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-860">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="61bea-861">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-861">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="61bea-862">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-862">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="61bea-863">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-863">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="61bea-864">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-864">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="61bea-865">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-865">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="61bea-866">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-866">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="61bea-867">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-867">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="61bea-868">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="61bea-868">Deployment Manager</span></span>
* <span data-ttu-id="61bea-869">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="61bea-869">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="61bea-870">ラボ</span><span class="sxs-lookup"><span data-stu-id="61bea-870">Lab</span></span>
* <span data-ttu-id="61bea-871">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-871">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="61bea-872">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-872">Network</span></span>
* <span data-ttu-id="61bea-873">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-873">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-874">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-874">Resource</span></span>
* <span data-ttu-id="61bea-875">[非推奨]`resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="61bea-875">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="61bea-876">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-876">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="61bea-877">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-877">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="61bea-878">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-878">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-879">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-879">SQL</span></span>
* <span data-ttu-id="61bea-880">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-880">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="61bea-881">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-881">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="61bea-882">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-882">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="61bea-883">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-883">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-884">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-884">Storage</span></span>
* <span data-ttu-id="61bea-885">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-885">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-886">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-886">VM</span></span>
* <span data-ttu-id="61bea-887">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-887">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="61bea-888">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-888">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="61bea-889">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-889">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="61bea-890">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="61bea-890">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="61bea-891">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-891">Core</span></span>
* <span data-ttu-id="61bea-892">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-892">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-893">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-893">ACR</span></span>
* <span data-ttu-id="61bea-894">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-894">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="61bea-895">AMS</span><span class="sxs-lookup"><span data-stu-id="61bea-895">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="61bea-898">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-898">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="61bea-899">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-899">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-900">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-900">AppService</span></span>
* <span data-ttu-id="61bea-901">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-901">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="61bea-902">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-902">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="61bea-903">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-903">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="61bea-904">[重大な変更]`devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="61bea-904">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="61bea-905">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-905">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="61bea-906">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-906">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="61bea-907">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-907">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="61bea-908">CDN</span><span class="sxs-lookup"><span data-stu-id="61bea-908">CDN</span></span>
* <span data-ttu-id="61bea-909">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-909">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="61bea-910">フィードバック</span><span class="sxs-lookup"><span data-stu-id="61bea-910">Feedback</span></span>
* <span data-ttu-id="61bea-911">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-911">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="61bea-912">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-912">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="61bea-913">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-913">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-914">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-914">Monitor</span></span>
* <span data-ttu-id="61bea-915">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-915">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="61bea-916">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-916">Network</span></span>
* <span data-ttu-id="61bea-917">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-917">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="61bea-918">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-918">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="61bea-919">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-919">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="61bea-920">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-920">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="61bea-921">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="61bea-921">PrivateDNS</span></span>
* <span data-ttu-id="61bea-922">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-922">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-923">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-923">Resource</span></span>
* <span data-ttu-id="61bea-924">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-924">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="61bea-925">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-925">Role</span></span>
* <span data-ttu-id="61bea-926">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-926">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="61bea-927">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-927">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-928">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-928">SQL</span></span>
* <span data-ttu-id="61bea-929">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-929">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-930">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-930">Storage</span></span>
* <span data-ttu-id="61bea-931">[重大な変更]`storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-931">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="61bea-932">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-932">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="61bea-933">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-933">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="61bea-934">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-934">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="61bea-935">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="61bea-935">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="61bea-936">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-936">Core</span></span>
* <span data-ttu-id="61bea-937">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-937">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="61bea-938">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-938">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="61bea-939">クラウド</span><span class="sxs-lookup"><span data-stu-id="61bea-939">Cloud</span></span>
* <span data-ttu-id="61bea-940">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-940">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-941">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-941">ACR</span></span>
* <span data-ttu-id="61bea-942">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-942">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="61bea-943">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-943">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="61bea-944">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-944">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="61bea-945">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-945">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-946">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-946">AppService</span></span>
* <span data-ttu-id="61bea-947">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-947">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="61bea-948">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-948">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="61bea-949">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="61bea-949">BOT Service</span></span>
* <span data-ttu-id="61bea-950">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-950">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="61bea-951">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-951">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="61bea-952">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-952">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="61bea-953">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-953">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="61bea-954">CDN</span><span class="sxs-lookup"><span data-stu-id="61bea-954">CDN</span></span>
* <span data-ttu-id="61bea-955">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-955">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="61bea-957">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="61bea-957">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="61bea-958">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-958">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-959">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="61bea-959">Cosmosdb</span></span>
* <span data-ttu-id="61bea-960">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-960">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="61bea-961">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-961">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-962">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-962">Interactive</span></span>
* <span data-ttu-id="61bea-963">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-963">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-964">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-964">Monitor</span></span>
* <span data-ttu-id="61bea-965">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-965">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-966">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-966">Network</span></span>
* <span data-ttu-id="61bea-967">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-967">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-968">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-968">Profile</span></span>
* <span data-ttu-id="61bea-969">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-969">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="61bea-970">Postgres</span><span class="sxs-lookup"><span data-stu-id="61bea-970">Postgres</span></span> 
* <span data-ttu-id="61bea-971">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-971">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="61bea-972">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="61bea-972">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-973">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-973">Resource</span></span>
* <span data-ttu-id="61bea-974">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-974">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="61bea-975">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-975">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="61bea-976">グラフ</span><span class="sxs-lookup"><span data-stu-id="61bea-976">Graph</span></span>
* <span data-ttu-id="61bea-977">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-977">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="61bea-978">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-978">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="61bea-979">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-979">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="61bea-980">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-980">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="61bea-981">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-981">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-982">storage</span><span class="sxs-lookup"><span data-stu-id="61bea-982">storage</span></span>
* <span data-ttu-id="61bea-983">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-983">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="61bea-984">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-984">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="61bea-985">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-985">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="61bea-986">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-986">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-987">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-987">VM</span></span>
* <span data-ttu-id="61bea-988">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-988">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="61bea-989">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="61bea-989">March 12, 2019</span></span>

<span data-ttu-id="61bea-990">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="61bea-990">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="61bea-991">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-991">Core</span></span>

* <span data-ttu-id="61bea-992">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-992">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-993">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-993">ACR</span></span>

* <span data-ttu-id="61bea-994">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-994">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-995">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-995">ACS</span></span>

* <span data-ttu-id="61bea-996">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-996">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="61bea-997">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-997">AppService</span></span>

* <span data-ttu-id="61bea-998">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-998">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="61bea-999">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-999">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="61bea-1000">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1000">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="61bea-1001">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1001">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="61bea-1002">Botservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1002">Botservice</span></span>

* <span data-ttu-id="61bea-1003">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1003">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="61bea-1004">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1004">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="61bea-1005">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1005">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="61bea-1006">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1006">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1007">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1007">Container</span></span>

* <span data-ttu-id="61bea-1008">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1008">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="61bea-1009">EventHub</span><span class="sxs-lookup"><span data-stu-id="61bea-1009">EventHub</span></span>

* <span data-ttu-id="61bea-1010">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1010">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="61bea-1011">Find</span><span class="sxs-lookup"><span data-stu-id="61bea-1011">Find</span></span>

* <span data-ttu-id="61bea-1012">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="61bea-1012">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="61bea-1013">HDInsight</span><span class="sxs-lookup"><span data-stu-id="61bea-1013">HDInsight</span></span>

* <span data-ttu-id="61bea-1014">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1014">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1015">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1015">Network</span></span>

* <span data-ttu-id="61bea-1016">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1016">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-1017">Rdbms</span><span class="sxs-lookup"><span data-stu-id="61bea-1017">Rdbms</span></span>

* <span data-ttu-id="61bea-1018">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="61bea-1018">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1019">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1019">Role</span></span>

* <span data-ttu-id="61bea-1020">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1020">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="61bea-1021">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1021">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="61bea-1022">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="61bea-1022">Service Fabric</span></span>

* <span data-ttu-id="61bea-1023">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1023">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="61bea-1024">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1024">February 26, 2019</span></span>

<span data-ttu-id="61bea-1025">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="61bea-1025">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1026">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1026">Core</span></span>

* <span data-ttu-id="61bea-1027">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1027">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1028">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1028">ACR</span></span>

* <span data-ttu-id="61bea-1029">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1029">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="61bea-1030">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1030">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1031">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1031">ACS</span></span>

* <span data-ttu-id="61bea-1032">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1032">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1033">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-1033">AppService</span></span>

* <span data-ttu-id="61bea-1034">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1034">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-1035">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-1035">Batch</span></span>
* <span data-ttu-id="61bea-1036">[重大な変更]`batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1036">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="61bea-1037">[重大な変更]`Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1037">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="61bea-1038">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1038">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="61bea-1039">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1039">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="61bea-1040">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1040">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="61bea-1041">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="61bea-1041">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-1042">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-1042">CosmosDB</span></span>

* <span data-ttu-id="61bea-1043">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1043">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="61bea-1044">Kusto</span><span class="sxs-lookup"><span data-stu-id="61bea-1044">Kusto</span></span>

* <span data-ttu-id="61bea-1045">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1045">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1046">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1046">Network</span></span>

* <span data-ttu-id="61bea-1047">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1047">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="61bea-1048">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1048">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="61bea-1049">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1049">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="61bea-1050">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1050">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="61bea-1051">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1051">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="61bea-1052">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1052">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="61bea-1053">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1053">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-1054">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-1054">Resource</span></span>

* <span data-ttu-id="61bea-1055">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1055">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="61bea-1056">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1056">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="61bea-1057">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1057">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="61bea-1058">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1058">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="61bea-1059">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1059">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1060">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1060">Role</span></span>

* <span data-ttu-id="61bea-1061">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1061">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1062">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1062">VM</span></span>

* <span data-ttu-id="61bea-1063">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1063">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="61bea-1064">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1064">February 12, 2019</span></span>

<span data-ttu-id="61bea-1065">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="61bea-1065">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1066">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1066">Core</span></span>

* <span data-ttu-id="61bea-1067">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-1067">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="61bea-1068">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1068">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1069">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1069">ACR</span></span>
* <span data-ttu-id="61bea-1070">[重大な変更]`acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1070">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="61bea-1071">[重大な変更]`acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1071">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1072">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1072">ACS</span></span>
* <span data-ttu-id="61bea-1073">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1073">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="61bea-1074">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1074">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="61bea-1075">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1075">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="61bea-1076">AMS</span><span class="sxs-lookup"><span data-stu-id="61bea-1076">AMS</span></span>
* <span data-ttu-id="61bea-1077">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1077">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="61bea-1078">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1078">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1079">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1079">Appservice</span></span>
* <span data-ttu-id="61bea-1080">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1080">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="61bea-1081">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-1081">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="61bea-1082">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1082">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="61bea-1083">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1083">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="61bea-1084">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1084">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="61bea-1085">Botservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1085">Botservice</span></span>
* <span data-ttu-id="61bea-1086">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1086">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="61bea-1087">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1087">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="61bea-1088">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1088">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="61bea-1089">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1089">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="61bea-1090">[非推奨]`--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1090">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="61bea-1091">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1091">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="61bea-1092">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1092">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="61bea-1093">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1093">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="61bea-1094">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="61bea-1094">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="61bea-1095">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1095">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="61bea-1096">Key Vault</span><span class="sxs-lookup"><span data-stu-id="61bea-1096">Key Vault</span></span>
* <span data-ttu-id="61bea-1097">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1097">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-1098">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-1098">Monitor</span></span>
* <span data-ttu-id="61bea-1099">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1099">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1100">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1100">Network</span></span>
* <span data-ttu-id="61bea-1101">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1101">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="61bea-1102">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1102">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="61bea-1103">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1103">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="61bea-1104">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1104">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="61bea-1105">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="61bea-1105">Policy Insights</span></span>
* <span data-ttu-id="61bea-1106">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1106">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-1107">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61bea-1107">RDBMS</span></span>
* <span data-ttu-id="61bea-1108">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1108">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="61bea-1109">Redis</span><span class="sxs-lookup"><span data-stu-id="61bea-1109">Redis</span></span>
* <span data-ttu-id="61bea-1110">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1110">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="61bea-1111">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1111">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="61bea-1112">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1112">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="61bea-1113">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1113">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="61bea-1114">[重大な変更]`redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1114">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="61bea-1115">[重大な変更]`redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="61bea-1115">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="61bea-1116">[非推奨]`redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1116">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1117">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1117">Role</span></span>
* <span data-ttu-id="61bea-1118">[重大な変更]`az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1118">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="61bea-1119">SQL VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1119">SQL VM</span></span>
* <span data-ttu-id="61bea-1120">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1120">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1121">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1121">VM</span></span>
* <span data-ttu-id="61bea-1122">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1122">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="61bea-1123">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1123">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="61bea-1124">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1124">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="61bea-1125">[重大な変更]`az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1125">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="61bea-1126">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1126">January 31, 2019</span></span>

<span data-ttu-id="61bea-1127">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="61bea-1127">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1128">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1128">Core</span></span>

* <span data-ttu-id="61bea-1129">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="61bea-1129">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="61bea-1130">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1130">January 28, 2019</span></span>

<span data-ttu-id="61bea-1131">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="61bea-1131">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1132">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1132">ACR</span></span>
* <span data-ttu-id="61bea-1133">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1133">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1134">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1134">ACS</span></span>
* <span data-ttu-id="61bea-1135">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1135">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="61bea-1136">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1136">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="61bea-1137">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1137">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="61bea-1138">AMS</span><span class="sxs-lookup"><span data-stu-id="61bea-1138">AMS</span></span>
* <span data-ttu-id="61bea-1139">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1139">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="61bea-1140">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1140">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1141">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1141">Appservice</span></span>
* <span data-ttu-id="61bea-1142">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1142">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="61bea-1143">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1143">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="61bea-1144">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1144">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1145">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1145">Container</span></span>
* <span data-ttu-id="61bea-1146">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1146">Added `container start` command</span></span>
* <span data-ttu-id="61bea-1147">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1147">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="61bea-1148">EventGrid</span><span class="sxs-lookup"><span data-stu-id="61bea-1148">EventGrid</span></span>
* <span data-ttu-id="61bea-1149">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1149">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="61bea-1150">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1150">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="61bea-1151">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1151">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="61bea-1152">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1152">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="61bea-1153">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1153">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="61bea-1154">HDInsight</span><span class="sxs-lookup"><span data-stu-id="61bea-1154">HDInsight</span></span>
* <span data-ttu-id="61bea-1155">[重大な変更]`hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1155">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="61bea-1156">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1156">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="61bea-1157">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1157">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="61bea-1158">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-1158">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="61bea-1159">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1159">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="61bea-1160">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1160">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-1161">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-1161">IoT</span></span>
* <span data-ttu-id="61bea-1162">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1162">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="61bea-1163">Kusto</span><span class="sxs-lookup"><span data-stu-id="61bea-1163">Kusto</span></span>
* <span data-ttu-id="61bea-1164">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="61bea-1164">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-1165">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-1165">Monitor</span></span>
* <span data-ttu-id="61bea-1166">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1166">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-1167">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-1167">Profile</span></span>
* <span data-ttu-id="61bea-1168">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1168">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1169">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1169">Network</span></span>
* <span data-ttu-id="61bea-1170">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1170">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="61bea-1171">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1171">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-1172">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-1172">Resource</span></span>
* <span data-ttu-id="61bea-1173">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1173">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="61bea-1174">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1174">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="61bea-1175">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="61bea-1175">SQL Virtual Machine</span></span>
* <span data-ttu-id="61bea-1176">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="61bea-1176">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1177">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1177">Storage</span></span>
* <span data-ttu-id="61bea-1178">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1178">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="61bea-1179">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="61bea-1179">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1180">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1180">VM</span></span>
* <span data-ttu-id="61bea-1181">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1181">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="61bea-1182">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1182">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="61bea-1183">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1183">January 15, 2019</span></span>

<span data-ttu-id="61bea-1184">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="61bea-1184">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1185">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1185">ACR</span></span>
* <span data-ttu-id="61bea-1186">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1186">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="61bea-1187">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1187">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="61bea-1188">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1188">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="61bea-1189">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1189">ACS</span></span>
* <span data-ttu-id="61bea-1190">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1190">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1191">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1191">Appservice</span></span>
* <span data-ttu-id="61bea-1192">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1192">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="61bea-1193">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1193">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="61bea-1194">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1194">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="61bea-1195">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1195">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="61bea-1196">Botservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1196">Botservice</span></span>
* <span data-ttu-id="61bea-1197">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1197">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="61bea-1198">[構成]</span><span class="sxs-lookup"><span data-stu-id="61bea-1198">Configure</span></span>
* <span data-ttu-id="61bea-1199">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1199">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-1200">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-1200">CosmosDB</span></span>
* <span data-ttu-id="61bea-1201">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1201">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="61bea-1202">HDInsight</span><span class="sxs-lookup"><span data-stu-id="61bea-1202">HDInsight</span></span>
* <span data-ttu-id="61bea-1203">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1203">Added commands for managing applications</span></span>
* <span data-ttu-id="61bea-1204">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1204">Added commands for managing script actions</span></span>
* <span data-ttu-id="61bea-1205">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1205">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="61bea-1206">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1206">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="61bea-1207">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1207">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1208">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1208">Network</span></span>
* <span data-ttu-id="61bea-1209">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1209">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="61bea-1210">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1210">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="61bea-1211">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1211">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="61bea-1212">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1212">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1213">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1213">Role</span></span>
* <span data-ttu-id="61bea-1214">[非推奨]`create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1214">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="61bea-1215">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="61bea-1215">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="61bea-1216">Security</span><span class="sxs-lookup"><span data-stu-id="61bea-1216">Security</span></span>
* <span data-ttu-id="61bea-1217">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-1217">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1218">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1218">Storage</span></span>
* <span data-ttu-id="61bea-1219">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1219">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="61bea-1220">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="61bea-1220">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="61bea-1221">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1221">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="61bea-1222">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1222">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="61bea-1223">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1223">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1224">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1224">VM</span></span>
* <span data-ttu-id="61bea-1225">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1225">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="61bea-1226">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1226">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="61bea-1227">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1227">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="61bea-1228">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1228">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="61bea-1229">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1229">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="61bea-1230">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1230">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="61bea-1231">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1231">December 20, 2018</span></span>

<span data-ttu-id="61bea-1232">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="61bea-1232">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="61bea-1233">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1233">Appservice</span></span>
* <span data-ttu-id="61bea-1234">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1234">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="61bea-1235">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1235">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="61bea-1236">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1236">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="61bea-1237">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="61bea-1237">IoTCentral</span></span>
* <span data-ttu-id="61bea-1238">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1238">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1239">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1239">Role</span></span>
* <span data-ttu-id="61bea-1240">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1240">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-1241">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-1241">SQL</span></span>
* <span data-ttu-id="61bea-1242">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1242">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1243">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1243">VM</span></span>
* <span data-ttu-id="61bea-1244">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1244">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="61bea-1245">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1245">December 18, 2018</span></span>

<span data-ttu-id="61bea-1246">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="61bea-1246">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="61bea-1247">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1247">ACR</span></span>
* <span data-ttu-id="61bea-1248">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1248">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="61bea-1249">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1249">Condensed the table layout for task list</span></span>
* <span data-ttu-id="61bea-1250">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1250">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1251">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1251">ACS</span></span>
* <span data-ttu-id="61bea-1252">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1252">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="61bea-1253">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1253">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="61bea-1254">[非推奨]`az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1254">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="61bea-1255">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="61bea-1255">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="61bea-1256">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1256">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="61bea-1257">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1257">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1258">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1258">Appservice</span></span>
* <span data-ttu-id="61bea-1259">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1259">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="61bea-1260">Botservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1260">Botservice</span></span>
* <span data-ttu-id="61bea-1261">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1261">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="61bea-1262">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1262">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="61bea-1263">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1263">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="61bea-1264">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1264">Reduced Kudu network calls</span></span>
* <span data-ttu-id="61bea-1265">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1265">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="61bea-1266">従量課金</span><span class="sxs-lookup"><span data-stu-id="61bea-1266">Consumption</span></span>
* <span data-ttu-id="61bea-1267">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1267">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-1268">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-1268">CosmosDB</span></span>
* <span data-ttu-id="61bea-1269">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1269">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="61bea-1270">マップ</span><span class="sxs-lookup"><span data-stu-id="61bea-1270">Maps</span></span>
* <span data-ttu-id="61bea-1271">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1271">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1272">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1272">Network</span></span>
* <span data-ttu-id="61bea-1273">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1273">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="61bea-1274">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1274">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-1275">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-1275">Resource</span></span>
* <span data-ttu-id="61bea-1276">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1276">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="61bea-1277">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1277">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1278">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1278">Storage</span></span>
*  <span data-ttu-id="61bea-1279">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1279">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1280">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1280">VM</span></span>
* <span data-ttu-id="61bea-1281">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1281">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="61bea-1282">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1282">December 4, 2018</span></span>

<span data-ttu-id="61bea-1283">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="61bea-1283">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="61bea-1284">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1284">Core</span></span>
* <span data-ttu-id="61bea-1285">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1285">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="61bea-1286">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1286">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1287">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1287">Appservice</span></span>
* <span data-ttu-id="61bea-1288">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1288">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="61bea-1289">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1289">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1290">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1290">Network</span></span>
* <span data-ttu-id="61bea-1291">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1291">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1292">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1292">Role</span></span>
* <span data-ttu-id="61bea-1293">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1293">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="61bea-1294">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1294">VM</span></span>
* <span data-ttu-id="61bea-1295">[非推奨]`vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1295">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="61bea-1296">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1296">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="61bea-1297">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1297">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="61bea-1298">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1298">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="61bea-1299">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1299">November 20, 2018</span></span>

<span data-ttu-id="61bea-1300">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="61bea-1300">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="61bea-1301">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1301">Core</span></span>
* <span data-ttu-id="61bea-1302">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1302">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1303">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1303">ACR</span></span>
* <span data-ttu-id="61bea-1304">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1304">Added context token to task step</span></span>
* <span data-ttu-id="61bea-1305">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1305">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="61bea-1306">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1306">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1307">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1307">Appservice</span></span>
* <span data-ttu-id="61bea-1308">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1308">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="61bea-1309">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1309">Updated the default `node_version`.</span></span> <span data-ttu-id="61bea-1310">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="61bea-1310">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="61bea-1311">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1311">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="61bea-1312">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1312">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="61bea-1313">IotCentral</span><span class="sxs-lookup"><span data-stu-id="61bea-1313">IotCentral</span></span>
* <span data-ttu-id="61bea-1314">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1314">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="61bea-1315">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61bea-1315">KeyVault</span></span>
* <span data-ttu-id="61bea-1316">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1316">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1317">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1317">Network</span></span>
* <span data-ttu-id="61bea-1318">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1318">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="61bea-1319">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1319">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="61bea-1320">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1320">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="61bea-1321">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1321">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-1322">Rdbms</span><span class="sxs-lookup"><span data-stu-id="61bea-1322">Rdbms</span></span>
* <span data-ttu-id="61bea-1323">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1323">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="61bea-1324">Rbac</span><span class="sxs-lookup"><span data-stu-id="61bea-1324">Rbac</span></span>
* <span data-ttu-id="61bea-1325">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1325">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="61bea-1326">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1326">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="61bea-1327">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1327">Storage</span></span>
* <span data-ttu-id="61bea-1328">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1328">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="61bea-1329">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1329">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="61bea-1330">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1330">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="61bea-1331">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="61bea-1331">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1332">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1332">VM</span></span>
* <span data-ttu-id="61bea-1333">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1333">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="61bea-1334">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1334">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="61bea-1335">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="61bea-1335">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="61bea-1336">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1336">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="61bea-1337">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1337">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="61bea-1338">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1338">Added `snapshot wait` command</span></span>
* <span data-ttu-id="61bea-1339">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1339">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="61bea-1340">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1340">November 6, 2018</span></span>

<span data-ttu-id="61bea-1341">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="61bea-1341">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1342">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1342">Core</span></span>
* <span data-ttu-id="61bea-1343">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1343">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1344">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1344">ACR</span></span>
* <span data-ttu-id="61bea-1345">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1345">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="61bea-1346">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1346">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1347">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1347">ACS</span></span>
* <span data-ttu-id="61bea-1348">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1348">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="61bea-1349">Advisor</span><span class="sxs-lookup"><span data-stu-id="61bea-1349">Advisor</span></span>
* <span data-ttu-id="61bea-1350">GA リリース</span><span class="sxs-lookup"><span data-stu-id="61bea-1350">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="61bea-1351">AMS</span><span class="sxs-lookup"><span data-stu-id="61bea-1351">AMS</span></span>
* <span data-ttu-id="61bea-1352">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1352">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="61bea-1353">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1353">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="61bea-1354">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1354">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="61bea-1355">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-1355">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="61bea-1356">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1356">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="61bea-1357">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1357">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="61bea-1358">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1358">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="61bea-1359">[重大な変更]`ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="61bea-1359">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="61bea-1360">[重大な変更]`ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1360">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="61bea-1361">[重大な変更]`ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1361">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="61bea-1362">[重大な変更]`ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="61bea-1362">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="61bea-1363">[重大な変更]`ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1363">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="61bea-1364">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="61bea-1364">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="61bea-1365">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="61bea-1365">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="61bea-1366">[重大な変更]`ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1366">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="61bea-1367">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1367">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="61bea-1368">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="61bea-1368">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1369">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-1369">AppService</span></span>
* <span data-ttu-id="61bea-1370">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1370">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="61bea-1371">[構成]</span><span class="sxs-lookup"><span data-stu-id="61bea-1371">Configure</span></span>
* <span data-ttu-id="61bea-1372">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1372">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1373">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1373">Container</span></span>
* <span data-ttu-id="61bea-1374">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1374">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="61bea-1375">EventHub</span><span class="sxs-lookup"><span data-stu-id="61bea-1375">EventHub</span></span>
* <span data-ttu-id="61bea-1376">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1376">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-1377">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-1377">Interactive</span></span>
* <span data-ttu-id="61bea-1378">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="61bea-1378">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-1379">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-1379">Monitor</span></span>
* <span data-ttu-id="61bea-1380">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-1380">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1381">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1381">Network</span></span>
* <span data-ttu-id="61bea-1382">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1382">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="61bea-1383">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1383">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="61bea-1384">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1384">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="61bea-1385">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-1385">Profile</span></span>
* <span data-ttu-id="61bea-1386">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1386">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-1387">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61bea-1387">RDBMS</span></span>
* <span data-ttu-id="61bea-1388">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1388">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-1389">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-1389">Resource</span></span>
* <span data-ttu-id="61bea-1390">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1390">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1391">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1391">Role</span></span>
* <span data-ttu-id="61bea-1392">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-1392">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="61bea-1393">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1393">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="61bea-1394">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1394">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1395">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1395">Storage</span></span>
* <span data-ttu-id="61bea-1396">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="61bea-1396">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1397">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1397">VM</span></span>
* <span data-ttu-id="61bea-1398">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1398">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="61bea-1399">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1399">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="61bea-1400">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1400">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="61bea-1401">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1401">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="61bea-1402">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="61bea-1402">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="61bea-1403">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1403">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="61bea-1404">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1404">October 23, 2018</span></span>

<span data-ttu-id="61bea-1405">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="61bea-1405">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1406">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1406">Core</span></span>
* <span data-ttu-id="61bea-1407">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1407">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="61bea-1408">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1408">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1409">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1409">ACR</span></span>
* <span data-ttu-id="61bea-1410">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1410">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="61bea-1411">CDN</span><span class="sxs-lookup"><span data-stu-id="61bea-1411">CDN</span></span>
* <span data-ttu-id="61bea-1412">[重大な変更]`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1412">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="61bea-1413">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-1413">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1414">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1414">Container</span></span>
* <span data-ttu-id="61bea-1415">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1415">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="61bea-1416">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1416">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="61bea-1417">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1417">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="61bea-1418">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1418">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="61bea-1419">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1419">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="61bea-1420">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1420">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="61bea-1421">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1421">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-1422">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-1422">CosmosDB</span></span>
* <span data-ttu-id="61bea-1423">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1423">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-1424">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-1424">Interactive</span></span>
* <span data-ttu-id="61bea-1425">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1425">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="61bea-1426">IoT Central</span><span class="sxs-lookup"><span data-stu-id="61bea-1426">IoT Central</span></span>
* <span data-ttu-id="61bea-1427">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1427">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="61bea-1428">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-1428">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-1429">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-1429">Monitor</span></span>
* <span data-ttu-id="61bea-1430">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="61bea-1430">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="61bea-1431">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1431">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="61bea-1432">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1432">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="61bea-1433">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1433">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="61bea-1434">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1434">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="61bea-1435">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1435">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="61bea-1436">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="61bea-1436">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="61bea-1437">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1437">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="61bea-1438">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1438">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="61bea-1439">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1439">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1440">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1440">Network</span></span>
* <span data-ttu-id="61bea-1441">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1441">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="61bea-1442">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1442">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="61bea-1443">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="61bea-1443">ServiceBus</span></span>
* <span data-ttu-id="61bea-1444">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1444">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-1445">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-1445">SQL</span></span>
* <span data-ttu-id="61bea-1446">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1446">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1447">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1447">Storage</span></span>
* <span data-ttu-id="61bea-1448">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1448">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="61bea-1449">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1449">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1450">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1450">VM</span></span>
* <span data-ttu-id="61bea-1451">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="61bea-1451">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="61bea-1452">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1452">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="61bea-1453">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1453">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="61bea-1454">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1454">October 16, 2018</span></span>

<span data-ttu-id="61bea-1455">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="61bea-1455">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1456">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1456">VM</span></span>
* <span data-ttu-id="61bea-1457">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1457">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="61bea-1458">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1458">October 9, 2018</span></span>

<span data-ttu-id="61bea-1459">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="61bea-1459">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1460">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1460">Core</span></span>
* <span data-ttu-id="61bea-1461">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1461">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1462">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1462">ACR</span></span>
* <span data-ttu-id="61bea-1463">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1463">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1464">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1464">ACS</span></span>
* <span data-ttu-id="61bea-1465">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="61bea-1465">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="61bea-1466">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1466">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="61bea-1467">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1467">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="61bea-1468">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1468">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1469">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1469">Container</span></span>
* <span data-ttu-id="61bea-1470">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1470">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="61bea-1471">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1471">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="61bea-1472">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="61bea-1472">Event Hub</span></span>
* <span data-ttu-id="61bea-1473">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1473">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="61bea-1474">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1474">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="61bea-1475">拡張機能</span><span class="sxs-lookup"><span data-stu-id="61bea-1475">Extensions</span></span>
* <span data-ttu-id="61bea-1476">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1476">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="61bea-1477">HDInsight</span><span class="sxs-lookup"><span data-stu-id="61bea-1477">HDInsight</span></span>
* <span data-ttu-id="61bea-1478">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-1478">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-1479">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-1479">IoT</span></span>
* <span data-ttu-id="61bea-1480">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1480">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="61bea-1481">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61bea-1481">KeyVault</span></span>
* <span data-ttu-id="61bea-1482">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1482">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1483">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1483">Network</span></span>
* <span data-ttu-id="61bea-1484">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="61bea-1484">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="61bea-1485">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="61bea-1485">See #6052</span></span>
* <span data-ttu-id="61bea-1486">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1486">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="61bea-1487">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="61bea-1487">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="61bea-1488">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1488">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="61bea-1489">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1489">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="61bea-1490">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1490">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="61bea-1491">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1491">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1492">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1492">Role</span></span>
* <span data-ttu-id="61bea-1493">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1493">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="61bea-1494">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1494">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="61bea-1495">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1495">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="61bea-1496">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1496">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="61bea-1497">Service Bus</span><span class="sxs-lookup"><span data-stu-id="61bea-1497">Service Bus</span></span>
* <span data-ttu-id="61bea-1498">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1498">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1499">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1499">VM</span></span>
* <span data-ttu-id="61bea-1500">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1500">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="61bea-1501">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1501">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="61bea-1502">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1502">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="61bea-1503">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1503">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="61bea-1504">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1504">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="61bea-1505">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1505">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="61bea-1506">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1506">September 21, 2018</span></span>

<span data-ttu-id="61bea-1507">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="61bea-1507">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1508">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1508">ACR</span></span>
* <span data-ttu-id="61bea-1509">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1509">Added ACR Task commands</span></span>
* <span data-ttu-id="61bea-1510">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1510">Added quick run command</span></span>
* <span data-ttu-id="61bea-1511">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1511">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="61bea-1512">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1512">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="61bea-1513">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1513">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="61bea-1514">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1514">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1515">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1515">ACS</span></span>
* <span data-ttu-id="61bea-1516">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1516">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="61bea-1517">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1517">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1518">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-1518">AppService</span></span>

* <span data-ttu-id="61bea-1519">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1519">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="61bea-1520">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1520">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="61bea-1521">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1521">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="61bea-1522">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1522">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-1523">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-1523">Batch</span></span>
* <span data-ttu-id="61bea-1524">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1524">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="61bea-1525">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1525">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="61bea-1526">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1526">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="61bea-1527">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1527">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="61bea-1528">Batch AI</span><span class="sxs-lookup"><span data-stu-id="61bea-1528">Batch AI</span></span> 
* <span data-ttu-id="61bea-1529">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1529">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="61bea-1530">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="61bea-1530">Cognitive Services</span></span>
* <span data-ttu-id="61bea-1531">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1531">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="61bea-1532">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1532">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="61bea-1533">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1533">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="61bea-1534">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1534">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="61bea-1535">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1535">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="61bea-1536">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1536">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1537">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1537">Container</span></span>
* <span data-ttu-id="61bea-1538">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1538">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="61bea-1539">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1539">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="61bea-1540">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1540">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="61bea-1541">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1541">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="61bea-1542">DataLake</span><span class="sxs-lookup"><span data-stu-id="61bea-1542">Datalake</span></span>
* <span data-ttu-id="61bea-1543">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1543">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="61bea-1544">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="61bea-1544">Interactive Shell</span></span>
* <span data-ttu-id="61bea-1545">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1545">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="61bea-1546">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1546">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-1547">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-1547">IoT</span></span>
* <span data-ttu-id="61bea-1548">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1548">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="61bea-1549">Key Vault</span><span class="sxs-lookup"><span data-stu-id="61bea-1549">Key Vault</span></span>
* <span data-ttu-id="61bea-1550">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1550">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1551">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1551">Network</span></span>
* <span data-ttu-id="61bea-1552">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1552">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="61bea-1553">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1553">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="61bea-1554">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1554">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="61bea-1555">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1555">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="61bea-1556">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1556">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="61bea-1557">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1557">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="61bea-1558">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1558">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="61bea-1559">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-1559">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="61bea-1560">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1560">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="61bea-1561">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1561">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="61bea-1562">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1562">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="61bea-1563">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1563">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="61bea-1564">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1564">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="61bea-1565">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="61bea-1565">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="61bea-1566">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1566">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="61bea-1567">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1567">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="61bea-1568">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1568">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="61bea-1569">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1569">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-1570">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61bea-1570">RDBMS</span></span>
* <span data-ttu-id="61bea-1571">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1571">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="61bea-1572">予約</span><span class="sxs-lookup"><span data-stu-id="61bea-1572">Reservation</span></span>
* <span data-ttu-id="61bea-1573">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1573">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="61bea-1574">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1574">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="61bea-1575">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="61bea-1575">Manage App</span></span>
* <span data-ttu-id="61bea-1576">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1576">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="61bea-1577">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1577">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1578">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1578">Role</span></span>
* <span data-ttu-id="61bea-1579">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1579">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="61bea-1580">SignalR</span><span class="sxs-lookup"><span data-stu-id="61bea-1580">SignalR</span></span>
* <span data-ttu-id="61bea-1581">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-1581">First release</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1582">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1582">Storage</span></span>
* <span data-ttu-id="61bea-1583">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1583">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="61bea-1584">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1584">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1585">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1585">VM</span></span>
* <span data-ttu-id="61bea-1586">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="61bea-1586">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="61bea-1587">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1587">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="61bea-1588">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1588">August 28, 2018</span></span>

<span data-ttu-id="61bea-1589">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="61bea-1589">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1590">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1590">Core</span></span>

* <span data-ttu-id="61bea-1591">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1591">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="61bea-1592">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1592">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1593">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1593">ACR</span></span>

* <span data-ttu-id="61bea-1594">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1594">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="61bea-1595">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1595">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1596">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1596">ACS</span></span>

* <span data-ttu-id="61bea-1597">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1597">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="61bea-1598">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1598">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1599">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-1599">AppService</span></span>

* <span data-ttu-id="61bea-1600">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1600">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="61bea-1601">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1601">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="61bea-1602">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1602">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="61bea-1603">バックアップ</span><span class="sxs-lookup"><span data-stu-id="61bea-1603">Backup</span></span>

* <span data-ttu-id="61bea-1604">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1604">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="61bea-1605">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="61bea-1605">Bot Service</span></span>

* <span data-ttu-id="61bea-1606">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="61bea-1606">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="61bea-1607">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="61bea-1607">Cognitive Services</span></span>

* <span data-ttu-id="61bea-1608">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1608">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-1609">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-1609">IoT</span></span>

* <span data-ttu-id="61bea-1610">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1610">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-1611">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-1611">Monitor</span></span>

* <span data-ttu-id="61bea-1612">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1612">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="61bea-1613">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1613">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1614">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1614">Network</span></span>

* <span data-ttu-id="61bea-1615">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1615">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-1616">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-1616">Resource</span></span>

* <span data-ttu-id="61bea-1617">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1617">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1618">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1618">Storage</span></span>

* <span data-ttu-id="61bea-1619">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1619">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1620">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1620">VM</span></span>

* <span data-ttu-id="61bea-1621">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1621">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="61bea-1622">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1622">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="61bea-1623">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1623">Auguest 14, 2018</span></span>

<span data-ttu-id="61bea-1624">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="61bea-1624">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1625">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1625">Core</span></span>

* <span data-ttu-id="61bea-1626">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1626">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="61bea-1627">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1627">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="61bea-1628">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="61bea-1628">Telemetry</span></span>

* <span data-ttu-id="61bea-1629">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1629">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1630">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1630">ACR</span></span>

* <span data-ttu-id="61bea-1631">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1631">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="61bea-1632">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1632">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1633">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1633">ACS</span></span>

* <span data-ttu-id="61bea-1634">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1634">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="61bea-1635">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1635">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="61bea-1636">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1636">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="61bea-1637">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1637">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="61bea-1638">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1638">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="61bea-1639">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-1639">AppService</span></span>

* <span data-ttu-id="61bea-1640">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1640">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="61bea-1641">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1641">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="61bea-1642">BatchAI</span><span class="sxs-lookup"><span data-stu-id="61bea-1642">BatchAI</span></span>

* <span data-ttu-id="61bea-1643">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1643">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="61bea-1644">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1644">Container</span></span>

* <span data-ttu-id="61bea-1645">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1645">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="61bea-1646">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-1646">IoT</span></span>

* <span data-ttu-id="61bea-1647">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1647">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="61bea-1648">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1648">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="61bea-1649">Iot Central</span><span class="sxs-lookup"><span data-stu-id="61bea-1649">Iot Central</span></span>

* <span data-ttu-id="61bea-1650">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-1650">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="61bea-1651">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61bea-1651">KeyVault</span></span>


* <span data-ttu-id="61bea-1652">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1652">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="61bea-1653">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1653">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="61bea-1654">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1654">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="61bea-1655">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1655">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="61bea-1656">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1656">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="61bea-1657">リレー</span><span class="sxs-lookup"><span data-stu-id="61bea-1657">Relay</span></span>

* <span data-ttu-id="61bea-1658">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-1658">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-1659">Sql</span><span class="sxs-lookup"><span data-stu-id="61bea-1659">Sql</span></span>

* <span data-ttu-id="61bea-1660">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1660">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1661">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1661">Storage</span></span>

* <span data-ttu-id="61bea-1662">[重大な変更]`--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="61bea-1662">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="61bea-1663">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1663">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="61bea-1664">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1664">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="61bea-1665">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1665">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="61bea-1666">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1666">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1667">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1667">VM</span></span>

* <span data-ttu-id="61bea-1668">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1668">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="61bea-1669">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="61bea-1669">July 31, 2018</span></span>

<span data-ttu-id="61bea-1670">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="61bea-1670">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1671">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1671">ACR</span></span>

* <span data-ttu-id="61bea-1672">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1672">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="61bea-1673">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1673">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1674">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1674">ACS</span></span>

* <span data-ttu-id="61bea-1675">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1675">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-1676">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-1676">Batch</span></span>

* <span data-ttu-id="61bea-1677">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1677">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1678">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1678">Container</span></span>

* <span data-ttu-id="61bea-1679">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1679">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1680">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1680">Network</span></span>

* <span data-ttu-id="61bea-1681">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1681">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="61bea-1682">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-1682">Resource</span></span>

* <span data-ttu-id="61bea-1683">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1683">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="61bea-1684">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1684">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1685">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1685">Role</span></span>

* <span data-ttu-id="61bea-1686">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1686">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="61bea-1687">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1687">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="61bea-1688">検索</span><span class="sxs-lookup"><span data-stu-id="61bea-1688">Search</span></span>

* <span data-ttu-id="61bea-1689">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1689">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="61bea-1690">Service Bus</span><span class="sxs-lookup"><span data-stu-id="61bea-1690">Service Bus</span></span>

* <span data-ttu-id="61bea-1691">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1691">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="61bea-1692">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1692">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="61bea-1693">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="61bea-1693">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="61bea-1694">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="61bea-1694">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1695">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1695">Storage</span></span>

* <span data-ttu-id="61bea-1696">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-1696">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="61bea-1697">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1697">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1698">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1698">VM</span></span>

* <span data-ttu-id="61bea-1699">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-1699">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="61bea-1700">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1700">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="61bea-1701">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1701">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="61bea-1702">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1702">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="61bea-1703">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1703">July 18, 2018</span></span>

<span data-ttu-id="61bea-1704">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="61bea-1704">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1705">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1705">Core</span></span>

* <span data-ttu-id="61bea-1706">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1706">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="61bea-1707">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1707">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="61bea-1708">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1708">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1709">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1709">ACR</span></span>

* <span data-ttu-id="61bea-1710">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1710">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="61bea-1711">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1711">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="61bea-1712">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1712">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="61bea-1713">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1713">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1714">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1714">ACS</span></span>

* <span data-ttu-id="61bea-1715">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1715">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1716">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-1716">AppService</span></span>

* <span data-ttu-id="61bea-1717">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1717">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-1718">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-1718">Batch</span></span>

* <span data-ttu-id="61bea-1719">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1719">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="61bea-1720">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1720">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="61bea-1721">Batch AI</span><span class="sxs-lookup"><span data-stu-id="61bea-1721">Batch AI</span></span>

* <span data-ttu-id="61bea-1722">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1722">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1723">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1723">Container</span></span>

* <span data-ttu-id="61bea-1724">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1724">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="61bea-1725">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1725">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1726">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1726">Network</span></span>

* <span data-ttu-id="61bea-1727">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1727">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="61bea-1728">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1728">Added `network nic wait`</span></span>
* <span data-ttu-id="61bea-1729">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1729">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="61bea-1730">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1730">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="61bea-1731">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-1731">Resource</span></span>

* <span data-ttu-id="61bea-1732">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1732">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="61bea-1733">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1733">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="61bea-1734">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1734">Added `deployment wait` command</span></span>
* <span data-ttu-id="61bea-1735">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1735">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-1736">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-1736">SQL</span></span>

* <span data-ttu-id="61bea-1737">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1737">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="61bea-1738">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-1738">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="61bea-1739">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1739">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1740">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1740">Storage</span></span>

* <span data-ttu-id="61bea-1741">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1741">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1742">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1742">VM</span></span>

* <span data-ttu-id="61bea-1743">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1743">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="61bea-1744">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1744">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="61bea-1745">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1745">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="61bea-1746">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1746">July 3, 2018</span></span>

<span data-ttu-id="61bea-1747">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="61bea-1747">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="61bea-1748">AKS</span><span class="sxs-lookup"><span data-stu-id="61bea-1748">AKS</span></span>

* <span data-ttu-id="61bea-1749">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1749">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="61bea-1750">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1750">July 3, 2018</span></span>

<span data-ttu-id="61bea-1751">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="61bea-1751">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1752">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1752">Core</span></span>

* <span data-ttu-id="61bea-1753">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1753">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1754">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1754">ACR</span></span>

* <span data-ttu-id="61bea-1755">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1755">Added polling build status</span></span>
* <span data-ttu-id="61bea-1756">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1756">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="61bea-1757">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1757">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1758">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1758">ACS</span></span>

* <span data-ttu-id="61bea-1759">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1759">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="61bea-1760">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1760">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="61bea-1761">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1761">Updated options for `aks browse` command.</span></span> <span data-ttu-id="61bea-1762">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1762">Added `--listen-port` support</span></span>
* <span data-ttu-id="61bea-1763">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1763">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="61bea-1764">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-1764">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="61bea-1765">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1765">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1766">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-1766">AppService</span></span>

* <span data-ttu-id="61bea-1767">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-1767">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="61bea-1768">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1768">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="61bea-1769">バックアップ</span><span class="sxs-lookup"><span data-stu-id="61bea-1769">Backup</span></span>

* <span data-ttu-id="61bea-1770">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1770">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="61bea-1771">BatchAI</span><span class="sxs-lookup"><span data-stu-id="61bea-1771">BatchAI</span></span>

* <span data-ttu-id="61bea-1772">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1772">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="61bea-1773">クラウド</span><span class="sxs-lookup"><span data-stu-id="61bea-1773">Cloud</span></span>

* <span data-ttu-id="61bea-1774">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1774">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1775">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1775">Container</span></span>

* <span data-ttu-id="61bea-1776">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1776">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="61bea-1777">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1777">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="61bea-1778">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1778">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="61bea-1779">拡張機能</span><span class="sxs-lookup"><span data-stu-id="61bea-1779">Extension</span></span>

* <span data-ttu-id="61bea-1780">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1780">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1781">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1781">Network</span></span>

* <span data-ttu-id="61bea-1782">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1782">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-1783">Rdbms</span><span class="sxs-lookup"><span data-stu-id="61bea-1783">Rdbms</span></span>

* <span data-ttu-id="61bea-1784">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1784">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-1785">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-1785">Resource</span></span>

* <span data-ttu-id="61bea-1786">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1786">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1787">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1787">VM</span></span>

* <span data-ttu-id="61bea-1788">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-1788">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="61bea-1789">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1789">June 25, 2018</span></span>

<span data-ttu-id="61bea-1790">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="61bea-1790">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="61bea-1791">CLI</span><span class="sxs-lookup"><span data-stu-id="61bea-1791">CLI</span></span>

* <span data-ttu-id="61bea-1792">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1792">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="61bea-1793">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1793">June 19, 2018</span></span>

<span data-ttu-id="61bea-1794">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="61bea-1794">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1795">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1795">Core</span></span>

* <span data-ttu-id="61bea-1796">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1796">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1797">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1797">ACR</span></span>

* <span data-ttu-id="61bea-1798">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1798">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="61bea-1799">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1799">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1800">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1800">ACS</span></span>

* <span data-ttu-id="61bea-1801">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1801">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="61bea-1802">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1802">Added `--update` support</span></span>
* <span data-ttu-id="61bea-1803">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1803">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="61bea-1804">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1804">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="61bea-1805">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1805">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="61bea-1806">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1806">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="61bea-1807">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1807">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="61bea-1808">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1808">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1809">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-1809">AppService</span></span>

* <span data-ttu-id="61bea-1810">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1810">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="61bea-1811">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1811">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-1812">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-1812">Batch</span></span>

* <span data-ttu-id="61bea-1813">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1813">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="61bea-1814">Batch AI</span><span class="sxs-lookup"><span data-stu-id="61bea-1814">Batch AI</span></span>

* <span data-ttu-id="61bea-1815">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1815">Added support for workspaces.</span></span> <span data-ttu-id="61bea-1816">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="61bea-1816">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="61bea-1817">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1817">Added support for experiments.</span></span> <span data-ttu-id="61bea-1818">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="61bea-1818">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="61bea-1819">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1819">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="61bea-1820">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1820">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="61bea-1821">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="61bea-1821">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="61bea-1822">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1822">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="61bea-1823">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="61bea-1823">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="61bea-1824">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="61bea-1824">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="61bea-1825">[重大な変更]`--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1825">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="61bea-1826">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="61bea-1826">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="61bea-1827">[重大な変更]`--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1827">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="61bea-1828">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="61bea-1828">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="61bea-1829">[重大な変更]`location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1829">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="61bea-1830">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="61bea-1830">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="61bea-1831">[重大な変更]`--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1831">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="61bea-1832">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1832">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="61bea-1833">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1833">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="61bea-1834">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1834">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="61bea-1835">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1835">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="61bea-1836">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1836">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="61bea-1837">マップ</span><span class="sxs-lookup"><span data-stu-id="61bea-1837">Maps</span></span>

* <span data-ttu-id="61bea-1838">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1838">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1839">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1839">Network</span></span>

* <span data-ttu-id="61bea-1840">`https` のサポートを `network lb probe create` に追加しました ([#6571](https://github.com/Azure/azure-cli/issues/6571))</span><span class="sxs-lookup"><span data-stu-id="61bea-1840">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="61bea-1841">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1841">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="61bea-1842">#6502</span><span class="sxs-lookup"><span data-stu-id="61bea-1842">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="61bea-1843">Reservations</span><span class="sxs-lookup"><span data-stu-id="61bea-1843">Reservations</span></span>

* <span data-ttu-id="61bea-1844">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1844">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="61bea-1845">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1845">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="61bea-1846">[重大な変更]`kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1846">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="61bea-1847">[重大な変更]`Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1847">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="61bea-1848">[重大な変更]`Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1848">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="61bea-1849">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1849">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="61bea-1850">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-1850">Role</span></span>

* <span data-ttu-id="61bea-1851">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1851">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-1852">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-1852">SQL</span></span>

* <span data-ttu-id="61bea-1853">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1853">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1854">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1854">Storage</span></span>

* <span data-ttu-id="61bea-1855">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1855">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1856">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1856">VM</span></span>

* <span data-ttu-id="61bea-1857">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1857">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="61bea-1858">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1858">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="61bea-1859">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1859">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="61bea-1860">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1860">June 13, 2018</span></span>

<span data-ttu-id="61bea-1861">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="61bea-1861">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1862">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1862">Core</span></span>

* <span data-ttu-id="61bea-1863">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1863">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="61bea-1864">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1864">June 13, 2018</span></span>

<span data-ttu-id="61bea-1865">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="61bea-1865">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="61bea-1866">AKS</span><span class="sxs-lookup"><span data-stu-id="61bea-1866">AKS</span></span>

* <span data-ttu-id="61bea-1867">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1867">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="61bea-1868">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-1868">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="61bea-1869">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1869">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="61bea-1870">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1870">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="61bea-1871">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1871">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1872">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-1872">AppService</span></span>

* <span data-ttu-id="61bea-1873">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1873">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="61bea-1874">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1874">June 5, 2018</span></span>

<span data-ttu-id="61bea-1875">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="61bea-1875">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-1876">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-1876">Interactive</span></span>

* <span data-ttu-id="61bea-1877">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1877">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="61bea-1878">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1878">June 5, 2018</span></span>

<span data-ttu-id="61bea-1879">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="61bea-1879">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1880">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1880">Core</span></span>

* <span data-ttu-id="61bea-1881">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1881">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="61bea-1882">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1882">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1883">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1883">ACR</span></span>

* <span data-ttu-id="61bea-1884">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1884">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="61bea-1885">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1885">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="61bea-1886">AKS</span><span class="sxs-lookup"><span data-stu-id="61bea-1886">AKS</span></span>

* <span data-ttu-id="61bea-1887">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1887">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-1888">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-1888">Batch</span></span>

* <span data-ttu-id="61bea-1889">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1889">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-1890">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-1890">IOT</span></span>

* <span data-ttu-id="61bea-1891">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1891">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1892">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1892">Network</span></span>

* <span data-ttu-id="61bea-1893">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1893">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="61bea-1894">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="61bea-1894">Policy Insights</span></span>

* <span data-ttu-id="61bea-1895">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-1895">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="61bea-1896">ARM</span><span class="sxs-lookup"><span data-stu-id="61bea-1896">ARM</span></span>

* <span data-ttu-id="61bea-1897">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1897">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-1898">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-1898">SQL</span></span>

* <span data-ttu-id="61bea-1899">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1899">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="61bea-1900">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1900">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="61bea-1901">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1901">Storage</span></span>

* <span data-ttu-id="61bea-1902">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1902">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1903">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1903">VM</span></span>

* <span data-ttu-id="61bea-1904">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1904">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="61bea-1905">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1905">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="61bea-1906">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1906">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="61bea-1907">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1907">May 22, 2018</span></span>

<span data-ttu-id="61bea-1908">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="61bea-1908">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1909">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1909">Core</span></span>

* <span data-ttu-id="61bea-1910">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1910">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1911">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1911">ACS</span></span>

* <span data-ttu-id="61bea-1912">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1912">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="61bea-1913">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1913">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1914">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-1914">AppService</span></span>

* <span data-ttu-id="61bea-1915">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1915">Improved generic update commands</span></span>
* <span data-ttu-id="61bea-1916">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1916">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1917">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1917">Container</span></span>

* <span data-ttu-id="61bea-1918">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1918">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="61bea-1919">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1919">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="61bea-1920">拡張機能</span><span class="sxs-lookup"><span data-stu-id="61bea-1920">Extension</span></span>

* <span data-ttu-id="61bea-1921">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1921">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-1922">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-1922">Interactive</span></span>

* <span data-ttu-id="61bea-1923">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1923">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="61bea-1924">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1924">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="61bea-1925">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61bea-1925">KeyVault</span></span>

* <span data-ttu-id="61bea-1926">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1926">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="61bea-1927">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-1927">Network</span></span>

* <span data-ttu-id="61bea-1928">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1928">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="61bea-1929">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1929">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-1930">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-1930">SQL</span></span>

* <span data-ttu-id="61bea-1931">[重大な変更]`db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1931">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="61bea-1932">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1932">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="61bea-1933">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1933">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="61bea-1934">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1934">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="61bea-1935">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1935">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="61bea-1936">[https://login.microsoftonline.com/consumers/](`requestedServiceObjectiveName`)</span><span class="sxs-lookup"><span data-stu-id="61bea-1936">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="61bea-1937">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="61bea-1937">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="61bea-1938">[https://login.microsoftonline.com/consumers/](`edition`)</span><span class="sxs-lookup"><span data-stu-id="61bea-1938">`edition`.</span></span> <span data-ttu-id="61bea-1939">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="61bea-1939">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="61bea-1940">[https://login.microsoftonline.com/consumers/](`elasticPoolName`)</span><span class="sxs-lookup"><span data-stu-id="61bea-1940">`elasticPoolName`.</span></span> <span data-ttu-id="61bea-1941">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="61bea-1941">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="61bea-1942">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1942">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="61bea-1943">[https://login.microsoftonline.com/consumers/](`edition`)</span><span class="sxs-lookup"><span data-stu-id="61bea-1943">`edition`.</span></span> <span data-ttu-id="61bea-1944">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-1944">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="61bea-1945">[https://login.microsoftonline.com/consumers/](`dtu`)</span><span class="sxs-lookup"><span data-stu-id="61bea-1945">`dtu`.</span></span> <span data-ttu-id="61bea-1946">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-1946">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="61bea-1947">[https://login.microsoftonline.com/consumers/](`databaseDtuMin`)</span><span class="sxs-lookup"><span data-stu-id="61bea-1947">`databaseDtuMin`.</span></span> <span data-ttu-id="61bea-1948">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-1948">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="61bea-1949">[https://login.microsoftonline.com/consumers/](`databaseDtuMax`)</span><span class="sxs-lookup"><span data-stu-id="61bea-1949">`databaseDtuMax`.</span></span> <span data-ttu-id="61bea-1950">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-1950">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="61bea-1951">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1951">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="61bea-1952">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1952">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-1953">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-1953">Storage</span></span>

* <span data-ttu-id="61bea-1954">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1954">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="61bea-1955">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1955">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-1956">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-1956">VM</span></span>

* <span data-ttu-id="61bea-1957">[重大な変更]`--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1957">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="61bea-1958">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="61bea-1958">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="61bea-1959">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1959">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="61bea-1960">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1960">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="61bea-1961">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1961">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="61bea-1962">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="61bea-1962">May 7, 2018</span></span>

<span data-ttu-id="61bea-1963">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="61bea-1963">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="61bea-1964">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-1964">Core</span></span>

* <span data-ttu-id="61bea-1965">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1965">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="61bea-1966">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1966">Added limited support for positional arguments</span></span>
* <span data-ttu-id="61bea-1967">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1967">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="61bea-1968">#5591</span><span class="sxs-lookup"><span data-stu-id="61bea-1968">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="61bea-1969">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-1969">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="61bea-1970">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="61bea-1970">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="61bea-1971">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1971">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="61bea-1972">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1972">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="61bea-1973">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1973">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-1974">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-1974">ACR</span></span>

* <span data-ttu-id="61bea-1975">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1975">Added ACR Build commands</span></span>
* <span data-ttu-id="61bea-1976">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1976">Improved resource not found error messages</span></span>
* <span data-ttu-id="61bea-1977">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1977">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="61bea-1978">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1978">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="61bea-1979">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1979">Improved repository commands error messages</span></span>
* <span data-ttu-id="61bea-1980">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1980">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-1981">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-1981">ACS</span></span>

* <span data-ttu-id="61bea-1982">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1982">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="61bea-1983">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1983">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="61bea-1984">AMS</span><span class="sxs-lookup"><span data-stu-id="61bea-1984">AMS</span></span>

* <span data-ttu-id="61bea-1985">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="61bea-1985">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-1986">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-1986">Appservice</span></span>

* <span data-ttu-id="61bea-1987">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1987">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="61bea-1988">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1988">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="61bea-1989">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1989">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="61bea-1990">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1990">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="61bea-1991">Batch AI</span><span class="sxs-lookup"><span data-stu-id="61bea-1991">Batch AI</span></span>

* <span data-ttu-id="61bea-1992">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1992">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="61bea-1993">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="61bea-1993">Cognitive Services</span></span>

* <span data-ttu-id="61bea-1994">`cognitiveservices account create` の例の誤りを修正しました ([#5603](https://github.com/Azure/azure-cli/issues/5603))</span><span class="sxs-lookup"><span data-stu-id="61bea-1994">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="61bea-1995">従量課金</span><span class="sxs-lookup"><span data-stu-id="61bea-1995">Consumption</span></span>

* <span data-ttu-id="61bea-1996">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1996">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="61bea-1997">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-1997">Container</span></span>

* <span data-ttu-id="61bea-1998">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-1998">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="61bea-1999">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-1999">Cosmos DB</span></span>

* <span data-ttu-id="61bea-2000">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2000">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="61bea-2001">DMS</span><span class="sxs-lookup"><span data-stu-id="61bea-2001">DMS</span></span>

* <span data-ttu-id="61bea-2002">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2002">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="61bea-2003">拡張機能</span><span class="sxs-lookup"><span data-stu-id="61bea-2003">Extension</span></span>

* <span data-ttu-id="61bea-2004">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2004">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-2005">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-2005">Interactive</span></span>

* <span data-ttu-id="61bea-2006">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2006">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="61bea-2007">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2007">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="61bea-2008">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2008">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="61bea-2009">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2009">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="61bea-2010">ラボ</span><span class="sxs-lookup"><span data-stu-id="61bea-2010">Lab</span></span>

* <span data-ttu-id="61bea-2011">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2011">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2012">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2012">Network</span></span>

* <span data-ttu-id="61bea-2013">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2013">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="61bea-2014">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-2014">Profile</span></span>

* <span data-ttu-id="61bea-2015">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2015">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="61bea-2016">[重大な変更]`--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2016">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="61bea-2017">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2017">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="61bea-2018">Redis</span><span class="sxs-lookup"><span data-stu-id="61bea-2018">Redis</span></span>

* <span data-ttu-id="61bea-2019">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2019">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="61bea-2020">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2020">Deprecated `redis list-all`.</span></span> <span data-ttu-id="61bea-2021">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="61bea-2021">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="61bea-2022">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2022">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="61bea-2023">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2023">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="61bea-2024">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-2024">Role</span></span>

* <span data-ttu-id="61bea-2025">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2025">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2026">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2026">Storage</span></span>

* <span data-ttu-id="61bea-2027">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="61bea-2027">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="61bea-2028">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2028">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="61bea-2029">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="61bea-2029">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="61bea-2030">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="61bea-2030">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="61bea-2031">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2031">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2032">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2032">VM</span></span>

* <span data-ttu-id="61bea-2033">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2033">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="61bea-2034">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2034">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="61bea-2035">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="61bea-2035">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="61bea-2036">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2036">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="61bea-2037">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2037">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="61bea-2038">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2038">Added write accelerator support</span></span>
* <span data-ttu-id="61bea-2039">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2039">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="61bea-2040">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2040">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="61bea-2041">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2041">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="61bea-2042">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2042">April 10, 2018</span></span>

<span data-ttu-id="61bea-2043">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="61bea-2043">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-2044">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-2044">ACR</span></span>

* <span data-ttu-id="61bea-2045">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2045">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2046">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2046">ACS</span></span>

* <span data-ttu-id="61bea-2047">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2047">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2048">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2048">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="61bea-2050">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2050">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="61bea-2051">BatchAI</span><span class="sxs-lookup"><span data-stu-id="61bea-2051">BatchAI</span></span>

* <span data-ttu-id="61bea-2052">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2052">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="61bea-2053">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="61bea-2053">Job level mounting</span></span>
  - <span data-ttu-id="61bea-2054">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="61bea-2054">Environment variables with secret values</span></span>
  - <span data-ttu-id="61bea-2055">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="61bea-2055">Performance counters settings</span></span>
  - <span data-ttu-id="61bea-2056">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="61bea-2056">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="61bea-2057">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="61bea-2057">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="61bea-2058">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="61bea-2058">Usage and limits reporting</span></span>
  - <span data-ttu-id="61bea-2059">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="61bea-2059">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="61bea-2060">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="61bea-2060">Support for custom images</span></span>
  - <span data-ttu-id="61bea-2061">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2061">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="61bea-2062">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2062">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="61bea-2063">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="61bea-2063">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="61bea-2064">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="61bea-2064">National clouds are supported</span></span>
* <span data-ttu-id="61bea-2065">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2065">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="61bea-2066">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2066">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="61bea-2067">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2067">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="61bea-2068">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2068">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="61bea-2069">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="61bea-2069">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="61bea-2070">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="61bea-2070">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="61bea-2071">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2071">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="61bea-2072">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2072">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="61bea-2073">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="61bea-2073">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="61bea-2074">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2074">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="61bea-2075">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2075">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="61bea-2076">[重大な変更]`job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2076">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="61bea-2077">[重大な変更]`cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2077">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="61bea-2078">課金</span><span class="sxs-lookup"><span data-stu-id="61bea-2078">Billing</span></span>

* <span data-ttu-id="61bea-2079">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2079">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="61bea-2080">従量課金</span><span class="sxs-lookup"><span data-stu-id="61bea-2080">Consumption</span></span>

* <span data-ttu-id="61bea-2081">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2081">Added `marketplace` commands</span></span>
* <span data-ttu-id="61bea-2082">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2082">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="61bea-2083">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2083">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="61bea-2084">[重大な変更]`reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2084">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="61bea-2085">[重大な変更]`reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2085">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="61bea-2086">[重大な変更]`pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2086">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="61bea-2087">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-2087">Container</span></span>

* <span data-ttu-id="61bea-2088">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2088">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="61bea-2089">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2089">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="61bea-2090">拡張機能</span><span class="sxs-lookup"><span data-stu-id="61bea-2090">Extension</span></span>

* <span data-ttu-id="61bea-2091">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2091">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-2092">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-2092">Interactive</span></span>

* <span data-ttu-id="61bea-2093">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2093">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="61bea-2094">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2094">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="61bea-2095">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2095">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2096">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2096">Network</span></span>

* <span data-ttu-id="61bea-2097">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2097">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="61bea-2098">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2098">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="61bea-2099">#4910</span><span class="sxs-lookup"><span data-stu-id="61bea-2099">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="61bea-2100">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2100">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="61bea-2101">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="61bea-2101">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="61bea-2102">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2102">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="61bea-2103">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2103">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="61bea-2104">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2104">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-2105">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-2105">Profile</span></span>

* <span data-ttu-id="61bea-2106">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2106">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="61bea-2107">[重大な変更]`--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2107">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-2108">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61bea-2108">RDBMS</span></span>

* <span data-ttu-id="61bea-2109">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2109">Added `georestore` command</span></span>
* <span data-ttu-id="61bea-2110">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2110">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2111">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2111">Resource</span></span>

* <span data-ttu-id="61bea-2112">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2112">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="61bea-2113">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2113">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-2114">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-2114">SQL</span></span>

* <span data-ttu-id="61bea-2115">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2115">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2116">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2116">Storage</span></span>

* <span data-ttu-id="61bea-2117">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2117">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2118">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2118">VM</span></span>

* <span data-ttu-id="61bea-2119">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2119">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="61bea-2120">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2120">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="61bea-2122">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2122">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="61bea-2123">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2123">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="61bea-2124">#5718</span><span class="sxs-lookup"><span data-stu-id="61bea-2124">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="61bea-2125">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2125">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="61bea-2126">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2126">March 27, 2018</span></span>

<span data-ttu-id="61bea-2127">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="61bea-2127">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="61bea-2128">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-2128">Core</span></span>

* <span data-ttu-id="61bea-2129">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="61bea-2129">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2130">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2130">ACS</span></span>

* <span data-ttu-id="61bea-2131">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2131">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2132">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2132">Appservice</span></span>

* <span data-ttu-id="61bea-2133">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2133">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="61bea-2134">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2134">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="61bea-2135">バックアップ</span><span class="sxs-lookup"><span data-stu-id="61bea-2135">Backup</span></span>

* <span data-ttu-id="61bea-2136">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2136">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="61bea-2137">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="61bea-2137">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="61bea-2138">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2138">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="61bea-2139">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2139">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="61bea-2140">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-2140">Container</span></span>

* <span data-ttu-id="61bea-2141">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2141">Added `container exec` command.</span></span> <span data-ttu-id="61bea-2142">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="61bea-2142">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="61bea-2143">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="61bea-2143">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="61bea-2144">拡張機能</span><span class="sxs-lookup"><span data-stu-id="61bea-2144">Extension</span></span>

* <span data-ttu-id="61bea-2145">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2145">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="61bea-2146">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2146">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="61bea-2147">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2147">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-2148">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-2148">Interactive</span></span>

* <span data-ttu-id="61bea-2149">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2149">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="61bea-2150">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2150">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="61bea-2151">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2151">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="61bea-2152">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2152">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="61bea-2153">ラボ</span><span class="sxs-lookup"><span data-stu-id="61bea-2153">Lab</span></span>

* <span data-ttu-id="61bea-2154">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2154">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-2155">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-2155">Monitor</span></span>

* <span data-ttu-id="61bea-2156">`--top`、`--orderby`、および `--namespace` のサポートを `metrics list` に追加しました ([#5785](https://github.com/Azure/azure-cli/issues/5785))</span><span class="sxs-lookup"><span data-stu-id="61bea-2156">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="61bea-2157">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="61bea-2157">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="61bea-2158">`--namespace` のサポートを `metrics list-definitions` に追加しました ([#5785](https://github.com/Azure/azure-cli/issues/5785))</span><span class="sxs-lookup"><span data-stu-id="61bea-2158">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2159">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2159">Network</span></span>

* <span data-ttu-id="61bea-2160">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2160">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-2161">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-2161">Profile</span></span>

* <span data-ttu-id="61bea-2162">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2162">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-2163">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61bea-2163">RDBMS</span></span>

* <span data-ttu-id="61bea-2164">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2164">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2165">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2165">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="61bea-2167">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-2167">Role</span></span>

* <span data-ttu-id="61bea-2168">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2168">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="61bea-2169">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2169">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="61bea-2170">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2170">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="61bea-2171">[重大な変更]`az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2171">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="61bea-2172">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2172">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2173">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2173">Storage</span></span>

* <span data-ttu-id="61bea-2174">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2174">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="61bea-2175">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="61bea-2175">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2176">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2176">VM</span></span>

* <span data-ttu-id="61bea-2177">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2177">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="61bea-2178">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2178">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="61bea-2179">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2179">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="61bea-2180">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2180">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="61bea-2181">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2181">March 13, 2018</span></span>

<span data-ttu-id="61bea-2182">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="61bea-2182">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-2183">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-2183">ACR</span></span>

* <span data-ttu-id="61bea-2184">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2184">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="61bea-2185">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2185">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="61bea-2186">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2186">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2187">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2187">ACS</span></span>

* <span data-ttu-id="61bea-2188">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2188">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="61bea-2189">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2189">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="61bea-2190">Advisor</span><span class="sxs-lookup"><span data-stu-id="61bea-2190">Advisor</span></span>

* <span data-ttu-id="61bea-2191">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2191">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="61bea-2192">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2192">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="61bea-2193">[重大な変更]`advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2193">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="61bea-2194">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2194">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="61bea-2195">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2195">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2196">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2196">Appservice</span></span>

* <span data-ttu-id="61bea-2197">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2197">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="61bea-2198">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2198">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="61bea-2199">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="61bea-2199">Eventhubs</span></span>

* <span data-ttu-id="61bea-2200">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-2200">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="61bea-2201">拡張機能</span><span class="sxs-lookup"><span data-stu-id="61bea-2201">Extension</span></span>

* <span data-ttu-id="61bea-2202">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2202">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-2203">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-2203">Interactive</span></span>

* <span data-ttu-id="61bea-2204">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="61bea-2204">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="61bea-2205">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="61bea-2205">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="61bea-2206">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="61bea-2206">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="61bea-2207">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2207">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-2208">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-2208">Monitor</span></span>

* <span data-ttu-id="61bea-2209">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2209">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="61bea-2210">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2210">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="61bea-2211">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2211">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="61bea-2212">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2212">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2213">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2213">Network</span></span>

* <span data-ttu-id="61bea-2214">[重大な変更]`route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2214">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="61bea-2215">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2215">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="61bea-2216">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2216">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="61bea-2217">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2217">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-2218">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-2218">Profile</span></span>

* <span data-ttu-id="61bea-2219">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2219">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="61bea-2220">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2220">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-2221">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61bea-2221">RDBMS</span></span>

* <span data-ttu-id="61bea-2222">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2222">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="61bea-2223">Service Bus</span><span class="sxs-lookup"><span data-stu-id="61bea-2223">Service Bus</span></span>

* <span data-ttu-id="61bea-2224">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-2224">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2225">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2225">Storage</span></span>

* <span data-ttu-id="61bea-2226">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2226">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="61bea-2227">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2227">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2228">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2228">VM</span></span>

* <span data-ttu-id="61bea-2229">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2229">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="61bea-2230">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2230">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="61bea-2231">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2231">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="61bea-2232">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2232">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="61bea-2233">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2233">February 27, 2018</span></span>

<span data-ttu-id="61bea-2234">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="61bea-2234">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="61bea-2235">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-2235">Core</span></span>

* <span data-ttu-id="61bea-2236">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="61bea-2236">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="61bea-2237">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2237">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="61bea-2238">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2238">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2239">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2239">ACS</span></span>

* <span data-ttu-id="61bea-2240">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2240">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="61bea-2241">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="61bea-2241">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="61bea-2242">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2242">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="61bea-2243">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2243">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2244">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2244">Appservice</span></span>

* <span data-ttu-id="61bea-2245">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="61bea-2245">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="61bea-2246">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="61bea-2246">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="61bea-2247">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="61bea-2247">Cognitive Services</span></span>

* <span data-ttu-id="61bea-2248">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2248">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="61bea-2249">従量課金</span><span class="sxs-lookup"><span data-stu-id="61bea-2249">Consumption</span></span>

* <span data-ttu-id="61bea-2250">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2250">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="61bea-2251">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2251">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="61bea-2252">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-2252">Container</span></span>

* <span data-ttu-id="61bea-2253">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2253">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2254">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2254">Network</span></span>

* <span data-ttu-id="61bea-2255">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="61bea-2255">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2256">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2256">Resource</span></span>

* <span data-ttu-id="61bea-2257">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2257">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="61bea-2258">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-2258">Role</span></span>

* <span data-ttu-id="61bea-2259">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2259">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-2260">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-2260">SQL</span></span>

* <span data-ttu-id="61bea-2261">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2261">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2262">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2262">Storage</span></span>

* <span data-ttu-id="61bea-2263">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2263">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2264">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2264">VM</span></span>

* <span data-ttu-id="61bea-2265">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2265">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="61bea-2266">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2266">February 13, 2018</span></span>

<span data-ttu-id="61bea-2267">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="61bea-2267">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="61bea-2268">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-2268">Core</span></span>

* <span data-ttu-id="61bea-2269">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2269">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2270">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2270">ACS</span></span>

* <span data-ttu-id="61bea-2271">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2271">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="61bea-2272">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2272">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="61bea-2273">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2273">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="61bea-2274">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2274">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="61bea-2275">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2275">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="61bea-2276">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2276">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="61bea-2277">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2277">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="61bea-2278">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="61bea-2278">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2279">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2279">Appservice</span></span>

* <span data-ttu-id="61bea-2280">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2280">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="61bea-2281">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2281">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="61bea-2282">CDN</span><span class="sxs-lookup"><span data-stu-id="61bea-2282">CDN</span></span>

* <span data-ttu-id="61bea-2283">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2283">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="61bea-2284">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-2284">Container</span></span>

* <span data-ttu-id="61bea-2285">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2285">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="61bea-2286">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2286">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-2287">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-2287">CosmosDB</span></span>

* <span data-ttu-id="61bea-2288">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2288">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="61bea-2289">拡張機能</span><span class="sxs-lookup"><span data-stu-id="61bea-2289">Extension</span></span>

* <span data-ttu-id="61bea-2290">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2290">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="61bea-2291">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2291">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="61bea-2292">フィードバック</span><span class="sxs-lookup"><span data-stu-id="61bea-2292">Feedback</span></span>

* <span data-ttu-id="61bea-2293">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2293">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-2294">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-2294">Interactive</span></span>

* <span data-ttu-id="61bea-2295">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2295">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="61bea-2296">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2296">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-2297">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-2297">IoT</span></span>

* <span data-ttu-id="61bea-2298">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2298">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="61bea-2299">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2299">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="61bea-2300">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2300">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="61bea-2301">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2301">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-2302">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-2302">Monitor</span></span>

* <span data-ttu-id="61bea-2303">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2303">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2304">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2304">Network</span></span>

* <span data-ttu-id="61bea-2305">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2305">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="61bea-2306">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-2306">Profile</span></span>

* <span data-ttu-id="61bea-2307">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2307">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2308">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2308">Resource</span></span>

* <span data-ttu-id="61bea-2309">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2309">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="61bea-2310">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-2310">Role</span></span>

* <span data-ttu-id="61bea-2311">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2311">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-2312">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-2312">SQL</span></span>

* <span data-ttu-id="61bea-2313">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2313">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="61bea-2314">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2314">Added `sql db rename`</span></span>
* <span data-ttu-id="61bea-2315">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2315">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2316">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2316">Storage</span></span>

* <span data-ttu-id="61bea-2317">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2317">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2318">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2318">VM</span></span>

* <span data-ttu-id="61bea-2319">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2319">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="61bea-2320">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2320">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="61bea-2321">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="61bea-2321">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="61bea-2322">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2322">January 31, 2018</span></span>

<span data-ttu-id="61bea-2323">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="61bea-2323">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="61bea-2324">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-2324">Core</span></span>

* <span data-ttu-id="61bea-2325">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2325">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="61bea-2326">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2326">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="61bea-2327">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2327">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="61bea-2328">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-2328">Use `--verbose` to see</span></span>
* <span data-ttu-id="61bea-2329">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="61bea-2329">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2330">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2330">ACS</span></span>

* <span data-ttu-id="61bea-2331">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2331">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="61bea-2332">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2332">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2333">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2333">Appservice</span></span>

* <span data-ttu-id="61bea-2334">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="61bea-2334">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="61bea-2335">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2335">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="61bea-2336">CDN</span><span class="sxs-lookup"><span data-stu-id="61bea-2336">CDN</span></span>

* <span data-ttu-id="61bea-2337">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2337">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-2338">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-2338">CosmosDB</span></span>

* <span data-ttu-id="61bea-2339">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2339">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-2340">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-2340">Interactive</span></span>

* <span data-ttu-id="61bea-2341">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2341">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2342">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2342">Network</span></span>

* <span data-ttu-id="61bea-2343">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2343">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="61bea-2344">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2344">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="61bea-2345">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2345">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="61bea-2346">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2346">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="61bea-2347">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2347">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="61bea-2348">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2348">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="61bea-2349">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2349">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="61bea-2350">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2350">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="61bea-2351">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2351">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="61bea-2352">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2352">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-2353">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-2353">Profile</span></span>

* <span data-ttu-id="61bea-2354">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2354">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2355">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2355">Resource</span></span>

* <span data-ttu-id="61bea-2356">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2356">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2357">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2357">Storage</span></span>

* <span data-ttu-id="61bea-2358">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2358">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="61bea-2359">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2359">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="61bea-2360">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2360">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="61bea-2361">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2361">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="61bea-2362">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2362">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2363">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2363">VM</span></span>

* <span data-ttu-id="61bea-2364">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2364">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="61bea-2365">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2365">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="61bea-2366">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2366">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="61bea-2367">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2367">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="61bea-2368">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2368">January 17, 2018</span></span>

<span data-ttu-id="61bea-2369">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="61bea-2369">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-2370">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-2370">ACR</span></span>

* <span data-ttu-id="61bea-2371">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2371">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="61bea-2372">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2372">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2373">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2373">ACS</span></span>

* <span data-ttu-id="61bea-2374">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2374">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="61bea-2375">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2375">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2376">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2376">Appservice</span></span>

* <span data-ttu-id="61bea-2377">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2377">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="61bea-2378">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2378">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="61bea-2379">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2379">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="61bea-2380">バックアップ</span><span class="sxs-lookup"><span data-stu-id="61bea-2380">Backup</span></span>

* <span data-ttu-id="61bea-2381">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2381">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="61bea-2382">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2382">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="61bea-2383">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2383">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="61bea-2384">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2384">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="61bea-2385">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2385">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-2386">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-2386">Batch</span></span>

* <span data-ttu-id="61bea-2387">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2387">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="61bea-2388">クラウド</span><span class="sxs-lookup"><span data-stu-id="61bea-2388">Cloud</span></span>

* <span data-ttu-id="61bea-2389">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2389">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="61bea-2390">従量課金</span><span class="sxs-lookup"><span data-stu-id="61bea-2390">Consumption</span></span>

* <span data-ttu-id="61bea-2391">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2391">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="61bea-2392">Event Grid</span><span class="sxs-lookup"><span data-stu-id="61bea-2392">Event Grid</span></span>

* <span data-ttu-id="61bea-2393">[重大な変更]`az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2393">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="61bea-2394">[重大な変更]`az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2394">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="61bea-2395">[重大な変更]`eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2395">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="61bea-2396">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="61bea-2396">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="61bea-2397">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2397">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="61bea-2398">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2398">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="61bea-2399">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2399">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="61bea-2400">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2400">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-2401">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-2401">Interactive</span></span>

* <span data-ttu-id="61bea-2402">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2402">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="61bea-2403">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2403">Fixed errors on startup</span></span>
* <span data-ttu-id="61bea-2404">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2404">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-2405">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-2405">IoT</span></span>

* <span data-ttu-id="61bea-2406">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2406">Added support for device provisioning service</span></span>
* <span data-ttu-id="61bea-2407">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2407">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="61bea-2408">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2408">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-2409">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-2409">Monitor</span></span>

* <span data-ttu-id="61bea-2410">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2410">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="61bea-2411">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2411">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="61bea-2412">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2412">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2413">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2413">Network</span></span>

* <span data-ttu-id="61bea-2414">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2414">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="61bea-2415">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2415">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-2416">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-2416">Profile</span></span>

* <span data-ttu-id="61bea-2417">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2417">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="61bea-2418">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-2418">Role</span></span>

* <span data-ttu-id="61bea-2419">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2419">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="61bea-2420">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="61bea-2420">Service Fabric</span></span>

* <span data-ttu-id="61bea-2421">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2421">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="61bea-2422">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2422">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2423">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2423">VM</span></span>

* <span data-ttu-id="61bea-2424">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="61bea-2424">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="61bea-2425">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2425">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="61bea-2426">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2426">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="61bea-2427">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2427">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="61bea-2428">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2428">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="61bea-2429">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2429">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="61bea-2430">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2430">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="61bea-2431">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2431">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="61bea-2432">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2432">December 19, 2017</span></span>

<span data-ttu-id="61bea-2433">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="61bea-2433">Version 2.0.23</span></span>

* <span data-ttu-id="61bea-2434">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2434">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="61bea-2435">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-2435">Container</span></span>

* <span data-ttu-id="61bea-2436">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2436">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2437">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2437">Network</span></span>

* <span data-ttu-id="61bea-2438">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2438">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="61bea-2439">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2439">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2440">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2440">Storage</span></span>

* <span data-ttu-id="61bea-2441">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2441">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2442">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2442">VM</span></span>

* <span data-ttu-id="61bea-2443">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2443">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="61bea-2444">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2444">December 5, 2017</span></span>

<span data-ttu-id="61bea-2445">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="61bea-2445">Version 2.0.22</span></span>

* <span data-ttu-id="61bea-2446">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2446">Removed `az component` commands.</span></span> <span data-ttu-id="61bea-2447">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="61bea-2447">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="61bea-2448">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-2448">Core</span></span>
* <span data-ttu-id="61bea-2449">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2449">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="61bea-2450">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2450">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2451">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2451">ACS</span></span>

* <span data-ttu-id="61bea-2452">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2452">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="61bea-2453">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2453">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="61bea-2454">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2454">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="61bea-2455">Advisor</span><span class="sxs-lookup"><span data-stu-id="61bea-2455">Advisor</span></span>

* <span data-ttu-id="61bea-2456">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-2456">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2457">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2457">Appservice</span></span>

* <span data-ttu-id="61bea-2458">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2458">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="61bea-2459">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2459">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="61bea-2460">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2460">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="61bea-2461">従量課金</span><span class="sxs-lookup"><span data-stu-id="61bea-2461">Consumption</span></span>

* <span data-ttu-id="61bea-2462">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2462">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="61bea-2463">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-2463">Container</span></span>

* <span data-ttu-id="61bea-2464">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2464">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-2465">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-2465">Monitor</span></span>

* <span data-ttu-id="61bea-2466">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2466">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2467">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2467">Resource</span></span>

* <span data-ttu-id="61bea-2468">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2468">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="61bea-2469">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-2469">Role</span></span>

* <span data-ttu-id="61bea-2470">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2470">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="61bea-2471">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2471">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="61bea-2472">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2472">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-2473">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-2473">SQL</span></span>

* <span data-ttu-id="61bea-2474">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2474">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="61bea-2475">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2475">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2476">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2476">VM</span></span>

* <span data-ttu-id="61bea-2477">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2477">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="61bea-2478">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2478">November 14, 2017</span></span>

<span data-ttu-id="61bea-2479">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="61bea-2479">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-2480">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-2480">ACR</span></span>

* <span data-ttu-id="61bea-2481">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2481">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="61bea-2482">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2482">ACS</span></span>

* <span data-ttu-id="61bea-2483">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2483">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="61bea-2484">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2484">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="61bea-2485">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2485">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="61bea-2486">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2486">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="61bea-2487">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2487">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2488">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2488">Appservice</span></span>

* <span data-ttu-id="61bea-2489">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2489">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="61bea-2490">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2490">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="61bea-2491">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2491">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="61bea-2492">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2492">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="61bea-2493">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2493">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="61bea-2494">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="61bea-2494">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-2495">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-2495">Batch</span></span>

* <span data-ttu-id="61bea-2496">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2496">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="61bea-2497">Batchai</span><span class="sxs-lookup"><span data-stu-id="61bea-2497">Batchai</span></span>

* <span data-ttu-id="61bea-2498">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2498">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="61bea-2499">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2499">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="61bea-2500">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2500">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="61bea-2501">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2501">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="61bea-2502">クラウド</span><span class="sxs-lookup"><span data-stu-id="61bea-2502">Cloud</span></span>

* <span data-ttu-id="61bea-2503">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2503">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="61bea-2504">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-2504">Container</span></span>

* <span data-ttu-id="61bea-2505">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2505">Added support to open multiple ports</span></span>
* <span data-ttu-id="61bea-2506">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2506">Added container group restart policy</span></span>
* <span data-ttu-id="61bea-2507">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2507">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="61bea-2508">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2508">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="61bea-2509">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="61bea-2509">Data Lake Analytics</span></span>

* <span data-ttu-id="61bea-2510">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2510">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="61bea-2511">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="61bea-2511">Data Lake Store</span></span>

* <span data-ttu-id="61bea-2512">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2512">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="61bea-2513">拡張機能</span><span class="sxs-lookup"><span data-stu-id="61bea-2513">Extension</span></span>

* <span data-ttu-id="61bea-2514">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2514">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="61bea-2515">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2515">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-2516">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-2516">IoT</span></span>

* <span data-ttu-id="61bea-2517">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2517">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-2518">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-2518">Monitor</span></span>

* <span data-ttu-id="61bea-2519">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2519">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2520">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2520">Network</span></span>

* <span data-ttu-id="61bea-2521">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2521">Added support for CAA DNS records</span></span>
* <span data-ttu-id="61bea-2522">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2522">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="61bea-2523">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2523">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="61bea-2524">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2524">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="61bea-2525">Reservations</span><span class="sxs-lookup"><span data-stu-id="61bea-2525">Reservations</span></span>

* <span data-ttu-id="61bea-2526">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="61bea-2526">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2527">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2527">Resource</span></span>

* <span data-ttu-id="61bea-2528">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2528">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-2529">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-2529">SQL</span></span>

* <span data-ttu-id="61bea-2530">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2530">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2531">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2531">Storage</span></span>

* <span data-ttu-id="61bea-2532">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2532">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="61bea-2533">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2533">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="61bea-2534">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2534">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="61bea-2535">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2535">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="61bea-2536">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2536">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="61bea-2537">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2537">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="61bea-2538">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2538">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2539">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2539">VM</span></span>

* <span data-ttu-id="61bea-2540">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2540">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="61bea-2541">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2541">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="61bea-2542">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2542">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="61bea-2543">`vm format-secret` から `vm secret format` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-2543">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="61bea-2544">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2544">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="61bea-2545">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2545">October 24, 2017</span></span>

<span data-ttu-id="61bea-2546">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="61bea-2546">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="61bea-2547">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-2547">Core</span></span>

* <span data-ttu-id="61bea-2548">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2548">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-2549">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-2549">ACR</span></span>

* <span data-ttu-id="61bea-2550">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2550">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="61bea-2551">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2551">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="61bea-2552">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2552">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2553">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2553">ACS</span></span>

* <span data-ttu-id="61bea-2554">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2554">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="61bea-2555">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2555">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2556">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2556">Appservice</span></span>

* <span data-ttu-id="61bea-2557">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2557">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="61bea-2558">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="61bea-2558">Component</span></span>

* <span data-ttu-id="61bea-2559">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2559">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-2560">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-2560">Monitor</span></span>

* <span data-ttu-id="61bea-2561">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2561">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2562">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2562">Resource</span></span>

* <span data-ttu-id="61bea-2563">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2563">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="61bea-2564">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2564">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2565">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2565">VM</span></span>

* <span data-ttu-id="61bea-2566">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2566">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="61bea-2567">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2567">October 9, 2017</span></span>

<span data-ttu-id="61bea-2568">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="61bea-2568">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="61bea-2569">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-2569">Core</span></span>

* <span data-ttu-id="61bea-2570">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2570">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2571">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2571">Appservice</span></span>

* <span data-ttu-id="61bea-2572">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2572">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-2573">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-2573">Batch</span></span>

* <span data-ttu-id="61bea-2574">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2574">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="61bea-2575">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2575">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="61bea-2576">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2576">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="61bea-2577">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2577">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="61bea-2578">Batchai</span><span class="sxs-lookup"><span data-stu-id="61bea-2578">Batchai</span></span>

* <span data-ttu-id="61bea-2579">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-2579">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="61bea-2580">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61bea-2580">Keyvault</span></span>

* <span data-ttu-id="61bea-2581">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2581">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="61bea-2582">(#4448)</span><span class="sxs-lookup"><span data-stu-id="61bea-2582">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="61bea-2583">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2583">Network</span></span>

* <span data-ttu-id="61bea-2584">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2584">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="61bea-2585">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2585">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2586">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2586">Resource</span></span>

* <span data-ttu-id="61bea-2587">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2587">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="61bea-2588">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2588">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="61bea-2589">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2589">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="61bea-2590">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2590">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-2591">Sql</span><span class="sxs-lookup"><span data-stu-id="61bea-2591">Sql</span></span>

* <span data-ttu-id="61bea-2592">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2592">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="61bea-2593">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2593">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="61bea-2594">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2594">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2595">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2595">Storage</span></span>

* <span data-ttu-id="61bea-2596">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2596">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2597">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2597">Vm</span></span>

* <span data-ttu-id="61bea-2598">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2598">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="61bea-2599">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2599">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="61bea-2600">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2600">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="61bea-2601">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2601">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="61bea-2602">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2602">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="61bea-2603">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2603">September 22, 2017</span></span>

<span data-ttu-id="61bea-2604">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="61bea-2604">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2605">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2605">Resource</span></span>

* <span data-ttu-id="61bea-2606">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2606">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="61bea-2607">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2607">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="61bea-2608">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2608">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="61bea-2609">[重大な変更]`managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2609">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2610">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2610">Network</span></span>

* <span data-ttu-id="61bea-2611">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2611">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="61bea-2612">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2612">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="61bea-2613">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2613">Added `asg` application security group commands</span></span>
* <span data-ttu-id="61bea-2614">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2614">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="61bea-2615">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2615">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="61bea-2616">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2616">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="61bea-2617">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2617">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2618">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2618">Storage</span></span>

* <span data-ttu-id="61bea-2619">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2619">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="61bea-2620">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="61bea-2620">Eventgrid</span></span>

* <span data-ttu-id="61bea-2621">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2621">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-2622">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-2622">SQL</span></span>

* <span data-ttu-id="61bea-2623">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2623">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="61bea-2624">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="61bea-2624">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="61bea-2625">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2625">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="61bea-2626">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61bea-2626">Keyvault</span></span>

* <span data-ttu-id="61bea-2627">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2627">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2628">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2628">VM</span></span>

* <span data-ttu-id="61bea-2629">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2629">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="61bea-2630">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2630">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="61bea-2631">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2631">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="61bea-2632">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2632">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="61bea-2633">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2633">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="61bea-2634">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2634">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2635">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2635">ACS</span></span>

* <span data-ttu-id="61bea-2636">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2636">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2637">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2637">Appservice</span></span>

* <span data-ttu-id="61bea-2638">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2638">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="61bea-2639">バックアップ</span><span class="sxs-lookup"><span data-stu-id="61bea-2639">Backup</span></span>

* <span data-ttu-id="61bea-2640">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="61bea-2640">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="61bea-2641">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2641">September 11, 2017</span></span>

<span data-ttu-id="61bea-2642">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="61bea-2642">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="61bea-2643">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-2643">Core</span></span>

* <span data-ttu-id="61bea-2644">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2644">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="61bea-2645">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2645">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2646">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2646">Acs</span></span>

* <span data-ttu-id="61bea-2647">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2647">Added `acs list-locations` command</span></span>
* <span data-ttu-id="61bea-2648">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2648">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2649">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2649">Appservice</span></span>

* <span data-ttu-id="61bea-2650">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2650">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="61bea-2651">CDN</span><span class="sxs-lookup"><span data-stu-id="61bea-2651">CDN</span></span>

* <span data-ttu-id="61bea-2652">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2652">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="61bea-2653">拡張機能</span><span class="sxs-lookup"><span data-stu-id="61bea-2653">Extension</span></span>

* <span data-ttu-id="61bea-2654">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-2654">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="61bea-2655">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61bea-2655">Keyvault</span></span>

* <span data-ttu-id="61bea-2656">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2656">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2657">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2657">Network</span></span>

* <span data-ttu-id="61bea-2658">`vnet list-private-access-services` から `vnet list-endpoint-services` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-2658">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="61bea-2659">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2659">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="61bea-2660">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2660">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="61bea-2661">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2661">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="61bea-2662">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2662">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2663">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2663">Resource</span></span>

* <span data-ttu-id="61bea-2664">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="61bea-2664">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="61bea-2665">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="61bea-2665">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="61bea-2666">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="61bea-2666">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="61bea-2667">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2667">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-2668">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-2668">SQL</span></span>

* <span data-ttu-id="61bea-2669">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2669">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2670">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2670">VM</span></span>

* <span data-ttu-id="61bea-2671">固定:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="61bea-2671">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="61bea-2672">固定:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="61bea-2672">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="61bea-2673">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2673">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="61bea-2674">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="61bea-2674">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="61bea-2675">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="61bea-2675">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="61bea-2676">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2676">August 31, 2017</span></span>

<span data-ttu-id="61bea-2677">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="61bea-2677">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="61bea-2678">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61bea-2678">Keyvault</span></span>

* <span data-ttu-id="61bea-2679">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2679">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="61bea-2680">SF</span><span class="sxs-lookup"><span data-stu-id="61bea-2680">Sf</span></span>

* <span data-ttu-id="61bea-2681">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="61bea-2681">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2682">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2682">Storage</span></span>

* <span data-ttu-id="61bea-2683">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2683">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="61bea-2684">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="61bea-2684">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="61bea-2685">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2685">August 28, 2017</span></span>

<span data-ttu-id="61bea-2686">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="61bea-2686">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="61bea-2687">CLI</span><span class="sxs-lookup"><span data-stu-id="61bea-2687">CLI</span></span>

* <span data-ttu-id="61bea-2688">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2688">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2689">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2689">ACS</span></span>

* <span data-ttu-id="61bea-2690">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2690">Corrected preview regions</span></span>
* <span data-ttu-id="61bea-2691">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2691">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="61bea-2692">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2692">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2693">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2693">Appservice</span></span>

* <span data-ttu-id="61bea-2694">[重大な変更]`az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2694">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="61bea-2695">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2695">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="61bea-2696">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2696">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="61bea-2697">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2697">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="61bea-2698">固定:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="61bea-2698">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-2699">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-2699">IoT</span></span>

* <span data-ttu-id="61bea-2700">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2700">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2701">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2701">Network</span></span>

* <span data-ttu-id="61bea-2702">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2702">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="61bea-2703">[重大な変更]`vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2703">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="61bea-2704">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2704">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="61bea-2705">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2705">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="61bea-2706">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2706">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-2707">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-2707">Profile</span></span>

* <span data-ttu-id="61bea-2708">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2708">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="61bea-2709">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="61bea-2709">Service Fabric</span></span>

* <span data-ttu-id="61bea-2710">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="61bea-2710">Preview release</span></span>
* <span data-ttu-id="61bea-2711">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2711">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="61bea-2712">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2712">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="61bea-2713">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2713">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2714">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2714">Storage</span></span>

* <span data-ttu-id="61bea-2715">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2715">Enabled setting blob tier</span></span>
* <span data-ttu-id="61bea-2716">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2716">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="61bea-2717">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2717">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="61bea-2718">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2718">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="61bea-2719">[重大な変更]`az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2719">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="61bea-2720">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="61bea-2720">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2721">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2721">VM</span></span>

* <span data-ttu-id="61bea-2722">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2722">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="61bea-2723">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2723">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="61bea-2724">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2724">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="61bea-2725">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2725">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="61bea-2726">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2726">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="61bea-2727">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2727">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="61bea-2728">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2728">August 15, 2017</span></span>

<span data-ttu-id="61bea-2729">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="61bea-2729">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2730">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2730">ACS</span></span>

* <span data-ttu-id="61bea-2731">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2731">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2732">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2732">Appservice</span></span>

* <span data-ttu-id="61bea-2733">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2733">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="61bea-2734">Event Grid</span><span class="sxs-lookup"><span data-stu-id="61bea-2734">Event Grid</span></span>

* <span data-ttu-id="61bea-2735">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2735">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="61bea-2736">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2736">August 11, 2017</span></span>

<span data-ttu-id="61bea-2737">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="61bea-2737">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2738">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2738">ACS</span></span>

* <span data-ttu-id="61bea-2739">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2739">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-2740">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-2740">Batch</span></span>

* <span data-ttu-id="61bea-2741">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2741">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="61bea-2742">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2742">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="61bea-2743">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2743">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="61bea-2744">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2744">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="61bea-2745">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2745">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="61bea-2746">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2746">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="61bea-2747">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="61bea-2747">Component</span></span>

* <span data-ttu-id="61bea-2748">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2748">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="61bea-2749">コンテナー</span><span class="sxs-lookup"><span data-stu-id="61bea-2749">Container</span></span>

* <span data-ttu-id="61bea-2750">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2750">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="61bea-2751">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="61bea-2751">Data Lake Store</span></span>

* <span data-ttu-id="61bea-2752">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2752">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="61bea-2753">Event Grid</span><span class="sxs-lookup"><span data-stu-id="61bea-2753">Event Grid</span></span>

* <span data-ttu-id="61bea-2754">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-2754">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2755">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2755">Network</span></span>

* <span data-ttu-id="61bea-2756">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2756">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="61bea-2757">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2757">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="61bea-2758">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2758">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="61bea-2759">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2759">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-2760">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-2760">Profile</span></span>

* <span data-ttu-id="61bea-2761">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2761">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2762">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2762">Storage</span></span>

* <span data-ttu-id="61bea-2763">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="61bea-2763">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2764">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2764">VM</span></span>

* <span data-ttu-id="61bea-2765">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2765">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="61bea-2766">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2766">Exposed `list-skus` command</span></span>
* <span data-ttu-id="61bea-2767">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2767">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="61bea-2768">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="61bea-2768">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="61bea-2769">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2769">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="61bea-2770">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2770">July 28, 2017</span></span>

<span data-ttu-id="61bea-2771">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="61bea-2771">Version 2.0.12</span></span>

* <span data-ttu-id="61bea-2772">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2772">Added container commands</span></span>
* <span data-ttu-id="61bea-2773">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2773">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="61bea-2774">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-2774">Core</span></span>

* <span data-ttu-id="61bea-2775">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="61bea-2775">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="61bea-2776">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2776">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="61bea-2777">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="61bea-2777">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="61bea-2778">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="61bea-2778">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="61bea-2779">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="61bea-2779">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="61bea-2780">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="61bea-2780">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="61bea-2781">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="61bea-2781">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="61bea-2782">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="61bea-2782">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="61bea-2783">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="61bea-2783">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="61bea-2784">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="61bea-2784">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="61bea-2785">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="61bea-2785">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="61bea-2786">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="61bea-2786">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="61bea-2787">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2787">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="61bea-2788">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2788">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="61bea-2789">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2789">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="61bea-2790">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="61bea-2790">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="61bea-2791">ACR</span><span class="sxs-lookup"><span data-stu-id="61bea-2791">ACR</span></span>

* <span data-ttu-id="61bea-2792">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2792">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="61bea-2793">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2793">Support SKU update for managed registries</span></span>
* <span data-ttu-id="61bea-2794">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2794">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="61bea-2795">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2795">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="61bea-2796">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2796">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="61bea-2797">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2797">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2798">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2798">ACS</span></span>

* <span data-ttu-id="61bea-2799">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2799">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2800">Appservice</span><span class="sxs-lookup"><span data-stu-id="61bea-2800">Appservice</span></span>

* <span data-ttu-id="61bea-2801">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2801">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="61bea-2802">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2802">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="61bea-2803">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="61bea-2803">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="61bea-2804">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="61bea-2804">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="61bea-2805">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="61bea-2805">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="61bea-2806">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="61bea-2806">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="61bea-2807">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="61bea-2807">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="61bea-2808">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="61bea-2808">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="61bea-2809">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2809">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="61bea-2810">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="61bea-2810">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="61bea-2811">Batch</span><span class="sxs-lookup"><span data-stu-id="61bea-2811">Batch</span></span>

* <span data-ttu-id="61bea-2812">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2812">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="61bea-2813">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2813">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="61bea-2814">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2814">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="61bea-2815">CDN</span><span class="sxs-lookup"><span data-stu-id="61bea-2815">CDN</span></span>

* <span data-ttu-id="61bea-2816">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2816">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="61bea-2817">クラウド</span><span class="sxs-lookup"><span data-stu-id="61bea-2817">Cloud</span></span>

* <span data-ttu-id="61bea-2818">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2818">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="61bea-2819">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="61bea-2819">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="61bea-2820">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2820">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="61bea-2821">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2821">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="61bea-2822">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2822">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-2823">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-2823">CosmosDB</span></span>

* <span data-ttu-id="61bea-2824">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2824">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="61bea-2825">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2825">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="61bea-2826">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="61bea-2826">Data Lake Analytics</span></span>

* <span data-ttu-id="61bea-2827">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2827">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="61bea-2828">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2828">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="61bea-2829">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2829">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="61bea-2830">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="61bea-2830">Data Lake Store</span></span>

* <span data-ttu-id="61bea-2831">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2831">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="61bea-2832">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2832">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="61bea-2833">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2833">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="61bea-2834">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="61bea-2834">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="61bea-2835">Interactive</span><span class="sxs-lookup"><span data-stu-id="61bea-2835">Interactive</span></span>

* <span data-ttu-id="61bea-2836">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2836">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="61bea-2837">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="61bea-2837">Increased test coverage</span></span>
* <span data-ttu-id="61bea-2838">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2838">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="61bea-2839">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="61bea-2839">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="61bea-2840">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="61bea-2840">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="61bea-2841">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="61bea-2841">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="61bea-2842">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="61bea-2842">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="61bea-2843">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2843">Added `--progress` flag</span></span>
* <span data-ttu-id="61bea-2844">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2844">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="61bea-2845">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="61bea-2845">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="61bea-2846">IoT</span><span class="sxs-lookup"><span data-stu-id="61bea-2846">IoT</span></span>

* <span data-ttu-id="61bea-2847">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2847">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="61bea-2848">(#3934)</span><span class="sxs-lookup"><span data-stu-id="61bea-2848">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="61bea-2849">Key Vault</span><span class="sxs-lookup"><span data-stu-id="61bea-2849">Key vault</span></span>

* <span data-ttu-id="61bea-2850">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2850">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="61bea-2851">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="61bea-2851">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="61bea-2852">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="61bea-2852">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="61bea-2853">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="61bea-2853">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="61bea-2854">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="61bea-2854">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="61bea-2855">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="61bea-2855">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="61bea-2856">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2856">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="61bea-2857">(#3307)</span><span class="sxs-lookup"><span data-stu-id="61bea-2857">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="61bea-2858">ラボ</span><span class="sxs-lookup"><span data-stu-id="61bea-2858">Lab</span></span>

* <span data-ttu-id="61bea-2859">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2859">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="61bea-2860">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2860">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-2861">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-2861">Monitor</span></span>

* <span data-ttu-id="61bea-2862">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="61bea-2862">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="61bea-2863">`monitor alert-rule-incidents list` から `monitor alert list-incidents` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-2863">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="61bea-2864">`monitor alert-rule-incidents show` から `monitor alert show-incident` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-2864">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="61bea-2865">`monitor metric-defintions list` から `monitor metrics list-definitions` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-2865">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="61bea-2866">`monitor alert-rules` から `monitor alert` への名称変更</span><span class="sxs-lookup"><span data-stu-id="61bea-2866">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="61bea-2867">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="61bea-2867">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="61bea-2868">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2868">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="61bea-2869">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="61bea-2869">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="61bea-2870">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2870">`location` no longer required</span></span>
  * <span data-ttu-id="61bea-2871">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="61bea-2871">Add name and ID support for target</span></span>
  * <span data-ttu-id="61bea-2872">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="61bea-2872">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="61bea-2873">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2873">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="61bea-2874">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2874">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="61bea-2875">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="61bea-2875">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="61bea-2876">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2876">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="61bea-2877">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2877">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="61bea-2878">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-2878">Network</span></span>

* <span data-ttu-id="61bea-2879">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2879">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="61bea-2880">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2880">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="61bea-2881">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2881">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="61bea-2882">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2882">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="61bea-2883">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2883">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="61bea-2884">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2884">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="61bea-2885">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2885">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="61bea-2886">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2886">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="61bea-2887">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2887">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="61bea-2888">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2888">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="61bea-2889">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2889">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="61bea-2890">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2890">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="61bea-2891">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2891">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="61bea-2892">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2892">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="61bea-2893">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2893">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="61bea-2894">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2894">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="61bea-2895">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2895">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="61bea-2896">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2896">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="61bea-2897">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2897">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="61bea-2898">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2898">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="61bea-2899">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2899">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="61bea-2900">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2900">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="61bea-2901">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2901">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="61bea-2902">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="61bea-2902">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="61bea-2903">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="61bea-2903">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="61bea-2904">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="61bea-2904">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="61bea-2905">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="61bea-2905">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-2906">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-2906">Profile</span></span>

* <span data-ttu-id="61bea-2907">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2907">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="61bea-2908">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2908">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="61bea-2909">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="61bea-2909">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="61bea-2910">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2910">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="61bea-2911">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2911">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="61bea-2912">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61bea-2912">RDBMS</span></span>

* <span data-ttu-id="61bea-2913">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="61bea-2913">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="61bea-2914">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="61bea-2914">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="61bea-2915">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="61bea-2915">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="61bea-2916">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="61bea-2916">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-2917">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-2917">Resource</span></span>

* <span data-ttu-id="61bea-2918">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2918">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="61bea-2919">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2919">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="61bea-2920">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2920">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="61bea-2921">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2921">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="61bea-2922">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="61bea-2922">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="61bea-2923">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2923">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="61bea-2924">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="61bea-2924">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="61bea-2925">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2925">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="61bea-2926">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-2926">Role</span></span>

* <span data-ttu-id="61bea-2927">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2927">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="61bea-2928">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="61bea-2928">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="61bea-2929">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="61bea-2929">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="61bea-2930">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="61bea-2930">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="61bea-2931">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2931">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="61bea-2932">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="61bea-2932">Service Fabric</span></span>
* <span data-ttu-id="61bea-2933">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="61bea-2933">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="61bea-2934">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="61bea-2934">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="61bea-2935">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="61bea-2935">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-2936">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-2936">SQL</span></span>

* <span data-ttu-id="61bea-2937">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2937">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="61bea-2938">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2938">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="61bea-2939">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2939">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-2940">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-2940">Storage</span></span>

* <span data-ttu-id="61bea-2941">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="61bea-2941">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="61bea-2942">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-2942">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="61bea-2943">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="61bea-2943">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="61bea-2944">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="61bea-2944">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="61bea-2945">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="61bea-2945">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="61bea-2946">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="61bea-2946">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-2947">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-2947">VM</span></span>

* <span data-ttu-id="61bea-2948">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2948">Support configuring nsg</span></span>
* <span data-ttu-id="61bea-2949">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2949">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="61bea-2950">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="61bea-2950">Support managed service identities</span></span>
* <span data-ttu-id="61bea-2951">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-2951">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="61bea-2952">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="61bea-2952">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="61bea-2953">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="61bea-2953">May 10, 2017</span></span>

<span data-ttu-id="61bea-2954">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="61bea-2954">Version 2.0.6</span></span>

* <span data-ttu-id="61bea-2955">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2955">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="61bea-2956">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2956">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="61bea-2957">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2957">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="61bea-2958">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2958">Include Cognitive Services module</span></span>
* <span data-ttu-id="61bea-2959">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2959">Include Service Fabric module</span></span>
* <span data-ttu-id="61bea-2960">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="61bea-2960">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="61bea-2961">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2961">Add support for CDN commands</span></span>
* <span data-ttu-id="61bea-2962">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2962">Remove Container module</span></span>
* <span data-ttu-id="61bea-2963">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="61bea-2963">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="61bea-2964">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="61bea-2964">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="61bea-2965">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-2965">Core</span></span>

* <span data-ttu-id="61bea-2966">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="61bea-2966">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="61bea-2967">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="61bea-2967">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="61bea-2968">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="61bea-2968">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="61bea-2969">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="61bea-2969">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="61bea-2970">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="61bea-2970">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="61bea-2971">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="61bea-2971">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="61bea-2972">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="61bea-2972">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="61bea-2973">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="61bea-2973">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="61bea-2974">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="61bea-2974">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="61bea-2975">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="61bea-2975">core: Improved performance</span></span>
* <span data-ttu-id="61bea-2976">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="61bea-2976">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="61bea-2977">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="61bea-2977">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-2978">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-2978">ACS</span></span>

* <span data-ttu-id="61bea-2979">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2979">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="61bea-2980">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2980">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="61bea-2981">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2981">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="61bea-2982">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="61bea-2982">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-2983">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-2983">AppService</span></span>

* <span data-ttu-id="61bea-2984">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2984">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="61bea-2985">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2985">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="61bea-2986">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="61bea-2986">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="61bea-2987">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2987">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="61bea-2988">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2988">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="61bea-2989">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="61bea-2989">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="61bea-2990">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="61bea-2990">support slot swap with preview</span></span>
* <span data-ttu-id="61bea-2991">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="61bea-2991">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="61bea-2992">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="61bea-2992">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61bea-2993">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61bea-2993">CosmosDB</span></span>

* <span data-ttu-id="61bea-2994">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2994">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="61bea-2995">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2995">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="61bea-2996">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2996">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="61bea-2997">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-2997">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="61bea-2998">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="61bea-2998">Data Lake Analytics</span></span>

* <span data-ttu-id="61bea-2999">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-2999">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="61bea-3000">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="61bea-3000">Add support for new catalog item type: package.</span></span> <span data-ttu-id="61bea-3001">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="61bea-3001">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="61bea-3002">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="61bea-3002">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="61bea-3003">テーブル</span><span class="sxs-lookup"><span data-stu-id="61bea-3003">Table</span></span>
  * <span data-ttu-id="61bea-3004">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="61bea-3004">Table valued function</span></span>
  * <span data-ttu-id="61bea-3005">表示</span><span class="sxs-lookup"><span data-stu-id="61bea-3005">View</span></span>
  * <span data-ttu-id="61bea-3006">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="61bea-3006">Table Statistics.</span></span> <span data-ttu-id="61bea-3007">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="61bea-3007">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="61bea-3008">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="61bea-3008">Data Lake Store</span></span>

* <span data-ttu-id="61bea-3009">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3009">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="61bea-3010">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="61bea-3010">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="61bea-3011">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="61bea-3011">missed help for access show.</span></span> <span data-ttu-id="61bea-3012">追加しました</span><span class="sxs-lookup"><span data-stu-id="61bea-3012">adding it.</span></span> <span data-ttu-id="61bea-3013">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="61bea-3013">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="61bea-3014">Find</span><span class="sxs-lookup"><span data-stu-id="61bea-3014">Find</span></span>

* <span data-ttu-id="61bea-3015">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="61bea-3015">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="61bea-3016">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61bea-3016">KeyVault</span></span>

* <span data-ttu-id="61bea-3017">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="61bea-3017">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="61bea-3018">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3018">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="61bea-3019">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="61bea-3019">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="61bea-3020">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3020">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="61bea-3021">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="61bea-3021">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="61bea-3022">ラボ</span><span class="sxs-lookup"><span data-stu-id="61bea-3022">Lab</span></span>

* <span data-ttu-id="61bea-3023">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3023">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="61bea-3024">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3024">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="61bea-3025">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3025">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="61bea-3026">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3026">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="61bea-3027">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3027">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="61bea-3028">モニター</span><span class="sxs-lookup"><span data-stu-id="61bea-3028">Monitor</span></span>

* <span data-ttu-id="61bea-3029">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="61bea-3029">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="61bea-3030">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="61bea-3030">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="61bea-3031">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-3031">Network</span></span>

* <span data-ttu-id="61bea-3032">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3032">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="61bea-3033">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3033">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="61bea-3034">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3034">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="61bea-3035">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3035">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="61bea-3036">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3036">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="61bea-3037">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3037">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="61bea-3038">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3038">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="61bea-3039">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3039">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="61bea-3040">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3040">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="61bea-3041">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3041">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="61bea-3042">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3042">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="61bea-3043">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3043">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="61bea-3044">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3044">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="61bea-3045">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3045">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="61bea-3046">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="61bea-3046">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="61bea-3047">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3047">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="61bea-3048">プロファイル</span><span class="sxs-lookup"><span data-stu-id="61bea-3048">Profile</span></span>

* <span data-ttu-id="61bea-3049">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="61bea-3049">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="61bea-3050">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="61bea-3050">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="61bea-3051">Redis</span><span class="sxs-lookup"><span data-stu-id="61bea-3051">Redis</span></span>

* <span data-ttu-id="61bea-3052">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3052">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="61bea-3053">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3053">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="61bea-3054">リソース</span><span class="sxs-lookup"><span data-stu-id="61bea-3054">Resource</span></span>

* <span data-ttu-id="61bea-3055">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="61bea-3055">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="61bea-3056">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="61bea-3056">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="61bea-3057">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="61bea-3057">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="61bea-3058">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3058">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="61bea-3059">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="61bea-3059">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="61bea-3060">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3060">Add docs for az lock update.</span></span> <span data-ttu-id="61bea-3061">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="61bea-3061">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="61bea-3062">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="61bea-3062">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="61bea-3063">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="61bea-3063">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="61bea-3064">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="61bea-3064">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="61bea-3065">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="61bea-3065">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="61bea-3066">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="61bea-3066">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="61bea-3067">Role</span><span class="sxs-lookup"><span data-stu-id="61bea-3067">Role</span></span>

* <span data-ttu-id="61bea-3068">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="61bea-3068">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="61bea-3069">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="61bea-3069">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="61bea-3070">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="61bea-3070">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="61bea-3071">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="61bea-3071">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="61bea-3072">SQL</span><span class="sxs-lookup"><span data-stu-id="61bea-3072">SQL</span></span>

* <span data-ttu-id="61bea-3073">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="61bea-3073">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="61bea-3074">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="61bea-3074">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="61bea-3075">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-3075">Storage</span></span>

* <span data-ttu-id="61bea-3076">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="61bea-3076">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="61bea-3077">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3077">Add support for incremental blob copy</span></span>
* <span data-ttu-id="61bea-3078">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3078">Add support for large block blob upload</span></span>
* <span data-ttu-id="61bea-3079">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="61bea-3079">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-3080">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-3080">VM</span></span>

* <span data-ttu-id="61bea-3081">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="61bea-3081">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="61bea-3082">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="61bea-3082">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="61bea-3083">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="61bea-3083">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="61bea-3084">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="61bea-3084">az vm/vmss disk</span></span>
  3. <span data-ttu-id="61bea-3085">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="61bea-3085">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="61bea-3086">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="61bea-3086">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="61bea-3087">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="61bea-3087">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="61bea-3088">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="61bea-3088">April 3, 2017</span></span>

<span data-ttu-id="61bea-3089">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="61bea-3089">Version 2.0.2</span></span>

<span data-ttu-id="61bea-3090">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="61bea-3090">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="61bea-3091">コア</span><span class="sxs-lookup"><span data-stu-id="61bea-3091">Core</span></span>

* <span data-ttu-id="61bea-3092">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="61bea-3092">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="61bea-3093">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="61bea-3093">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="61bea-3094">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="61bea-3094">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="61bea-3095">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="61bea-3095">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="61bea-3096">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="61bea-3096">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="61bea-3097">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="61bea-3097">Add prompting for missing template parameters.</span></span> <span data-ttu-id="61bea-3098">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="61bea-3098">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="61bea-3099">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="61bea-3099">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="61bea-3100">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="61bea-3100">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="61bea-3101">ACS</span><span class="sxs-lookup"><span data-stu-id="61bea-3101">ACS</span></span>

* <span data-ttu-id="61bea-3102">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="61bea-3102">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="61bea-3103">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="61bea-3103">Add support for ssh key password prompting.</span></span> <span data-ttu-id="61bea-3104">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="61bea-3104">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="61bea-3105">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="61bea-3105">Add support for windows clusters.</span></span> <span data-ttu-id="61bea-3106">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="61bea-3106">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="61bea-3107">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="61bea-3107">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="61bea-3108">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="61bea-3108">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="61bea-3109">AppService</span><span class="sxs-lookup"><span data-stu-id="61bea-3109">AppService</span></span>

* <span data-ttu-id="61bea-3110">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="61bea-3110">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="61bea-3111">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="61bea-3111">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="61bea-3112">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="61bea-3112">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="61bea-3113">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="61bea-3113">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="61bea-3114">DataLake</span><span class="sxs-lookup"><span data-stu-id="61bea-3114">DataLake</span></span>

* <span data-ttu-id="61bea-3115">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-3115">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="61bea-3116">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="61bea-3116">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="61bea-3117">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="61bea-3117">DocuemntDB</span></span>

* <span data-ttu-id="61bea-3118">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="61bea-3118">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="61bea-3119">VM</span><span class="sxs-lookup"><span data-stu-id="61bea-3119">VM</span></span>

* <span data-ttu-id="61bea-3120">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="61bea-3120">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="61bea-3121">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="61bea-3121">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="61bea-3122">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="61bea-3122">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="61bea-3123">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="61bea-3123">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="61bea-3124">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="61bea-3124">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="61bea-3125">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="61bea-3125">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="61bea-3126">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="61bea-3126">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="61bea-3127">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="61bea-3127">February 27, 2017</span></span>

<span data-ttu-id="61bea-3128">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="61bea-3128">Version 2.0.0</span></span>

<span data-ttu-id="61bea-3129">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="61bea-3129">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="61bea-3130">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="61bea-3130">Container Service (acs)</span></span>
- <span data-ttu-id="61bea-3131">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="61bea-3131">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="61bea-3132">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="61bea-3132">Networking</span></span>
- <span data-ttu-id="61bea-3133">ストレージ</span><span class="sxs-lookup"><span data-stu-id="61bea-3133">Storage</span></span>

<span data-ttu-id="61bea-3134">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="61bea-3134">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="61bea-3135">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="61bea-3135">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="61bea-3136">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="61bea-3136">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="61bea-3137">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="61bea-3137">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="61bea-3138">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="61bea-3138">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="61bea-3139">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="61bea-3139">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="61bea-3140">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="61bea-3140">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="61bea-3141">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="61bea-3141">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="61bea-3142">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="61bea-3142">Provide feedback from the command line with the `az feedback` command</span></span>

