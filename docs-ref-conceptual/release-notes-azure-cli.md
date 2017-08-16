---
title: "Azure CLI 2.0 リリース ノート"
description: "Azure CLI 2.0 の最新情報について説明します"
keywords: "Azure CLI 2.0, リリース ノート"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/03/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ce0428f7-0a59-4e72-9237-d907b171af51
ms.openlocfilehash: 3bd4b9c059da3b841fc0757a11bc7ce78ec64b08
ms.sourcegitcommit: 66d997a5afcf32143a4d4817ec1608cbdf58a59f
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="63a86-104">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="63a86-104">Azure CLI 2.0 release notes</span></span>

## <a name="may-10-2017"></a><span data-ttu-id="63a86-105">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="63a86-105">May 10, 2017</span></span>

<span data-ttu-id="63a86-106">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="63a86-106">Version 2.0.6</span></span>

* <span data-ttu-id="63a86-107">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="63a86-107">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="63a86-108">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="63a86-108">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="63a86-109">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-109">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="63a86-110">Cognitive Services モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-110">Include Cognitive Services module.</span></span>
* <span data-ttu-id="63a86-111">Service Fabric モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-111">Include Service Fabric module.</span></span>
* <span data-ttu-id="63a86-112">対話型モジュールが追加されました (az-shell の名前変更)。</span><span class="sxs-lookup"><span data-stu-id="63a86-112">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="63a86-113">CDN コマンドに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="63a86-113">Add support for CDN commands.</span></span>
* <span data-ttu-id="63a86-114">コンテナー モジュールが削除されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-114">Remove Container module.</span></span>
* <span data-ttu-id="63a86-115">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="63a86-115">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="63a86-116">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="63a86-116">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="63a86-117">コア</span><span class="sxs-lookup"><span data-stu-id="63a86-117">Core</span></span>

* <span data-ttu-id="63a86-118">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="63a86-118">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="63a86-119">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="63a86-119">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="63a86-120">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="63a86-120">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="63a86-121">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="63a86-121">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="63a86-122">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="63a86-122">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="63a86-123">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="63a86-123">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="63a86-124">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="63a86-124">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="63a86-125">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="63a86-125">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="63a86-126">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="63a86-126">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="63a86-127">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="63a86-127">core: Improved performance</span></span>
* <span data-ttu-id="63a86-128">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="63a86-128">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="63a86-129">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="63a86-129">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="63a86-130">ACS</span><span class="sxs-lookup"><span data-stu-id="63a86-130">ACS</span></span>

* <span data-ttu-id="63a86-131">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="63a86-131">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="63a86-132">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="63a86-132">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="63a86-133">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="63a86-133">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="63a86-134">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="63a86-134">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="63a86-135">AppService</span><span class="sxs-lookup"><span data-stu-id="63a86-135">AppService</span></span>

* <span data-ttu-id="63a86-136">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="63a86-136">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="63a86-137">Team Services (VSTS) が継続的な配信オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="63a86-137">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="63a86-138">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="63a86-138">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="63a86-139">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="63a86-139">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="63a86-140">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="63a86-140">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="63a86-141">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="63a86-141">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="63a86-142">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="63a86-142">support slot swap with preview</span></span>
* <span data-ttu-id="63a86-143">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="63a86-143">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="63a86-144">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="63a86-144">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="63a86-145">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="63a86-145">CosmosDB</span></span>

* <span data-ttu-id="63a86-146">documentdb モジュールから cosmosdb に名前が変更されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-146">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="63a86-147">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="63a86-147">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="63a86-148">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="63a86-148">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="63a86-149">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="63a86-149">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="63a86-150">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="63a86-150">Data Lake Analytics</span></span>

* <span data-ttu-id="63a86-151">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-151">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="63a86-152">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="63a86-152">Add support for new catalog item type: package.</span></span> <span data-ttu-id="63a86-153">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="63a86-153">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="63a86-154">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="63a86-154">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="63a86-155">テーブル</span><span class="sxs-lookup"><span data-stu-id="63a86-155">Table</span></span>
  * <span data-ttu-id="63a86-156">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="63a86-156">Table valued function</span></span>
  * <span data-ttu-id="63a86-157">表示</span><span class="sxs-lookup"><span data-stu-id="63a86-157">View</span></span>
  * <span data-ttu-id="63a86-158">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="63a86-158">Table Statistics.</span></span> <span data-ttu-id="63a86-159">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="63a86-159">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="63a86-160">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="63a86-160">Data Lake Store</span></span>

* <span data-ttu-id="63a86-161">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-161">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="63a86-162">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="63a86-162">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="63a86-163">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="63a86-163">missed help for access show.</span></span> <span data-ttu-id="63a86-164">追加しました </span><span class="sxs-lookup"><span data-stu-id="63a86-164">adding it.</span></span> <span data-ttu-id="63a86-165">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="63a86-165">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="63a86-166">検索</span><span class="sxs-lookup"><span data-stu-id="63a86-166">Find</span></span>

* <span data-ttu-id="63a86-167">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="63a86-167">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="63a86-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="63a86-168">KeyVault</span></span>

* <span data-ttu-id="63a86-169">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="63a86-169">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="63a86-170">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-170">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="63a86-171">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="63a86-171">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="63a86-172">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-172">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="63a86-173">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="63a86-173">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="63a86-174">ラボ</span><span class="sxs-lookup"><span data-stu-id="63a86-174">Lab</span></span>

* <span data-ttu-id="63a86-175">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-175">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="63a86-176">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-176">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="63a86-177">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-177">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="63a86-178">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-178">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="63a86-179">ラボ内でシークレットを管理するためのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-179">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="63a86-180">監視</span><span class="sxs-lookup"><span data-stu-id="63a86-180">Monitor</span></span>

* <span data-ttu-id="63a86-181">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="63a86-181">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="63a86-182">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="63a86-182">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="63a86-183">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="63a86-183">Network</span></span>

* <span data-ttu-id="63a86-184">`network watcher test-connectivity` コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-184">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="63a86-185">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="63a86-185">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="63a86-186">Application Gateway 接続のドレインに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="63a86-186">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="63a86-187">Application Gateway WAF 規則セットの構成に対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="63a86-187">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="63a86-188">ExpressRoute ルート フィルターとルールに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="63a86-188">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="63a86-189">TrafficManager の地理的なルーティングに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="63a86-189">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="63a86-190">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="63a86-190">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="63a86-191">VPN 接続 IPSec ポリシーに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="63a86-191">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="63a86-192">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-192">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="63a86-193">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="63a86-193">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="63a86-194">`network vpn-connection list/show` コマンドの出力から null 値が削除されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-194">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="63a86-195">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="63a86-195">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="63a86-196">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-196">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="63a86-197">`dns zone import` でレコードが適切にインポートされないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-197">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="63a86-198">`traffic-manager endpoint update` が動作しないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="63a86-198">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="63a86-199">"Network Watcher" プレビューのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-199">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="63a86-200">プロファイル</span><span class="sxs-lookup"><span data-stu-id="63a86-200">Profile</span></span>

* <span data-ttu-id="63a86-201">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="63a86-201">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="63a86-202">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="63a86-202">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="63a86-203">Redis</span><span class="sxs-lookup"><span data-stu-id="63a86-203">Redis</span></span>

* <span data-ttu-id="63a86-204">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="63a86-204">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="63a86-205">"update-settings" コマンドが廃止されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-205">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="63a86-206">リソース</span><span class="sxs-lookup"><span data-stu-id="63a86-206">Resource</span></span>

* <span data-ttu-id="63a86-207">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="63a86-207">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="63a86-208">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="63a86-208">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="63a86-209">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="63a86-209">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="63a86-210">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="63a86-210">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="63a86-211">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="63a86-211">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="63a86-212">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="63a86-212">Add docs for az lock update.</span></span> <span data-ttu-id="63a86-213">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="63a86-213">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="63a86-214">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="63a86-214">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="63a86-215">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="63a86-215">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="63a86-216">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-216">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="63a86-217">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="63a86-217">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="63a86-218">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="63a86-218">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="63a86-219">役割</span><span class="sxs-lookup"><span data-stu-id="63a86-219">Role</span></span>

* <span data-ttu-id="63a86-220">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="63a86-220">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="63a86-221">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="63a86-221">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="63a86-222">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="63a86-222">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="63a86-223">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="63a86-223">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="63a86-224">SQL</span><span class="sxs-lookup"><span data-stu-id="63a86-224">SQL</span></span>

* <span data-ttu-id="63a86-225">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="63a86-225">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="63a86-226">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="63a86-226">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="63a86-227">Storage</span><span class="sxs-lookup"><span data-stu-id="63a86-227">Storage</span></span>

* <span data-ttu-id="63a86-228">`storage account create` のリソース グループの場所に対する既定の場所。</span><span class="sxs-lookup"><span data-stu-id="63a86-228">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="63a86-229">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="63a86-229">Add support for incremental blob copy</span></span>
* <span data-ttu-id="63a86-230">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="63a86-230">Add support for large block blob upload</span></span>
* <span data-ttu-id="63a86-231">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="63a86-231">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="63a86-232">VM</span><span class="sxs-lookup"><span data-stu-id="63a86-232">VM</span></span>

* <span data-ttu-id="63a86-233">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="63a86-233">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="63a86-234">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="63a86-234">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="63a86-235">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="63a86-235">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="63a86-236">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="63a86-236">az vm/vmss disk</span></span>
  3. <span data-ttu-id="63a86-237">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="63a86-237">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="63a86-238">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="63a86-238">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="63a86-239">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="63a86-239">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="63a86-240">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="63a86-240">April 3, 2017</span></span>

<span data-ttu-id="63a86-241">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="63a86-241">Version 2.0.2</span></span>

<span data-ttu-id="63a86-242">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました。</span><span class="sxs-lookup"><span data-stu-id="63a86-242">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="63a86-243">コア</span><span class="sxs-lookup"><span data-stu-id="63a86-243">Core</span></span>

* <span data-ttu-id="63a86-244">既定の一覧に acr、lab、monitor、find モジュールを追加。</span><span class="sxs-lookup"><span data-stu-id="63a86-244">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="63a86-245">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="63a86-245">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="63a86-246">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="63a86-246">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="63a86-247">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="63a86-247">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="63a86-248">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="63a86-248">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="63a86-249">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="63a86-249">Add prompting for missing template parameters.</span></span> <span data-ttu-id="63a86-250">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="63a86-250">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="63a86-251">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="63a86-251">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="63a86-252">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="63a86-252">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="63a86-253">ACS</span><span class="sxs-lookup"><span data-stu-id="63a86-253">ACS</span></span>

* [<span data-ttu-id="63a86-254">ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554</span><span class="sxs-lookup"><span data-stu-id="63a86-254">ACS] Adding support for configuring a default ACS cluster ([#2554</span></span>](https://github.com/Azure/azure-cli/pull/2554))
* <span data-ttu-id="63a86-255">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="63a86-255">Add support for ssh key password prompting.</span></span> <span data-ttu-id="63a86-256">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="63a86-256">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="63a86-257">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="63a86-257">Add support for windows clusters.</span></span> <span data-ttu-id="63a86-258">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="63a86-258">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="63a86-259">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="63a86-259">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="63a86-260">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="63a86-260">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="63a86-261">AppService</span><span class="sxs-lookup"><span data-stu-id="63a86-261">AppService</span></span>

* <span data-ttu-id="63a86-262">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="63a86-262">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="63a86-263">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="63a86-263">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="63a86-264">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="63a86-264">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="63a86-265">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="63a86-265">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="63a86-266">DataLake</span><span class="sxs-lookup"><span data-stu-id="63a86-266">DataLake</span></span>

* <span data-ttu-id="63a86-267">Data Lake Analytics モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="63a86-267">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="63a86-268">Data Lake Store モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="63a86-268">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="63a86-269">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="63a86-269">DocuemntDB</span></span>

* <span data-ttu-id="63a86-270">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="63a86-270">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="63a86-271">VM</span><span class="sxs-lookup"><span data-stu-id="63a86-271">VM</span></span>

* [<span data-ttu-id="63a86-272">コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570</span><span class="sxs-lookup"><span data-stu-id="63a86-272">Compute] Add AppGateway support to virtual machine scale set create ([#2570</span></span>](https://github.com/Azure/azure-cli/pull/2570))
* [<span data-ttu-id="63a86-273">VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522</span><span class="sxs-lookup"><span data-stu-id="63a86-273">VM/VMSS] Improved disk caching support ([#2522</span></span>](https://github.com/Azure/azure-cli/pull/2522))
* <span data-ttu-id="63a86-274">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="63a86-274">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="63a86-275">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="63a86-275">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="63a86-276">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート * ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="63a86-276">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="63a86-277">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="63a86-277">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="63a86-278">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="63a86-278">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="63a86-279">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="63a86-279">February 27, 2017</span></span>

<span data-ttu-id="63a86-280">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="63a86-280">Version 2.0.0</span></span>

<span data-ttu-id="63a86-281">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。</span><span class="sxs-lookup"><span data-stu-id="63a86-281">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="63a86-282">一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="63a86-282">General availability applies to these command modules:</span></span>
- <span data-ttu-id="63a86-283">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="63a86-283">Container Service (acs)</span></span>
- <span data-ttu-id="63a86-284">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="63a86-284">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="63a86-285">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="63a86-285">Networking</span></span>
- <span data-ttu-id="63a86-286">Storage</span><span class="sxs-lookup"><span data-stu-id="63a86-286">Storage</span></span>

<span data-ttu-id="63a86-287">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="63a86-287">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="63a86-288">問題は、Microsoft サポートで直接開くことも、[github の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="63a86-288">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="63a86-289">[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="63a86-289">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
<span data-ttu-id="63a86-290">`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="63a86-290">You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="63a86-291">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません。</span><span class="sxs-lookup"><span data-stu-id="63a86-291">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="63a86-292">CLI のバージョンを確認するには、`az --version` を使用します。</span><span class="sxs-lookup"><span data-stu-id="63a86-292">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="63a86-293">出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="63a86-293">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="63a86-294">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。</span><span class="sxs-lookup"><span data-stu-id="63a86-294">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="63a86-295">これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です。</span><span class="sxs-lookup"><span data-stu-id="63a86-295">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="63a86-296">CLI のナイトリー プレビュー ビルドもあります。</span><span class="sxs-lookup"><span data-stu-id="63a86-296">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="63a86-297">詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63a86-297">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="63a86-298">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="63a86-298">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="63a86-299">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="63a86-299">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="63a86-300">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる。</span><span class="sxs-lookup"><span data-stu-id="63a86-300">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="63a86-301">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る。</span><span class="sxs-lookup"><span data-stu-id="63a86-301">Provide feedback from the command line with the `az feedback` command.</span></span>

