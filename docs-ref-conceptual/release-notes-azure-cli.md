---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 10/09/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 0aec9dce0eda007c71df3693b39c7ec8cc9856cd
ms.sourcegitcommit: 0fc354c24454f5c9c5ff4b7296ad7b18ffdf31b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2018
ms.locfileid: "48904788"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="84595-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="84595-103">Azure CLI release notes</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="84595-104">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="84595-104">October 9, 2018</span></span>

<span data-ttu-id="84595-105">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="84595-105">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="84595-106">コア</span><span class="sxs-lookup"><span data-stu-id="84595-106">Core</span></span>
* <span data-ttu-id="84595-107">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-107">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="84595-108">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-108">ACR</span></span>
* <span data-ttu-id="84595-109">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-109">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="84595-110">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-110">ACS</span></span>
* <span data-ttu-id="84595-111">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="84595-111">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="84595-112">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-112">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="84595-113">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-113">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="84595-114">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-114">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="84595-115">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-115">Container</span></span>
* <span data-ttu-id="84595-116">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-116">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="84595-117">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-117">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="84595-118">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="84595-118">Event Hub</span></span>
* <span data-ttu-id="84595-119">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-119">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="84595-120">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-120">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="84595-121">拡張機能</span><span class="sxs-lookup"><span data-stu-id="84595-121">Extensions</span></span>
* <span data-ttu-id="84595-122">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-122">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="84595-123">HDInsight</span><span class="sxs-lookup"><span data-stu-id="84595-123">HDInsight</span></span>
* <span data-ttu-id="84595-124">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-124">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="84595-125">IoT</span><span class="sxs-lookup"><span data-stu-id="84595-125">IoT</span></span>
* <span data-ttu-id="84595-126">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-126">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="84595-127">KeyVault</span><span class="sxs-lookup"><span data-stu-id="84595-127">KeyVault</span></span>
* <span data-ttu-id="84595-128">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-128">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="84595-129">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-129">Network</span></span>
* <span data-ttu-id="84595-130">`network dns zone create` を修正しました: ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="84595-130">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="84595-131">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="84595-131">See #6052</span></span>
* <span data-ttu-id="84595-132">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-132">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="84595-133">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="84595-133">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="84595-134">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-134">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="84595-135">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-135">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="84595-136">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-136">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="84595-137">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-137">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="84595-138">Role</span><span class="sxs-lookup"><span data-stu-id="84595-138">Role</span></span>
* <span data-ttu-id="84595-139">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-139">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="84595-140">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-140">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="84595-141">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-141">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="84595-142">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-142">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="84595-143">Service Bus</span><span class="sxs-lookup"><span data-stu-id="84595-143">Service Bus</span></span>
* <span data-ttu-id="84595-144">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-144">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="84595-145">VM</span><span class="sxs-lookup"><span data-stu-id="84595-145">VM</span></span>
* <span data-ttu-id="84595-146">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-146">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="84595-147">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-147">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="84595-148">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-148">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="84595-149">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-149">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="84595-150">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-150">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="84595-151">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-151">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="84595-152">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="84595-152">September 21, 2018</span></span>

<span data-ttu-id="84595-153">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="84595-153">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="84595-154">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-154">ACR</span></span>
* <span data-ttu-id="84595-155">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-155">Added ACR Task commands</span></span>
* <span data-ttu-id="84595-156">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-156">Added quick run command</span></span>
* <span data-ttu-id="84595-157">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-157">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="84595-158">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-158">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="84595-159">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-159">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="84595-160">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-160">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="84595-161">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-161">ACS</span></span>
* <span data-ttu-id="84595-162">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-162">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="84595-163">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-163">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-164">AppService</span><span class="sxs-lookup"><span data-stu-id="84595-164">AppService</span></span>

* <span data-ttu-id="84595-165">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-165">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="84595-166">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-166">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="84595-167">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-167">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="84595-168">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-168">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="84595-169">Batch</span><span class="sxs-lookup"><span data-stu-id="84595-169">Batch</span></span>
* <span data-ttu-id="84595-170">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-170">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="84595-171">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-171">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="84595-172">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-172">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="84595-173">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-173">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="84595-174">Batch AI</span><span class="sxs-lookup"><span data-stu-id="84595-174">Batch AI</span></span> 
* <span data-ttu-id="84595-175">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-175">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="84595-176">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="84595-176">Cognitive Services</span></span>
* <span data-ttu-id="84595-177">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-177">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="84595-178">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-178">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="84595-179">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-179">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="84595-180">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-180">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="84595-181">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-181">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="84595-182">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-182">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="84595-183">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-183">Container</span></span>
* <span data-ttu-id="84595-184">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-184">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="84595-185">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-185">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="84595-186">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-186">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="84595-187">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-187">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="84595-188">DataLake</span><span class="sxs-lookup"><span data-stu-id="84595-188">Datalake</span></span>
* <span data-ttu-id="84595-189">仮想ネットワーク ルール用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-189">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="84595-190">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="84595-190">Interactive Shell</span></span>
* <span data-ttu-id="84595-191">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-191">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="84595-192">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-192">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="84595-193">IoT</span><span class="sxs-lookup"><span data-stu-id="84595-193">IoT</span></span>
* <span data-ttu-id="84595-194">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-194">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="84595-195">Key Vault</span><span class="sxs-lookup"><span data-stu-id="84595-195">Key Vault</span></span>
* <span data-ttu-id="84595-196">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-196">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="84595-197">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-197">Network</span></span>
* <span data-ttu-id="84595-198">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-198">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="84595-199">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-199">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="84595-200">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-200">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="84595-201">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-201">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="84595-202">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-202">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="84595-203">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-203">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="84595-204">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="84595-204">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="84595-205">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-205">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="84595-206">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-206">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="84595-207">`network express-route create/update`: `--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-207">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="84595-208">`network vnet subnet create/update`: `--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-208">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="84595-209">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-209">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="84595-210">`network traffic-manager profile create/update`: 監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、`--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-210">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="84595-211">`network lb frontend-ip create/update`: プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="84595-211">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="84595-212">`dns record-set * create/update`: `--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-212">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="84595-213">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-213">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="84595-214">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-214">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="84595-215">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-215">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="84595-216">RDBMS</span><span class="sxs-lookup"><span data-stu-id="84595-216">RDBMS</span></span>
* <span data-ttu-id="84595-217">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-217">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="84595-218">予約</span><span class="sxs-lookup"><span data-stu-id="84595-218">Reservation</span></span>
* <span data-ttu-id="84595-219">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-219">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="84595-220">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-220">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="84595-221">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="84595-221">Manage App</span></span>
* <span data-ttu-id="84595-222">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-222">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="84595-223">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-223">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="84595-224">Role</span><span class="sxs-lookup"><span data-stu-id="84595-224">Role</span></span>
* <span data-ttu-id="84595-225">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-225">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="84595-226">SignalR</span><span class="sxs-lookup"><span data-stu-id="84595-226">SignalR</span></span>
* <span data-ttu-id="84595-227">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-227">First release</span></span>

### <a name="storage"></a><span data-ttu-id="84595-228">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-228">Storage</span></span>
* <span data-ttu-id="84595-229">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-229">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="84595-230">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-230">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="84595-231">VM</span><span class="sxs-lookup"><span data-stu-id="84595-231">VM</span></span>
* <span data-ttu-id="84595-232">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="84595-232">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="84595-233">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-233">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="84595-234">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="84595-234">August 28, 2018</span></span>

<span data-ttu-id="84595-235">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="84595-235">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="84595-236">コア</span><span class="sxs-lookup"><span data-stu-id="84595-236">Core</span></span>

* <span data-ttu-id="84595-237">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-237">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="84595-238">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-238">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="84595-239">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-239">ACR</span></span>

* <span data-ttu-id="84595-240">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-240">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="84595-241">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-241">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="84595-242">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-242">ACS</span></span>

* <span data-ttu-id="84595-243">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-243">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="84595-244">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-244">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-245">AppService</span><span class="sxs-lookup"><span data-stu-id="84595-245">AppService</span></span>

* <span data-ttu-id="84595-246">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-246">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="84595-247">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-247">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="84595-248">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-248">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="84595-249">バックアップ</span><span class="sxs-lookup"><span data-stu-id="84595-249">Backup</span></span>

* <span data-ttu-id="84595-250">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-250">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="84595-251">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="84595-251">Bot Service</span></span>

* <span data-ttu-id="84595-252">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="84595-252">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="84595-253">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="84595-253">Cognitive Services</span></span>

* <span data-ttu-id="84595-254">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-254">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="84595-255">IoT</span><span class="sxs-lookup"><span data-stu-id="84595-255">IoT</span></span>

* <span data-ttu-id="84595-256">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-256">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="84595-257">監視</span><span class="sxs-lookup"><span data-stu-id="84595-257">Monitor</span></span>

* <span data-ttu-id="84595-258">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-258">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="84595-259">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-259">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="84595-260">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-260">Network</span></span>

* <span data-ttu-id="84595-261">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-261">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="84595-262">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-262">Resource</span></span>

* <span data-ttu-id="84595-263">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-263">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="84595-264">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-264">Storage</span></span>

* <span data-ttu-id="84595-265">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-265">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="84595-266">VM</span><span class="sxs-lookup"><span data-stu-id="84595-266">VM</span></span>

* <span data-ttu-id="84595-267">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-267">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="84595-268">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-268">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="84595-269">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="84595-269">Auguest 14, 2018</span></span>

<span data-ttu-id="84595-270">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="84595-270">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="84595-271">コア</span><span class="sxs-lookup"><span data-stu-id="84595-271">Core</span></span>

* <span data-ttu-id="84595-272">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-272">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="84595-273">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-273">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="84595-274">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="84595-274">Telemetry</span></span>

* <span data-ttu-id="84595-275">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-275">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="84595-276">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-276">ACR</span></span>

* <span data-ttu-id="84595-277">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-277">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="84595-278">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-278">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="84595-279">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-279">ACS</span></span>

* <span data-ttu-id="84595-280">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-280">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="84595-281">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-281">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="84595-282">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-282">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="84595-283">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-283">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="84595-284">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-284">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="84595-285">AppService</span><span class="sxs-lookup"><span data-stu-id="84595-285">AppService</span></span>

* <span data-ttu-id="84595-286">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-286">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="84595-287">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-287">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="84595-288">BatchAI</span><span class="sxs-lookup"><span data-stu-id="84595-288">BatchAI</span></span>

* <span data-ttu-id="84595-289">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="84595-289">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="84595-290">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-290">Container</span></span>

* <span data-ttu-id="84595-291">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-291">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="84595-292">IoT</span><span class="sxs-lookup"><span data-stu-id="84595-292">IoT</span></span>

* <span data-ttu-id="84595-293">[破壊的変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-293">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="84595-294">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-294">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="84595-295">Iot Central</span><span class="sxs-lookup"><span data-stu-id="84595-295">Iot Central</span></span>

* <span data-ttu-id="84595-296">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-296">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="84595-297">KeyVault</span><span class="sxs-lookup"><span data-stu-id="84595-297">KeyVault</span></span>


* <span data-ttu-id="84595-298">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-298">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="84595-299">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-299">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="84595-300">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-300">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="84595-301">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-301">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="84595-302">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-302">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="84595-303">リレー</span><span class="sxs-lookup"><span data-stu-id="84595-303">Relay</span></span>

* <span data-ttu-id="84595-304">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-304">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="84595-305">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-305">Sql</span></span>

* <span data-ttu-id="84595-306">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-306">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="84595-307">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-307">Storage</span></span>

* <span data-ttu-id="84595-308">[破壊的変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="84595-308">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="84595-309">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-309">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="84595-310">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="84595-310">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="84595-311">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-311">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="84595-312">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-312">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="84595-313">VM</span><span class="sxs-lookup"><span data-stu-id="84595-313">VM</span></span>

* <span data-ttu-id="84595-314">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-314">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="84595-315">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="84595-315">July 31, 2018</span></span>

<span data-ttu-id="84595-316">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="84595-316">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="84595-317">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-317">ACR</span></span>

* <span data-ttu-id="84595-318">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-318">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="84595-319">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-319">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="84595-320">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-320">ACS</span></span>

* <span data-ttu-id="84595-321">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-321">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="84595-322">Batch</span><span class="sxs-lookup"><span data-stu-id="84595-322">Batch</span></span>

* <span data-ttu-id="84595-323">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-323">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="84595-324">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-324">Container</span></span>

* <span data-ttu-id="84595-325">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-325">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="84595-326">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-326">Network</span></span>

* <span data-ttu-id="84595-327">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-327">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="84595-328">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-328">Resource</span></span>

* <span data-ttu-id="84595-329">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-329">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="84595-330">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-330">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="84595-331">Role</span><span class="sxs-lookup"><span data-stu-id="84595-331">Role</span></span>

* <span data-ttu-id="84595-332">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-332">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="84595-333">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-333">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="84595-334">Search</span><span class="sxs-lookup"><span data-stu-id="84595-334">Search</span></span>

* <span data-ttu-id="84595-335">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-335">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="84595-336">Service Bus</span><span class="sxs-lookup"><span data-stu-id="84595-336">Service Bus</span></span>

* <span data-ttu-id="84595-337">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-337">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="84595-338">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-338">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="84595-339">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="84595-339">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="84595-340">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="84595-340">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="84595-341">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-341">Storage</span></span>

* <span data-ttu-id="84595-342">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-342">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="84595-343">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="84595-343">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="84595-344">VM</span><span class="sxs-lookup"><span data-stu-id="84595-344">VM</span></span>

* <span data-ttu-id="84595-345">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-345">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="84595-346">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-346">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="84595-347">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-347">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="84595-348">[破壊的変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-348">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="84595-349">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="84595-349">July 18, 2018</span></span>

<span data-ttu-id="84595-350">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="84595-350">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="84595-351">コア</span><span class="sxs-lookup"><span data-stu-id="84595-351">Core</span></span>

* <span data-ttu-id="84595-352">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-352">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="84595-353">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-353">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="84595-354">[破壊的変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-354">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="84595-355">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-355">ACR</span></span>

* <span data-ttu-id="84595-356">[破壊的変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-356">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="84595-357">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-357">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="84595-358">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-358">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="84595-359">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-359">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="84595-360">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-360">ACS</span></span>

* <span data-ttu-id="84595-361">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-361">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-362">AppService</span><span class="sxs-lookup"><span data-stu-id="84595-362">AppService</span></span>

* <span data-ttu-id="84595-363">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-363">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="84595-364">Batch</span><span class="sxs-lookup"><span data-stu-id="84595-364">Batch</span></span>

* <span data-ttu-id="84595-365">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-365">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="84595-366">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-366">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="84595-367">Batch AI</span><span class="sxs-lookup"><span data-stu-id="84595-367">Batch AI</span></span>

* <span data-ttu-id="84595-368">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-368">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="84595-369">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-369">Container</span></span>

* <span data-ttu-id="84595-370">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-370">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="84595-371">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-371">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="84595-372">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-372">Network</span></span>

* <span data-ttu-id="84595-373">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-373">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="84595-374">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-374">Added `network nic wait`</span></span>
* <span data-ttu-id="84595-375">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-375">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="84595-376">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-376">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="84595-377">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-377">Resource</span></span>

* <span data-ttu-id="84595-378">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-378">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="84595-379">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-379">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="84595-380">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-380">Added `deployment wait` command</span></span>
* <span data-ttu-id="84595-381">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-381">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="84595-382">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-382">SQL</span></span>

* <span data-ttu-id="84595-383">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-383">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="84595-384">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-384">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="84595-385">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="84595-385">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="84595-386">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-386">Storage</span></span>

* <span data-ttu-id="84595-387">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-387">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="84595-388">VM</span><span class="sxs-lookup"><span data-stu-id="84595-388">VM</span></span>

* <span data-ttu-id="84595-389">[破壊的変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-389">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="84595-390">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-390">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="84595-391">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-391">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="84595-392">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="84595-392">July 3, 2018</span></span>

<span data-ttu-id="84595-393">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="84595-393">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="84595-394">AKS</span><span class="sxs-lookup"><span data-stu-id="84595-394">AKS</span></span>

* <span data-ttu-id="84595-395">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-395">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="84595-396">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="84595-396">July 3, 2018</span></span>

<span data-ttu-id="84595-397">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="84595-397">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="84595-398">コア</span><span class="sxs-lookup"><span data-stu-id="84595-398">Core</span></span>

* <span data-ttu-id="84595-399">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-399">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="84595-400">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-400">ACR</span></span>

* <span data-ttu-id="84595-401">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-401">Added polling build status</span></span>
* <span data-ttu-id="84595-402">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-402">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="84595-403">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-403">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="84595-404">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-404">ACS</span></span>

* <span data-ttu-id="84595-405">[破壊的変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-405">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="84595-406">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-406">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="84595-407">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="84595-407">Updated options for `aks browse` command.</span></span> <span data-ttu-id="84595-408">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-408">Added `--listen-port` support</span></span>
* <span data-ttu-id="84595-409">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="84595-409">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="84595-410">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="84595-410">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="84595-411">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-411">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-412">AppService</span><span class="sxs-lookup"><span data-stu-id="84595-412">AppService</span></span>

* <span data-ttu-id="84595-413">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-413">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="84595-414">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-414">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="84595-415">バックアップ</span><span class="sxs-lookup"><span data-stu-id="84595-415">Backup</span></span>

* <span data-ttu-id="84595-416">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-416">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="84595-417">BatchAI</span><span class="sxs-lookup"><span data-stu-id="84595-417">BatchAI</span></span>

* <span data-ttu-id="84595-418">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-418">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="84595-419">クラウド</span><span class="sxs-lookup"><span data-stu-id="84595-419">Cloud</span></span>

* <span data-ttu-id="84595-420">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-420">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="84595-421">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-421">Container</span></span>

* <span data-ttu-id="84595-422">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-422">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="84595-423">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-423">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="84595-424">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-424">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="84595-425">内線番号</span><span class="sxs-lookup"><span data-stu-id="84595-425">Extension</span></span>

* <span data-ttu-id="84595-426">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-426">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="84595-427">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-427">Network</span></span>

* <span data-ttu-id="84595-428">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-428">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="84595-429">Rdbms</span><span class="sxs-lookup"><span data-stu-id="84595-429">Rdbms</span></span>

* <span data-ttu-id="84595-430">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-430">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="84595-431">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-431">Resource</span></span>

* <span data-ttu-id="84595-432">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-432">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="84595-433">VM</span><span class="sxs-lookup"><span data-stu-id="84595-433">VM</span></span>

* <span data-ttu-id="84595-434">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-434">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="84595-435">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="84595-435">June 25, 2018</span></span>

<span data-ttu-id="84595-436">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="84595-436">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="84595-437">CLI</span><span class="sxs-lookup"><span data-stu-id="84595-437">CLI</span></span>

* <span data-ttu-id="84595-438">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-438">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="84595-439">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="84595-439">June 19, 2018</span></span>

<span data-ttu-id="84595-440">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="84595-440">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="84595-441">コア</span><span class="sxs-lookup"><span data-stu-id="84595-441">Core</span></span>

* <span data-ttu-id="84595-442">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-442">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="84595-443">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-443">ACR</span></span>

* <span data-ttu-id="84595-444">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-444">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="84595-445">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-445">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="84595-446">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-446">ACS</span></span>

* <span data-ttu-id="84595-447">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="84595-447">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="84595-448">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-448">Added `--update` support</span></span>
* <span data-ttu-id="84595-449">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-449">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="84595-450">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="84595-450">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="84595-451">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-451">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="84595-452">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="84595-452">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="84595-453">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-453">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="84595-454">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-454">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-455">AppService</span><span class="sxs-lookup"><span data-stu-id="84595-455">AppService</span></span>

* <span data-ttu-id="84595-456">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-456">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="84595-457">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-457">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="84595-458">Batch</span><span class="sxs-lookup"><span data-stu-id="84595-458">Batch</span></span>

* <span data-ttu-id="84595-459">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-459">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="84595-460">Batch AI</span><span class="sxs-lookup"><span data-stu-id="84595-460">Batch AI</span></span>

* <span data-ttu-id="84595-461">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-461">Added support for workspaces.</span></span> <span data-ttu-id="84595-462">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="84595-462">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="84595-463">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-463">Added support for experiments.</span></span> <span data-ttu-id="84595-464">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="84595-464">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="84595-465">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-465">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="84595-466">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-466">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="84595-467">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="84595-467">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="84595-468">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-468">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="84595-469">[破壊的変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="84595-469">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="84595-470">[破壊的変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="84595-470">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="84595-471">[破壊的変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="84595-471">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="84595-472">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="84595-472">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="84595-473">[破壊的変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="84595-473">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="84595-474">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="84595-474">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="84595-475">[破壊的変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="84595-475">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="84595-476">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="84595-476">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="84595-477">[破壊的変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-477">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="84595-478">[破壊的変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="84595-478">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
 - <span data-ttu-id="84595-479">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-479">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
 - <span data-ttu-id="84595-480">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-480">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="84595-481">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-481">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="84595-482">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-482">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="84595-483">マップ</span><span class="sxs-lookup"><span data-stu-id="84595-483">Maps</span></span>

* <span data-ttu-id="84595-484">[破壊的変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-484">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="84595-485">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-485">Network</span></span>

* <span data-ttu-id="84595-486">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="84595-486">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="84595-487">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="84595-487">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="84595-488">#6502</span><span class="sxs-lookup"><span data-stu-id="84595-488">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="84595-489">Reservations</span><span class="sxs-lookup"><span data-stu-id="84595-489">Reservations</span></span>

* <span data-ttu-id="84595-490">[破壊的変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-490">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="84595-491">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-491">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="84595-492">[破壊的変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-492">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="84595-493">[破壊的変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-493">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="84595-494">[破壊的変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-494">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="84595-495">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-495">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="84595-496">Role</span><span class="sxs-lookup"><span data-stu-id="84595-496">Role</span></span>

* <span data-ttu-id="84595-497">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-497">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="84595-498">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-498">SQL</span></span>

* <span data-ttu-id="84595-499">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-499">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="84595-500">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-500">Storage</span></span>

* <span data-ttu-id="84595-501">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="84595-501">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="84595-502">VM</span><span class="sxs-lookup"><span data-stu-id="84595-502">VM</span></span>

* <span data-ttu-id="84595-503">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-503">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="84595-504">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-504">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="84595-505">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-505">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="84595-506">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="84595-506">June 13, 2018</span></span>

<span data-ttu-id="84595-507">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="84595-507">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="84595-508">コア</span><span class="sxs-lookup"><span data-stu-id="84595-508">Core</span></span>

* <span data-ttu-id="84595-509">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-509">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="84595-510">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="84595-510">June 13, 2018</span></span>

<span data-ttu-id="84595-511">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="84595-511">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="84595-512">AKS</span><span class="sxs-lookup"><span data-stu-id="84595-512">AKS</span></span>

* <span data-ttu-id="84595-513">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-513">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="84595-514">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-514">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="84595-515">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-515">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="84595-516">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-516">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="84595-517">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-517">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-518">AppService</span><span class="sxs-lookup"><span data-stu-id="84595-518">AppService</span></span>

* <span data-ttu-id="84595-519">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-519">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="84595-520">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="84595-520">June 5, 2018</span></span>

<span data-ttu-id="84595-521">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="84595-521">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="84595-522">Interactive</span><span class="sxs-lookup"><span data-stu-id="84595-522">Interactive</span></span>

* <span data-ttu-id="84595-523">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-523">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="84595-524">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="84595-524">June 5, 2018</span></span>

<span data-ttu-id="84595-525">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="84595-525">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="84595-526">コア</span><span class="sxs-lookup"><span data-stu-id="84595-526">Core</span></span>

* <span data-ttu-id="84595-527">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-527">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="84595-528">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="84595-528">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="84595-529">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-529">ACR</span></span>

* <span data-ttu-id="84595-530">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-530">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="84595-531">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-531">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="84595-532">AKS</span><span class="sxs-lookup"><span data-stu-id="84595-532">AKS</span></span>

* <span data-ttu-id="84595-533">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-533">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="84595-534">Batch</span><span class="sxs-lookup"><span data-stu-id="84595-534">Batch</span></span>

* <span data-ttu-id="84595-535">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-535">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="84595-536">IoT</span><span class="sxs-lookup"><span data-stu-id="84595-536">IOT</span></span>

* <span data-ttu-id="84595-537">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-537">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="84595-538">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-538">Network</span></span>

* <span data-ttu-id="84595-539">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="84595-539">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="84595-540">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="84595-540">Policy Insights</span></span>

* <span data-ttu-id="84595-541">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-541">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="84595-542">ARM</span><span class="sxs-lookup"><span data-stu-id="84595-542">ARM</span></span>

* <span data-ttu-id="84595-543">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-543">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="84595-544">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-544">SQL</span></span>

* <span data-ttu-id="84595-545">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-545">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="84595-546">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-546">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="84595-547">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-547">Storage</span></span>

* <span data-ttu-id="84595-548">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-548">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="84595-549">VM</span><span class="sxs-lookup"><span data-stu-id="84595-549">VM</span></span>

* <span data-ttu-id="84595-550">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-550">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="84595-551">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-551">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="84595-552">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-552">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="84595-553">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="84595-553">May 22, 2018</span></span>

<span data-ttu-id="84595-554">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="84595-554">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="84595-555">コア</span><span class="sxs-lookup"><span data-stu-id="84595-555">Core</span></span>

* <span data-ttu-id="84595-556">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-556">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="84595-557">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-557">ACS</span></span>

* <span data-ttu-id="84595-558">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-558">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="84595-559">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-559">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-560">AppService</span><span class="sxs-lookup"><span data-stu-id="84595-560">AppService</span></span>

* <span data-ttu-id="84595-561">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="84595-561">Improved generic update commands</span></span>
* <span data-ttu-id="84595-562">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-562">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="84595-563">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-563">Container</span></span>

* <span data-ttu-id="84595-564">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-564">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="84595-565">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-565">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="84595-566">内線番号</span><span class="sxs-lookup"><span data-stu-id="84595-566">Extension</span></span>

* <span data-ttu-id="84595-567">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="84595-567">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="84595-568">Interactive</span><span class="sxs-lookup"><span data-stu-id="84595-568">Interactive</span></span>

* <span data-ttu-id="84595-569">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-569">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="84595-570">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="84595-570">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="84595-571">KeyVault</span><span class="sxs-lookup"><span data-stu-id="84595-571">KeyVault</span></span>

* <span data-ttu-id="84595-572">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-572">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="84595-573">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-573">Network</span></span>

* <span data-ttu-id="84595-574">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-574">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="84595-575">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-575">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="84595-576">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-576">SQL</span></span>

* <span data-ttu-id="84595-577">[破壊的変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="84595-577">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="84595-578">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-578">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="84595-579">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-579">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="84595-580">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-580">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="84595-581">[破壊的変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="84595-581">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="84595-582">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="84595-582">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="84595-583">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="84595-583">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="84595-584">`edition`</span><span class="sxs-lookup"><span data-stu-id="84595-584">`edition`.</span></span> <span data-ttu-id="84595-585">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="84595-585">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="84595-586">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="84595-586">`elasticPoolName`.</span></span> <span data-ttu-id="84595-587">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="84595-587">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="84595-588">[破壊的変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="84595-588">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="84595-589">`edition`</span><span class="sxs-lookup"><span data-stu-id="84595-589">`edition`.</span></span> <span data-ttu-id="84595-590">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="84595-590">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="84595-591">`dtu`</span><span class="sxs-lookup"><span data-stu-id="84595-591">`dtu`.</span></span> <span data-ttu-id="84595-592">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="84595-592">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="84595-593">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="84595-593">`databaseDtuMin`.</span></span> <span data-ttu-id="84595-594">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="84595-594">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="84595-595">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="84595-595">`databaseDtuMax`.</span></span> <span data-ttu-id="84595-596">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="84595-596">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="84595-597">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-597">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="84595-598">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-598">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="84595-599">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-599">Storage</span></span>

* <span data-ttu-id="84595-600">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-600">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="84595-601">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-601">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="84595-602">VM</span><span class="sxs-lookup"><span data-stu-id="84595-602">VM</span></span>

* <span data-ttu-id="84595-603">[破壊的変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="84595-603">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="84595-604">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="84595-604">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="84595-605">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-605">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="84595-606">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-606">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="84595-607">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-607">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="84595-608">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="84595-608">May 7, 2018</span></span>

<span data-ttu-id="84595-609">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="84595-609">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="84595-610">コア</span><span class="sxs-lookup"><span data-stu-id="84595-610">Core</span></span>

* <span data-ttu-id="84595-611">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-611">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="84595-612">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-612">Added limited support for positional arguments</span></span>
* <span data-ttu-id="84595-613">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="84595-613">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="84595-614">#5591</span><span class="sxs-lookup"><span data-stu-id="84595-614">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="84595-615">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="84595-615">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="84595-616">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="84595-616">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="84595-617">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-617">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="84595-618">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-618">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="84595-619">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-619">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="84595-620">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-620">ACR</span></span>

* <span data-ttu-id="84595-621">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-621">Added ACR Build commands</span></span>
* <span data-ttu-id="84595-622">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-622">Improved resource not found error messages</span></span>
* <span data-ttu-id="84595-623">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-623">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="84595-624">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-624">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="84595-625">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-625">Improved repository commands error messages</span></span>
* <span data-ttu-id="84595-626">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-626">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="84595-627">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-627">ACS</span></span>

* <span data-ttu-id="84595-628">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-628">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="84595-629">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-629">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="84595-630">AMS</span><span class="sxs-lookup"><span data-stu-id="84595-630">AMS</span></span>

* <span data-ttu-id="84595-631">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="84595-631">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-632">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-632">Appservice</span></span>

* <span data-ttu-id="84595-633">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-633">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="84595-634">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-634">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="84595-635">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-635">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="84595-636">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-636">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="84595-637">Batch AI</span><span class="sxs-lookup"><span data-stu-id="84595-637">Batch AI</span></span>

* <span data-ttu-id="84595-638">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-638">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="84595-639">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="84595-639">Cognitive Services</span></span>

* <span data-ttu-id="84595-640">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-640">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="84595-641">消費</span><span class="sxs-lookup"><span data-stu-id="84595-641">Consumption</span></span>

* <span data-ttu-id="84595-642">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-642">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="84595-643">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-643">Container</span></span>

* <span data-ttu-id="84595-644">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-644">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="84595-645">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="84595-645">Cosmos DB</span></span>

* <span data-ttu-id="84595-646">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="84595-646">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="84595-647">DMS</span><span class="sxs-lookup"><span data-stu-id="84595-647">DMS</span></span>

* <span data-ttu-id="84595-648">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-648">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="84595-649">内線番号</span><span class="sxs-lookup"><span data-stu-id="84595-649">Extension</span></span>

* <span data-ttu-id="84595-650">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-650">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="84595-651">Interactive</span><span class="sxs-lookup"><span data-stu-id="84595-651">Interactive</span></span>

* <span data-ttu-id="84595-652">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-652">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="84595-653">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="84595-653">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="84595-654">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-654">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="84595-655">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-655">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="84595-656">ラボ</span><span class="sxs-lookup"><span data-stu-id="84595-656">Lab</span></span>

* <span data-ttu-id="84595-657">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-657">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="84595-658">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-658">Network</span></span>

* <span data-ttu-id="84595-659">[破壊的変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-659">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="84595-660">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-660">Profile</span></span>

* <span data-ttu-id="84595-661">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-661">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="84595-662">[破壊的変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-662">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="84595-663">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-663">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="84595-664">Redis</span><span class="sxs-lookup"><span data-stu-id="84595-664">Redis</span></span>

* <span data-ttu-id="84595-665">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-665">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="84595-666">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="84595-666">Deprecated `redis list-all`.</span></span> <span data-ttu-id="84595-667">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="84595-667">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="84595-668">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-668">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="84595-669">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-669">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="84595-670">Role</span><span class="sxs-lookup"><span data-stu-id="84595-670">Role</span></span>

* <span data-ttu-id="84595-671">[破壊的変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-671">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="84595-672">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-672">Storage</span></span>

* <span data-ttu-id="84595-673">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="84595-673">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="84595-674">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="84595-674">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="84595-675">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="84595-675">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="84595-676">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="84595-676">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="84595-677">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-677">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="84595-678">VM</span><span class="sxs-lookup"><span data-stu-id="84595-678">VM</span></span>

* <span data-ttu-id="84595-679">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-679">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="84595-680">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-680">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="84595-681">[破壊的変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="84595-681">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="84595-682">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-682">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="84595-683">[破壊的変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-683">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="84595-684">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-684">Added write accelerator support</span></span>
* <span data-ttu-id="84595-685">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-685">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="84595-686">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-686">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="84595-687">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-687">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="84595-688">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="84595-688">April 10, 2018</span></span>

<span data-ttu-id="84595-689">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="84595-689">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="84595-690">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-690">ACR</span></span>

* <span data-ttu-id="84595-691">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-691">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="84595-692">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-692">ACS</span></span>

* <span data-ttu-id="84595-693">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-693">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-694">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-694">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="84595-696">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-696">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="84595-697">BatchAI</span><span class="sxs-lookup"><span data-stu-id="84595-697">BatchAI</span></span>

* <span data-ttu-id="84595-698">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-698">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="84595-699">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="84595-699">Job level mounting</span></span>
 - <span data-ttu-id="84595-700">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="84595-700">Environment variables with secret values</span></span>
 - <span data-ttu-id="84595-701">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="84595-701">Performance counters settings</span></span>
 - <span data-ttu-id="84595-702">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="84595-702">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="84595-703">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="84595-703">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="84595-704">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="84595-704">Usage and limits reporting</span></span>
 - <span data-ttu-id="84595-705">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="84595-705">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="84595-706">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="84595-706">Support for custom images</span></span>
 - <span data-ttu-id="84595-707">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-707">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="84595-708">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="84595-708">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="84595-709">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="84595-709">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="84595-710">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="84595-710">National clouds are supported</span></span>
* <span data-ttu-id="84595-711">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-711">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="84595-712">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-712">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="84595-713">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-713">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="84595-714">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="84595-714">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="84595-715">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="84595-715">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="84595-716">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="84595-716">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="84595-717">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-717">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="84595-718">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-718">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="84595-719">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="84595-719">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="84595-720">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-720">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="84595-721">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="84595-721">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="84595-722">[破壊的変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="84595-722">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="84595-723">[破壊的変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-723">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="84595-724">課金</span><span class="sxs-lookup"><span data-stu-id="84595-724">Billing</span></span>

* <span data-ttu-id="84595-725">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-725">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="84595-726">消費</span><span class="sxs-lookup"><span data-stu-id="84595-726">Consumption</span></span>

* <span data-ttu-id="84595-727">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-727">Added `marketplace` commands</span></span>
* <span data-ttu-id="84595-728">[破壊的変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-728">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="84595-729">[破壊的変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-729">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="84595-730">[破壊的変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-730">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="84595-731">[破壊的変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-731">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="84595-732">[破壊的変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-732">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="84595-733">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-733">Container</span></span>

* <span data-ttu-id="84595-734">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-734">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="84595-735">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-735">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="84595-736">内線番号</span><span class="sxs-lookup"><span data-stu-id="84595-736">Extension</span></span>

* <span data-ttu-id="84595-737">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-737">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="84595-738">Interactive</span><span class="sxs-lookup"><span data-stu-id="84595-738">Interactive</span></span>

* <span data-ttu-id="84595-739">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-739">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="84595-740">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-740">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="84595-741">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-741">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="84595-742">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-742">Network</span></span>

* <span data-ttu-id="84595-743">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-743">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="84595-744">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-744">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="84595-745">#4910</span><span class="sxs-lookup"><span data-stu-id="84595-745">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="84595-746">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-746">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="84595-747">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="84595-747">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="84595-748">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-748">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="84595-749">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-749">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="84595-750">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-750">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="84595-751">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-751">Profile</span></span>

* <span data-ttu-id="84595-752">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-752">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="84595-753">[破壊的変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-753">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="84595-754">RDBMS</span><span class="sxs-lookup"><span data-stu-id="84595-754">RDBMS</span></span>

* <span data-ttu-id="84595-755">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-755">Added `georestore` command</span></span>
* <span data-ttu-id="84595-756">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-756">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="84595-757">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-757">Resource</span></span>

* <span data-ttu-id="84595-758">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-758">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="84595-759">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-759">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="84595-760">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-760">SQL</span></span>

* <span data-ttu-id="84595-761">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-761">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="84595-762">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-762">Storage</span></span>

* <span data-ttu-id="84595-763">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-763">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="84595-764">VM</span><span class="sxs-lookup"><span data-stu-id="84595-764">VM</span></span>

* <span data-ttu-id="84595-765">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-765">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="84595-766">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-766">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大な変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="84595-768">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-768">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="84595-769">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-769">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="84595-770">#5718</span><span class="sxs-lookup"><span data-stu-id="84595-770">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="84595-771">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-771">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="84595-772">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="84595-772">March 27, 2018</span></span>

<span data-ttu-id="84595-773">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="84595-773">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="84595-774">コア</span><span class="sxs-lookup"><span data-stu-id="84595-774">Core</span></span>

* <span data-ttu-id="84595-775">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="84595-775">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="84595-776">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-776">ACS</span></span>

* <span data-ttu-id="84595-777">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-777">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-778">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-778">Appservice</span></span>

* <span data-ttu-id="84595-779">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-779">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="84595-780">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-780">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="84595-781">バックアップ</span><span class="sxs-lookup"><span data-stu-id="84595-781">Backup</span></span>

* <span data-ttu-id="84595-782">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-782">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="84595-783">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="84595-783">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="84595-784">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-784">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="84595-785">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-785">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="84595-786">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-786">Container</span></span>

* <span data-ttu-id="84595-787">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-787">Added `container exec` command.</span></span> <span data-ttu-id="84595-788">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="84595-788">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="84595-789">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="84595-789">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="84595-790">内線番号</span><span class="sxs-lookup"><span data-stu-id="84595-790">Extension</span></span>

* <span data-ttu-id="84595-791">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-791">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="84595-792">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-792">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="84595-793">[破壊的変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-793">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="84595-794">Interactive</span><span class="sxs-lookup"><span data-stu-id="84595-794">Interactive</span></span>

* <span data-ttu-id="84595-795">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-795">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="84595-796">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-796">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="84595-797">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="84595-797">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="84595-798">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="84595-798">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="84595-799">ラボ</span><span class="sxs-lookup"><span data-stu-id="84595-799">Lab</span></span>

* <span data-ttu-id="84595-800">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-800">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="84595-801">監視</span><span class="sxs-lookup"><span data-stu-id="84595-801">Monitor</span></span>

* <span data-ttu-id="84595-802">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="84595-802">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="84595-803">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="84595-803">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="84595-804">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="84595-804">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="84595-805">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-805">Network</span></span>

* <span data-ttu-id="84595-806">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-806">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="84595-807">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-807">Profile</span></span>

* <span data-ttu-id="84595-808">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-808">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="84595-809">RDBMS</span><span class="sxs-lookup"><span data-stu-id="84595-809">RDBMS</span></span>

* <span data-ttu-id="84595-810">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-810">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="84595-811">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-811">Resource</span></span>

* [重大な変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="84595-813">Role</span><span class="sxs-lookup"><span data-stu-id="84595-813">Role</span></span>

* <span data-ttu-id="84595-814">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-814">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="84595-815">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-815">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="84595-816">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-816">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="84595-817">[破壊的変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-817">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="84595-818">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-818">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="84595-819">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-819">Storage</span></span>

* <span data-ttu-id="84595-820">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-820">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="84595-821">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-821">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="84595-822">VM</span><span class="sxs-lookup"><span data-stu-id="84595-822">VM</span></span>

* <span data-ttu-id="84595-823">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-823">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="84595-824">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-824">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="84595-825">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-825">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="84595-826">[破壊的変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-826">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="84595-827">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="84595-827">March 13, 2018</span></span>

<span data-ttu-id="84595-828">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="84595-828">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="84595-829">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-829">ACR</span></span>

* <span data-ttu-id="84595-830">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-830">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="84595-831">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-831">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="84595-832">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-832">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="84595-833">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-833">ACS</span></span>

* <span data-ttu-id="84595-834">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-834">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="84595-835">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-835">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="84595-836">Advisor</span><span class="sxs-lookup"><span data-stu-id="84595-836">Advisor</span></span>

* <span data-ttu-id="84595-837">[破壊的変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-837">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="84595-838">[破壊的変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-838">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="84595-839">[破壊的変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-839">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="84595-840">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-840">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="84595-841">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-841">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-842">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-842">Appservice</span></span>

* <span data-ttu-id="84595-843">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-843">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="84595-844">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-844">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="84595-845">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="84595-845">Eventhubs</span></span>

* <span data-ttu-id="84595-846">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-846">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="84595-847">内線番号</span><span class="sxs-lookup"><span data-stu-id="84595-847">Extension</span></span>

* <span data-ttu-id="84595-848">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-848">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="84595-849">Interactive</span><span class="sxs-lookup"><span data-stu-id="84595-849">Interactive</span></span>

* <span data-ttu-id="84595-850">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="84595-850">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="84595-851">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="84595-851">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="84595-852">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="84595-852">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="84595-853">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-853">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="84595-854">監視</span><span class="sxs-lookup"><span data-stu-id="84595-854">Monitor</span></span>

* <span data-ttu-id="84595-855">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-855">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="84595-856">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-856">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="84595-857">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-857">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="84595-858">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-858">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="84595-859">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-859">Network</span></span>

* <span data-ttu-id="84595-860">[破壊的変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-860">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="84595-861">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="84595-861">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="84595-862">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-862">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="84595-863">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-863">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="84595-864">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-864">Profile</span></span>

* <span data-ttu-id="84595-865">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-865">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="84595-866">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-866">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="84595-867">RDBMS</span><span class="sxs-lookup"><span data-stu-id="84595-867">RDBMS</span></span>

* <span data-ttu-id="84595-868">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-868">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="84595-869">Service Bus</span><span class="sxs-lookup"><span data-stu-id="84595-869">Service Bus</span></span>

* <span data-ttu-id="84595-870">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-870">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="84595-871">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-871">Storage</span></span>

* <span data-ttu-id="84595-872">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-872">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="84595-873">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="84595-873">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="84595-874">VM</span><span class="sxs-lookup"><span data-stu-id="84595-874">VM</span></span>

* <span data-ttu-id="84595-875">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-875">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="84595-876">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-876">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="84595-877">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-877">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="84595-878">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-878">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="84595-879">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="84595-879">February 27, 2018</span></span>

<span data-ttu-id="84595-880">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="84595-880">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="84595-881">コア</span><span class="sxs-lookup"><span data-stu-id="84595-881">Core</span></span>

* <span data-ttu-id="84595-882">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="84595-882">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="84595-883">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-883">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="84595-884">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-884">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="84595-885">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-885">ACS</span></span>

* <span data-ttu-id="84595-886">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-886">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="84595-887">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="84595-887">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="84595-888">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-888">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="84595-889">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-889">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-890">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-890">Appservice</span></span>

* <span data-ttu-id="84595-891">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="84595-891">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="84595-892">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="84595-892">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="84595-893">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="84595-893">Cognitive Services</span></span>

* <span data-ttu-id="84595-894">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-894">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="84595-895">消費</span><span class="sxs-lookup"><span data-stu-id="84595-895">Consumption</span></span>

* <span data-ttu-id="84595-896">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-896">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="84595-897">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-897">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="84595-898">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-898">Container</span></span>

* <span data-ttu-id="84595-899">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-899">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="84595-900">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-900">Network</span></span>

* <span data-ttu-id="84595-901">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="84595-901">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="84595-902">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-902">Resource</span></span>

* <span data-ttu-id="84595-903">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-903">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="84595-904">Role</span><span class="sxs-lookup"><span data-stu-id="84595-904">Role</span></span>

* <span data-ttu-id="84595-905">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-905">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="84595-906">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-906">SQL</span></span>

* <span data-ttu-id="84595-907">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-907">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="84595-908">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-908">Storage</span></span>

* <span data-ttu-id="84595-909">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-909">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="84595-910">VM</span><span class="sxs-lookup"><span data-stu-id="84595-910">VM</span></span>

* <span data-ttu-id="84595-911">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-911">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="84595-912">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="84595-912">February 13, 2018</span></span>

<span data-ttu-id="84595-913">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="84595-913">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="84595-914">コア</span><span class="sxs-lookup"><span data-stu-id="84595-914">Core</span></span>

* <span data-ttu-id="84595-915">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-915">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="84595-916">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-916">ACS</span></span>

* <span data-ttu-id="84595-917">[破壊的変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-917">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="84595-918">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-918">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="84595-919">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-919">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="84595-920">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-920">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="84595-921">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-921">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="84595-922">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="84595-922">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="84595-923">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-923">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="84595-924">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="84595-924">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-925">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-925">Appservice</span></span>

* <span data-ttu-id="84595-926">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-926">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="84595-927">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-927">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="84595-928">CDN</span><span class="sxs-lookup"><span data-stu-id="84595-928">CDN</span></span>

* <span data-ttu-id="84595-929">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-929">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="84595-930">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-930">Container</span></span>

* <span data-ttu-id="84595-931">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-931">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="84595-932">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-932">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="84595-933">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="84595-933">CosmosDB</span></span>

* <span data-ttu-id="84595-934">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-934">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="84595-935">内線番号</span><span class="sxs-lookup"><span data-stu-id="84595-935">Extension</span></span>

* <span data-ttu-id="84595-936">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-936">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="84595-937">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-937">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="84595-938">フィードバック</span><span class="sxs-lookup"><span data-stu-id="84595-938">Feedback</span></span>

* <span data-ttu-id="84595-939">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-939">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="84595-940">Interactive</span><span class="sxs-lookup"><span data-stu-id="84595-940">Interactive</span></span>

* <span data-ttu-id="84595-941">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-941">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="84595-942">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-942">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="84595-943">IoT</span><span class="sxs-lookup"><span data-stu-id="84595-943">IoT</span></span>

* <span data-ttu-id="84595-944">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-944">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="84595-945">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-945">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="84595-946">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-946">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="84595-947">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-947">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="84595-948">監視</span><span class="sxs-lookup"><span data-stu-id="84595-948">Monitor</span></span>

* <span data-ttu-id="84595-949">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-949">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="84595-950">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-950">Network</span></span>

* <span data-ttu-id="84595-951">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="84595-951">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="84595-952">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-952">Profile</span></span>

* <span data-ttu-id="84595-953">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-953">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="84595-954">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-954">Resource</span></span>

* <span data-ttu-id="84595-955">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-955">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="84595-956">Role</span><span class="sxs-lookup"><span data-stu-id="84595-956">Role</span></span>

* <span data-ttu-id="84595-957">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-957">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="84595-958">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-958">SQL</span></span>

* <span data-ttu-id="84595-959">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-959">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="84595-960">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-960">Added `sql db rename`</span></span>
* <span data-ttu-id="84595-961">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-961">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="84595-962">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-962">Storage</span></span>

* <span data-ttu-id="84595-963">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-963">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="84595-964">VM</span><span class="sxs-lookup"><span data-stu-id="84595-964">VM</span></span>

* <span data-ttu-id="84595-965">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-965">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="84595-966">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-966">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="84595-967">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="84595-967">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="84595-968">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="84595-968">January 31, 2018</span></span>

<span data-ttu-id="84595-969">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="84595-969">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="84595-970">コア</span><span class="sxs-lookup"><span data-stu-id="84595-970">Core</span></span>

* <span data-ttu-id="84595-971">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-971">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="84595-972">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-972">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="84595-973">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-973">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="84595-974">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="84595-974">Use `--verbose` to see</span></span>
* <span data-ttu-id="84595-975">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="84595-975">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="84595-976">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-976">ACS</span></span>

* <span data-ttu-id="84595-977">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="84595-977">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="84595-978">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="84595-978">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-979">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-979">Appservice</span></span>

* <span data-ttu-id="84595-980">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="84595-980">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="84595-981">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-981">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="84595-982">CDN</span><span class="sxs-lookup"><span data-stu-id="84595-982">CDN</span></span>

* <span data-ttu-id="84595-983">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-983">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="84595-984">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="84595-984">CosmosDB</span></span>

* <span data-ttu-id="84595-985">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-985">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="84595-986">Interactive</span><span class="sxs-lookup"><span data-stu-id="84595-986">Interactive</span></span>

* <span data-ttu-id="84595-987">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-987">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="84595-988">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-988">Network</span></span>

* <span data-ttu-id="84595-989">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-989">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="84595-990">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-990">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="84595-991">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-991">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="84595-992">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-992">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="84595-993">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-993">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="84595-994">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="84595-994">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="84595-995">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-995">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="84595-996">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-996">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="84595-997">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-997">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="84595-998">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="84595-998">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="84595-999">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-999">Profile</span></span>

* <span data-ttu-id="84595-1000">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1000">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="84595-1001">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-1001">Resource</span></span>

* <span data-ttu-id="84595-1002">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1002">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="84595-1003">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1003">Storage</span></span>

* <span data-ttu-id="84595-1004">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1004">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="84595-1005">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1005">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="84595-1006">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1006">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="84595-1007">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1007">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="84595-1008">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1008">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1009">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1009">VM</span></span>

* <span data-ttu-id="84595-1010">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1010">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="84595-1011">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1011">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="84595-1012">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1012">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="84595-1013">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1013">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="84595-1014">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="84595-1014">January 17, 2018</span></span>

<span data-ttu-id="84595-1015">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="84595-1015">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="84595-1016">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-1016">ACR</span></span>

* <span data-ttu-id="84595-1017">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1017">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="84595-1018">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-1018">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1019">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1019">ACS</span></span>

* <span data-ttu-id="84595-1020">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1020">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="84595-1021">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1021">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1022">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-1022">Appservice</span></span>

* <span data-ttu-id="84595-1023">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1023">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="84595-1024">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1024">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="84595-1025">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1025">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="84595-1026">バックアップ</span><span class="sxs-lookup"><span data-stu-id="84595-1026">Backup</span></span>

* <span data-ttu-id="84595-1027">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1027">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="84595-1028">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1028">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="84595-1029">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1029">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="84595-1030">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1030">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="84595-1031">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1031">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="84595-1032">Batch</span><span class="sxs-lookup"><span data-stu-id="84595-1032">Batch</span></span>

* <span data-ttu-id="84595-1033">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1033">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="84595-1034">クラウド</span><span class="sxs-lookup"><span data-stu-id="84595-1034">Cloud</span></span>

* <span data-ttu-id="84595-1035">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1035">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="84595-1036">消費</span><span class="sxs-lookup"><span data-stu-id="84595-1036">Consumption</span></span>

* <span data-ttu-id="84595-1037">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1037">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="84595-1038">Event Grid</span><span class="sxs-lookup"><span data-stu-id="84595-1038">Event Grid</span></span>

* <span data-ttu-id="84595-1039">[破壊的変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="84595-1039">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="84595-1040">[破壊的変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="84595-1040">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="84595-1041">[破壊的変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1041">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="84595-1042">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="84595-1042">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="84595-1043">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1043">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="84595-1044">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1044">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="84595-1045">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1045">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="84595-1046">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1046">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="84595-1047">Interactive</span><span class="sxs-lookup"><span data-stu-id="84595-1047">Interactive</span></span>

* <span data-ttu-id="84595-1048">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="84595-1048">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="84595-1049">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1049">Fixed errors on startup</span></span>
* <span data-ttu-id="84595-1050">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1050">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="84595-1051">IoT</span><span class="sxs-lookup"><span data-stu-id="84595-1051">IoT</span></span>

* <span data-ttu-id="84595-1052">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1052">Added support for device provisioning service</span></span>
* <span data-ttu-id="84595-1053">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1053">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="84595-1054">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1054">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="84595-1055">監視</span><span class="sxs-lookup"><span data-stu-id="84595-1055">Monitor</span></span>

* <span data-ttu-id="84595-1056">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1056">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="84595-1057">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="84595-1057">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="84595-1058">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1058">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="84595-1059">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1059">Network</span></span>

* <span data-ttu-id="84595-1060">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1060">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="84595-1061">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1061">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="84595-1062">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-1062">Profile</span></span>

* <span data-ttu-id="84595-1063">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1063">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="84595-1064">Role</span><span class="sxs-lookup"><span data-stu-id="84595-1064">Role</span></span>

* <span data-ttu-id="84595-1065">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1065">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="84595-1066">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="84595-1066">Service Fabric</span></span>

* <span data-ttu-id="84595-1067">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1067">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="84595-1068">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1068">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1069">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1069">VM</span></span>

* <span data-ttu-id="84595-1070">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="84595-1070">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="84595-1071">[破壊的変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1071">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="84595-1072">[破壊的変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1072">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="84595-1073">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1073">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="84595-1074">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1074">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="84595-1075">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1075">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="84595-1076">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1076">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="84595-1077">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1077">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="84595-1078">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="84595-1078">December 19, 2017</span></span>

<span data-ttu-id="84595-1079">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="84595-1079">Version 2.0.23</span></span>

* <span data-ttu-id="84595-1080">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1080">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="84595-1081">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-1081">Container</span></span>

* <span data-ttu-id="84595-1082">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1082">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="84595-1083">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1083">Network</span></span>

* <span data-ttu-id="84595-1084">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1084">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="84595-1085">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1085">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="84595-1086">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1086">Storage</span></span>

* <span data-ttu-id="84595-1087">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1087">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1088">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1088">VM</span></span>

* <span data-ttu-id="84595-1089">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1089">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="84595-1090">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="84595-1090">December 5, 2017</span></span>

<span data-ttu-id="84595-1091">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="84595-1091">Version 2.0.22</span></span>

* <span data-ttu-id="84595-1092">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="84595-1092">Removed `az component` commands.</span></span> <span data-ttu-id="84595-1093">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="84595-1093">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="84595-1094">コア</span><span class="sxs-lookup"><span data-stu-id="84595-1094">Core</span></span>
* <span data-ttu-id="84595-1095">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1095">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="84595-1096">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1096">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1097">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1097">ACS</span></span>

* <span data-ttu-id="84595-1098">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1098">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="84595-1099">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-1099">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="84595-1100">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1100">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="84595-1101">Advisor</span><span class="sxs-lookup"><span data-stu-id="84595-1101">Advisor</span></span>

* <span data-ttu-id="84595-1102">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-1102">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1103">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-1103">Appservice</span></span>

* <span data-ttu-id="84595-1104">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1104">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="84595-1105">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1105">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="84595-1106">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1106">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="84595-1107">消費</span><span class="sxs-lookup"><span data-stu-id="84595-1107">Consumption</span></span>

* <span data-ttu-id="84595-1108">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1108">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="84595-1109">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-1109">Container</span></span>

* <span data-ttu-id="84595-1110">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1110">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="84595-1111">監視</span><span class="sxs-lookup"><span data-stu-id="84595-1111">Monitor</span></span>

* <span data-ttu-id="84595-1112">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1112">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="84595-1113">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-1113">Resource</span></span>

* <span data-ttu-id="84595-1114">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1114">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="84595-1115">Role</span><span class="sxs-lookup"><span data-stu-id="84595-1115">Role</span></span>

* <span data-ttu-id="84595-1116">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1116">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="84595-1117">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="84595-1117">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="84595-1118">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-1118">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="84595-1119">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-1119">SQL</span></span>

* <span data-ttu-id="84595-1120">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1120">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="84595-1121">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1121">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1122">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1122">VM</span></span>

* <span data-ttu-id="84595-1123">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1123">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="84595-1124">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="84595-1124">November 14, 2017</span></span>

<span data-ttu-id="84595-1125">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="84595-1125">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="84595-1126">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-1126">ACR</span></span>

* <span data-ttu-id="84595-1127">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1127">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="84595-1128">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1128">ACS</span></span>

* <span data-ttu-id="84595-1129">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1129">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="84595-1130">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="84595-1130">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="84595-1131">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1131">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="84595-1132">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1132">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="84595-1133">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1133">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1134">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-1134">Appservice</span></span>

* <span data-ttu-id="84595-1135">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1135">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="84595-1136">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1136">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="84595-1137">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1137">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="84595-1138">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-1138">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="84595-1139">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1139">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="84595-1140">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="84595-1140">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="84595-1141">Batch</span><span class="sxs-lookup"><span data-stu-id="84595-1141">Batch</span></span>

* <span data-ttu-id="84595-1142">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1142">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="84595-1143">Batchai</span><span class="sxs-lookup"><span data-stu-id="84595-1143">Batchai</span></span>

* <span data-ttu-id="84595-1144">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1144">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="84595-1145">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1145">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="84595-1146">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1146">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="84595-1147">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1147">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="84595-1148">クラウド</span><span class="sxs-lookup"><span data-stu-id="84595-1148">Cloud</span></span>

* <span data-ttu-id="84595-1149">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1149">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="84595-1150">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-1150">Container</span></span>

* <span data-ttu-id="84595-1151">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1151">Added support to open multiple ports</span></span>
* <span data-ttu-id="84595-1152">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1152">Added container group restart policy</span></span>
* <span data-ttu-id="84595-1153">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1153">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="84595-1154">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-1154">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="84595-1155">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="84595-1155">Data Lake Analytics</span></span>

* <span data-ttu-id="84595-1156">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1156">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="84595-1157">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="84595-1157">Data Lake Store</span></span>

* <span data-ttu-id="84595-1158">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1158">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="84595-1159">内線番号</span><span class="sxs-lookup"><span data-stu-id="84595-1159">Extension</span></span>

* <span data-ttu-id="84595-1160">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1160">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="84595-1161">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1161">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="84595-1162">IoT</span><span class="sxs-lookup"><span data-stu-id="84595-1162">IoT</span></span>

* <span data-ttu-id="84595-1163">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1163">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="84595-1164">監視</span><span class="sxs-lookup"><span data-stu-id="84595-1164">Monitor</span></span>

* <span data-ttu-id="84595-1165">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1165">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="84595-1166">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1166">Network</span></span>

* <span data-ttu-id="84595-1167">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1167">Added support for CAA DNS records</span></span>
* <span data-ttu-id="84595-1168">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1168">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="84595-1169">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1169">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="84595-1170">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1170">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="84595-1171">Reservations</span><span class="sxs-lookup"><span data-stu-id="84595-1171">Reservations</span></span>

* <span data-ttu-id="84595-1172">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="84595-1172">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="84595-1173">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-1173">Resource</span></span>

* <span data-ttu-id="84595-1174">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1174">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="84595-1175">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-1175">SQL</span></span>

* <span data-ttu-id="84595-1176">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1176">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="84595-1177">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1177">Storage</span></span>

* <span data-ttu-id="84595-1178">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1178">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="84595-1179">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1179">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="84595-1180">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1180">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="84595-1181">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1181">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="84595-1182">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1182">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="84595-1183">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1183">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="84595-1184">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1184">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1185">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1185">VM</span></span>

* <span data-ttu-id="84595-1186">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1186">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="84595-1187">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1187">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="84595-1188">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1188">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="84595-1189">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1189">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="84595-1190">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1190">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="84595-1191">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="84595-1191">October 24, 2017</span></span>

<span data-ttu-id="84595-1192">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="84595-1192">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="84595-1193">コア</span><span class="sxs-lookup"><span data-stu-id="84595-1193">Core</span></span>

* <span data-ttu-id="84595-1194">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-1194">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="84595-1195">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-1195">ACR</span></span>

* <span data-ttu-id="84595-1196">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-1196">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="84595-1197">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1197">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="84595-1198">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1198">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1199">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1199">ACS</span></span>

* <span data-ttu-id="84595-1200">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1200">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="84595-1201">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1201">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1202">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-1202">Appservice</span></span>

* <span data-ttu-id="84595-1203">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1203">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="84595-1204">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="84595-1204">Component</span></span>

* <span data-ttu-id="84595-1205">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1205">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="84595-1206">監視</span><span class="sxs-lookup"><span data-stu-id="84595-1206">Monitor</span></span>

* <span data-ttu-id="84595-1207">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1207">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="84595-1208">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-1208">Resource</span></span>

* <span data-ttu-id="84595-1209">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1209">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="84595-1210">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1210">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1211">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1211">VM</span></span>

* <span data-ttu-id="84595-1212">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1212">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="84595-1213">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="84595-1213">October 9, 2017</span></span>

<span data-ttu-id="84595-1214">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="84595-1214">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="84595-1215">コア</span><span class="sxs-lookup"><span data-stu-id="84595-1215">Core</span></span>

* <span data-ttu-id="84595-1216">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1216">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1217">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-1217">Appservice</span></span>

* <span data-ttu-id="84595-1218">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1218">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="84595-1219">Batch</span><span class="sxs-lookup"><span data-stu-id="84595-1219">Batch</span></span>

* <span data-ttu-id="84595-1220">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-1220">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="84595-1221">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-1221">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="84595-1222">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1222">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="84595-1223">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1223">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="84595-1224">Batchai</span><span class="sxs-lookup"><span data-stu-id="84595-1224">Batchai</span></span>

* <span data-ttu-id="84595-1225">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-1225">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="84595-1226">KeyVault</span><span class="sxs-lookup"><span data-stu-id="84595-1226">Keyvault</span></span>

* <span data-ttu-id="84595-1227">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="84595-1227">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="84595-1228">(#4448)</span><span class="sxs-lookup"><span data-stu-id="84595-1228">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="84595-1229">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1229">Network</span></span>

* <span data-ttu-id="84595-1230">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1230">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="84595-1231">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-1231">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="84595-1232">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-1232">Resource</span></span>

* <span data-ttu-id="84595-1233">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1233">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="84595-1234">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1234">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="84595-1235">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1235">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="84595-1236">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1236">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="84595-1237">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-1237">Sql</span></span>

* <span data-ttu-id="84595-1238">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1238">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="84595-1239">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="84595-1239">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="84595-1240">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="84595-1240">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="84595-1241">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1241">Storage</span></span>

* <span data-ttu-id="84595-1242">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1242">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1243">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1243">Vm</span></span>

* <span data-ttu-id="84595-1244">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1244">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="84595-1245">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1245">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="84595-1246">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1246">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="84595-1247">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1247">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="84595-1248">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1248">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="84595-1249">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="84595-1249">September 22, 2017</span></span>

<span data-ttu-id="84595-1250">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="84595-1250">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="84595-1251">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-1251">Resource</span></span>

* <span data-ttu-id="84595-1252">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1252">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="84595-1253">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1253">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="84595-1254">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1254">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="84595-1255">[破壊的変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1255">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="84595-1256">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1256">Network</span></span>

* <span data-ttu-id="84595-1257">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1257">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="84595-1258">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1258">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="84595-1259">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1259">Added `asg` application security group commands</span></span>
* <span data-ttu-id="84595-1260">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1260">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="84595-1261">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1261">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="84595-1262">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1262">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="84595-1263">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1263">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="84595-1264">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1264">Storage</span></span>

* <span data-ttu-id="84595-1265">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1265">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="84595-1266">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="84595-1266">Eventgrid</span></span>

* <span data-ttu-id="84595-1267">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-1267">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="84595-1268">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-1268">SQL</span></span>

* <span data-ttu-id="84595-1269">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="84595-1269">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="84595-1270">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="84595-1270">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="84595-1271">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1271">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="84595-1272">KeyVault</span><span class="sxs-lookup"><span data-stu-id="84595-1272">Keyvault</span></span>

* <span data-ttu-id="84595-1273">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1273">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1274">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1274">VM</span></span>

* <span data-ttu-id="84595-1275">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1275">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="84595-1276">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1276">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="84595-1277">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1277">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="84595-1278">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1278">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="84595-1279">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1279">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="84595-1280">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1280">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1281">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1281">ACS</span></span>

* <span data-ttu-id="84595-1282">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1282">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1283">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-1283">Appservice</span></span>

* <span data-ttu-id="84595-1284">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1284">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="84595-1285">バックアップ</span><span class="sxs-lookup"><span data-stu-id="84595-1285">Backup</span></span>

* <span data-ttu-id="84595-1286">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="84595-1286">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="84595-1287">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="84595-1287">September 11, 2017</span></span>

<span data-ttu-id="84595-1288">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="84595-1288">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="84595-1289">コア</span><span class="sxs-lookup"><span data-stu-id="84595-1289">Core</span></span>

* <span data-ttu-id="84595-1290">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-1290">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="84595-1291">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1291">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1292">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1292">Acs</span></span>

* <span data-ttu-id="84595-1293">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1293">Added `acs list-locations` command</span></span>
* <span data-ttu-id="84595-1294">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="84595-1294">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1295">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-1295">Appservice</span></span>

* <span data-ttu-id="84595-1296">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1296">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="84595-1297">CDN</span><span class="sxs-lookup"><span data-stu-id="84595-1297">CDN</span></span>

* <span data-ttu-id="84595-1298">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1298">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="84595-1299">内線番号</span><span class="sxs-lookup"><span data-stu-id="84595-1299">Extension</span></span>

* <span data-ttu-id="84595-1300">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-1300">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="84595-1301">KeyVault</span><span class="sxs-lookup"><span data-stu-id="84595-1301">Keyvault</span></span>

* <span data-ttu-id="84595-1302">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1302">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="84595-1303">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1303">Network</span></span>

* <span data-ttu-id="84595-1304">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1304">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="84595-1305">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1305">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="84595-1306">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1306">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="84595-1307">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1307">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="84595-1308">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1308">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="84595-1309">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-1309">Resource</span></span>

* <span data-ttu-id="84595-1310">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="84595-1310">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="84595-1311">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="84595-1311">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="84595-1312">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="84595-1312">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="84595-1313">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="84595-1313">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="84595-1314">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-1314">SQL</span></span>

* <span data-ttu-id="84595-1315">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1315">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1316">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1316">VM</span></span>

* <span data-ttu-id="84595-1317">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="84595-1317">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="84595-1318">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="84595-1318">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="84595-1319">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1319">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="84595-1320">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="84595-1320">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="84595-1321">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="84595-1321">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="84595-1322">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="84595-1322">August 31, 2017</span></span>

<span data-ttu-id="84595-1323">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="84595-1323">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="84595-1324">KeyVault</span><span class="sxs-lookup"><span data-stu-id="84595-1324">Keyvault</span></span>

* <span data-ttu-id="84595-1325">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1325">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="84595-1326">SF</span><span class="sxs-lookup"><span data-stu-id="84595-1326">Sf</span></span>

* <span data-ttu-id="84595-1327">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="84595-1327">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="84595-1328">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1328">Storage</span></span>

* <span data-ttu-id="84595-1329">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1329">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="84595-1330">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="84595-1330">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="84595-1331">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="84595-1331">August 28, 2017</span></span>

<span data-ttu-id="84595-1332">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="84595-1332">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="84595-1333">CLI</span><span class="sxs-lookup"><span data-stu-id="84595-1333">CLI</span></span>

* <span data-ttu-id="84595-1334">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1334">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1335">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1335">ACS</span></span>

* <span data-ttu-id="84595-1336">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1336">Corrected preview regions</span></span>
* <span data-ttu-id="84595-1337">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="84595-1337">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="84595-1338">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="84595-1338">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1339">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-1339">Appservice</span></span>

* <span data-ttu-id="84595-1340">[破壊的変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1340">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="84595-1341">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1341">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="84595-1342">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="84595-1342">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="84595-1343">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="84595-1343">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="84595-1344">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="84595-1344">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="84595-1345">IoT</span><span class="sxs-lookup"><span data-stu-id="84595-1345">IoT</span></span>

* <span data-ttu-id="84595-1346">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="84595-1346">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="84595-1347">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1347">Network</span></span>

* <span data-ttu-id="84595-1348">[破壊的変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1348">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="84595-1349">[破壊的変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1349">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="84595-1350">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1350">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="84595-1351">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1351">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="84595-1352">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1352">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="84595-1353">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-1353">Profile</span></span>

* <span data-ttu-id="84595-1354">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="84595-1354">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="84595-1355">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="84595-1355">Service Fabric</span></span>

* <span data-ttu-id="84595-1356">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="84595-1356">Preview release</span></span>
* <span data-ttu-id="84595-1357">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="84595-1357">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="84595-1358">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1358">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="84595-1359">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1359">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="84595-1360">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1360">Storage</span></span>

* <span data-ttu-id="84595-1361">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-1361">Enabled setting blob tier</span></span>
* <span data-ttu-id="84595-1362">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1362">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="84595-1363">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1363">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="84595-1364">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-1364">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="84595-1365">[破壊的変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1365">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="84595-1366">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="84595-1366">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1367">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1367">VM</span></span>

* <span data-ttu-id="84595-1368">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1368">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="84595-1369">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-1369">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="84595-1370">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1370">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="84595-1371">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1371">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="84595-1372">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1372">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="84595-1373">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1373">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="84595-1374">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="84595-1374">August 15, 2017</span></span>

<span data-ttu-id="84595-1375">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="84595-1375">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1376">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1376">ACS</span></span>

* <span data-ttu-id="84595-1377">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1377">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1378">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-1378">Appservice</span></span>

* <span data-ttu-id="84595-1379">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1379">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="84595-1380">Event Grid</span><span class="sxs-lookup"><span data-stu-id="84595-1380">Event Grid</span></span>

* <span data-ttu-id="84595-1381">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1381">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="84595-1382">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="84595-1382">August 11, 2017</span></span>

<span data-ttu-id="84595-1383">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="84595-1383">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1384">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1384">ACS</span></span>

* <span data-ttu-id="84595-1385">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1385">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="84595-1386">Batch</span><span class="sxs-lookup"><span data-stu-id="84595-1386">Batch</span></span>

* <span data-ttu-id="84595-1387">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="84595-1387">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="84595-1388">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1388">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="84595-1389">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1389">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="84595-1390">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1390">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="84595-1391">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1391">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="84595-1392">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1392">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="84595-1393">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="84595-1393">Component</span></span>

* <span data-ttu-id="84595-1394">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1394">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="84595-1395">コンテナー</span><span class="sxs-lookup"><span data-stu-id="84595-1395">Container</span></span>

* <span data-ttu-id="84595-1396">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1396">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="84595-1397">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="84595-1397">Data Lake Store</span></span>

* <span data-ttu-id="84595-1398">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-1398">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="84595-1399">Event Grid</span><span class="sxs-lookup"><span data-stu-id="84595-1399">Event Grid</span></span>

* <span data-ttu-id="84595-1400">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-1400">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="84595-1401">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1401">Network</span></span>

* <span data-ttu-id="84595-1402">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1402">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="84595-1403">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1403">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="84595-1404">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1404">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="84595-1405">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1405">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="84595-1406">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-1406">Profile</span></span>

* <span data-ttu-id="84595-1407">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1407">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="84595-1408">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1408">Storage</span></span>

* <span data-ttu-id="84595-1409">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="84595-1409">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1410">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1410">VM</span></span>

* <span data-ttu-id="84595-1411">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="84595-1411">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="84595-1412">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="84595-1412">Exposed `list-skus` command</span></span>
* <span data-ttu-id="84595-1413">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1413">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="84595-1414">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="84595-1414">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="84595-1415">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1415">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="84595-1416">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="84595-1416">July 28, 2017</span></span>

<span data-ttu-id="84595-1417">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="84595-1417">Version 2.0.12</span></span>

* <span data-ttu-id="84595-1418">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1418">Added container commands</span></span>
* <span data-ttu-id="84595-1419">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1419">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="84595-1420">コア</span><span class="sxs-lookup"><span data-stu-id="84595-1420">Core</span></span>

* <span data-ttu-id="84595-1421">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="84595-1421">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="84595-1422">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1422">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="84595-1423">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="84595-1423">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="84595-1424">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="84595-1424">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="84595-1425">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="84595-1425">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="84595-1426">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="84595-1426">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="84595-1427">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="84595-1427">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="84595-1428">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="84595-1428">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="84595-1429">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="84595-1429">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="84595-1430">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="84595-1430">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="84595-1431">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="84595-1431">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="84595-1432">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="84595-1432">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="84595-1433">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="84595-1433">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="84595-1434">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="84595-1434">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="84595-1435">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1435">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="84595-1436">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="84595-1436">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="84595-1437">ACR</span><span class="sxs-lookup"><span data-stu-id="84595-1437">ACR</span></span>

* <span data-ttu-id="84595-1438">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1438">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="84595-1439">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1439">Support SKU update for managed registries</span></span>
* <span data-ttu-id="84595-1440">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1440">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="84595-1441">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1441">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="84595-1442">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1442">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="84595-1443">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1443">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1444">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1444">ACS</span></span>

* <span data-ttu-id="84595-1445">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1445">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1446">Appservice</span><span class="sxs-lookup"><span data-stu-id="84595-1446">Appservice</span></span>

* <span data-ttu-id="84595-1447">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1447">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="84595-1448">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1448">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="84595-1449">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="84595-1449">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="84595-1450">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="84595-1450">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="84595-1451">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="84595-1451">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="84595-1452">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="84595-1452">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="84595-1453">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="84595-1453">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="84595-1454">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="84595-1454">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="84595-1455">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="84595-1455">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="84595-1456">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="84595-1456">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="84595-1457">Batch</span><span class="sxs-lookup"><span data-stu-id="84595-1457">Batch</span></span>

* <span data-ttu-id="84595-1458">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="84595-1458">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="84595-1459">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1459">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="84595-1460">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1460">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="84595-1461">CDN</span><span class="sxs-lookup"><span data-stu-id="84595-1461">CDN</span></span>

* <span data-ttu-id="84595-1462">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1462">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="84595-1463">クラウド</span><span class="sxs-lookup"><span data-stu-id="84595-1463">Cloud</span></span>

* <span data-ttu-id="84595-1464">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1464">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="84595-1465">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="84595-1465">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="84595-1466">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1466">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="84595-1467">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="84595-1467">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="84595-1468">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="84595-1468">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="84595-1469">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="84595-1469">CosmosDB</span></span>

* <span data-ttu-id="84595-1470">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1470">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="84595-1471">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1471">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="84595-1472">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="84595-1472">Data Lake Analytics</span></span>

* <span data-ttu-id="84595-1473">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1473">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="84595-1474">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1474">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="84595-1475">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1475">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="84595-1476">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="84595-1476">Data Lake Store</span></span>

* <span data-ttu-id="84595-1477">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1477">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="84595-1478">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="84595-1478">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="84595-1479">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-1479">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="84595-1480">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="84595-1480">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="84595-1481">対話</span><span class="sxs-lookup"><span data-stu-id="84595-1481">Interactive</span></span>

* <span data-ttu-id="84595-1482">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="84595-1482">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="84595-1483">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="84595-1483">Increased test coverage</span></span>
* <span data-ttu-id="84595-1484">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="84595-1484">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="84595-1485">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="84595-1485">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="84595-1486">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="84595-1486">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="84595-1487">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="84595-1487">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="84595-1488">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="84595-1488">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="84595-1489">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1489">Added `--progress` flag</span></span>
* <span data-ttu-id="84595-1490">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1490">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="84595-1491">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="84595-1491">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="84595-1492">IoT</span><span class="sxs-lookup"><span data-stu-id="84595-1492">IoT</span></span>

* <span data-ttu-id="84595-1493">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="84595-1493">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="84595-1494">(#3934)</span><span class="sxs-lookup"><span data-stu-id="84595-1494">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="84595-1495">Key Vault</span><span class="sxs-lookup"><span data-stu-id="84595-1495">Key vault</span></span>

* <span data-ttu-id="84595-1496">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="84595-1496">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="84595-1497">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="84595-1497">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="84595-1498">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="84595-1498">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="84595-1499">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="84595-1499">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="84595-1500">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="84595-1500">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="84595-1501">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="84595-1501">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="84595-1502">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="84595-1502">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="84595-1503">(#3307)</span><span class="sxs-lookup"><span data-stu-id="84595-1503">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="84595-1504">ラボ</span><span class="sxs-lookup"><span data-stu-id="84595-1504">Lab</span></span>

* <span data-ttu-id="84595-1505">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1505">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="84595-1506">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1506">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="84595-1507">監視</span><span class="sxs-lookup"><span data-stu-id="84595-1507">Monitor</span></span>

* <span data-ttu-id="84595-1508">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="84595-1508">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="84595-1509">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1509">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="84595-1510">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1510">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="84595-1511">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1511">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="84595-1512">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="84595-1512">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="84595-1513">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="84595-1513">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="84595-1514">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="84595-1514">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="84595-1515">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="84595-1515">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="84595-1516">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="84595-1516">`location` no longer required</span></span>
  * <span data-ttu-id="84595-1517">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="84595-1517">Add name and ID support for target</span></span>
  * <span data-ttu-id="84595-1518">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="84595-1518">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="84595-1519">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="84595-1519">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="84595-1520">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1520">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="84595-1521">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="84595-1521">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="84595-1522">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1522">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="84595-1523">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1523">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="84595-1524">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1524">Network</span></span>

* <span data-ttu-id="84595-1525">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1525">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="84595-1526">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1526">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="84595-1527">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1527">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="84595-1528">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1528">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="84595-1529">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1529">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="84595-1530">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1530">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="84595-1531">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1531">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="84595-1532">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1532">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="84595-1533">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1533">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="84595-1534">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1534">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="84595-1535">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1535">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="84595-1536">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1536">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="84595-1537">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1537">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="84595-1538">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1538">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="84595-1539">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1539">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="84595-1540">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1540">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="84595-1541">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1541">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="84595-1542">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1542">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="84595-1543">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1543">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="84595-1544">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1544">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="84595-1545">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1545">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="84595-1546">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1546">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="84595-1547">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-1547">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="84595-1548">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="84595-1548">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="84595-1549">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="84595-1549">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="84595-1550">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="84595-1550">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="84595-1551">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="84595-1551">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="84595-1552">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-1552">Profile</span></span>

* <span data-ttu-id="84595-1553">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1553">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="84595-1554">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1554">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="84595-1555">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="84595-1555">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="84595-1556">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1556">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="84595-1557">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1557">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="84595-1558">RDBMS</span><span class="sxs-lookup"><span data-stu-id="84595-1558">RDBMS</span></span>

* <span data-ttu-id="84595-1559">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="84595-1559">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="84595-1560">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="84595-1560">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="84595-1561">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="84595-1561">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="84595-1562">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="84595-1562">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="84595-1563">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-1563">Resource</span></span>

* <span data-ttu-id="84595-1564">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-1564">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="84595-1565">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="84595-1565">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="84595-1566">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1566">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="84595-1567">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1567">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="84595-1568">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="84595-1568">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="84595-1569">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1569">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="84595-1570">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="84595-1570">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="84595-1571">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1571">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="84595-1572">Role</span><span class="sxs-lookup"><span data-stu-id="84595-1572">Role</span></span>

* <span data-ttu-id="84595-1573">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1573">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="84595-1574">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="84595-1574">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="84595-1575">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="84595-1575">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="84595-1576">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="84595-1576">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="84595-1577">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1577">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="84595-1578">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="84595-1578">Service Fabric</span></span>
* <span data-ttu-id="84595-1579">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="84595-1579">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="84595-1580">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="84595-1580">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="84595-1581">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="84595-1581">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="84595-1582">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-1582">SQL</span></span>

* <span data-ttu-id="84595-1583">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1583">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="84595-1584">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="84595-1584">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="84595-1585">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="84595-1585">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="84595-1586">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1586">Storage</span></span>

* <span data-ttu-id="84595-1587">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="84595-1587">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="84595-1588">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="84595-1588">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="84595-1589">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="84595-1589">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="84595-1590">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="84595-1590">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="84595-1591">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="84595-1591">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="84595-1592">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="84595-1592">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1593">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1593">VM</span></span>

* <span data-ttu-id="84595-1594">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1594">Support configuring nsg</span></span>
* <span data-ttu-id="84595-1595">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1595">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="84595-1596">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="84595-1596">Support managed service identities</span></span>
* <span data-ttu-id="84595-1597">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1597">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="84595-1598">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="84595-1598">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="84595-1599">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="84595-1599">May 10, 2017</span></span>

<span data-ttu-id="84595-1600">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="84595-1600">Version 2.0.6</span></span>

* <span data-ttu-id="84595-1601">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="84595-1601">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="84595-1602">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1602">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="84595-1603">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1603">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="84595-1604">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1604">Include Cognitive Services module</span></span>
* <span data-ttu-id="84595-1605">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1605">Include Service Fabric module</span></span>
* <span data-ttu-id="84595-1606">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="84595-1606">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="84595-1607">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1607">Add support for CDN commands</span></span>
* <span data-ttu-id="84595-1608">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="84595-1608">Remove Container module</span></span>
* <span data-ttu-id="84595-1609">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="84595-1609">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="84595-1610">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="84595-1610">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="84595-1611">コア</span><span class="sxs-lookup"><span data-stu-id="84595-1611">Core</span></span>

* <span data-ttu-id="84595-1612">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="84595-1612">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="84595-1613">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="84595-1613">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="84595-1614">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="84595-1614">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="84595-1615">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="84595-1615">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="84595-1616">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="84595-1616">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="84595-1617">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="84595-1617">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="84595-1618">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="84595-1618">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="84595-1619">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="84595-1619">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="84595-1620">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="84595-1620">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="84595-1621">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="84595-1621">core: Improved performance</span></span>
* <span data-ttu-id="84595-1622">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="84595-1622">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="84595-1623">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="84595-1623">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1624">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1624">ACS</span></span>

* <span data-ttu-id="84595-1625">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="84595-1625">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="84595-1626">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="84595-1626">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="84595-1627">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="84595-1627">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="84595-1628">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="84595-1628">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1629">AppService</span><span class="sxs-lookup"><span data-stu-id="84595-1629">AppService</span></span>

* <span data-ttu-id="84595-1630">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1630">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="84595-1631">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1631">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="84595-1632">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="84595-1632">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="84595-1633">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="84595-1633">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="84595-1634">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="84595-1634">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="84595-1635">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="84595-1635">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="84595-1636">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="84595-1636">support slot swap with preview</span></span>
* <span data-ttu-id="84595-1637">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="84595-1637">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="84595-1638">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="84595-1638">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="84595-1639">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="84595-1639">CosmosDB</span></span>

* <span data-ttu-id="84595-1640">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="84595-1640">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="84595-1641">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1641">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="84595-1642">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1642">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="84595-1643">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1643">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="84595-1644">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="84595-1644">Data Lake Analytics</span></span>

* <span data-ttu-id="84595-1645">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="84595-1645">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="84595-1646">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="84595-1646">Add support for new catalog item type: package.</span></span> <span data-ttu-id="84595-1647">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="84595-1647">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="84595-1648">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="84595-1648">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="84595-1649">テーブル</span><span class="sxs-lookup"><span data-stu-id="84595-1649">Table</span></span>
  * <span data-ttu-id="84595-1650">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="84595-1650">Table valued function</span></span>
  * <span data-ttu-id="84595-1651">表示</span><span class="sxs-lookup"><span data-stu-id="84595-1651">View</span></span>
  * <span data-ttu-id="84595-1652">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="84595-1652">Table Statistics.</span></span> <span data-ttu-id="84595-1653">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="84595-1653">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="84595-1654">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="84595-1654">Data Lake Store</span></span>

* <span data-ttu-id="84595-1655">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="84595-1655">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="84595-1656">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="84595-1656">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="84595-1657">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="84595-1657">missed help for access show.</span></span> <span data-ttu-id="84595-1658">追加しました </span><span class="sxs-lookup"><span data-stu-id="84595-1658">adding it.</span></span> <span data-ttu-id="84595-1659">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="84595-1659">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="84595-1660">検索</span><span class="sxs-lookup"><span data-stu-id="84595-1660">Find</span></span>

* <span data-ttu-id="84595-1661">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="84595-1661">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="84595-1662">KeyVault</span><span class="sxs-lookup"><span data-stu-id="84595-1662">KeyVault</span></span>

* <span data-ttu-id="84595-1663">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="84595-1663">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="84595-1664">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="84595-1664">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="84595-1665">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="84595-1665">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="84595-1666">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="84595-1666">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="84595-1667">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="84595-1667">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="84595-1668">ラボ</span><span class="sxs-lookup"><span data-stu-id="84595-1668">Lab</span></span>

* <span data-ttu-id="84595-1669">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1669">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="84595-1670">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1670">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="84595-1671">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1671">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="84595-1672">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1672">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="84595-1673">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1673">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="84595-1674">監視</span><span class="sxs-lookup"><span data-stu-id="84595-1674">Monitor</span></span>

* <span data-ttu-id="84595-1675">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="84595-1675">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="84595-1676">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="84595-1676">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="84595-1677">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1677">Network</span></span>

* <span data-ttu-id="84595-1678">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1678">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="84595-1679">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1679">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="84595-1680">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1680">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="84595-1681">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1681">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="84595-1682">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1682">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="84595-1683">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1683">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="84595-1684">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1684">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="84595-1685">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1685">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="84595-1686">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="84595-1686">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="84595-1687">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1687">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="84595-1688">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="84595-1688">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="84595-1689">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="84595-1689">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="84595-1690">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="84595-1690">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="84595-1691">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="84595-1691">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="84595-1692">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="84595-1692">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="84595-1693">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1693">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="84595-1694">プロファイル</span><span class="sxs-lookup"><span data-stu-id="84595-1694">Profile</span></span>

* <span data-ttu-id="84595-1695">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="84595-1695">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="84595-1696">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="84595-1696">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="84595-1697">Redis</span><span class="sxs-lookup"><span data-stu-id="84595-1697">Redis</span></span>

* <span data-ttu-id="84595-1698">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1698">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="84595-1699">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="84595-1699">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="84595-1700">リソース</span><span class="sxs-lookup"><span data-stu-id="84595-1700">Resource</span></span>

* <span data-ttu-id="84595-1701">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="84595-1701">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="84595-1702">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="84595-1702">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="84595-1703">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="84595-1703">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="84595-1704">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="84595-1704">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="84595-1705">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="84595-1705">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="84595-1706">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="84595-1706">Add docs for az lock update.</span></span> <span data-ttu-id="84595-1707">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="84595-1707">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="84595-1708">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="84595-1708">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="84595-1709">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="84595-1709">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="84595-1710">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="84595-1710">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="84595-1711">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="84595-1711">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="84595-1712">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="84595-1712">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="84595-1713">Role</span><span class="sxs-lookup"><span data-stu-id="84595-1713">Role</span></span>

* <span data-ttu-id="84595-1714">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="84595-1714">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="84595-1715">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="84595-1715">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="84595-1716">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="84595-1716">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="84595-1717">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="84595-1717">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="84595-1718">SQL</span><span class="sxs-lookup"><span data-stu-id="84595-1718">SQL</span></span>

* <span data-ttu-id="84595-1719">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="84595-1719">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="84595-1720">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="84595-1720">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="84595-1721">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1721">Storage</span></span>

* <span data-ttu-id="84595-1722">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="84595-1722">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="84595-1723">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1723">Add support for incremental blob copy</span></span>
* <span data-ttu-id="84595-1724">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="84595-1724">Add support for large block blob upload</span></span>
* <span data-ttu-id="84595-1725">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="84595-1725">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1726">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1726">VM</span></span>

* <span data-ttu-id="84595-1727">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="84595-1727">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="84595-1728">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="84595-1728">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="84595-1729">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="84595-1729">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="84595-1730">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="84595-1730">az vm/vmss disk</span></span>
  3. <span data-ttu-id="84595-1731">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="84595-1731">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="84595-1732">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="84595-1732">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="84595-1733">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="84595-1733">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="84595-1734">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="84595-1734">April 3, 2017</span></span>

<span data-ttu-id="84595-1735">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="84595-1735">Version 2.0.2</span></span>

<span data-ttu-id="84595-1736">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="84595-1736">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="84595-1737">コア</span><span class="sxs-lookup"><span data-stu-id="84595-1737">Core</span></span>

* <span data-ttu-id="84595-1738">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="84595-1738">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="84595-1739">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="84595-1739">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="84595-1740">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="84595-1740">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="84595-1741">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="84595-1741">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="84595-1742">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="84595-1742">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="84595-1743">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="84595-1743">Add prompting for missing template parameters.</span></span> <span data-ttu-id="84595-1744">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="84595-1744">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="84595-1745">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="84595-1745">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="84595-1746">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="84595-1746">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="84595-1747">ACS</span><span class="sxs-lookup"><span data-stu-id="84595-1747">ACS</span></span>

* <span data-ttu-id="84595-1748">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="84595-1748">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="84595-1749">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="84595-1749">Add support for ssh key password prompting.</span></span> <span data-ttu-id="84595-1750">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="84595-1750">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="84595-1751">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="84595-1751">Add support for windows clusters.</span></span> <span data-ttu-id="84595-1752">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="84595-1752">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="84595-1753">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="84595-1753">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="84595-1754">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="84595-1754">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="84595-1755">AppService</span><span class="sxs-lookup"><span data-stu-id="84595-1755">AppService</span></span>

* <span data-ttu-id="84595-1756">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="84595-1756">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="84595-1757">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="84595-1757">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="84595-1758">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="84595-1758">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="84595-1759">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="84595-1759">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="84595-1760">DataLake</span><span class="sxs-lookup"><span data-stu-id="84595-1760">DataLake</span></span>

* <span data-ttu-id="84595-1761">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-1761">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="84595-1762">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="84595-1762">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="84595-1763">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="84595-1763">DocuemntDB</span></span>

* <span data-ttu-id="84595-1764">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="84595-1764">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="84595-1765">VM</span><span class="sxs-lookup"><span data-stu-id="84595-1765">VM</span></span>

* <span data-ttu-id="84595-1766">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="84595-1766">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="84595-1767">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="84595-1767">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="84595-1768">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="84595-1768">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="84595-1769">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="84595-1769">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="84595-1770">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="84595-1770">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="84595-1771">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="84595-1771">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="84595-1772">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="84595-1772">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="84595-1773">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="84595-1773">February 27, 2017</span></span>

<span data-ttu-id="84595-1774">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="84595-1774">Version 2.0.0</span></span>

<span data-ttu-id="84595-1775">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="84595-1775">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="84595-1776">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="84595-1776">Container Service (acs)</span></span>
- <span data-ttu-id="84595-1777">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="84595-1777">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="84595-1778">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="84595-1778">Networking</span></span>
- <span data-ttu-id="84595-1779">Storage</span><span class="sxs-lookup"><span data-stu-id="84595-1779">Storage</span></span>

<span data-ttu-id="84595-1780">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="84595-1780">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="84595-1781">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="84595-1781">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="84595-1782">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="84595-1782">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="84595-1783">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="84595-1783">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="84595-1784">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="84595-1784">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="84595-1785">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="84595-1785">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="84595-1786">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="84595-1786">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="84595-1787">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="84595-1787">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="84595-1788">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="84595-1788">Provide feedback from the command line with the `az feedback` command</span></span>

