---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 07/16/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 8cb0e2f43a3f40fdf15a00ebc7bdb931bf8f41f0
ms.sourcegitcommit: 49e1dea60942fce02d9c3ce249ac633a83f303e7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2019
ms.locfileid: "68246923"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="26833-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="26833-103">Azure CLI release notes</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="26833-104">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="26833-104">July 16, 2019</span></span>

<span data-ttu-id="26833-105">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="26833-105">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-106">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-106">Appservice</span></span>

* <span data-ttu-id="26833-107">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="26833-107">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="26833-108">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-108">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="26833-109">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-109">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="26833-110">コア</span><span class="sxs-lookup"><span data-stu-id="26833-110">Core</span></span>

* <span data-ttu-id="26833-111">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-111">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="26833-112">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-112">Batch</span></span>

* <span data-ttu-id="26833-113">[重大な変更] `batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="26833-113">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="26833-114">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-114">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="26833-115">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-115">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="26833-116">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-116">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="26833-117">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="26833-117">Eventhubs</span></span>

* <span data-ttu-id="26833-118">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-118">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-119">RDBMS</span><span class="sxs-lookup"><span data-stu-id="26833-119">RDBMS</span></span>

* <span data-ttu-id="26833-120">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-120">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="26833-121">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-121">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="26833-122">リレー</span><span class="sxs-lookup"><span data-stu-id="26833-122">Relay</span></span>

* <span data-ttu-id="26833-123">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="26833-123">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="26833-124">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-124">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="26833-125">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="26833-125">Servicebus</span></span>

* <span data-ttu-id="26833-126">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-126">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="26833-127">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-127">Storage</span></span>

* <span data-ttu-id="26833-128">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="26833-128">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="26833-129">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="26833-129">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="26833-130">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="26833-130">July 2, 2019</span></span>

<span data-ttu-id="26833-131">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="26833-131">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="26833-132">コア</span><span class="sxs-lookup"><span data-stu-id="26833-132">Core</span></span>

* <span data-ttu-id="26833-133">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="26833-133">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="26833-134">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="26833-134">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="26833-135">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="26833-135">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="26833-136">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-136">ACR</span></span>

* <span data-ttu-id="26833-137">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-137">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-138">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-138">Appservice</span></span>

* <span data-ttu-id="26833-139">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-139">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="26833-140">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="26833-140">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="26833-141">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="26833-141">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="26833-142">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-142">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="26833-143">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-143">Cosmos DB</span></span>

* <span data-ttu-id="26833-144">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-144">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="26833-145">DLS</span><span class="sxs-lookup"><span data-stu-id="26833-145">DLS</span></span>

* <span data-ttu-id="26833-146">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="26833-146">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="26833-147">フィードバック</span><span class="sxs-lookup"><span data-stu-id="26833-147">Feedback</span></span>

* <span data-ttu-id="26833-148">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-148">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="26833-149">HDInsight</span><span class="sxs-lookup"><span data-stu-id="26833-149">HDInsight</span></span>

* <span data-ttu-id="26833-150">[重大な変更] `oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-150">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="26833-151">[重大な変更] `--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="26833-151">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="26833-152">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-152">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="26833-153">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-153">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="26833-154">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-154">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="26833-155">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-155">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="26833-156">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-156">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="26833-157">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="26833-157">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="26833-158">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-158">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="26833-159">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="26833-159">Managed Services</span></span>

* <span data-ttu-id="26833-160">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="26833-160">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="26833-161">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-161">Profile</span></span>
* <span data-ttu-id="26833-162">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="26833-162">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="26833-163">RBAC</span><span class="sxs-lookup"><span data-stu-id="26833-163">RBAC</span></span>

* <span data-ttu-id="26833-164">[重大な変更] `create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-164">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="26833-165">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-165">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="26833-166">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-166">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="26833-167">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-167">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-168">RDBMS</span><span class="sxs-lookup"><span data-stu-id="26833-168">RDBMS</span></span>

* <span data-ttu-id="26833-169">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-169">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="26833-170">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-170">SQL</span></span>

* <span data-ttu-id="26833-171">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="26833-171">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-172">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-172">Storage</span></span>

* <span data-ttu-id="26833-173">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-173">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="26833-174">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-174">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="26833-175">VM</span><span class="sxs-lookup"><span data-stu-id="26833-175">VM</span></span>

* <span data-ttu-id="26833-176">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-176">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="26833-177">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="26833-177">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="26833-178">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="26833-178">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="26833-179">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-179">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="26833-180">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="26833-180">June 18, 2019</span></span>

<span data-ttu-id="26833-181">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="26833-181">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="26833-182">コア</span><span class="sxs-lookup"><span data-stu-id="26833-182">Core</span></span>

<span data-ttu-id="26833-183">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="26833-183">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="26833-184">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="26833-184">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="26833-185">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="26833-185">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="26833-186">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="26833-186">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="26833-187">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="26833-187">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="26833-188">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="26833-188">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="26833-189">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="26833-189">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="26833-190">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-190">ACR</span></span>
* <span data-ttu-id="26833-191">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-191">Added 'acr check-health' command</span></span>
* <span data-ttu-id="26833-192">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-192">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="26833-193">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-193">ACS</span></span>
* <span data-ttu-id="26833-194">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="26833-194">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="26833-195">AMS</span><span class="sxs-lookup"><span data-stu-id="26833-195">AMS</span></span>
* <span data-ttu-id="26833-196">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-196">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-197">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-197">AppService</span></span>
* <span data-ttu-id="26833-198">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-198">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="26833-199">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-199">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="26833-200">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-200">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="26833-201">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-201">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="26833-202">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-202">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="26833-203">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-203">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="26833-204">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-204">Batch</span></span>
* <span data-ttu-id="26833-205">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-205">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="26833-206">BatchAI</span><span class="sxs-lookup"><span data-stu-id="26833-206">BatchAI</span></span>
* <span data-ttu-id="26833-207">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="26833-207">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="26833-208">BotService</span><span class="sxs-lookup"><span data-stu-id="26833-208">BotService</span></span>
* <span data-ttu-id="26833-209">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-209">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="26833-210">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-210">CosmosDB</span></span>
* <span data-ttu-id="26833-211">[非推奨] `cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-211">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="26833-212">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="26833-212">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="26833-213">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-213">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="26833-214">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-214">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="26833-215">EventGrid</span><span class="sxs-lookup"><span data-stu-id="26833-215">EventGrid</span></span>
* <span data-ttu-id="26833-216">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-216">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="26833-217">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-217">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="26833-218">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-218">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="26833-219">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-219">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="26833-220">[重大な変更] `eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-220">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="26833-221">HDInsight</span><span class="sxs-lookup"><span data-stu-id="26833-221">HDInsight</span></span>
* <span data-ttu-id="26833-222">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-222">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="26833-223">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-223">IoT</span></span>
* <span data-ttu-id="26833-224">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-224">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="26833-225">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-225">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="26833-226">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-226">Network</span></span>
* <span data-ttu-id="26833-227">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-227">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="26833-228">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-228">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="26833-229">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-229">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="26833-230">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-230">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="26833-231">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-231">Resource</span></span>
* <span data-ttu-id="26833-232">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-232">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="26833-233">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-233">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="26833-234">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="26833-234">ServiceBus</span></span>
* <span data-ttu-id="26833-235">`servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319) での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-235">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="26833-236">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-236">SQL</span></span>
* <span data-ttu-id="26833-237">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="26833-237">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="26833-238">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-238">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="26833-239">SQLVm</span><span class="sxs-lookup"><span data-stu-id="26833-239">SQLVm</span></span>
* <span data-ttu-id="26833-240">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-240">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="26833-241">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-241">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="26833-242">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-242">Storage</span></span>
* <span data-ttu-id="26833-243">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-243">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="26833-244">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-244">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="26833-245">VM</span><span class="sxs-lookup"><span data-stu-id="26833-245">VM</span></span>
* <span data-ttu-id="26833-246">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-246">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="26833-247">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="26833-247">June 4, 2019</span></span>

<span data-ttu-id="26833-248">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="26833-248">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="26833-249">コア</span><span class="sxs-lookup"><span data-stu-id="26833-249">Core</span></span>
* <span data-ttu-id="26833-250">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-250">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="26833-251">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-251">ACR</span></span>
* <span data-ttu-id="26833-252">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-252">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="26833-253">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-253">ACS</span></span>
* <span data-ttu-id="26833-254">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-254">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="26833-255">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="26833-255">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="26833-256">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-256">Batch</span></span>
* <span data-ttu-id="26833-257">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-257">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="26833-258">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-258">IoT</span></span>
* <span data-ttu-id="26833-259">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-259">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="26833-260">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-260">Network</span></span>
* <span data-ttu-id="26833-261">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-261">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="26833-262">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-262">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="26833-263">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-263">Resource</span></span>
* <span data-ttu-id="26833-264">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-264">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="26833-265">Role</span><span class="sxs-lookup"><span data-stu-id="26833-265">Role</span></span>
* <span data-ttu-id="26833-266">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="26833-266">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="26833-267">Compute</span><span class="sxs-lookup"><span data-stu-id="26833-267">Compute</span></span>
* <span data-ttu-id="26833-268">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-268">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="26833-269">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="26833-269">May 21, 2019</span></span>

<span data-ttu-id="26833-270">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="26833-270">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="26833-271">コア</span><span class="sxs-lookup"><span data-stu-id="26833-271">Core</span></span>
* <span data-ttu-id="26833-272">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-272">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="26833-273">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-273">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="26833-274">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-274">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="26833-275">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-275">ACR</span></span>
* <span data-ttu-id="26833-276">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-276">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="26833-277">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-277">ACS</span></span>
* <span data-ttu-id="26833-278">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-278">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-279">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-279">AppService</span></span>
* <span data-ttu-id="26833-280">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="26833-280">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="26833-281">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-281">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="26833-282">[重大な変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="26833-282">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="26833-283">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-283">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="26833-284">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-284">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="26833-285">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-285">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="26833-286">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-286">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="26833-287">BotService</span><span class="sxs-lookup"><span data-stu-id="26833-287">BotService</span></span>
* <span data-ttu-id="26833-288">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-288">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="26833-289">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-289">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="26833-290">消費</span><span class="sxs-lookup"><span data-stu-id="26833-290">Consumption</span></span>
* <span data-ttu-id="26833-291">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-291">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="26833-292">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-292">IoT</span></span>
* <span data-ttu-id="26833-293">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-293">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="26833-294">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-294">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="26833-296">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-296">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="26833-297">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-297">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-298">RDBMS</span><span class="sxs-lookup"><span data-stu-id="26833-298">RDBMS</span></span>
* <span data-ttu-id="26833-299">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-299">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="26833-300">RBAC</span><span class="sxs-lookup"><span data-stu-id="26833-300">RBAC</span></span>
* <span data-ttu-id="26833-301">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-301">Added support for mangement group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-302">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-302">Storage</span></span>
* <span data-ttu-id="26833-303">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="26833-303">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="26833-304">Compute</span><span class="sxs-lookup"><span data-stu-id="26833-304">Compute</span></span>
* <span data-ttu-id="26833-305">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-305">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="26833-306">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-306">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="26833-307">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="26833-307">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="26833-308">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-308">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="26833-309">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="26833-309">May 6, 2019</span></span>

<span data-ttu-id="26833-310">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="26833-310">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="26833-311">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-311">ACS</span></span>
* <span data-ttu-id="26833-312">[重大な変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-312">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="26833-313">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-313">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="26833-314">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-314">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="26833-315">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-315">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-316">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-316">Appservice</span></span>
* <span data-ttu-id="26833-317">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-317">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="26833-318">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-318">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="26833-319">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="26833-319">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="26833-320">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-320">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="26833-321">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-321">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="26833-322">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-322">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="26833-323">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-323">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="26833-324">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-324">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="26833-325">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-325">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="26833-326">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-326">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="26833-327">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-327">Batch</span></span>
* <span data-ttu-id="26833-328">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-328">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="26833-329">Botservice</span><span class="sxs-lookup"><span data-stu-id="26833-329">Botservice</span></span>
* <span data-ttu-id="26833-330">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="26833-330">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="26833-331">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-331">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="26833-332">[重大な変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-332">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="26833-333">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="26833-333">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="26833-334">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-334">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="26833-335">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="26833-335">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="26833-336">[重大な変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-336">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="26833-337">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-337">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="26833-338">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-338">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="26833-339">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-339">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="26833-340">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-340">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="26833-341">[重大な変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-341">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="26833-342">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-342">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="26833-343">[重大な変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-343">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="26833-344">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="26833-344">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="26833-345">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-345">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="26833-346">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-346">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="26833-347">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-347">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="26833-348">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-348">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="26833-349">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-349">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="26833-350">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-350">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="26833-351">構成</span><span class="sxs-lookup"><span data-stu-id="26833-351">Configure</span></span>
* <span data-ttu-id="26833-352">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-352">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="26833-353">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="26833-353">Eventhubs</span></span>
* <span data-ttu-id="26833-354">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-354">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="26833-355">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-355">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="26833-356">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-356">Network</span></span>
* <span data-ttu-id="26833-357">[重大な変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="26833-357">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="26833-358">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="26833-358">Policy Insights</span></span>
* <span data-ttu-id="26833-359">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-359">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="26833-360">Role</span><span class="sxs-lookup"><span data-stu-id="26833-360">Role</span></span>
* <span data-ttu-id="26833-361">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="26833-361">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="26833-362">Service Bus</span><span class="sxs-lookup"><span data-stu-id="26833-362">Service Bus</span></span>
* <span data-ttu-id="26833-363">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-363">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="26833-364">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-364">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="26833-365">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-365">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="26833-366">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-366">SQL</span></span>
* <span data-ttu-id="26833-367">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-367">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="26833-368">VM</span><span class="sxs-lookup"><span data-stu-id="26833-368">VM</span></span>
* <span data-ttu-id="26833-369">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-369">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="26833-370">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-370">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="26833-371">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-371">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="26833-372">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-372">Added new `ppg` command group for manging Proximity Placement Groups</span></span>
* <span data-ttu-id="26833-373">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-373">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="26833-374">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-374">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="26833-375">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="26833-375">April 23, 2019</span></span>

<span data-ttu-id="26833-376">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="26833-376">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="26833-377">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-377">ACS</span></span>
* <span data-ttu-id="26833-378">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-378">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="26833-379">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-379">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="26833-380">AMS</span><span class="sxs-lookup"><span data-stu-id="26833-380">AMS</span></span>
* <span data-ttu-id="26833-381">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-381">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-382">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-382">AppService</span></span>
* <span data-ttu-id="26833-383">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-383">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="26833-384">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-384">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="26833-385">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-385">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="26833-386">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-386">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="26833-387">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-387">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="26833-388">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-388">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="26833-389">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-389">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="26833-390">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-390">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="26833-391">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-391">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="26833-392">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="26833-392">Deployment Manager</span></span>
* <span data-ttu-id="26833-393">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="26833-393">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="26833-394">ラボ</span><span class="sxs-lookup"><span data-stu-id="26833-394">Lab</span></span>
* <span data-ttu-id="26833-395">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-395">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="26833-396">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-396">Network</span></span>
* <span data-ttu-id="26833-397">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-397">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="26833-398">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-398">Resource</span></span>
* <span data-ttu-id="26833-399">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="26833-399">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="26833-400">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="26833-400">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="26833-401">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-401">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="26833-402">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-402">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="26833-403">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-403">SQL</span></span>
* <span data-ttu-id="26833-404">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-404">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="26833-405">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-405">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="26833-406">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-406">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="26833-407">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-407">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-408">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-408">Storage</span></span>
* <span data-ttu-id="26833-409">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-409">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="26833-410">VM</span><span class="sxs-lookup"><span data-stu-id="26833-410">VM</span></span>
* <span data-ttu-id="26833-411">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-411">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="26833-412">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-412">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="26833-413">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-413">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="26833-414">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="26833-414">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="26833-415">コア</span><span class="sxs-lookup"><span data-stu-id="26833-415">Core</span></span>
* <span data-ttu-id="26833-416">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-416">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="26833-417">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-417">ACR</span></span>
* <span data-ttu-id="26833-418">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-418">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="26833-419">AMS</span><span class="sxs-lookup"><span data-stu-id="26833-419">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="26833-422">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-422">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="26833-423">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-423">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-424">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-424">AppService</span></span>
* <span data-ttu-id="26833-425">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-425">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="26833-426">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-426">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="26833-427">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-427">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="26833-428">[重大な変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="26833-428">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="26833-429">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-429">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="26833-430">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-430">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="26833-431">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-431">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="26833-432">CDN</span><span class="sxs-lookup"><span data-stu-id="26833-432">CDN</span></span>
* <span data-ttu-id="26833-433">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-433">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="26833-434">フィードバック</span><span class="sxs-lookup"><span data-stu-id="26833-434">Feedback</span></span>
* <span data-ttu-id="26833-435">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-435">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="26833-436">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-436">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="26833-437">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-437">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-438">監視</span><span class="sxs-lookup"><span data-stu-id="26833-438">Monitor</span></span>
* <span data-ttu-id="26833-439">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-439">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="26833-440">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-440">Network</span></span>
* <span data-ttu-id="26833-441">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-441">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="26833-442">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-442">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="26833-443">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-443">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="26833-444">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-444">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="26833-445">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="26833-445">PrivateDNS</span></span>
* <span data-ttu-id="26833-446">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-446">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="26833-447">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-447">Resource</span></span>
* <span data-ttu-id="26833-448">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-448">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="26833-449">Role</span><span class="sxs-lookup"><span data-stu-id="26833-449">Role</span></span>
* <span data-ttu-id="26833-450">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-450">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="26833-451">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-451">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="26833-452">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-452">SQL</span></span>
* <span data-ttu-id="26833-453">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-453">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="26833-454">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-454">Storage</span></span>
* <span data-ttu-id="26833-455">[重大な変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-455">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="26833-456">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-456">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="26833-457">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-457">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="26833-458">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-458">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="26833-459">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="26833-459">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="26833-460">コア</span><span class="sxs-lookup"><span data-stu-id="26833-460">Core</span></span>
* <span data-ttu-id="26833-461">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-461">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="26833-462">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-462">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="26833-463">クラウド</span><span class="sxs-lookup"><span data-stu-id="26833-463">Cloud</span></span>
* <span data-ttu-id="26833-464">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-464">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="26833-465">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-465">ACR</span></span>
* <span data-ttu-id="26833-466">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-466">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="26833-467">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-467">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="26833-468">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-468">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="26833-469">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-469">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-470">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-470">AppService</span></span>
* <span data-ttu-id="26833-471">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-471">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="26833-472">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-472">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="26833-473">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="26833-473">BOT Service</span></span>
* <span data-ttu-id="26833-474">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-474">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="26833-475">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-475">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="26833-476">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-476">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="26833-477">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-477">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="26833-478">CDN</span><span class="sxs-lookup"><span data-stu-id="26833-478">CDN</span></span>
* <span data-ttu-id="26833-479">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-479">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="26833-481">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="26833-481">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="26833-482">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-482">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="26833-483">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="26833-483">Cosmosdb</span></span>
* <span data-ttu-id="26833-484">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-484">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="26833-485">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-485">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-486">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-486">Interactive</span></span>
* <span data-ttu-id="26833-487">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-487">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-488">監視</span><span class="sxs-lookup"><span data-stu-id="26833-488">Monitor</span></span>
* <span data-ttu-id="26833-489">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-489">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="26833-490">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-490">Network</span></span>
* <span data-ttu-id="26833-491">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-491">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="26833-492">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-492">Profile</span></span>
* <span data-ttu-id="26833-493">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-493">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="26833-494">Postgres</span><span class="sxs-lookup"><span data-stu-id="26833-494">Postgres</span></span> 
* <span data-ttu-id="26833-495">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-495">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="26833-496">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="26833-496">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="26833-497">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-497">Resource</span></span>
* <span data-ttu-id="26833-498">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-498">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="26833-499">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-499">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="26833-500">Graph</span><span class="sxs-lookup"><span data-stu-id="26833-500">Graph</span></span>
* <span data-ttu-id="26833-501">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-501">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="26833-502">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-502">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="26833-503">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-503">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="26833-504">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-504">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="26833-505">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-505">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="26833-506">storage</span><span class="sxs-lookup"><span data-stu-id="26833-506">storage</span></span>
* <span data-ttu-id="26833-507">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-507">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="26833-508">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-508">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="26833-509">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-509">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="26833-510">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-510">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="26833-511">VM</span><span class="sxs-lookup"><span data-stu-id="26833-511">VM</span></span>
* <span data-ttu-id="26833-512">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-512">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="26833-513">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="26833-513">March 12, 2019</span></span>

<span data-ttu-id="26833-514">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="26833-514">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="26833-515">コア</span><span class="sxs-lookup"><span data-stu-id="26833-515">Core</span></span>

* <span data-ttu-id="26833-516">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-516">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="26833-517">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-517">ACR</span></span>

* <span data-ttu-id="26833-518">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-518">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="26833-519">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-519">ACS</span></span>

* <span data-ttu-id="26833-520">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-520">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="26833-521">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-521">AppService</span></span>

* <span data-ttu-id="26833-522">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-522">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="26833-523">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-523">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="26833-524">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-524">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="26833-525">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-525">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="26833-526">Botservice</span><span class="sxs-lookup"><span data-stu-id="26833-526">Botservice</span></span>

* <span data-ttu-id="26833-527">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-527">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="26833-528">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-528">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="26833-529">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-529">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="26833-530">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-530">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="26833-531">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-531">Container</span></span>

* <span data-ttu-id="26833-532">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-532">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="26833-533">EventHub</span><span class="sxs-lookup"><span data-stu-id="26833-533">EventHub</span></span>

* <span data-ttu-id="26833-534">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-534">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="26833-535">Find</span><span class="sxs-lookup"><span data-stu-id="26833-535">Find</span></span>

* <span data-ttu-id="26833-536">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="26833-536">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="26833-537">HDInsight</span><span class="sxs-lookup"><span data-stu-id="26833-537">HDInsight</span></span>

* <span data-ttu-id="26833-538">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-538">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="26833-539">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-539">Network</span></span>

* <span data-ttu-id="26833-540">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-540">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-541">Rdbms</span><span class="sxs-lookup"><span data-stu-id="26833-541">Rdbms</span></span>

* <span data-ttu-id="26833-542">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="26833-542">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="26833-543">Role</span><span class="sxs-lookup"><span data-stu-id="26833-543">Role</span></span>

* <span data-ttu-id="26833-544">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-544">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="26833-545">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-545">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="26833-546">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="26833-546">Service Fabric</span></span>

* <span data-ttu-id="26833-547">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-547">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="26833-548">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="26833-548">February 26, 2019</span></span>

<span data-ttu-id="26833-549">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="26833-549">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="26833-550">コア</span><span class="sxs-lookup"><span data-stu-id="26833-550">Core</span></span>

* <span data-ttu-id="26833-551">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-551">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="26833-552">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-552">ACR</span></span>

* <span data-ttu-id="26833-553">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-553">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="26833-554">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-554">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="26833-555">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-555">ACS</span></span>

* <span data-ttu-id="26833-556">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-556">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-557">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-557">AppService</span></span>

* <span data-ttu-id="26833-558">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-558">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="26833-559">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-559">Batch</span></span>
* <span data-ttu-id="26833-560">[重大な変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-560">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="26833-561">[重大な変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-561">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="26833-562">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-562">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="26833-563">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-563">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="26833-564">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-564">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="26833-565">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="26833-565">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="26833-566">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-566">CosmosDB</span></span>

* <span data-ttu-id="26833-567">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-567">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="26833-568">Kusto</span><span class="sxs-lookup"><span data-stu-id="26833-568">Kusto</span></span>

* <span data-ttu-id="26833-569">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-569">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="26833-570">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-570">Network</span></span>

* <span data-ttu-id="26833-571">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-571">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="26833-572">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-572">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="26833-573">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-573">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="26833-574">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-574">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="26833-575">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-575">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="26833-576">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-576">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="26833-577">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-577">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="26833-578">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-578">Resource</span></span>

* <span data-ttu-id="26833-579">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-579">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="26833-580">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-580">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="26833-581">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-581">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="26833-582">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-582">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="26833-583">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-583">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="26833-584">Role</span><span class="sxs-lookup"><span data-stu-id="26833-584">Role</span></span>

* <span data-ttu-id="26833-585">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-585">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="26833-586">VM</span><span class="sxs-lookup"><span data-stu-id="26833-586">VM</span></span>

* <span data-ttu-id="26833-587">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-587">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="26833-588">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="26833-588">February 12, 2019</span></span>

<span data-ttu-id="26833-589">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="26833-589">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="26833-590">コア</span><span class="sxs-lookup"><span data-stu-id="26833-590">Core</span></span>

* <span data-ttu-id="26833-591">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-591">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="26833-592">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-592">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="26833-593">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-593">ACR</span></span>
* <span data-ttu-id="26833-594">[重大な変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-594">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="26833-595">[重大な変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-595">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="26833-596">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-596">ACS</span></span>
* <span data-ttu-id="26833-597">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-597">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="26833-598">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-598">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="26833-599">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-599">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="26833-600">AMS</span><span class="sxs-lookup"><span data-stu-id="26833-600">AMS</span></span>
* <span data-ttu-id="26833-601">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-601">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="26833-602">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-602">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-603">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-603">Appservice</span></span>
* <span data-ttu-id="26833-604">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-604">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="26833-605">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-605">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="26833-606">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-606">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="26833-607">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-607">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="26833-608">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-608">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="26833-609">Botservice</span><span class="sxs-lookup"><span data-stu-id="26833-609">Botservice</span></span>
* <span data-ttu-id="26833-610">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-610">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="26833-611">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-611">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="26833-612">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-612">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="26833-613">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-613">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="26833-614">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-614">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="26833-615">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-615">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="26833-616">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-616">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="26833-617">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-617">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="26833-618">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="26833-618">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="26833-619">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-619">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="26833-620">Key Vault</span><span class="sxs-lookup"><span data-stu-id="26833-620">Key Vault</span></span>
* <span data-ttu-id="26833-621">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-621">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-622">監視</span><span class="sxs-lookup"><span data-stu-id="26833-622">Monitor</span></span>
* <span data-ttu-id="26833-623">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-623">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="26833-624">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-624">Network</span></span>
* <span data-ttu-id="26833-625">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-625">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="26833-626">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-626">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="26833-627">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-627">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="26833-628">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-628">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="26833-629">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="26833-629">Policy Insights</span></span>
* <span data-ttu-id="26833-630">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-630">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-631">RDBMS</span><span class="sxs-lookup"><span data-stu-id="26833-631">RDBMS</span></span>
* <span data-ttu-id="26833-632">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-632">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="26833-633">Redis</span><span class="sxs-lookup"><span data-stu-id="26833-633">Redis</span></span>
* <span data-ttu-id="26833-634">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-634">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="26833-635">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-635">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="26833-636">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-636">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="26833-637">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-637">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="26833-638">[重大な変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-638">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="26833-639">[重大な変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="26833-639">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="26833-640">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-640">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="26833-641">Role</span><span class="sxs-lookup"><span data-stu-id="26833-641">Role</span></span>
* <span data-ttu-id="26833-642">[重大な変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="26833-642">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="26833-643">SQL VM</span><span class="sxs-lookup"><span data-stu-id="26833-643">SQL VM</span></span>
* <span data-ttu-id="26833-644">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-644">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="26833-645">VM</span><span class="sxs-lookup"><span data-stu-id="26833-645">VM</span></span>
* <span data-ttu-id="26833-646">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-646">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="26833-647">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-647">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="26833-648">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-648">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="26833-649">[重大な変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="26833-649">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="26833-650">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="26833-650">January 31, 2019</span></span>

<span data-ttu-id="26833-651">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="26833-651">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="26833-652">コア</span><span class="sxs-lookup"><span data-stu-id="26833-652">Core</span></span>

* <span data-ttu-id="26833-653">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="26833-653">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="26833-654">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="26833-654">January 28, 2019</span></span>

<span data-ttu-id="26833-655">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="26833-655">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="26833-656">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-656">ACR</span></span>
* <span data-ttu-id="26833-657">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-657">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="26833-658">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-658">ACS</span></span>
* <span data-ttu-id="26833-659">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-659">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="26833-660">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-660">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="26833-661">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-661">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="26833-662">AMS</span><span class="sxs-lookup"><span data-stu-id="26833-662">AMS</span></span>
* <span data-ttu-id="26833-663">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-663">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="26833-664">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-664">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-665">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-665">Appservice</span></span>
* <span data-ttu-id="26833-666">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-666">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="26833-667">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-667">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="26833-668">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-668">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="26833-669">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-669">Container</span></span>
* <span data-ttu-id="26833-670">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-670">Added `container start` command</span></span>
* <span data-ttu-id="26833-671">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-671">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="26833-672">EventGrid</span><span class="sxs-lookup"><span data-stu-id="26833-672">EventGrid</span></span>
* <span data-ttu-id="26833-673">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-673">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="26833-674">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-674">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="26833-675">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-675">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="26833-676">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-676">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="26833-677">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="26833-677">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="26833-678">HDInsight</span><span class="sxs-lookup"><span data-stu-id="26833-678">HDInsight</span></span>
* <span data-ttu-id="26833-679">[重大な変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-679">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="26833-680">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-680">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="26833-681">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-681">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="26833-682">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-682">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="26833-683">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-683">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="26833-684">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-684">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="26833-685">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-685">IoT</span></span>
* <span data-ttu-id="26833-686">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-686">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="26833-687">Kusto</span><span class="sxs-lookup"><span data-stu-id="26833-687">Kusto</span></span>
* <span data-ttu-id="26833-688">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="26833-688">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-689">監視</span><span class="sxs-lookup"><span data-stu-id="26833-689">Monitor</span></span>
* <span data-ttu-id="26833-690">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-690">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="26833-691">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-691">Profile</span></span>
* <span data-ttu-id="26833-692">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-692">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="26833-693">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-693">Network</span></span>
* <span data-ttu-id="26833-694">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-694">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="26833-695">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-695">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="26833-696">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-696">Resource</span></span>
* <span data-ttu-id="26833-697">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-697">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="26833-698">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-698">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="26833-699">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="26833-699">SQL Virtual Machine</span></span>
* <span data-ttu-id="26833-700">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="26833-700">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="26833-701">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-701">Storage</span></span>
* <span data-ttu-id="26833-702">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-702">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="26833-703">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="26833-703">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="26833-704">VM</span><span class="sxs-lookup"><span data-stu-id="26833-704">VM</span></span>
* <span data-ttu-id="26833-705">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-705">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="26833-706">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-706">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="26833-707">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="26833-707">January 15, 2019</span></span>

<span data-ttu-id="26833-708">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="26833-708">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="26833-709">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-709">ACR</span></span>
* <span data-ttu-id="26833-710">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-710">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="26833-711">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-711">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="26833-712">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-712">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="26833-713">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-713">ACS</span></span>
* <span data-ttu-id="26833-714">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-714">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-715">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-715">Appservice</span></span>
* <span data-ttu-id="26833-716">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-716">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="26833-717">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-717">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="26833-718">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-718">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="26833-719">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-719">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="26833-720">Botservice</span><span class="sxs-lookup"><span data-stu-id="26833-720">Botservice</span></span>
* <span data-ttu-id="26833-721">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-721">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="26833-722">構成</span><span class="sxs-lookup"><span data-stu-id="26833-722">Configure</span></span>
* <span data-ttu-id="26833-723">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-723">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="26833-724">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-724">CosmosDB</span></span>
* <span data-ttu-id="26833-725">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-725">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="26833-726">HDInsight</span><span class="sxs-lookup"><span data-stu-id="26833-726">HDInsight</span></span>
* <span data-ttu-id="26833-727">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-727">Added commands for managing applications</span></span>
* <span data-ttu-id="26833-728">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-728">Added commands for managing script actions</span></span>
* <span data-ttu-id="26833-729">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-729">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="26833-730">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-730">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="26833-731">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-731">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="26833-732">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-732">Network</span></span>
* <span data-ttu-id="26833-733">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-733">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="26833-734">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-734">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="26833-735">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-735">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="26833-736">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-736">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="26833-737">Role</span><span class="sxs-lookup"><span data-stu-id="26833-737">Role</span></span>
* <span data-ttu-id="26833-738">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="26833-738">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="26833-739">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="26833-739">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="26833-740">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="26833-740">Security</span></span>
* <span data-ttu-id="26833-741">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-741">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="26833-742">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-742">Storage</span></span>
* <span data-ttu-id="26833-743">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-743">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="26833-744">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="26833-744">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="26833-745">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-745">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="26833-746">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-746">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="26833-747">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-747">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="26833-748">VM</span><span class="sxs-lookup"><span data-stu-id="26833-748">VM</span></span>
* <span data-ttu-id="26833-749">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-749">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="26833-750">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-750">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="26833-751">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-751">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="26833-752">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-752">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="26833-753">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-753">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="26833-754">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-754">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="26833-755">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="26833-755">December 20, 2018</span></span>

<span data-ttu-id="26833-756">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="26833-756">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="26833-757">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-757">Appservice</span></span>
* <span data-ttu-id="26833-758">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-758">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="26833-759">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-759">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="26833-760">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-760">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="26833-761">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="26833-761">IoTCentral</span></span>
* <span data-ttu-id="26833-762">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-762">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="26833-763">Role</span><span class="sxs-lookup"><span data-stu-id="26833-763">Role</span></span>
* <span data-ttu-id="26833-764">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-764">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="26833-765">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-765">SQL</span></span>
* <span data-ttu-id="26833-766">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-766">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="26833-767">VM</span><span class="sxs-lookup"><span data-stu-id="26833-767">VM</span></span>
* <span data-ttu-id="26833-768">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-768">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="26833-769">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="26833-769">December 18, 2018</span></span>

<span data-ttu-id="26833-770">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="26833-770">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="26833-771">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-771">ACR</span></span>
* <span data-ttu-id="26833-772">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-772">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="26833-773">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="26833-773">Condensed the table layout for task list</span></span>
* <span data-ttu-id="26833-774">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-774">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="26833-775">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-775">ACS</span></span>
* <span data-ttu-id="26833-776">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-776">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="26833-777">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-777">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="26833-778">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="26833-778">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="26833-779">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="26833-779">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="26833-780">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-780">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="26833-781">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-781">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-782">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-782">Appservice</span></span>
* <span data-ttu-id="26833-783">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-783">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="26833-784">Botservice</span><span class="sxs-lookup"><span data-stu-id="26833-784">Botservice</span></span>
* <span data-ttu-id="26833-785">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-785">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="26833-786">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-786">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="26833-787">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-787">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="26833-788">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="26833-788">Reduced Kudu network calls</span></span>
* <span data-ttu-id="26833-789">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-789">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="26833-790">消費</span><span class="sxs-lookup"><span data-stu-id="26833-790">Consumption</span></span>
* <span data-ttu-id="26833-791">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-791">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="26833-792">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-792">CosmosDB</span></span>
* <span data-ttu-id="26833-793">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-793">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="26833-794">マップ</span><span class="sxs-lookup"><span data-stu-id="26833-794">Maps</span></span>
* <span data-ttu-id="26833-795">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-795">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="26833-796">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-796">Network</span></span>
* <span data-ttu-id="26833-797">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-797">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="26833-798">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-798">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="26833-799">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-799">Resource</span></span>
* <span data-ttu-id="26833-800">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-800">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="26833-801">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-801">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-802">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-802">Storage</span></span>
*  <span data-ttu-id="26833-803">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-803">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="26833-804">VM</span><span class="sxs-lookup"><span data-stu-id="26833-804">VM</span></span>
* <span data-ttu-id="26833-805">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-805">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="26833-806">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="26833-806">December 4, 2018</span></span>

<span data-ttu-id="26833-807">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="26833-807">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="26833-808">コア</span><span class="sxs-lookup"><span data-stu-id="26833-808">Core</span></span>
* <span data-ttu-id="26833-809">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-809">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="26833-810">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-810">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-811">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-811">Appservice</span></span>
* <span data-ttu-id="26833-812">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-812">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="26833-813">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-813">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="26833-814">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-814">Network</span></span>
* <span data-ttu-id="26833-815">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-815">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="26833-816">Role</span><span class="sxs-lookup"><span data-stu-id="26833-816">Role</span></span>
* <span data-ttu-id="26833-817">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-817">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="26833-818">VM</span><span class="sxs-lookup"><span data-stu-id="26833-818">VM</span></span>
* <span data-ttu-id="26833-819">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-819">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="26833-820">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-820">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="26833-821">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-821">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="26833-822">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-822">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="26833-823">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="26833-823">November 20, 2018</span></span>

<span data-ttu-id="26833-824">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="26833-824">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="26833-825">コア</span><span class="sxs-lookup"><span data-stu-id="26833-825">Core</span></span>
* <span data-ttu-id="26833-826">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-826">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="26833-827">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-827">ACR</span></span>
* <span data-ttu-id="26833-828">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-828">Added context token to task step</span></span>
* <span data-ttu-id="26833-829">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-829">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="26833-830">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-830">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-831">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-831">Appservice</span></span>
* <span data-ttu-id="26833-832">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-832">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="26833-833">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="26833-833">Updated the default `node_version`.</span></span> <span data-ttu-id="26833-834">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="26833-834">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="26833-835">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-835">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="26833-836">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-836">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="26833-837">IotCentral</span><span class="sxs-lookup"><span data-stu-id="26833-837">IotCentral</span></span>
* <span data-ttu-id="26833-838">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-838">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="26833-839">KeyVault</span><span class="sxs-lookup"><span data-stu-id="26833-839">KeyVault</span></span>
* <span data-ttu-id="26833-840">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-840">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="26833-841">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-841">Network</span></span>
* <span data-ttu-id="26833-842">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-842">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="26833-843">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-843">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="26833-844">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-844">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="26833-845">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-845">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-846">Rdbms</span><span class="sxs-lookup"><span data-stu-id="26833-846">Rdbms</span></span>
* <span data-ttu-id="26833-847">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-847">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="26833-848">Rbac</span><span class="sxs-lookup"><span data-stu-id="26833-848">Rbac</span></span>
* <span data-ttu-id="26833-849">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-849">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="26833-850">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-850">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="26833-851">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-851">Storage</span></span>
* <span data-ttu-id="26833-852">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-852">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="26833-853">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-853">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="26833-854">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-854">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="26833-855">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="26833-855">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="26833-856">VM</span><span class="sxs-lookup"><span data-stu-id="26833-856">VM</span></span>
* <span data-ttu-id="26833-857">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-857">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="26833-858">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-858">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="26833-859">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="26833-859">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="26833-860">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-860">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="26833-861">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-861">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="26833-862">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-862">Added `snapshot wait` command</span></span>
* <span data-ttu-id="26833-863">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-863">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="26833-864">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="26833-864">November 6, 2018</span></span>

<span data-ttu-id="26833-865">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="26833-865">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="26833-866">コア</span><span class="sxs-lookup"><span data-stu-id="26833-866">Core</span></span>
* <span data-ttu-id="26833-867">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-867">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="26833-868">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-868">ACR</span></span>
* <span data-ttu-id="26833-869">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-869">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="26833-870">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-870">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="26833-871">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-871">ACS</span></span>
* <span data-ttu-id="26833-872">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-872">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="26833-873">Advisor</span><span class="sxs-lookup"><span data-stu-id="26833-873">Advisor</span></span>
* <span data-ttu-id="26833-874">GA リリース</span><span class="sxs-lookup"><span data-stu-id="26833-874">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="26833-875">AMS</span><span class="sxs-lookup"><span data-stu-id="26833-875">AMS</span></span>
* <span data-ttu-id="26833-876">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-876">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="26833-877">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-877">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="26833-878">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-878">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="26833-879">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-879">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="26833-880">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-880">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="26833-881">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-881">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="26833-882">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-882">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="26833-883">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="26833-883">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="26833-884">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-884">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="26833-885">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-885">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="26833-886">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="26833-886">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="26833-887">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="26833-887">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="26833-888">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="26833-888">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="26833-889">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="26833-889">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="26833-890">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-890">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="26833-891">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="26833-891">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="26833-892">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="26833-892">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-893">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-893">AppService</span></span>
* <span data-ttu-id="26833-894">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-894">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="26833-895">構成</span><span class="sxs-lookup"><span data-stu-id="26833-895">Configure</span></span>
* <span data-ttu-id="26833-896">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-896">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="26833-897">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-897">Container</span></span>
* <span data-ttu-id="26833-898">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-898">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="26833-899">EventHub</span><span class="sxs-lookup"><span data-stu-id="26833-899">EventHub</span></span>
* <span data-ttu-id="26833-900">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-900">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-901">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-901">Interactive</span></span>
* <span data-ttu-id="26833-902">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="26833-902">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-903">監視</span><span class="sxs-lookup"><span data-stu-id="26833-903">Monitor</span></span>
* <span data-ttu-id="26833-904">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-904">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="26833-905">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-905">Network</span></span>
* <span data-ttu-id="26833-906">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-906">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="26833-907">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-907">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="26833-908">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-908">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="26833-909">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-909">Profile</span></span>
* <span data-ttu-id="26833-910">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-910">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-911">RDBMS</span><span class="sxs-lookup"><span data-stu-id="26833-911">RDBMS</span></span>
* <span data-ttu-id="26833-912">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-912">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="26833-913">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-913">Resource</span></span>
* <span data-ttu-id="26833-914">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-914">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="26833-915">Role</span><span class="sxs-lookup"><span data-stu-id="26833-915">Role</span></span>
* <span data-ttu-id="26833-916">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-916">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="26833-917">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-917">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="26833-918">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-918">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="26833-919">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-919">Storage</span></span>
* <span data-ttu-id="26833-920">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="26833-920">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="26833-921">VM</span><span class="sxs-lookup"><span data-stu-id="26833-921">VM</span></span>
* <span data-ttu-id="26833-922">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-922">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="26833-923">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-923">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="26833-924">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-924">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="26833-925">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-925">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="26833-926">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="26833-926">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="26833-927">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-927">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="26833-928">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="26833-928">October 23, 2018</span></span>

<span data-ttu-id="26833-929">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="26833-929">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="26833-930">コア</span><span class="sxs-lookup"><span data-stu-id="26833-930">Core</span></span>
* <span data-ttu-id="26833-931">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-931">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="26833-932">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-932">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="26833-933">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-933">ACR</span></span>
* <span data-ttu-id="26833-934">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-934">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="26833-935">CDN</span><span class="sxs-lookup"><span data-stu-id="26833-935">CDN</span></span>
* <span data-ttu-id="26833-936">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="26833-936">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="26833-937">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-937">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="26833-938">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-938">Container</span></span>
* <span data-ttu-id="26833-939">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-939">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="26833-940">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-940">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="26833-941">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-941">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="26833-942">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-942">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="26833-943">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-943">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="26833-944">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-944">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="26833-945">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-945">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="26833-946">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-946">CosmosDB</span></span>
* <span data-ttu-id="26833-947">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-947">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-948">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-948">Interactive</span></span>
* <span data-ttu-id="26833-949">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-949">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="26833-950">IoT Central</span><span class="sxs-lookup"><span data-stu-id="26833-950">IoT Central</span></span>
* <span data-ttu-id="26833-951">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-951">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="26833-952">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="26833-952">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-953">監視</span><span class="sxs-lookup"><span data-stu-id="26833-953">Monitor</span></span>
* <span data-ttu-id="26833-954">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="26833-954">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="26833-955">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-955">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="26833-956">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-956">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="26833-957">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-957">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="26833-958">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-958">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="26833-959">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-959">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="26833-960">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="26833-960">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="26833-961">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-961">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="26833-962">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-962">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="26833-963">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-963">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="26833-964">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-964">Network</span></span>
* <span data-ttu-id="26833-965">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-965">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="26833-966">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-966">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="26833-967">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="26833-967">ServiceBus</span></span>
* <span data-ttu-id="26833-968">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-968">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="26833-969">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-969">SQL</span></span>
* <span data-ttu-id="26833-970">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-970">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="26833-971">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-971">Storage</span></span>
* <span data-ttu-id="26833-972">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-972">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="26833-973">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-973">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="26833-974">VM</span><span class="sxs-lookup"><span data-stu-id="26833-974">VM</span></span>
* <span data-ttu-id="26833-975">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="26833-975">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="26833-976">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-976">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="26833-977">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-977">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="26833-978">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="26833-978">October 16, 2018</span></span>

<span data-ttu-id="26833-979">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="26833-979">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="26833-980">VM</span><span class="sxs-lookup"><span data-stu-id="26833-980">VM</span></span>
* <span data-ttu-id="26833-981">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-981">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="26833-982">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="26833-982">October 9, 2018</span></span>

<span data-ttu-id="26833-983">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="26833-983">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="26833-984">コア</span><span class="sxs-lookup"><span data-stu-id="26833-984">Core</span></span>
* <span data-ttu-id="26833-985">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-985">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="26833-986">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-986">ACR</span></span>
* <span data-ttu-id="26833-987">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-987">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="26833-988">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-988">ACS</span></span>
* <span data-ttu-id="26833-989">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="26833-989">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="26833-990">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-990">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="26833-991">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-991">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="26833-992">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-992">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="26833-993">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-993">Container</span></span>
* <span data-ttu-id="26833-994">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-994">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="26833-995">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-995">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="26833-996">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="26833-996">Event Hub</span></span>
* <span data-ttu-id="26833-997">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-997">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="26833-998">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-998">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="26833-999">Extensions</span><span class="sxs-lookup"><span data-stu-id="26833-999">Extensions</span></span>
* <span data-ttu-id="26833-1000">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1000">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="26833-1001">HDInsight</span><span class="sxs-lookup"><span data-stu-id="26833-1001">HDInsight</span></span>
* <span data-ttu-id="26833-1002">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-1002">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="26833-1003">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-1003">IoT</span></span>
* <span data-ttu-id="26833-1004">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1004">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="26833-1005">KeyVault</span><span class="sxs-lookup"><span data-stu-id="26833-1005">KeyVault</span></span>
* <span data-ttu-id="26833-1006">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1006">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="26833-1007">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1007">Network</span></span>
* <span data-ttu-id="26833-1008">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="26833-1008">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="26833-1009">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="26833-1009">See #6052</span></span>
* <span data-ttu-id="26833-1010">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1010">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="26833-1011">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="26833-1011">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="26833-1012">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1012">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="26833-1013">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1013">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="26833-1014">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1014">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="26833-1015">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1015">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="26833-1016">Role</span><span class="sxs-lookup"><span data-stu-id="26833-1016">Role</span></span>
* <span data-ttu-id="26833-1017">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1017">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="26833-1018">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1018">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="26833-1019">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1019">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="26833-1020">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1020">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="26833-1021">Service Bus</span><span class="sxs-lookup"><span data-stu-id="26833-1021">Service Bus</span></span>
* <span data-ttu-id="26833-1022">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1022">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1023">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1023">VM</span></span>
* <span data-ttu-id="26833-1024">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1024">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="26833-1025">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1025">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="26833-1026">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1026">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="26833-1027">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1027">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="26833-1028">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1028">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="26833-1029">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1029">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="26833-1030">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="26833-1030">September 21, 2018</span></span>

<span data-ttu-id="26833-1031">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="26833-1031">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1032">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1032">ACR</span></span>
* <span data-ttu-id="26833-1033">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1033">Added ACR Task commands</span></span>
* <span data-ttu-id="26833-1034">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1034">Added quick run command</span></span>
* <span data-ttu-id="26833-1035">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1035">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="26833-1036">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1036">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="26833-1037">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1037">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="26833-1038">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1038">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1039">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1039">ACS</span></span>
* <span data-ttu-id="26833-1040">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1040">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="26833-1041">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1041">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1042">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-1042">AppService</span></span>

* <span data-ttu-id="26833-1043">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1043">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="26833-1044">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1044">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="26833-1045">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1045">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="26833-1046">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1046">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="26833-1047">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-1047">Batch</span></span>
* <span data-ttu-id="26833-1048">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1048">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="26833-1049">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-1049">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="26833-1050">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1050">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="26833-1051">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1051">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="26833-1052">Batch AI</span><span class="sxs-lookup"><span data-stu-id="26833-1052">Batch AI</span></span> 
* <span data-ttu-id="26833-1053">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1053">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="26833-1054">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="26833-1054">Cognitive Services</span></span>
* <span data-ttu-id="26833-1055">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1055">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="26833-1056">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1056">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="26833-1057">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1057">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="26833-1058">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1058">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="26833-1059">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1059">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="26833-1060">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1060">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="26833-1061">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1061">Container</span></span>
* <span data-ttu-id="26833-1062">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1062">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="26833-1063">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1063">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="26833-1064">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1064">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="26833-1065">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1065">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="26833-1066">DataLake</span><span class="sxs-lookup"><span data-stu-id="26833-1066">Datalake</span></span>
* <span data-ttu-id="26833-1067">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1067">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="26833-1068">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="26833-1068">Interactive Shell</span></span>
* <span data-ttu-id="26833-1069">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1069">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="26833-1070">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1070">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="26833-1071">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-1071">IoT</span></span>
* <span data-ttu-id="26833-1072">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1072">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="26833-1073">Key Vault</span><span class="sxs-lookup"><span data-stu-id="26833-1073">Key Vault</span></span>
* <span data-ttu-id="26833-1074">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1074">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="26833-1075">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1075">Network</span></span>
* <span data-ttu-id="26833-1076">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1076">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="26833-1077">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1077">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="26833-1078">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1078">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="26833-1079">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1079">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="26833-1080">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1080">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="26833-1081">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1081">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="26833-1082">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="26833-1082">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="26833-1083">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-1083">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="26833-1084">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1084">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="26833-1085">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1085">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="26833-1086">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1086">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="26833-1087">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1087">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="26833-1088">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1088">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="26833-1089">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="26833-1089">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="26833-1090">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1090">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="26833-1091">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1091">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="26833-1092">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1092">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="26833-1093">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1093">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-1094">RDBMS</span><span class="sxs-lookup"><span data-stu-id="26833-1094">RDBMS</span></span>
* <span data-ttu-id="26833-1095">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1095">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="26833-1096">予約</span><span class="sxs-lookup"><span data-stu-id="26833-1096">Reservation</span></span>
* <span data-ttu-id="26833-1097">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1097">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="26833-1098">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1098">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="26833-1099">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="26833-1099">Manage App</span></span>
* <span data-ttu-id="26833-1100">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1100">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="26833-1101">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1101">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="26833-1102">Role</span><span class="sxs-lookup"><span data-stu-id="26833-1102">Role</span></span>
* <span data-ttu-id="26833-1103">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1103">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="26833-1104">SignalR</span><span class="sxs-lookup"><span data-stu-id="26833-1104">SignalR</span></span>
* <span data-ttu-id="26833-1105">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-1105">First release</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1106">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1106">Storage</span></span>
* <span data-ttu-id="26833-1107">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1107">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="26833-1108">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1108">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1109">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1109">VM</span></span>
* <span data-ttu-id="26833-1110">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="26833-1110">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="26833-1111">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1111">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="26833-1112">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="26833-1112">August 28, 2018</span></span>

<span data-ttu-id="26833-1113">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="26833-1113">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="26833-1114">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1114">Core</span></span>

* <span data-ttu-id="26833-1115">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1115">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="26833-1116">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1116">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1117">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1117">ACR</span></span>

* <span data-ttu-id="26833-1118">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1118">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="26833-1119">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1119">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1120">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1120">ACS</span></span>

* <span data-ttu-id="26833-1121">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1121">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="26833-1122">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1122">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1123">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-1123">AppService</span></span>

* <span data-ttu-id="26833-1124">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1124">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="26833-1125">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1125">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="26833-1126">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1126">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="26833-1127">バックアップ</span><span class="sxs-lookup"><span data-stu-id="26833-1127">Backup</span></span>

* <span data-ttu-id="26833-1128">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1128">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="26833-1129">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="26833-1129">Bot Service</span></span>

* <span data-ttu-id="26833-1130">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="26833-1130">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="26833-1131">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="26833-1131">Cognitive Services</span></span>

* <span data-ttu-id="26833-1132">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1132">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="26833-1133">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-1133">IoT</span></span>

* <span data-ttu-id="26833-1134">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1134">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-1135">監視</span><span class="sxs-lookup"><span data-stu-id="26833-1135">Monitor</span></span>

* <span data-ttu-id="26833-1136">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1136">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="26833-1137">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1137">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="26833-1138">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1138">Network</span></span>

* <span data-ttu-id="26833-1139">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1139">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="26833-1140">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-1140">Resource</span></span>

* <span data-ttu-id="26833-1141">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1141">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1142">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1142">Storage</span></span>

* <span data-ttu-id="26833-1143">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1143">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1144">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1144">VM</span></span>

* <span data-ttu-id="26833-1145">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1145">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="26833-1146">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1146">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="26833-1147">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="26833-1147">Auguest 14, 2018</span></span>

<span data-ttu-id="26833-1148">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="26833-1148">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="26833-1149">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1149">Core</span></span>

* <span data-ttu-id="26833-1150">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1150">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="26833-1151">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1151">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="26833-1152">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="26833-1152">Telemetry</span></span>

* <span data-ttu-id="26833-1153">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1153">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1154">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1154">ACR</span></span>

* <span data-ttu-id="26833-1155">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1155">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="26833-1156">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1156">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1157">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1157">ACS</span></span>

* <span data-ttu-id="26833-1158">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1158">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="26833-1159">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1159">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="26833-1160">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1160">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="26833-1161">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1161">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="26833-1162">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1162">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="26833-1163">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-1163">AppService</span></span>

* <span data-ttu-id="26833-1164">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1164">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="26833-1165">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1165">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="26833-1166">BatchAI</span><span class="sxs-lookup"><span data-stu-id="26833-1166">BatchAI</span></span>

* <span data-ttu-id="26833-1167">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1167">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="26833-1168">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1168">Container</span></span>

* <span data-ttu-id="26833-1169">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1169">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="26833-1170">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-1170">IoT</span></span>

* <span data-ttu-id="26833-1171">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1171">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="26833-1172">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-1172">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="26833-1173">Iot Central</span><span class="sxs-lookup"><span data-stu-id="26833-1173">Iot Central</span></span>

* <span data-ttu-id="26833-1174">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-1174">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="26833-1175">KeyVault</span><span class="sxs-lookup"><span data-stu-id="26833-1175">KeyVault</span></span>


* <span data-ttu-id="26833-1176">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1176">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="26833-1177">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1177">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="26833-1178">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1178">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="26833-1179">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1179">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="26833-1180">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1180">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="26833-1181">リレー</span><span class="sxs-lookup"><span data-stu-id="26833-1181">Relay</span></span>

* <span data-ttu-id="26833-1182">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-1182">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="26833-1183">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-1183">Sql</span></span>

* <span data-ttu-id="26833-1184">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1184">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1185">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1185">Storage</span></span>

* <span data-ttu-id="26833-1186">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="26833-1186">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="26833-1187">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1187">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="26833-1188">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="26833-1188">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="26833-1189">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1189">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="26833-1190">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1190">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1191">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1191">VM</span></span>

* <span data-ttu-id="26833-1192">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1192">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="26833-1193">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="26833-1193">July 31, 2018</span></span>

<span data-ttu-id="26833-1194">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="26833-1194">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1195">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1195">ACR</span></span>

* <span data-ttu-id="26833-1196">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1196">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="26833-1197">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1197">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1198">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1198">ACS</span></span>

* <span data-ttu-id="26833-1199">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1199">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="26833-1200">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-1200">Batch</span></span>

* <span data-ttu-id="26833-1201">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1201">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="26833-1202">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1202">Container</span></span>

* <span data-ttu-id="26833-1203">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1203">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="26833-1204">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1204">Network</span></span>

* <span data-ttu-id="26833-1205">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1205">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="26833-1206">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-1206">Resource</span></span>

* <span data-ttu-id="26833-1207">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1207">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="26833-1208">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1208">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="26833-1209">Role</span><span class="sxs-lookup"><span data-stu-id="26833-1209">Role</span></span>

* <span data-ttu-id="26833-1210">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1210">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="26833-1211">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1211">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="26833-1212">Search</span><span class="sxs-lookup"><span data-stu-id="26833-1212">Search</span></span>

* <span data-ttu-id="26833-1213">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1213">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="26833-1214">Service Bus</span><span class="sxs-lookup"><span data-stu-id="26833-1214">Service Bus</span></span>

* <span data-ttu-id="26833-1215">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1215">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="26833-1216">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1216">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="26833-1217">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="26833-1217">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="26833-1218">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="26833-1218">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1219">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1219">Storage</span></span>

* <span data-ttu-id="26833-1220">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-1220">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="26833-1221">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="26833-1221">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1222">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1222">VM</span></span>

* <span data-ttu-id="26833-1223">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-1223">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="26833-1224">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1224">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="26833-1225">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1225">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="26833-1226">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1226">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="26833-1227">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="26833-1227">July 18, 2018</span></span>

<span data-ttu-id="26833-1228">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="26833-1228">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="26833-1229">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1229">Core</span></span>

* <span data-ttu-id="26833-1230">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1230">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="26833-1231">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1231">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="26833-1232">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1232">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1233">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1233">ACR</span></span>

* <span data-ttu-id="26833-1234">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-1234">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="26833-1235">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1235">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="26833-1236">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1236">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="26833-1237">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1237">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1238">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1238">ACS</span></span>

* <span data-ttu-id="26833-1239">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1239">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1240">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-1240">AppService</span></span>

* <span data-ttu-id="26833-1241">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1241">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="26833-1242">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-1242">Batch</span></span>

* <span data-ttu-id="26833-1243">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1243">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="26833-1244">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1244">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="26833-1245">Batch AI</span><span class="sxs-lookup"><span data-stu-id="26833-1245">Batch AI</span></span>

* <span data-ttu-id="26833-1246">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1246">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="26833-1247">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1247">Container</span></span>

* <span data-ttu-id="26833-1248">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1248">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="26833-1249">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1249">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="26833-1250">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1250">Network</span></span>

* <span data-ttu-id="26833-1251">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1251">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="26833-1252">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1252">Added `network nic wait`</span></span>
* <span data-ttu-id="26833-1253">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1253">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="26833-1254">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1254">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="26833-1255">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-1255">Resource</span></span>

* <span data-ttu-id="26833-1256">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1256">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="26833-1257">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1257">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="26833-1258">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1258">Added `deployment wait` command</span></span>
* <span data-ttu-id="26833-1259">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1259">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="26833-1260">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-1260">SQL</span></span>

* <span data-ttu-id="26833-1261">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1261">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="26833-1262">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-1262">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="26833-1263">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="26833-1263">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1264">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1264">Storage</span></span>

* <span data-ttu-id="26833-1265">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1265">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1266">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1266">VM</span></span>

* <span data-ttu-id="26833-1267">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1267">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="26833-1268">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1268">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="26833-1269">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1269">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="26833-1270">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="26833-1270">July 3, 2018</span></span>

<span data-ttu-id="26833-1271">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="26833-1271">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="26833-1272">AKS</span><span class="sxs-lookup"><span data-stu-id="26833-1272">AKS</span></span>

* <span data-ttu-id="26833-1273">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1273">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="26833-1274">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="26833-1274">July 3, 2018</span></span>

<span data-ttu-id="26833-1275">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="26833-1275">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="26833-1276">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1276">Core</span></span>

* <span data-ttu-id="26833-1277">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1277">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1278">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1278">ACR</span></span>

* <span data-ttu-id="26833-1279">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1279">Added polling build status</span></span>
* <span data-ttu-id="26833-1280">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1280">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="26833-1281">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1281">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1282">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1282">ACS</span></span>

* <span data-ttu-id="26833-1283">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1283">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="26833-1284">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1284">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="26833-1285">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1285">Updated options for `aks browse` command.</span></span> <span data-ttu-id="26833-1286">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1286">Added `--listen-port` support</span></span>
* <span data-ttu-id="26833-1287">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1287">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="26833-1288">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="26833-1288">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="26833-1289">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1289">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1290">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-1290">AppService</span></span>

* <span data-ttu-id="26833-1291">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-1291">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="26833-1292">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1292">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="26833-1293">バックアップ</span><span class="sxs-lookup"><span data-stu-id="26833-1293">Backup</span></span>

* <span data-ttu-id="26833-1294">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-1294">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="26833-1295">BatchAI</span><span class="sxs-lookup"><span data-stu-id="26833-1295">BatchAI</span></span>

* <span data-ttu-id="26833-1296">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1296">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="26833-1297">クラウド</span><span class="sxs-lookup"><span data-stu-id="26833-1297">Cloud</span></span>

* <span data-ttu-id="26833-1298">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1298">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="26833-1299">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1299">Container</span></span>

* <span data-ttu-id="26833-1300">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1300">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="26833-1301">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1301">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="26833-1302">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1302">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="26833-1303">拡張機能</span><span class="sxs-lookup"><span data-stu-id="26833-1303">Extension</span></span>

* <span data-ttu-id="26833-1304">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1304">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="26833-1305">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1305">Network</span></span>

* <span data-ttu-id="26833-1306">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1306">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-1307">Rdbms</span><span class="sxs-lookup"><span data-stu-id="26833-1307">Rdbms</span></span>

* <span data-ttu-id="26833-1308">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1308">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="26833-1309">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-1309">Resource</span></span>

* <span data-ttu-id="26833-1310">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1310">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1311">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1311">VM</span></span>

* <span data-ttu-id="26833-1312">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-1312">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="26833-1313">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="26833-1313">June 25, 2018</span></span>

<span data-ttu-id="26833-1314">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="26833-1314">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="26833-1315">CLI</span><span class="sxs-lookup"><span data-stu-id="26833-1315">CLI</span></span>

* <span data-ttu-id="26833-1316">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-1316">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="26833-1317">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="26833-1317">June 19, 2018</span></span>

<span data-ttu-id="26833-1318">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="26833-1318">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="26833-1319">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1319">Core</span></span>

* <span data-ttu-id="26833-1320">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1320">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1321">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1321">ACR</span></span>

* <span data-ttu-id="26833-1322">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1322">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="26833-1323">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1323">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1324">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1324">ACS</span></span>

* <span data-ttu-id="26833-1325">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1325">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="26833-1326">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1326">Added `--update` support</span></span>
* <span data-ttu-id="26833-1327">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1327">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="26833-1328">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="26833-1328">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="26833-1329">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1329">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="26833-1330">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1330">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="26833-1331">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1331">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="26833-1332">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1332">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1333">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-1333">AppService</span></span>

* <span data-ttu-id="26833-1334">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1334">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="26833-1335">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1335">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="26833-1336">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-1336">Batch</span></span>

* <span data-ttu-id="26833-1337">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1337">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="26833-1338">Batch AI</span><span class="sxs-lookup"><span data-stu-id="26833-1338">Batch AI</span></span>

* <span data-ttu-id="26833-1339">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1339">Added support for workspaces.</span></span> <span data-ttu-id="26833-1340">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="26833-1340">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="26833-1341">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1341">Added support for experiments.</span></span> <span data-ttu-id="26833-1342">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="26833-1342">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="26833-1343">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1343">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="26833-1344">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1344">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="26833-1345">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="26833-1345">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="26833-1346">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1346">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="26833-1347">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="26833-1347">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="26833-1348">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="26833-1348">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="26833-1349">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1349">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="26833-1350">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="26833-1350">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="26833-1351">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1351">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="26833-1352">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="26833-1352">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="26833-1353">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1353">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="26833-1354">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="26833-1354">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="26833-1355">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1355">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="26833-1356">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1356">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="26833-1357">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1357">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="26833-1358">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1358">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="26833-1359">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1359">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="26833-1360">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1360">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="26833-1361">マップ</span><span class="sxs-lookup"><span data-stu-id="26833-1361">Maps</span></span>

* <span data-ttu-id="26833-1362">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1362">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="26833-1363">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1363">Network</span></span>

* <span data-ttu-id="26833-1364">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="26833-1364">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="26833-1365">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1365">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="26833-1366">#6502</span><span class="sxs-lookup"><span data-stu-id="26833-1366">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="26833-1367">Reservations</span><span class="sxs-lookup"><span data-stu-id="26833-1367">Reservations</span></span>

* <span data-ttu-id="26833-1368">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1368">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="26833-1369">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1369">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="26833-1370">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1370">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="26833-1371">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1371">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="26833-1372">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1372">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="26833-1373">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1373">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="26833-1374">Role</span><span class="sxs-lookup"><span data-stu-id="26833-1374">Role</span></span>

* <span data-ttu-id="26833-1375">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1375">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="26833-1376">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-1376">SQL</span></span>

* <span data-ttu-id="26833-1377">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1377">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1378">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1378">Storage</span></span>

* <span data-ttu-id="26833-1379">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="26833-1379">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1380">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1380">VM</span></span>

* <span data-ttu-id="26833-1381">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1381">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="26833-1382">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1382">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="26833-1383">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1383">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="26833-1384">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="26833-1384">June 13, 2018</span></span>

<span data-ttu-id="26833-1385">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="26833-1385">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="26833-1386">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1386">Core</span></span>

* <span data-ttu-id="26833-1387">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1387">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="26833-1388">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="26833-1388">June 13, 2018</span></span>

<span data-ttu-id="26833-1389">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="26833-1389">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="26833-1390">AKS</span><span class="sxs-lookup"><span data-stu-id="26833-1390">AKS</span></span>

* <span data-ttu-id="26833-1391">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1391">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="26833-1392">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1392">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="26833-1393">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1393">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="26833-1394">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1394">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="26833-1395">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1395">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1396">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-1396">AppService</span></span>

* <span data-ttu-id="26833-1397">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1397">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="26833-1398">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="26833-1398">June 5, 2018</span></span>

<span data-ttu-id="26833-1399">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="26833-1399">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-1400">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-1400">Interactive</span></span>

* <span data-ttu-id="26833-1401">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1401">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="26833-1402">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="26833-1402">June 5, 2018</span></span>

<span data-ttu-id="26833-1403">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="26833-1403">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="26833-1404">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1404">Core</span></span>

* <span data-ttu-id="26833-1405">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1405">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="26833-1406">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-1406">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1407">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1407">ACR</span></span>

* <span data-ttu-id="26833-1408">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1408">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="26833-1409">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1409">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="26833-1410">AKS</span><span class="sxs-lookup"><span data-stu-id="26833-1410">AKS</span></span>

* <span data-ttu-id="26833-1411">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1411">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="26833-1412">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-1412">Batch</span></span>

* <span data-ttu-id="26833-1413">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1413">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="26833-1414">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-1414">IOT</span></span>

* <span data-ttu-id="26833-1415">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1415">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="26833-1416">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1416">Network</span></span>

* <span data-ttu-id="26833-1417">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-1417">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="26833-1418">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="26833-1418">Policy Insights</span></span>

* <span data-ttu-id="26833-1419">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-1419">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="26833-1420">ARM</span><span class="sxs-lookup"><span data-stu-id="26833-1420">ARM</span></span>

* <span data-ttu-id="26833-1421">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1421">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="26833-1422">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-1422">SQL</span></span>

* <span data-ttu-id="26833-1423">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1423">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="26833-1424">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1424">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="26833-1425">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1425">Storage</span></span>

* <span data-ttu-id="26833-1426">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1426">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1427">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1427">VM</span></span>

* <span data-ttu-id="26833-1428">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1428">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="26833-1429">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1429">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="26833-1430">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1430">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="26833-1431">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="26833-1431">May 22, 2018</span></span>

<span data-ttu-id="26833-1432">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="26833-1432">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="26833-1433">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1433">Core</span></span>

* <span data-ttu-id="26833-1434">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1434">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1435">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1435">ACS</span></span>

* <span data-ttu-id="26833-1436">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1436">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="26833-1437">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1437">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1438">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-1438">AppService</span></span>

* <span data-ttu-id="26833-1439">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-1439">Improved generic update commands</span></span>
* <span data-ttu-id="26833-1440">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1440">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="26833-1441">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1441">Container</span></span>

* <span data-ttu-id="26833-1442">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1442">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="26833-1443">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1443">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="26833-1444">拡張機能</span><span class="sxs-lookup"><span data-stu-id="26833-1444">Extension</span></span>

* <span data-ttu-id="26833-1445">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-1445">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-1446">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-1446">Interactive</span></span>

* <span data-ttu-id="26833-1447">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1447">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="26833-1448">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-1448">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="26833-1449">KeyVault</span><span class="sxs-lookup"><span data-stu-id="26833-1449">KeyVault</span></span>

* <span data-ttu-id="26833-1450">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1450">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="26833-1451">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1451">Network</span></span>

* <span data-ttu-id="26833-1452">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1452">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="26833-1453">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1453">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="26833-1454">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-1454">SQL</span></span>

* <span data-ttu-id="26833-1455">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1455">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="26833-1456">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1456">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="26833-1457">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1457">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="26833-1458">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1458">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="26833-1459">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1459">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="26833-1460">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="26833-1460">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="26833-1461">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="26833-1461">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="26833-1462">`edition`</span><span class="sxs-lookup"><span data-stu-id="26833-1462">`edition`.</span></span> <span data-ttu-id="26833-1463">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="26833-1463">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="26833-1464">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="26833-1464">`elasticPoolName`.</span></span> <span data-ttu-id="26833-1465">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="26833-1465">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="26833-1466">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1466">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="26833-1467">`edition`</span><span class="sxs-lookup"><span data-stu-id="26833-1467">`edition`.</span></span> <span data-ttu-id="26833-1468">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="26833-1468">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="26833-1469">`dtu`</span><span class="sxs-lookup"><span data-stu-id="26833-1469">`dtu`.</span></span> <span data-ttu-id="26833-1470">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="26833-1470">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="26833-1471">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="26833-1471">`databaseDtuMin`.</span></span> <span data-ttu-id="26833-1472">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="26833-1472">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="26833-1473">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="26833-1473">`databaseDtuMax`.</span></span> <span data-ttu-id="26833-1474">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="26833-1474">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="26833-1475">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1475">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="26833-1476">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1476">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1477">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1477">Storage</span></span>

* <span data-ttu-id="26833-1478">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1478">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="26833-1479">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1479">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1480">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1480">VM</span></span>

* <span data-ttu-id="26833-1481">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1481">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="26833-1482">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="26833-1482">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="26833-1483">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1483">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="26833-1484">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1484">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="26833-1485">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1485">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="26833-1486">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="26833-1486">May 7, 2018</span></span>

<span data-ttu-id="26833-1487">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="26833-1487">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="26833-1488">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1488">Core</span></span>

* <span data-ttu-id="26833-1489">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1489">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="26833-1490">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1490">Added limited support for positional arguments</span></span>
* <span data-ttu-id="26833-1491">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1491">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="26833-1492">#5591</span><span class="sxs-lookup"><span data-stu-id="26833-1492">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="26833-1493">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1493">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="26833-1494">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="26833-1494">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="26833-1495">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1495">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="26833-1496">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1496">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="26833-1497">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1497">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1498">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1498">ACR</span></span>

* <span data-ttu-id="26833-1499">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1499">Added ACR Build commands</span></span>
* <span data-ttu-id="26833-1500">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1500">Improved resource not found error messages</span></span>
* <span data-ttu-id="26833-1501">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1501">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="26833-1502">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1502">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="26833-1503">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1503">Improved repository commands error messages</span></span>
* <span data-ttu-id="26833-1504">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-1504">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1505">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1505">ACS</span></span>

* <span data-ttu-id="26833-1506">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1506">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="26833-1507">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1507">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="26833-1508">AMS</span><span class="sxs-lookup"><span data-stu-id="26833-1508">AMS</span></span>

* <span data-ttu-id="26833-1509">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="26833-1509">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1510">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-1510">Appservice</span></span>

* <span data-ttu-id="26833-1511">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1511">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="26833-1512">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1512">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="26833-1513">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1513">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="26833-1514">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1514">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="26833-1515">Batch AI</span><span class="sxs-lookup"><span data-stu-id="26833-1515">Batch AI</span></span>

* <span data-ttu-id="26833-1516">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1516">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="26833-1517">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="26833-1517">Cognitive Services</span></span>

* <span data-ttu-id="26833-1518">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1518">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="26833-1519">消費</span><span class="sxs-lookup"><span data-stu-id="26833-1519">Consumption</span></span>

* <span data-ttu-id="26833-1520">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1520">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="26833-1521">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1521">Container</span></span>

* <span data-ttu-id="26833-1522">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1522">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="26833-1523">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-1523">Cosmos DB</span></span>

* <span data-ttu-id="26833-1524">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="26833-1524">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="26833-1525">DMS</span><span class="sxs-lookup"><span data-stu-id="26833-1525">DMS</span></span>

* <span data-ttu-id="26833-1526">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1526">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="26833-1527">拡張機能</span><span class="sxs-lookup"><span data-stu-id="26833-1527">Extension</span></span>

* <span data-ttu-id="26833-1528">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1528">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-1529">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-1529">Interactive</span></span>

* <span data-ttu-id="26833-1530">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-1530">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="26833-1531">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="26833-1531">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="26833-1532">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1532">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="26833-1533">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1533">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="26833-1534">ラボ</span><span class="sxs-lookup"><span data-stu-id="26833-1534">Lab</span></span>

* <span data-ttu-id="26833-1535">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1535">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="26833-1536">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1536">Network</span></span>

* <span data-ttu-id="26833-1537">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1537">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="26833-1538">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-1538">Profile</span></span>

* <span data-ttu-id="26833-1539">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1539">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="26833-1540">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1540">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="26833-1541">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1541">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="26833-1542">Redis</span><span class="sxs-lookup"><span data-stu-id="26833-1542">Redis</span></span>

* <span data-ttu-id="26833-1543">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1543">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="26833-1544">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="26833-1544">Deprecated `redis list-all`.</span></span> <span data-ttu-id="26833-1545">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="26833-1545">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="26833-1546">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1546">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="26833-1547">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1547">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="26833-1548">Role</span><span class="sxs-lookup"><span data-stu-id="26833-1548">Role</span></span>

* <span data-ttu-id="26833-1549">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1549">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1550">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1550">Storage</span></span>

* <span data-ttu-id="26833-1551">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="26833-1551">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="26833-1552">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="26833-1552">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="26833-1553">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="26833-1553">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="26833-1554">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="26833-1554">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="26833-1555">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1555">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1556">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1556">VM</span></span>

* <span data-ttu-id="26833-1557">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1557">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="26833-1558">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1558">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="26833-1559">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="26833-1559">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="26833-1560">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1560">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="26833-1561">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1561">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="26833-1562">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1562">Added write accelerator support</span></span>
* <span data-ttu-id="26833-1563">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1563">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="26833-1564">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1564">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="26833-1565">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1565">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="26833-1566">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="26833-1566">April 10, 2018</span></span>

<span data-ttu-id="26833-1567">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="26833-1567">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1568">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1568">ACR</span></span>

* <span data-ttu-id="26833-1569">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1569">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1570">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1570">ACS</span></span>

* <span data-ttu-id="26833-1571">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1571">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1572">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-1572">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="26833-1574">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1574">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="26833-1575">BatchAI</span><span class="sxs-lookup"><span data-stu-id="26833-1575">BatchAI</span></span>

* <span data-ttu-id="26833-1576">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1576">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="26833-1577">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="26833-1577">Job level mounting</span></span>
  - <span data-ttu-id="26833-1578">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="26833-1578">Environment variables with secret values</span></span>
  - <span data-ttu-id="26833-1579">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="26833-1579">Performance counters settings</span></span>
  - <span data-ttu-id="26833-1580">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="26833-1580">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="26833-1581">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="26833-1581">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="26833-1582">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="26833-1582">Usage and limits reporting</span></span>
  - <span data-ttu-id="26833-1583">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="26833-1583">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="26833-1584">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="26833-1584">Support for custom images</span></span>
  - <span data-ttu-id="26833-1585">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1585">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="26833-1586">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="26833-1586">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="26833-1587">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="26833-1587">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="26833-1588">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="26833-1588">National clouds are supported</span></span>
* <span data-ttu-id="26833-1589">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1589">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="26833-1590">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1590">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="26833-1591">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1591">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="26833-1592">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1592">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="26833-1593">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="26833-1593">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="26833-1594">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="26833-1594">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="26833-1595">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1595">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="26833-1596">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1596">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="26833-1597">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="26833-1597">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="26833-1598">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1598">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="26833-1599">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="26833-1599">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="26833-1600">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="26833-1600">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="26833-1601">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1601">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="26833-1602">課金</span><span class="sxs-lookup"><span data-stu-id="26833-1602">Billing</span></span>

* <span data-ttu-id="26833-1603">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1603">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="26833-1604">消費</span><span class="sxs-lookup"><span data-stu-id="26833-1604">Consumption</span></span>

* <span data-ttu-id="26833-1605">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1605">Added `marketplace` commands</span></span>
* <span data-ttu-id="26833-1606">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1606">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="26833-1607">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1607">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="26833-1608">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1608">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="26833-1609">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1609">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="26833-1610">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1610">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="26833-1611">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1611">Container</span></span>

* <span data-ttu-id="26833-1612">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1612">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="26833-1613">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1613">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="26833-1614">拡張機能</span><span class="sxs-lookup"><span data-stu-id="26833-1614">Extension</span></span>

* <span data-ttu-id="26833-1615">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1615">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-1616">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-1616">Interactive</span></span>

* <span data-ttu-id="26833-1617">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1617">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="26833-1618">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1618">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="26833-1619">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1619">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="26833-1620">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1620">Network</span></span>

* <span data-ttu-id="26833-1621">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1621">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="26833-1622">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1622">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="26833-1623">#4910</span><span class="sxs-lookup"><span data-stu-id="26833-1623">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="26833-1624">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1624">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="26833-1625">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="26833-1625">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="26833-1626">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1626">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="26833-1627">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1627">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="26833-1628">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1628">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="26833-1629">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-1629">Profile</span></span>

* <span data-ttu-id="26833-1630">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1630">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="26833-1631">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1631">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-1632">RDBMS</span><span class="sxs-lookup"><span data-stu-id="26833-1632">RDBMS</span></span>

* <span data-ttu-id="26833-1633">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1633">Added `georestore` command</span></span>
* <span data-ttu-id="26833-1634">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1634">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="26833-1635">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-1635">Resource</span></span>

* <span data-ttu-id="26833-1636">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1636">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="26833-1637">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1637">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="26833-1638">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-1638">SQL</span></span>

* <span data-ttu-id="26833-1639">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1639">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1640">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1640">Storage</span></span>

* <span data-ttu-id="26833-1641">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1641">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1642">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1642">VM</span></span>

* <span data-ttu-id="26833-1643">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1643">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="26833-1644">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1644">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="26833-1646">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1646">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="26833-1647">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1647">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="26833-1648">#5718</span><span class="sxs-lookup"><span data-stu-id="26833-1648">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="26833-1649">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1649">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="26833-1650">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="26833-1650">March 27, 2018</span></span>

<span data-ttu-id="26833-1651">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="26833-1651">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="26833-1652">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1652">Core</span></span>

* <span data-ttu-id="26833-1653">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="26833-1653">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1654">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1654">ACS</span></span>

* <span data-ttu-id="26833-1655">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1655">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1656">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-1656">Appservice</span></span>

* <span data-ttu-id="26833-1657">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1657">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="26833-1658">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1658">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="26833-1659">バックアップ</span><span class="sxs-lookup"><span data-stu-id="26833-1659">Backup</span></span>

* <span data-ttu-id="26833-1660">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1660">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="26833-1661">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="26833-1661">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="26833-1662">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1662">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="26833-1663">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1663">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="26833-1664">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1664">Container</span></span>

* <span data-ttu-id="26833-1665">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1665">Added `container exec` command.</span></span> <span data-ttu-id="26833-1666">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="26833-1666">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="26833-1667">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="26833-1667">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="26833-1668">拡張機能</span><span class="sxs-lookup"><span data-stu-id="26833-1668">Extension</span></span>

* <span data-ttu-id="26833-1669">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1669">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="26833-1670">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1670">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="26833-1671">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1671">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-1672">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-1672">Interactive</span></span>

* <span data-ttu-id="26833-1673">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1673">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="26833-1674">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1674">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="26833-1675">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="26833-1675">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="26833-1676">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-1676">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="26833-1677">ラボ</span><span class="sxs-lookup"><span data-stu-id="26833-1677">Lab</span></span>

* <span data-ttu-id="26833-1678">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1678">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-1679">監視</span><span class="sxs-lookup"><span data-stu-id="26833-1679">Monitor</span></span>

* <span data-ttu-id="26833-1680">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="26833-1680">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="26833-1681">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="26833-1681">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="26833-1682">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="26833-1682">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="26833-1683">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1683">Network</span></span>

* <span data-ttu-id="26833-1684">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1684">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="26833-1685">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-1685">Profile</span></span>

* <span data-ttu-id="26833-1686">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1686">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-1687">RDBMS</span><span class="sxs-lookup"><span data-stu-id="26833-1687">RDBMS</span></span>

* <span data-ttu-id="26833-1688">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1688">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="26833-1689">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-1689">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="26833-1691">Role</span><span class="sxs-lookup"><span data-stu-id="26833-1691">Role</span></span>

* <span data-ttu-id="26833-1692">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1692">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="26833-1693">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1693">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="26833-1694">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1694">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="26833-1695">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1695">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="26833-1696">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1696">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1697">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1697">Storage</span></span>

* <span data-ttu-id="26833-1698">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1698">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="26833-1699">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="26833-1699">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1700">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1700">VM</span></span>

* <span data-ttu-id="26833-1701">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1701">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="26833-1702">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1702">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="26833-1703">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1703">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="26833-1704">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1704">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="26833-1705">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="26833-1705">March 13, 2018</span></span>

<span data-ttu-id="26833-1706">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="26833-1706">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1707">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1707">ACR</span></span>

* <span data-ttu-id="26833-1708">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1708">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="26833-1709">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1709">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="26833-1710">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1710">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1711">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1711">ACS</span></span>

* <span data-ttu-id="26833-1712">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1712">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="26833-1713">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1713">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="26833-1714">Advisor</span><span class="sxs-lookup"><span data-stu-id="26833-1714">Advisor</span></span>

* <span data-ttu-id="26833-1715">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1715">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="26833-1716">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1716">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="26833-1717">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1717">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="26833-1718">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1718">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="26833-1719">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1719">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1720">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-1720">Appservice</span></span>

* <span data-ttu-id="26833-1721">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1721">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="26833-1722">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1722">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="26833-1723">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="26833-1723">Eventhubs</span></span>

* <span data-ttu-id="26833-1724">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-1724">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="26833-1725">拡張機能</span><span class="sxs-lookup"><span data-stu-id="26833-1725">Extension</span></span>

* <span data-ttu-id="26833-1726">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1726">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-1727">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-1727">Interactive</span></span>

* <span data-ttu-id="26833-1728">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="26833-1728">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="26833-1729">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="26833-1729">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="26833-1730">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="26833-1730">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="26833-1731">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1731">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-1732">監視</span><span class="sxs-lookup"><span data-stu-id="26833-1732">Monitor</span></span>

* <span data-ttu-id="26833-1733">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1733">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="26833-1734">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1734">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="26833-1735">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1735">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="26833-1736">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1736">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="26833-1737">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1737">Network</span></span>

* <span data-ttu-id="26833-1738">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1738">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="26833-1739">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1739">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="26833-1740">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1740">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="26833-1741">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1741">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="26833-1742">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-1742">Profile</span></span>

* <span data-ttu-id="26833-1743">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1743">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="26833-1744">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1744">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-1745">RDBMS</span><span class="sxs-lookup"><span data-stu-id="26833-1745">RDBMS</span></span>

* <span data-ttu-id="26833-1746">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1746">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="26833-1747">Service Bus</span><span class="sxs-lookup"><span data-stu-id="26833-1747">Service Bus</span></span>

* <span data-ttu-id="26833-1748">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-1748">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1749">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1749">Storage</span></span>

* <span data-ttu-id="26833-1750">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-1750">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="26833-1751">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="26833-1751">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1752">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1752">VM</span></span>

* <span data-ttu-id="26833-1753">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1753">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="26833-1754">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1754">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="26833-1755">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1755">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="26833-1756">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1756">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="26833-1757">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="26833-1757">February 27, 2018</span></span>

<span data-ttu-id="26833-1758">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="26833-1758">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="26833-1759">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1759">Core</span></span>

* <span data-ttu-id="26833-1760">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="26833-1760">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="26833-1761">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1761">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="26833-1762">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1762">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1763">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1763">ACS</span></span>

* <span data-ttu-id="26833-1764">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1764">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="26833-1765">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="26833-1765">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="26833-1766">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1766">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="26833-1767">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1767">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1768">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-1768">Appservice</span></span>

* <span data-ttu-id="26833-1769">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="26833-1769">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="26833-1770">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="26833-1770">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="26833-1771">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="26833-1771">Cognitive Services</span></span>

* <span data-ttu-id="26833-1772">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-1772">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="26833-1773">消費</span><span class="sxs-lookup"><span data-stu-id="26833-1773">Consumption</span></span>

* <span data-ttu-id="26833-1774">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1774">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="26833-1775">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-1775">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="26833-1776">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1776">Container</span></span>

* <span data-ttu-id="26833-1777">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1777">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="26833-1778">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1778">Network</span></span>

* <span data-ttu-id="26833-1779">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="26833-1779">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="26833-1780">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-1780">Resource</span></span>

* <span data-ttu-id="26833-1781">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1781">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="26833-1782">Role</span><span class="sxs-lookup"><span data-stu-id="26833-1782">Role</span></span>

* <span data-ttu-id="26833-1783">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1783">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="26833-1784">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-1784">SQL</span></span>

* <span data-ttu-id="26833-1785">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1785">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1786">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1786">Storage</span></span>

* <span data-ttu-id="26833-1787">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1787">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1788">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1788">VM</span></span>

* <span data-ttu-id="26833-1789">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1789">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="26833-1790">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="26833-1790">February 13, 2018</span></span>

<span data-ttu-id="26833-1791">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="26833-1791">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="26833-1792">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1792">Core</span></span>

* <span data-ttu-id="26833-1793">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1793">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1794">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1794">ACS</span></span>

* <span data-ttu-id="26833-1795">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1795">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="26833-1796">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1796">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="26833-1797">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1797">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="26833-1798">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-1798">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="26833-1799">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1799">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="26833-1800">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="26833-1800">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="26833-1801">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1801">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="26833-1802">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="26833-1802">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1803">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-1803">Appservice</span></span>

* <span data-ttu-id="26833-1804">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1804">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="26833-1805">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1805">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="26833-1806">CDN</span><span class="sxs-lookup"><span data-stu-id="26833-1806">CDN</span></span>

* <span data-ttu-id="26833-1807">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1807">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="26833-1808">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1808">Container</span></span>

* <span data-ttu-id="26833-1809">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1809">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="26833-1810">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1810">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="26833-1811">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-1811">CosmosDB</span></span>

* <span data-ttu-id="26833-1812">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1812">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="26833-1813">拡張機能</span><span class="sxs-lookup"><span data-stu-id="26833-1813">Extension</span></span>

* <span data-ttu-id="26833-1814">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1814">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="26833-1815">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1815">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="26833-1816">フィードバック</span><span class="sxs-lookup"><span data-stu-id="26833-1816">Feedback</span></span>

* <span data-ttu-id="26833-1817">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1817">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-1818">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-1818">Interactive</span></span>

* <span data-ttu-id="26833-1819">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1819">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="26833-1820">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1820">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="26833-1821">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-1821">IoT</span></span>

* <span data-ttu-id="26833-1822">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1822">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="26833-1823">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1823">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="26833-1824">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1824">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="26833-1825">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1825">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-1826">監視</span><span class="sxs-lookup"><span data-stu-id="26833-1826">Monitor</span></span>

* <span data-ttu-id="26833-1827">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1827">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="26833-1828">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1828">Network</span></span>

* <span data-ttu-id="26833-1829">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1829">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="26833-1830">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-1830">Profile</span></span>

* <span data-ttu-id="26833-1831">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1831">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="26833-1832">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-1832">Resource</span></span>

* <span data-ttu-id="26833-1833">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1833">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="26833-1834">Role</span><span class="sxs-lookup"><span data-stu-id="26833-1834">Role</span></span>

* <span data-ttu-id="26833-1835">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1835">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="26833-1836">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-1836">SQL</span></span>

* <span data-ttu-id="26833-1837">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1837">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="26833-1838">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1838">Added `sql db rename`</span></span>
* <span data-ttu-id="26833-1839">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1839">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1840">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1840">Storage</span></span>

* <span data-ttu-id="26833-1841">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1841">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1842">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1842">VM</span></span>

* <span data-ttu-id="26833-1843">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1843">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="26833-1844">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1844">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="26833-1845">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="26833-1845">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="26833-1846">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="26833-1846">January 31, 2018</span></span>

<span data-ttu-id="26833-1847">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="26833-1847">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="26833-1848">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1848">Core</span></span>

* <span data-ttu-id="26833-1849">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1849">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="26833-1850">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1850">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="26833-1851">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1851">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="26833-1852">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="26833-1852">Use `--verbose` to see</span></span>
* <span data-ttu-id="26833-1853">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="26833-1853">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1854">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1854">ACS</span></span>

* <span data-ttu-id="26833-1855">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="26833-1855">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="26833-1856">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-1856">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1857">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-1857">Appservice</span></span>

* <span data-ttu-id="26833-1858">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="26833-1858">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="26833-1859">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1859">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="26833-1860">CDN</span><span class="sxs-lookup"><span data-stu-id="26833-1860">CDN</span></span>

* <span data-ttu-id="26833-1861">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1861">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="26833-1862">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-1862">CosmosDB</span></span>

* <span data-ttu-id="26833-1863">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1863">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-1864">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-1864">Interactive</span></span>

* <span data-ttu-id="26833-1865">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1865">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="26833-1866">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1866">Network</span></span>

* <span data-ttu-id="26833-1867">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1867">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="26833-1868">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1868">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="26833-1869">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1869">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="26833-1870">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1870">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="26833-1871">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1871">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="26833-1872">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1872">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="26833-1873">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1873">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="26833-1874">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1874">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="26833-1875">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1875">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="26833-1876">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="26833-1876">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="26833-1877">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-1877">Profile</span></span>

* <span data-ttu-id="26833-1878">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1878">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="26833-1879">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-1879">Resource</span></span>

* <span data-ttu-id="26833-1880">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1880">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1881">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1881">Storage</span></span>

* <span data-ttu-id="26833-1882">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1882">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="26833-1883">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1883">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="26833-1884">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1884">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="26833-1885">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1885">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="26833-1886">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1886">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1887">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1887">VM</span></span>

* <span data-ttu-id="26833-1888">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1888">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="26833-1889">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1889">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="26833-1890">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1890">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="26833-1891">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1891">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="26833-1892">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="26833-1892">January 17, 2018</span></span>

<span data-ttu-id="26833-1893">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="26833-1893">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="26833-1894">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-1894">ACR</span></span>

* <span data-ttu-id="26833-1895">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1895">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="26833-1896">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-1896">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1897">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1897">ACS</span></span>

* <span data-ttu-id="26833-1898">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1898">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="26833-1899">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1899">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1900">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-1900">Appservice</span></span>

* <span data-ttu-id="26833-1901">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1901">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="26833-1902">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1902">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="26833-1903">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1903">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="26833-1904">バックアップ</span><span class="sxs-lookup"><span data-stu-id="26833-1904">Backup</span></span>

* <span data-ttu-id="26833-1905">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1905">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="26833-1906">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1906">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="26833-1907">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1907">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="26833-1908">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1908">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="26833-1909">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1909">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="26833-1910">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-1910">Batch</span></span>

* <span data-ttu-id="26833-1911">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1911">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="26833-1912">クラウド</span><span class="sxs-lookup"><span data-stu-id="26833-1912">Cloud</span></span>

* <span data-ttu-id="26833-1913">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1913">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="26833-1914">消費</span><span class="sxs-lookup"><span data-stu-id="26833-1914">Consumption</span></span>

* <span data-ttu-id="26833-1915">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1915">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="26833-1916">Event Grid</span><span class="sxs-lookup"><span data-stu-id="26833-1916">Event Grid</span></span>

* <span data-ttu-id="26833-1917">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="26833-1917">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="26833-1918">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="26833-1918">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="26833-1919">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-1919">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="26833-1920">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="26833-1920">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="26833-1921">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1921">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="26833-1922">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1922">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="26833-1923">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1923">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="26833-1924">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1924">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-1925">Interactive</span><span class="sxs-lookup"><span data-stu-id="26833-1925">Interactive</span></span>

* <span data-ttu-id="26833-1926">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="26833-1926">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="26833-1927">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1927">Fixed errors on startup</span></span>
* <span data-ttu-id="26833-1928">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1928">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="26833-1929">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-1929">IoT</span></span>

* <span data-ttu-id="26833-1930">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1930">Added support for device provisioning service</span></span>
* <span data-ttu-id="26833-1931">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1931">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="26833-1932">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1932">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-1933">監視</span><span class="sxs-lookup"><span data-stu-id="26833-1933">Monitor</span></span>

* <span data-ttu-id="26833-1934">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1934">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="26833-1935">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="26833-1935">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="26833-1936">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1936">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="26833-1937">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1937">Network</span></span>

* <span data-ttu-id="26833-1938">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1938">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="26833-1939">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1939">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="26833-1940">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-1940">Profile</span></span>

* <span data-ttu-id="26833-1941">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1941">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="26833-1942">Role</span><span class="sxs-lookup"><span data-stu-id="26833-1942">Role</span></span>

* <span data-ttu-id="26833-1943">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1943">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="26833-1944">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="26833-1944">Service Fabric</span></span>

* <span data-ttu-id="26833-1945">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1945">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="26833-1946">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1946">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1947">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1947">VM</span></span>

* <span data-ttu-id="26833-1948">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="26833-1948">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="26833-1949">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1949">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="26833-1950">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1950">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="26833-1951">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1951">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="26833-1952">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1952">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="26833-1953">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1953">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="26833-1954">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1954">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="26833-1955">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1955">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="26833-1956">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="26833-1956">December 19, 2017</span></span>

<span data-ttu-id="26833-1957">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="26833-1957">Version 2.0.23</span></span>

* <span data-ttu-id="26833-1958">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1958">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="26833-1959">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1959">Container</span></span>

* <span data-ttu-id="26833-1960">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1960">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="26833-1961">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-1961">Network</span></span>

* <span data-ttu-id="26833-1962">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1962">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="26833-1963">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1963">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-1964">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-1964">Storage</span></span>

* <span data-ttu-id="26833-1965">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1965">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="26833-1966">VM</span><span class="sxs-lookup"><span data-stu-id="26833-1966">VM</span></span>

* <span data-ttu-id="26833-1967">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1967">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="26833-1968">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="26833-1968">December 5, 2017</span></span>

<span data-ttu-id="26833-1969">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="26833-1969">Version 2.0.22</span></span>

* <span data-ttu-id="26833-1970">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="26833-1970">Removed `az component` commands.</span></span> <span data-ttu-id="26833-1971">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="26833-1971">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="26833-1972">コア</span><span class="sxs-lookup"><span data-stu-id="26833-1972">Core</span></span>
* <span data-ttu-id="26833-1973">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-1973">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="26833-1974">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1974">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="26833-1975">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-1975">ACS</span></span>

* <span data-ttu-id="26833-1976">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1976">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="26833-1977">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1977">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="26833-1978">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1978">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="26833-1979">Advisor</span><span class="sxs-lookup"><span data-stu-id="26833-1979">Advisor</span></span>

* <span data-ttu-id="26833-1980">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-1980">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-1981">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-1981">Appservice</span></span>

* <span data-ttu-id="26833-1982">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1982">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="26833-1983">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1983">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="26833-1984">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1984">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="26833-1985">消費</span><span class="sxs-lookup"><span data-stu-id="26833-1985">Consumption</span></span>

* <span data-ttu-id="26833-1986">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1986">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="26833-1987">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-1987">Container</span></span>

* <span data-ttu-id="26833-1988">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-1988">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-1989">監視</span><span class="sxs-lookup"><span data-stu-id="26833-1989">Monitor</span></span>

* <span data-ttu-id="26833-1990">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1990">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="26833-1991">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-1991">Resource</span></span>

* <span data-ttu-id="26833-1992">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1992">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="26833-1993">Role</span><span class="sxs-lookup"><span data-stu-id="26833-1993">Role</span></span>

* <span data-ttu-id="26833-1994">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1994">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="26833-1995">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="26833-1995">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="26833-1996">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-1996">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="26833-1997">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-1997">SQL</span></span>

* <span data-ttu-id="26833-1998">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1998">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="26833-1999">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-1999">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2000">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2000">VM</span></span>

* <span data-ttu-id="26833-2001">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2001">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="26833-2002">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="26833-2002">November 14, 2017</span></span>

<span data-ttu-id="26833-2003">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="26833-2003">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="26833-2004">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-2004">ACR</span></span>

* <span data-ttu-id="26833-2005">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2005">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="26833-2006">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-2006">ACS</span></span>

* <span data-ttu-id="26833-2007">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2007">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="26833-2008">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="26833-2008">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="26833-2009">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2009">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="26833-2010">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2010">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="26833-2011">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2011">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-2012">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-2012">Appservice</span></span>

* <span data-ttu-id="26833-2013">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2013">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="26833-2014">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2014">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="26833-2015">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-2015">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="26833-2016">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-2016">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="26833-2017">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2017">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="26833-2018">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="26833-2018">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="26833-2019">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-2019">Batch</span></span>

* <span data-ttu-id="26833-2020">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2020">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="26833-2021">Batchai</span><span class="sxs-lookup"><span data-stu-id="26833-2021">Batchai</span></span>

* <span data-ttu-id="26833-2022">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2022">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="26833-2023">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2023">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="26833-2024">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2024">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="26833-2025">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2025">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="26833-2026">クラウド</span><span class="sxs-lookup"><span data-stu-id="26833-2026">Cloud</span></span>

* <span data-ttu-id="26833-2027">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2027">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="26833-2028">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-2028">Container</span></span>

* <span data-ttu-id="26833-2029">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2029">Added support to open multiple ports</span></span>
* <span data-ttu-id="26833-2030">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2030">Added container group restart policy</span></span>
* <span data-ttu-id="26833-2031">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2031">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="26833-2032">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-2032">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="26833-2033">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="26833-2033">Data Lake Analytics</span></span>

* <span data-ttu-id="26833-2034">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2034">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="26833-2035">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="26833-2035">Data Lake Store</span></span>

* <span data-ttu-id="26833-2036">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2036">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="26833-2037">拡張機能</span><span class="sxs-lookup"><span data-stu-id="26833-2037">Extension</span></span>

* <span data-ttu-id="26833-2038">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2038">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="26833-2039">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2039">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="26833-2040">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-2040">IoT</span></span>

* <span data-ttu-id="26833-2041">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2041">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-2042">監視</span><span class="sxs-lookup"><span data-stu-id="26833-2042">Monitor</span></span>

* <span data-ttu-id="26833-2043">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2043">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="26833-2044">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-2044">Network</span></span>

* <span data-ttu-id="26833-2045">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2045">Added support for CAA DNS records</span></span>
* <span data-ttu-id="26833-2046">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2046">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="26833-2047">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2047">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="26833-2048">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2048">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="26833-2049">Reservations</span><span class="sxs-lookup"><span data-stu-id="26833-2049">Reservations</span></span>

* <span data-ttu-id="26833-2050">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="26833-2050">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="26833-2051">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-2051">Resource</span></span>

* <span data-ttu-id="26833-2052">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2052">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="26833-2053">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-2053">SQL</span></span>

* <span data-ttu-id="26833-2054">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2054">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-2055">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-2055">Storage</span></span>

* <span data-ttu-id="26833-2056">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2056">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="26833-2057">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2057">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="26833-2058">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2058">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="26833-2059">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2059">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="26833-2060">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2060">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="26833-2061">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2061">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="26833-2062">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2062">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2063">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2063">VM</span></span>

* <span data-ttu-id="26833-2064">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2064">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="26833-2065">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2065">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="26833-2066">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2066">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="26833-2067">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2067">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="26833-2068">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2068">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="26833-2069">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="26833-2069">October 24, 2017</span></span>

<span data-ttu-id="26833-2070">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="26833-2070">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="26833-2071">コア</span><span class="sxs-lookup"><span data-stu-id="26833-2071">Core</span></span>

* <span data-ttu-id="26833-2072">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-2072">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="26833-2073">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-2073">ACR</span></span>

* <span data-ttu-id="26833-2074">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-2074">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="26833-2075">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2075">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="26833-2076">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2076">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="26833-2077">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-2077">ACS</span></span>

* <span data-ttu-id="26833-2078">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2078">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="26833-2079">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2079">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-2080">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-2080">Appservice</span></span>

* <span data-ttu-id="26833-2081">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2081">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="26833-2082">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="26833-2082">Component</span></span>

* <span data-ttu-id="26833-2083">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2083">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-2084">監視</span><span class="sxs-lookup"><span data-stu-id="26833-2084">Monitor</span></span>

* <span data-ttu-id="26833-2085">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2085">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="26833-2086">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-2086">Resource</span></span>

* <span data-ttu-id="26833-2087">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2087">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="26833-2088">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2088">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2089">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2089">VM</span></span>

* <span data-ttu-id="26833-2090">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2090">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="26833-2091">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="26833-2091">October 9, 2017</span></span>

<span data-ttu-id="26833-2092">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="26833-2092">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="26833-2093">コア</span><span class="sxs-lookup"><span data-stu-id="26833-2093">Core</span></span>

* <span data-ttu-id="26833-2094">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2094">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-2095">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-2095">Appservice</span></span>

* <span data-ttu-id="26833-2096">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2096">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="26833-2097">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-2097">Batch</span></span>

* <span data-ttu-id="26833-2098">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-2098">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="26833-2099">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-2099">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="26833-2100">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2100">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="26833-2101">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-2101">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="26833-2102">Batchai</span><span class="sxs-lookup"><span data-stu-id="26833-2102">Batchai</span></span>

* <span data-ttu-id="26833-2103">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-2103">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="26833-2104">KeyVault</span><span class="sxs-lookup"><span data-stu-id="26833-2104">Keyvault</span></span>

* <span data-ttu-id="26833-2105">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="26833-2105">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="26833-2106">(#4448)</span><span class="sxs-lookup"><span data-stu-id="26833-2106">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="26833-2107">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-2107">Network</span></span>

* <span data-ttu-id="26833-2108">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2108">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="26833-2109">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-2109">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="26833-2110">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-2110">Resource</span></span>

* <span data-ttu-id="26833-2111">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2111">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="26833-2112">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2112">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="26833-2113">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2113">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="26833-2114">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2114">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="26833-2115">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-2115">Sql</span></span>

* <span data-ttu-id="26833-2116">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2116">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="26833-2117">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="26833-2117">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="26833-2118">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="26833-2118">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="26833-2119">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-2119">Storage</span></span>

* <span data-ttu-id="26833-2120">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2120">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2121">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2121">Vm</span></span>

* <span data-ttu-id="26833-2122">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2122">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="26833-2123">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2123">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="26833-2124">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2124">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="26833-2125">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2125">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="26833-2126">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2126">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="26833-2127">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="26833-2127">September 22, 2017</span></span>

<span data-ttu-id="26833-2128">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="26833-2128">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="26833-2129">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-2129">Resource</span></span>

* <span data-ttu-id="26833-2130">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2130">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="26833-2131">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2131">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="26833-2132">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2132">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="26833-2133">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2133">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="26833-2134">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-2134">Network</span></span>

* <span data-ttu-id="26833-2135">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2135">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="26833-2136">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2136">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="26833-2137">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2137">Added `asg` application security group commands</span></span>
* <span data-ttu-id="26833-2138">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2138">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="26833-2139">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2139">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="26833-2140">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2140">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="26833-2141">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2141">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="26833-2142">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-2142">Storage</span></span>

* <span data-ttu-id="26833-2143">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2143">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="26833-2144">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="26833-2144">Eventgrid</span></span>

* <span data-ttu-id="26833-2145">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-2145">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="26833-2146">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-2146">SQL</span></span>

* <span data-ttu-id="26833-2147">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-2147">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="26833-2148">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="26833-2148">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="26833-2149">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2149">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="26833-2150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="26833-2150">Keyvault</span></span>

* <span data-ttu-id="26833-2151">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2151">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2152">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2152">VM</span></span>

* <span data-ttu-id="26833-2153">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2153">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="26833-2154">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2154">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="26833-2155">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2155">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="26833-2156">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2156">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="26833-2157">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2157">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="26833-2158">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2158">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="26833-2159">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-2159">ACS</span></span>

* <span data-ttu-id="26833-2160">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2160">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-2161">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-2161">Appservice</span></span>

* <span data-ttu-id="26833-2162">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2162">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="26833-2163">バックアップ</span><span class="sxs-lookup"><span data-stu-id="26833-2163">Backup</span></span>

* <span data-ttu-id="26833-2164">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="26833-2164">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="26833-2165">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="26833-2165">September 11, 2017</span></span>

<span data-ttu-id="26833-2166">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="26833-2166">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="26833-2167">コア</span><span class="sxs-lookup"><span data-stu-id="26833-2167">Core</span></span>

* <span data-ttu-id="26833-2168">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-2168">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="26833-2169">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2169">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="26833-2170">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-2170">Acs</span></span>

* <span data-ttu-id="26833-2171">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2171">Added `acs list-locations` command</span></span>
* <span data-ttu-id="26833-2172">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="26833-2172">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-2173">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-2173">Appservice</span></span>

* <span data-ttu-id="26833-2174">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2174">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="26833-2175">CDN</span><span class="sxs-lookup"><span data-stu-id="26833-2175">CDN</span></span>

* <span data-ttu-id="26833-2176">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2176">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="26833-2177">拡張機能</span><span class="sxs-lookup"><span data-stu-id="26833-2177">Extension</span></span>

* <span data-ttu-id="26833-2178">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-2178">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="26833-2179">KeyVault</span><span class="sxs-lookup"><span data-stu-id="26833-2179">Keyvault</span></span>

* <span data-ttu-id="26833-2180">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2180">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="26833-2181">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-2181">Network</span></span>

* <span data-ttu-id="26833-2182">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2182">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="26833-2183">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2183">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="26833-2184">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2184">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="26833-2185">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2185">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="26833-2186">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2186">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="26833-2187">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-2187">Resource</span></span>

* <span data-ttu-id="26833-2188">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="26833-2188">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="26833-2189">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="26833-2189">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="26833-2190">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="26833-2190">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="26833-2191">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="26833-2191">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="26833-2192">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-2192">SQL</span></span>

* <span data-ttu-id="26833-2193">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2193">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2194">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2194">VM</span></span>

* <span data-ttu-id="26833-2195">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="26833-2195">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="26833-2196">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="26833-2196">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="26833-2197">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-2197">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="26833-2198">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="26833-2198">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="26833-2199">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="26833-2199">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="26833-2200">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="26833-2200">August 31, 2017</span></span>

<span data-ttu-id="26833-2201">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="26833-2201">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="26833-2202">KeyVault</span><span class="sxs-lookup"><span data-stu-id="26833-2202">Keyvault</span></span>

* <span data-ttu-id="26833-2203">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2203">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="26833-2204">SF</span><span class="sxs-lookup"><span data-stu-id="26833-2204">Sf</span></span>

* <span data-ttu-id="26833-2205">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="26833-2205">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="26833-2206">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-2206">Storage</span></span>

* <span data-ttu-id="26833-2207">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2207">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="26833-2208">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="26833-2208">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="26833-2209">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="26833-2209">August 28, 2017</span></span>

<span data-ttu-id="26833-2210">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="26833-2210">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="26833-2211">CLI</span><span class="sxs-lookup"><span data-stu-id="26833-2211">CLI</span></span>

* <span data-ttu-id="26833-2212">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2212">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="26833-2213">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-2213">ACS</span></span>

* <span data-ttu-id="26833-2214">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2214">Corrected preview regions</span></span>
* <span data-ttu-id="26833-2215">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="26833-2215">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="26833-2216">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="26833-2216">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-2217">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-2217">Appservice</span></span>

* <span data-ttu-id="26833-2218">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2218">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="26833-2219">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2219">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="26833-2220">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="26833-2220">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="26833-2221">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="26833-2221">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="26833-2222">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="26833-2222">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="26833-2223">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-2223">IoT</span></span>

* <span data-ttu-id="26833-2224">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="26833-2224">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="26833-2225">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-2225">Network</span></span>

* <span data-ttu-id="26833-2226">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2226">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="26833-2227">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2227">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="26833-2228">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2228">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="26833-2229">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2229">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="26833-2230">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2230">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="26833-2231">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-2231">Profile</span></span>

* <span data-ttu-id="26833-2232">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="26833-2232">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="26833-2233">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="26833-2233">Service Fabric</span></span>

* <span data-ttu-id="26833-2234">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="26833-2234">Preview release</span></span>
* <span data-ttu-id="26833-2235">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="26833-2235">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="26833-2236">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2236">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="26833-2237">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2237">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-2238">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-2238">Storage</span></span>

* <span data-ttu-id="26833-2239">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-2239">Enabled setting blob tier</span></span>
* <span data-ttu-id="26833-2240">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2240">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="26833-2241">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2241">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="26833-2242">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-2242">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="26833-2243">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2243">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="26833-2244">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="26833-2244">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2245">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2245">VM</span></span>

* <span data-ttu-id="26833-2246">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2246">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="26833-2247">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-2247">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="26833-2248">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-2248">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="26833-2249">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2249">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="26833-2250">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2250">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="26833-2251">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2251">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="26833-2252">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="26833-2252">August 15, 2017</span></span>

<span data-ttu-id="26833-2253">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="26833-2253">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="26833-2254">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-2254">ACS</span></span>

* <span data-ttu-id="26833-2255">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2255">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-2256">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-2256">Appservice</span></span>

* <span data-ttu-id="26833-2257">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2257">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="26833-2258">Event Grid</span><span class="sxs-lookup"><span data-stu-id="26833-2258">Event Grid</span></span>

* <span data-ttu-id="26833-2259">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2259">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="26833-2260">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="26833-2260">August 11, 2017</span></span>

<span data-ttu-id="26833-2261">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="26833-2261">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="26833-2262">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-2262">ACS</span></span>

* <span data-ttu-id="26833-2263">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2263">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="26833-2264">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-2264">Batch</span></span>

* <span data-ttu-id="26833-2265">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="26833-2265">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="26833-2266">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2266">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="26833-2267">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2267">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="26833-2268">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2268">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="26833-2269">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2269">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="26833-2270">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2270">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="26833-2271">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="26833-2271">Component</span></span>

* <span data-ttu-id="26833-2272">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2272">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="26833-2273">コンテナー</span><span class="sxs-lookup"><span data-stu-id="26833-2273">Container</span></span>

* <span data-ttu-id="26833-2274">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2274">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="26833-2275">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="26833-2275">Data Lake Store</span></span>

* <span data-ttu-id="26833-2276">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-2276">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="26833-2277">Event Grid</span><span class="sxs-lookup"><span data-stu-id="26833-2277">Event Grid</span></span>

* <span data-ttu-id="26833-2278">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-2278">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="26833-2279">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-2279">Network</span></span>

* <span data-ttu-id="26833-2280">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2280">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="26833-2281">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2281">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="26833-2282">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2282">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="26833-2283">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2283">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="26833-2284">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-2284">Profile</span></span>

* <span data-ttu-id="26833-2285">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2285">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="26833-2286">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-2286">Storage</span></span>

* <span data-ttu-id="26833-2287">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="26833-2287">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2288">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2288">VM</span></span>

* <span data-ttu-id="26833-2289">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="26833-2289">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="26833-2290">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="26833-2290">Exposed `list-skus` command</span></span>
* <span data-ttu-id="26833-2291">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2291">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="26833-2292">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="26833-2292">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="26833-2293">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-2293">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="26833-2294">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="26833-2294">July 28, 2017</span></span>

<span data-ttu-id="26833-2295">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="26833-2295">Version 2.0.12</span></span>

* <span data-ttu-id="26833-2296">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2296">Added container commands</span></span>
* <span data-ttu-id="26833-2297">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2297">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="26833-2298">コア</span><span class="sxs-lookup"><span data-stu-id="26833-2298">Core</span></span>

* <span data-ttu-id="26833-2299">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="26833-2299">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="26833-2300">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2300">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="26833-2301">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="26833-2301">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="26833-2302">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="26833-2302">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="26833-2303">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="26833-2303">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="26833-2304">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="26833-2304">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="26833-2305">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="26833-2305">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="26833-2306">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="26833-2306">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="26833-2307">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="26833-2307">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="26833-2308">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="26833-2308">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="26833-2309">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="26833-2309">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="26833-2310">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="26833-2310">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="26833-2311">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="26833-2311">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="26833-2312">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="26833-2312">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="26833-2313">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2313">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="26833-2314">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="26833-2314">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="26833-2315">ACR</span><span class="sxs-lookup"><span data-stu-id="26833-2315">ACR</span></span>

* <span data-ttu-id="26833-2316">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2316">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="26833-2317">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2317">Support SKU update for managed registries</span></span>
* <span data-ttu-id="26833-2318">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2318">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="26833-2319">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2319">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="26833-2320">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2320">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="26833-2321">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2321">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="26833-2322">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-2322">ACS</span></span>

* <span data-ttu-id="26833-2323">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2323">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-2324">Appservice</span><span class="sxs-lookup"><span data-stu-id="26833-2324">Appservice</span></span>

* <span data-ttu-id="26833-2325">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2325">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="26833-2326">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2326">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="26833-2327">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="26833-2327">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="26833-2328">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="26833-2328">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="26833-2329">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="26833-2329">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="26833-2330">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="26833-2330">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="26833-2331">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="26833-2331">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="26833-2332">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="26833-2332">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="26833-2333">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="26833-2333">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="26833-2334">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="26833-2334">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="26833-2335">Batch</span><span class="sxs-lookup"><span data-stu-id="26833-2335">Batch</span></span>

* <span data-ttu-id="26833-2336">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="26833-2336">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="26833-2337">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2337">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="26833-2338">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2338">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="26833-2339">CDN</span><span class="sxs-lookup"><span data-stu-id="26833-2339">CDN</span></span>

* <span data-ttu-id="26833-2340">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2340">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="26833-2341">クラウド</span><span class="sxs-lookup"><span data-stu-id="26833-2341">Cloud</span></span>

* <span data-ttu-id="26833-2342">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2342">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="26833-2343">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="26833-2343">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="26833-2344">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2344">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="26833-2345">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="26833-2345">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="26833-2346">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="26833-2346">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="26833-2347">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-2347">CosmosDB</span></span>

* <span data-ttu-id="26833-2348">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2348">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="26833-2349">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2349">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="26833-2350">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="26833-2350">Data Lake Analytics</span></span>

* <span data-ttu-id="26833-2351">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2351">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="26833-2352">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2352">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="26833-2353">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2353">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="26833-2354">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="26833-2354">Data Lake Store</span></span>

* <span data-ttu-id="26833-2355">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2355">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="26833-2356">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="26833-2356">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="26833-2357">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-2357">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="26833-2358">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="26833-2358">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="26833-2359">対話</span><span class="sxs-lookup"><span data-stu-id="26833-2359">Interactive</span></span>

* <span data-ttu-id="26833-2360">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="26833-2360">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="26833-2361">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="26833-2361">Increased test coverage</span></span>
* <span data-ttu-id="26833-2362">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="26833-2362">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="26833-2363">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="26833-2363">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="26833-2364">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="26833-2364">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="26833-2365">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="26833-2365">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="26833-2366">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="26833-2366">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="26833-2367">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2367">Added `--progress` flag</span></span>
* <span data-ttu-id="26833-2368">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-2368">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="26833-2369">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="26833-2369">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="26833-2370">IoT</span><span class="sxs-lookup"><span data-stu-id="26833-2370">IoT</span></span>

* <span data-ttu-id="26833-2371">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="26833-2371">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="26833-2372">(#3934)</span><span class="sxs-lookup"><span data-stu-id="26833-2372">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="26833-2373">Key Vault</span><span class="sxs-lookup"><span data-stu-id="26833-2373">Key vault</span></span>

* <span data-ttu-id="26833-2374">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="26833-2374">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="26833-2375">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="26833-2375">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="26833-2376">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="26833-2376">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="26833-2377">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="26833-2377">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="26833-2378">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="26833-2378">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="26833-2379">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="26833-2379">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="26833-2380">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="26833-2380">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="26833-2381">(#3307)</span><span class="sxs-lookup"><span data-stu-id="26833-2381">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="26833-2382">ラボ</span><span class="sxs-lookup"><span data-stu-id="26833-2382">Lab</span></span>

* <span data-ttu-id="26833-2383">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2383">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="26833-2384">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2384">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-2385">監視</span><span class="sxs-lookup"><span data-stu-id="26833-2385">Monitor</span></span>

* <span data-ttu-id="26833-2386">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="26833-2386">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="26833-2387">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2387">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="26833-2388">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2388">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="26833-2389">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2389">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="26833-2390">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="26833-2390">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="26833-2391">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="26833-2391">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="26833-2392">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="26833-2392">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="26833-2393">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="26833-2393">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="26833-2394">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="26833-2394">`location` no longer required</span></span>
  * <span data-ttu-id="26833-2395">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="26833-2395">Add name and ID support for target</span></span>
  * <span data-ttu-id="26833-2396">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="26833-2396">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="26833-2397">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="26833-2397">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="26833-2398">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2398">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="26833-2399">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="26833-2399">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="26833-2400">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2400">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="26833-2401">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2401">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="26833-2402">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-2402">Network</span></span>

* <span data-ttu-id="26833-2403">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2403">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="26833-2404">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2404">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="26833-2405">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2405">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="26833-2406">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2406">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="26833-2407">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2407">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="26833-2408">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2408">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="26833-2409">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2409">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="26833-2410">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2410">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="26833-2411">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2411">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="26833-2412">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2412">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="26833-2413">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2413">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="26833-2414">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2414">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="26833-2415">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2415">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="26833-2416">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2416">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="26833-2417">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2417">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="26833-2418">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-2418">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="26833-2419">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2419">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="26833-2420">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2420">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="26833-2421">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2421">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="26833-2422">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2422">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="26833-2423">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2423">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="26833-2424">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2424">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="26833-2425">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-2425">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="26833-2426">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="26833-2426">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="26833-2427">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="26833-2427">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="26833-2428">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="26833-2428">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="26833-2429">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="26833-2429">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="26833-2430">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-2430">Profile</span></span>

* <span data-ttu-id="26833-2431">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2431">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="26833-2432">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2432">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="26833-2433">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="26833-2433">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="26833-2434">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2434">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="26833-2435">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2435">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="26833-2436">RDBMS</span><span class="sxs-lookup"><span data-stu-id="26833-2436">RDBMS</span></span>

* <span data-ttu-id="26833-2437">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="26833-2437">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="26833-2438">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="26833-2438">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="26833-2439">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="26833-2439">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="26833-2440">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="26833-2440">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="26833-2441">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-2441">Resource</span></span>

* <span data-ttu-id="26833-2442">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-2442">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="26833-2443">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="26833-2443">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="26833-2444">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2444">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="26833-2445">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2445">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="26833-2446">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="26833-2446">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="26833-2447">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2447">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="26833-2448">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="26833-2448">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="26833-2449">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2449">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="26833-2450">Role</span><span class="sxs-lookup"><span data-stu-id="26833-2450">Role</span></span>

* <span data-ttu-id="26833-2451">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2451">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="26833-2452">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="26833-2452">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="26833-2453">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="26833-2453">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="26833-2454">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="26833-2454">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="26833-2455">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2455">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="26833-2456">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="26833-2456">Service Fabric</span></span>
* <span data-ttu-id="26833-2457">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="26833-2457">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="26833-2458">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="26833-2458">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="26833-2459">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="26833-2459">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="26833-2460">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-2460">SQL</span></span>

* <span data-ttu-id="26833-2461">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-2461">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="26833-2462">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="26833-2462">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="26833-2463">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2463">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="26833-2464">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-2464">Storage</span></span>

* <span data-ttu-id="26833-2465">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="26833-2465">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="26833-2466">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="26833-2466">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="26833-2467">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="26833-2467">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="26833-2468">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="26833-2468">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="26833-2469">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="26833-2469">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="26833-2470">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="26833-2470">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2471">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2471">VM</span></span>

* <span data-ttu-id="26833-2472">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2472">Support configuring nsg</span></span>
* <span data-ttu-id="26833-2473">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2473">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="26833-2474">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="26833-2474">Support managed service identities</span></span>
* <span data-ttu-id="26833-2475">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2475">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="26833-2476">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="26833-2476">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="26833-2477">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="26833-2477">May 10, 2017</span></span>

<span data-ttu-id="26833-2478">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="26833-2478">Version 2.0.6</span></span>

* <span data-ttu-id="26833-2479">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="26833-2479">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="26833-2480">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2480">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="26833-2481">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2481">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="26833-2482">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2482">Include Cognitive Services module</span></span>
* <span data-ttu-id="26833-2483">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2483">Include Service Fabric module</span></span>
* <span data-ttu-id="26833-2484">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="26833-2484">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="26833-2485">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2485">Add support for CDN commands</span></span>
* <span data-ttu-id="26833-2486">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="26833-2486">Remove Container module</span></span>
* <span data-ttu-id="26833-2487">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="26833-2487">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="26833-2488">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="26833-2488">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="26833-2489">コア</span><span class="sxs-lookup"><span data-stu-id="26833-2489">Core</span></span>

* <span data-ttu-id="26833-2490">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="26833-2490">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="26833-2491">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="26833-2491">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="26833-2492">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="26833-2492">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="26833-2493">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="26833-2493">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="26833-2494">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="26833-2494">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="26833-2495">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="26833-2495">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="26833-2496">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="26833-2496">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="26833-2497">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="26833-2497">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="26833-2498">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="26833-2498">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="26833-2499">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="26833-2499">core: Improved performance</span></span>
* <span data-ttu-id="26833-2500">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="26833-2500">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="26833-2501">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="26833-2501">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="26833-2502">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-2502">ACS</span></span>

* <span data-ttu-id="26833-2503">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-2503">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="26833-2504">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="26833-2504">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="26833-2505">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="26833-2505">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="26833-2506">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="26833-2506">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-2507">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-2507">AppService</span></span>

* <span data-ttu-id="26833-2508">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2508">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="26833-2509">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2509">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="26833-2510">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="26833-2510">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="26833-2511">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="26833-2511">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="26833-2512">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="26833-2512">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="26833-2513">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="26833-2513">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="26833-2514">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="26833-2514">support slot swap with preview</span></span>
* <span data-ttu-id="26833-2515">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="26833-2515">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="26833-2516">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="26833-2516">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="26833-2517">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="26833-2517">CosmosDB</span></span>

* <span data-ttu-id="26833-2518">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="26833-2518">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="26833-2519">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2519">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="26833-2520">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2520">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="26833-2521">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2521">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="26833-2522">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="26833-2522">Data Lake Analytics</span></span>

* <span data-ttu-id="26833-2523">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-2523">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="26833-2524">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="26833-2524">Add support for new catalog item type: package.</span></span> <span data-ttu-id="26833-2525">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="26833-2525">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="26833-2526">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="26833-2526">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="26833-2527">テーブル</span><span class="sxs-lookup"><span data-stu-id="26833-2527">Table</span></span>
  * <span data-ttu-id="26833-2528">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="26833-2528">Table valued function</span></span>
  * <span data-ttu-id="26833-2529">表示</span><span class="sxs-lookup"><span data-stu-id="26833-2529">View</span></span>
  * <span data-ttu-id="26833-2530">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="26833-2530">Table Statistics.</span></span> <span data-ttu-id="26833-2531">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="26833-2531">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="26833-2532">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="26833-2532">Data Lake Store</span></span>

* <span data-ttu-id="26833-2533">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="26833-2533">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="26833-2534">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="26833-2534">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="26833-2535">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="26833-2535">missed help for access show.</span></span> <span data-ttu-id="26833-2536">追加しました</span><span class="sxs-lookup"><span data-stu-id="26833-2536">adding it.</span></span> <span data-ttu-id="26833-2537">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="26833-2537">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="26833-2538">検索</span><span class="sxs-lookup"><span data-stu-id="26833-2538">Find</span></span>

* <span data-ttu-id="26833-2539">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="26833-2539">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="26833-2540">KeyVault</span><span class="sxs-lookup"><span data-stu-id="26833-2540">KeyVault</span></span>

* <span data-ttu-id="26833-2541">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="26833-2541">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="26833-2542">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="26833-2542">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="26833-2543">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="26833-2543">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="26833-2544">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-2544">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="26833-2545">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="26833-2545">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="26833-2546">ラボ</span><span class="sxs-lookup"><span data-stu-id="26833-2546">Lab</span></span>

* <span data-ttu-id="26833-2547">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2547">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="26833-2548">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2548">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="26833-2549">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2549">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="26833-2550">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2550">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="26833-2551">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2551">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="26833-2552">監視</span><span class="sxs-lookup"><span data-stu-id="26833-2552">Monitor</span></span>

* <span data-ttu-id="26833-2553">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="26833-2553">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="26833-2554">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="26833-2554">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="26833-2555">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-2555">Network</span></span>

* <span data-ttu-id="26833-2556">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2556">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="26833-2557">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2557">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="26833-2558">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2558">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="26833-2559">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2559">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="26833-2560">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2560">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="26833-2561">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2561">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="26833-2562">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2562">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="26833-2563">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2563">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="26833-2564">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-2564">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="26833-2565">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2565">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="26833-2566">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="26833-2566">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="26833-2567">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-2567">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="26833-2568">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-2568">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="26833-2569">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-2569">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="26833-2570">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="26833-2570">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="26833-2571">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2571">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="26833-2572">プロファイル</span><span class="sxs-lookup"><span data-stu-id="26833-2572">Profile</span></span>

* <span data-ttu-id="26833-2573">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="26833-2573">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="26833-2574">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="26833-2574">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="26833-2575">Redis</span><span class="sxs-lookup"><span data-stu-id="26833-2575">Redis</span></span>

* <span data-ttu-id="26833-2576">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2576">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="26833-2577">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="26833-2577">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="26833-2578">Resource</span><span class="sxs-lookup"><span data-stu-id="26833-2578">Resource</span></span>

* <span data-ttu-id="26833-2579">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="26833-2579">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="26833-2580">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="26833-2580">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="26833-2581">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="26833-2581">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="26833-2582">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="26833-2582">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="26833-2583">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="26833-2583">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="26833-2584">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2584">Add docs for az lock update.</span></span> <span data-ttu-id="26833-2585">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="26833-2585">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="26833-2586">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="26833-2586">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="26833-2587">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="26833-2587">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="26833-2588">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="26833-2588">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="26833-2589">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="26833-2589">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="26833-2590">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="26833-2590">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="26833-2591">Role</span><span class="sxs-lookup"><span data-stu-id="26833-2591">Role</span></span>

* <span data-ttu-id="26833-2592">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="26833-2592">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="26833-2593">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="26833-2593">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="26833-2594">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="26833-2594">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="26833-2595">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="26833-2595">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="26833-2596">SQL</span><span class="sxs-lookup"><span data-stu-id="26833-2596">SQL</span></span>

* <span data-ttu-id="26833-2597">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="26833-2597">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="26833-2598">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="26833-2598">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="26833-2599">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-2599">Storage</span></span>

* <span data-ttu-id="26833-2600">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="26833-2600">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="26833-2601">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2601">Add support for incremental blob copy</span></span>
* <span data-ttu-id="26833-2602">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="26833-2602">Add support for large block blob upload</span></span>
* <span data-ttu-id="26833-2603">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="26833-2603">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2604">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2604">VM</span></span>

* <span data-ttu-id="26833-2605">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="26833-2605">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="26833-2606">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="26833-2606">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="26833-2607">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="26833-2607">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="26833-2608">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="26833-2608">az vm/vmss disk</span></span>
  3. <span data-ttu-id="26833-2609">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="26833-2609">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="26833-2610">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="26833-2610">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="26833-2611">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="26833-2611">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="26833-2612">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="26833-2612">April 3, 2017</span></span>

<span data-ttu-id="26833-2613">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="26833-2613">Version 2.0.2</span></span>

<span data-ttu-id="26833-2614">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="26833-2614">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="26833-2615">コア</span><span class="sxs-lookup"><span data-stu-id="26833-2615">Core</span></span>

* <span data-ttu-id="26833-2616">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="26833-2616">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="26833-2617">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="26833-2617">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="26833-2618">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="26833-2618">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="26833-2619">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="26833-2619">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="26833-2620">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="26833-2620">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="26833-2621">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="26833-2621">Add prompting for missing template parameters.</span></span> <span data-ttu-id="26833-2622">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="26833-2622">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="26833-2623">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="26833-2623">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="26833-2624">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="26833-2624">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="26833-2625">ACS</span><span class="sxs-lookup"><span data-stu-id="26833-2625">ACS</span></span>

* <span data-ttu-id="26833-2626">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="26833-2626">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="26833-2627">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="26833-2627">Add support for ssh key password prompting.</span></span> <span data-ttu-id="26833-2628">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="26833-2628">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="26833-2629">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="26833-2629">Add support for windows clusters.</span></span> <span data-ttu-id="26833-2630">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="26833-2630">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="26833-2631">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="26833-2631">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="26833-2632">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="26833-2632">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="26833-2633">AppService</span><span class="sxs-lookup"><span data-stu-id="26833-2633">AppService</span></span>

* <span data-ttu-id="26833-2634">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="26833-2634">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="26833-2635">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="26833-2635">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="26833-2636">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="26833-2636">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="26833-2637">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="26833-2637">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="26833-2638">DataLake</span><span class="sxs-lookup"><span data-stu-id="26833-2638">DataLake</span></span>

* <span data-ttu-id="26833-2639">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-2639">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="26833-2640">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="26833-2640">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="26833-2641">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="26833-2641">DocuemntDB</span></span>

* <span data-ttu-id="26833-2642">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="26833-2642">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="26833-2643">VM</span><span class="sxs-lookup"><span data-stu-id="26833-2643">VM</span></span>

* <span data-ttu-id="26833-2644">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="26833-2644">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="26833-2645">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="26833-2645">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="26833-2646">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="26833-2646">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="26833-2647">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="26833-2647">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="26833-2648">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="26833-2648">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="26833-2649">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="26833-2649">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="26833-2650">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="26833-2650">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="26833-2651">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="26833-2651">February 27, 2017</span></span>

<span data-ttu-id="26833-2652">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="26833-2652">Version 2.0.0</span></span>

<span data-ttu-id="26833-2653">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="26833-2653">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="26833-2654">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="26833-2654">Container Service (acs)</span></span>
- <span data-ttu-id="26833-2655">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="26833-2655">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="26833-2656">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="26833-2656">Networking</span></span>
- <span data-ttu-id="26833-2657">Storage</span><span class="sxs-lookup"><span data-stu-id="26833-2657">Storage</span></span>

<span data-ttu-id="26833-2658">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="26833-2658">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="26833-2659">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="26833-2659">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="26833-2660">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="26833-2660">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="26833-2661">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="26833-2661">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="26833-2662">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="26833-2662">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="26833-2663">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="26833-2663">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="26833-2664">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="26833-2664">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="26833-2665">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="26833-2665">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="26833-2666">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="26833-2666">Provide feedback from the command line with the `az feedback` command</span></span>

