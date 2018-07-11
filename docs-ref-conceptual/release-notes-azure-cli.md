---
title: Azure CLI 2.0 リリース ノート
description: Azure CLI 2.0 の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 07/03/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 102152b7d99de253ccb2fea09b99be91e3c9135e
ms.sourcegitcommit: 308f9eb433a05b814999ac404f63d181169fffeb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37439671"
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="276c2-103">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="276c2-103">Azure CLI 2.0 release notes</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="276c2-104">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="276c2-104">July 3, 2018</span></span>

<span data-ttu-id="276c2-105">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="276c2-105">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="276c2-106">AKS</span><span class="sxs-lookup"><span data-stu-id="276c2-106">AKS</span></span>

* <span data-ttu-id="276c2-107">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-107">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="276c2-108">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="276c2-108">July 3, 2018</span></span>

<span data-ttu-id="276c2-109">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="276c2-109">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="276c2-110">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-110">Core</span></span>

* <span data-ttu-id="276c2-111">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-111">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="276c2-112">ACR</span><span class="sxs-lookup"><span data-stu-id="276c2-112">ACR</span></span>

* <span data-ttu-id="276c2-113">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-113">Added polling build status</span></span>
* <span data-ttu-id="276c2-114">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-114">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="276c2-115">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-115">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-116">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-116">ACS</span></span>

* <span data-ttu-id="276c2-117">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-117">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="276c2-118">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-118">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="276c2-119">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-119">Updated options for `aks browse` command.</span></span> <span data-ttu-id="276c2-120">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-120">Added `--listen-port` support</span></span>
* <span data-ttu-id="276c2-121">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-121">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="276c2-122">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="276c2-122">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="276c2-123">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-123">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-124">AppService</span><span class="sxs-lookup"><span data-stu-id="276c2-124">AppService</span></span>

* <span data-ttu-id="276c2-125">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-125">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="276c2-126">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-126">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="276c2-127">Backup</span><span class="sxs-lookup"><span data-stu-id="276c2-127">Backup</span></span>

* <span data-ttu-id="276c2-128">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-128">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="276c2-129">BatchAI</span><span class="sxs-lookup"><span data-stu-id="276c2-129">BatchAI</span></span>

* <span data-ttu-id="276c2-130">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-130">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="276c2-131">クラウド</span><span class="sxs-lookup"><span data-stu-id="276c2-131">Cloud</span></span>

* <span data-ttu-id="276c2-132">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-132">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="276c2-133">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-133">Container</span></span>

* <span data-ttu-id="276c2-134">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-134">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="276c2-135">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-135">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="276c2-136">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-136">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="276c2-137">内線番号</span><span class="sxs-lookup"><span data-stu-id="276c2-137">Extension</span></span>

* <span data-ttu-id="276c2-138">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-138">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="276c2-139">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-139">Network</span></span>

* <span data-ttu-id="276c2-140">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-140">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="276c2-141">Rdbms</span><span class="sxs-lookup"><span data-stu-id="276c2-141">Rdbms</span></span>

* <span data-ttu-id="276c2-142">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-142">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-143">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-143">Resource</span></span>

* <span data-ttu-id="276c2-144">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-144">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-145">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-145">VM</span></span>

* <span data-ttu-id="276c2-146">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-146">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="276c2-147">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="276c2-147">June 25, 2018</span></span>

<span data-ttu-id="276c2-148">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="276c2-148">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="276c2-149">CLI</span><span class="sxs-lookup"><span data-stu-id="276c2-149">CLI</span></span>

* <span data-ttu-id="276c2-150">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-150">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="276c2-151">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="276c2-151">June 19, 2018</span></span>

<span data-ttu-id="276c2-152">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="276c2-152">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="276c2-153">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-153">Core</span></span>

* <span data-ttu-id="276c2-154">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-154">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="276c2-155">ACR</span><span class="sxs-lookup"><span data-stu-id="276c2-155">ACR</span></span>

* <span data-ttu-id="276c2-156">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-156">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="276c2-157">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-157">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-158">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-158">ACS</span></span>

* <span data-ttu-id="276c2-159">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-159">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="276c2-160">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-160">Added `--update` support</span></span>
* <span data-ttu-id="276c2-161">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-161">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="276c2-162">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="276c2-162">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="276c2-163">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-163">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="276c2-164">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-164">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="276c2-165">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-165">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="276c2-166">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-166">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span> 

### <a name="appservice"></a><span data-ttu-id="276c2-167">AppService</span><span class="sxs-lookup"><span data-stu-id="276c2-167">AppService</span></span>

* <span data-ttu-id="276c2-168">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-168">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="276c2-169">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-169">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="276c2-170">Batch</span><span class="sxs-lookup"><span data-stu-id="276c2-170">Batch</span></span>

* <span data-ttu-id="276c2-171">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-171">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="276c2-172">Batch AI</span><span class="sxs-lookup"><span data-stu-id="276c2-172">Batch AI</span></span>

* <span data-ttu-id="276c2-173">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-173">Added support for workspaces.</span></span> <span data-ttu-id="276c2-174">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="276c2-174">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="276c2-175">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-175">Added support for experiments.</span></span> <span data-ttu-id="276c2-176">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="276c2-176">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="276c2-177">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-177">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="276c2-178">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-178">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="276c2-179">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="276c2-179">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="276c2-180">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-180">Added support for `--ids` to `batchai` commands</span></span> 
* <span data-ttu-id="276c2-181">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="276c2-181">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="276c2-182">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="276c2-182">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="276c2-183">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-183">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="276c2-184">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="276c2-184">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="276c2-185">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-185">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="276c2-186">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="276c2-186">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="276c2-187">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-187">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="276c2-188">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="276c2-188">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="276c2-189">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-189">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="276c2-190">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-190">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
 - <span data-ttu-id="276c2-191">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-191">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
 - <span data-ttu-id="276c2-192">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-192">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="276c2-193">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-193">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="276c2-194">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-194">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="276c2-195">マップ</span><span class="sxs-lookup"><span data-stu-id="276c2-195">Maps</span></span>

* <span data-ttu-id="276c2-196">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-196">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="276c2-197">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-197">Network</span></span>

* <span data-ttu-id="276c2-198">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="276c2-198">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="276c2-199">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-199">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="276c2-200">#6502</span><span class="sxs-lookup"><span data-stu-id="276c2-200">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="276c2-201">Reservations</span><span class="sxs-lookup"><span data-stu-id="276c2-201">Reservations</span></span>

* <span data-ttu-id="276c2-202">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-202">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="276c2-203">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-203">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="276c2-204">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-204">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="276c2-205">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-205">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="276c2-206">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-206">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="276c2-207">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-207">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="276c2-208">役割</span><span class="sxs-lookup"><span data-stu-id="276c2-208">Role</span></span>

* <span data-ttu-id="276c2-209">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-209">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-210">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-210">SQL</span></span>

* <span data-ttu-id="276c2-211">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-211">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-212">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-212">Storage</span></span>

* <span data-ttu-id="276c2-213">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="276c2-213">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-214">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-214">VM</span></span>

* <span data-ttu-id="276c2-215">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-215">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="276c2-216">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-216">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="276c2-217">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-217">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="276c2-218">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="276c2-218">June 13, 2018</span></span>

<span data-ttu-id="276c2-219">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="276c2-219">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="276c2-220">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-220">Core</span></span>

* <span data-ttu-id="276c2-221">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-221">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="276c2-222">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="276c2-222">June 13, 2018</span></span>

<span data-ttu-id="276c2-223">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="276c2-223">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="276c2-224">AKS</span><span class="sxs-lookup"><span data-stu-id="276c2-224">AKS</span></span>

* <span data-ttu-id="276c2-225">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-225">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="276c2-226">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-226">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span> 
* <span data-ttu-id="276c2-227">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-227">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="276c2-228">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-228">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="276c2-229">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-229">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-230">AppService</span><span class="sxs-lookup"><span data-stu-id="276c2-230">AppService</span></span>

* <span data-ttu-id="276c2-231">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-231">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="276c2-232">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="276c2-232">June 5, 2018</span></span>

<span data-ttu-id="276c2-233">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="276c2-233">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="276c2-234">対話</span><span class="sxs-lookup"><span data-stu-id="276c2-234">Interactive</span></span>

* <span data-ttu-id="276c2-235">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-235">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="276c2-236">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="276c2-236">June 5, 2018</span></span>

<span data-ttu-id="276c2-237">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="276c2-237">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="276c2-238">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-238">Core</span></span>

* <span data-ttu-id="276c2-239">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-239">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="276c2-240">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-240">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="276c2-241">ACR</span><span class="sxs-lookup"><span data-stu-id="276c2-241">ACR</span></span>

* <span data-ttu-id="276c2-242">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-242">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="276c2-243">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-243">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="276c2-244">AKS</span><span class="sxs-lookup"><span data-stu-id="276c2-244">AKS</span></span>

* <span data-ttu-id="276c2-245">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-245">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="276c2-246">Batch</span><span class="sxs-lookup"><span data-stu-id="276c2-246">Batch</span></span>

* <span data-ttu-id="276c2-247">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-247">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="276c2-248">IoT</span><span class="sxs-lookup"><span data-stu-id="276c2-248">IOT</span></span>

* <span data-ttu-id="276c2-249">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-249">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="276c2-250">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-250">Network</span></span>

* <span data-ttu-id="276c2-251">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-251">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="276c2-252">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="276c2-252">Policy Insights</span></span>

* <span data-ttu-id="276c2-253">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="276c2-253">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="276c2-254">ARM</span><span class="sxs-lookup"><span data-stu-id="276c2-254">ARM</span></span>

* <span data-ttu-id="276c2-255">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-255">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-256">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-256">SQL</span></span>

* <span data-ttu-id="276c2-257">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-257">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="276c2-258">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-258">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="276c2-259">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-259">Storage</span></span>

* <span data-ttu-id="276c2-260">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-260">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-261">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-261">VM</span></span>

* <span data-ttu-id="276c2-262">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-262">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="276c2-263">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-263">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="276c2-264">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-264">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="276c2-265">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="276c2-265">May 22, 2018</span></span>

<span data-ttu-id="276c2-266">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="276c2-266">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="276c2-267">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-267">Core</span></span>

* <span data-ttu-id="276c2-268">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-268">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-269">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-269">ACS</span></span>

* <span data-ttu-id="276c2-270">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-270">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="276c2-271">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-271">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-272">AppService</span><span class="sxs-lookup"><span data-stu-id="276c2-272">AppService</span></span>

* <span data-ttu-id="276c2-273">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-273">Improved generic update commands</span></span>
* <span data-ttu-id="276c2-274">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-274">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="276c2-275">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-275">Container</span></span>

* <span data-ttu-id="276c2-276">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-276">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="276c2-277">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-277">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="276c2-278">内線番号</span><span class="sxs-lookup"><span data-stu-id="276c2-278">Extension</span></span>

* <span data-ttu-id="276c2-279">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-279">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="276c2-280">対話</span><span class="sxs-lookup"><span data-stu-id="276c2-280">Interactive</span></span>

* <span data-ttu-id="276c2-281">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-281">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="276c2-282">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-282">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="276c2-283">KeyVault</span><span class="sxs-lookup"><span data-stu-id="276c2-283">KeyVault</span></span>

* <span data-ttu-id="276c2-284">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-284">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="276c2-285">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-285">Network</span></span>

* <span data-ttu-id="276c2-286">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-286">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="276c2-287">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-287">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-288">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-288">SQL</span></span>

* <span data-ttu-id="276c2-289">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-289">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="276c2-290">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-290">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="276c2-291">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-291">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span> 
    * <span data-ttu-id="276c2-292">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-292">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="276c2-293">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-293">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="276c2-294">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="276c2-294">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="276c2-295">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="276c2-295">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="276c2-296">`edition`</span><span class="sxs-lookup"><span data-stu-id="276c2-296">`edition`.</span></span> <span data-ttu-id="276c2-297">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="276c2-297">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="276c2-298">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="276c2-298">`elasticPoolName`.</span></span> <span data-ttu-id="276c2-299">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="276c2-299">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="276c2-300">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-300">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="276c2-301">`edition`</span><span class="sxs-lookup"><span data-stu-id="276c2-301">`edition`.</span></span> <span data-ttu-id="276c2-302">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="276c2-302">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="276c2-303">`dtu`</span><span class="sxs-lookup"><span data-stu-id="276c2-303">`dtu`.</span></span> <span data-ttu-id="276c2-304">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="276c2-304">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="276c2-305">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="276c2-305">`databaseDtuMin`.</span></span> <span data-ttu-id="276c2-306">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="276c2-306">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="276c2-307">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="276c2-307">`databaseDtuMax`.</span></span> <span data-ttu-id="276c2-308">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="276c2-308">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="276c2-309">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-309">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="276c2-310">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-310">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-311">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-311">Storage</span></span>

* <span data-ttu-id="276c2-312">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-312">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="276c2-313">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-313">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-314">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-314">VM</span></span>

* <span data-ttu-id="276c2-315">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-315">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="276c2-316">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="276c2-316">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="276c2-317">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-317">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="276c2-318">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-318">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="276c2-319">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-319">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="276c2-320">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="276c2-320">May 7, 2018</span></span>

<span data-ttu-id="276c2-321">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="276c2-321">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="276c2-322">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-322">Core</span></span>

* <span data-ttu-id="276c2-323">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-323">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="276c2-324">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-324">Added limited support for positional arguments</span></span>
* <span data-ttu-id="276c2-325">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-325">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="276c2-326">#5591</span><span class="sxs-lookup"><span data-stu-id="276c2-326">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="276c2-327">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-327">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="276c2-328">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="276c2-328">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="276c2-329">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-329">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="276c2-330">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-330">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="276c2-331">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-331">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="276c2-332">ACR</span><span class="sxs-lookup"><span data-stu-id="276c2-332">ACR</span></span>

* <span data-ttu-id="276c2-333">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-333">Added ACR Build commands</span></span>
* <span data-ttu-id="276c2-334">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-334">Improved resource not found error messages</span></span>
* <span data-ttu-id="276c2-335">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-335">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="276c2-336">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-336">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="276c2-337">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-337">Improved repository commands error messages</span></span>
* <span data-ttu-id="276c2-338">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-338">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-339">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-339">ACS</span></span>

* <span data-ttu-id="276c2-340">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-340">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="276c2-341">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-341">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="276c2-342">AMS</span><span class="sxs-lookup"><span data-stu-id="276c2-342">AMS</span></span>

* <span data-ttu-id="276c2-343">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="276c2-343">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-344">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-344">Appservice</span></span>

* <span data-ttu-id="276c2-345">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-345">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="276c2-346">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-346">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="276c2-347">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-347">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="276c2-348">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-348">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="276c2-349">Batch AI</span><span class="sxs-lookup"><span data-stu-id="276c2-349">Batch AI</span></span>

* <span data-ttu-id="276c2-350">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-350">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="276c2-351">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="276c2-351">Cognitive Services</span></span>

* <span data-ttu-id="276c2-352">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-352">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="276c2-353">消費</span><span class="sxs-lookup"><span data-stu-id="276c2-353">Consumption</span></span>

* <span data-ttu-id="276c2-354">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-354">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="276c2-355">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-355">Container</span></span>

* <span data-ttu-id="276c2-356">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-356">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="276c2-357">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="276c2-357">Cosmos DB</span></span>

* <span data-ttu-id="276c2-358">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="276c2-358">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="276c2-359">DMS</span><span class="sxs-lookup"><span data-stu-id="276c2-359">DMS</span></span>

* <span data-ttu-id="276c2-360">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-360">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="276c2-361">内線番号</span><span class="sxs-lookup"><span data-stu-id="276c2-361">Extension</span></span>

* <span data-ttu-id="276c2-362">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-362">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="276c2-363">対話</span><span class="sxs-lookup"><span data-stu-id="276c2-363">Interactive</span></span>

* <span data-ttu-id="276c2-364">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-364">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="276c2-365">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="276c2-365">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="276c2-366">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-366">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="276c2-367">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-367">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="276c2-368">ラボ</span><span class="sxs-lookup"><span data-stu-id="276c2-368">Lab</span></span>

* <span data-ttu-id="276c2-369">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-369">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="276c2-370">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-370">Network</span></span>

* <span data-ttu-id="276c2-371">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-371">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span> 
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="276c2-372">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-372">Profile</span></span>

* <span data-ttu-id="276c2-373">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-373">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="276c2-374">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-374">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="276c2-375">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-375">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="276c2-376">Redis</span><span class="sxs-lookup"><span data-stu-id="276c2-376">Redis</span></span>

* <span data-ttu-id="276c2-377">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-377">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="276c2-378">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="276c2-378">Deprecated `redis list-all`.</span></span> <span data-ttu-id="276c2-379">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="276c2-379">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="276c2-380">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-380">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="276c2-381">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-381">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="276c2-382">役割</span><span class="sxs-lookup"><span data-stu-id="276c2-382">Role</span></span>

* <span data-ttu-id="276c2-383">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-383">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-384">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-384">Storage</span></span>

* <span data-ttu-id="276c2-385">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="276c2-385">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="276c2-386">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="276c2-386">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="276c2-387">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="276c2-387">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="276c2-388">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="276c2-388">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="276c2-389">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-389">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-390">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-390">VM</span></span>

* <span data-ttu-id="276c2-391">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-391">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="276c2-392">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-392">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="276c2-393">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="276c2-393">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="276c2-394">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-394">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="276c2-395">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-395">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="276c2-396">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-396">Added write accelerator support</span></span> 
* <span data-ttu-id="276c2-397">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-397">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="276c2-398">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-398">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="276c2-399">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-399">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="276c2-400">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="276c2-400">April 10, 2018</span></span>

<span data-ttu-id="276c2-401">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="276c2-401">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="276c2-402">ACR</span><span class="sxs-lookup"><span data-stu-id="276c2-402">ACR</span></span>

* <span data-ttu-id="276c2-403">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-403">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-404">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-404">ACS</span></span>

* <span data-ttu-id="276c2-405">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-405">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-406">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-406">Appservice</span></span>

* [重大な変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="276c2-408">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-408">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="276c2-409">BatchAI</span><span class="sxs-lookup"><span data-stu-id="276c2-409">BatchAI</span></span>

* <span data-ttu-id="276c2-410">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-410">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="276c2-411">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="276c2-411">Job level mounting</span></span>
 - <span data-ttu-id="276c2-412">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="276c2-412">Environment variables with secret values</span></span>
 - <span data-ttu-id="276c2-413">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="276c2-413">Performance counters settings</span></span>
 - <span data-ttu-id="276c2-414">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="276c2-414">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="276c2-415">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="276c2-415">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="276c2-416">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="276c2-416">Usage and limits reporting</span></span>
 - <span data-ttu-id="276c2-417">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="276c2-417">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="276c2-418">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="276c2-418">Support for custom images</span></span>
 - <span data-ttu-id="276c2-419">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-419">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="276c2-420">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-420">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="276c2-421">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="276c2-421">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="276c2-422">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="276c2-422">National clouds are supported</span></span>
* <span data-ttu-id="276c2-423">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-423">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="276c2-424">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-424">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="276c2-425">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-425">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="276c2-426">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-426">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="276c2-427">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="276c2-427">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="276c2-428">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="276c2-428">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="276c2-429">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-429">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="276c2-430">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-430">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="276c2-431">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="276c2-431">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="276c2-432">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-432">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="276c2-433">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="276c2-433">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="276c2-434">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="276c2-434">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="276c2-435">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-435">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="276c2-436">課金</span><span class="sxs-lookup"><span data-stu-id="276c2-436">Billing</span></span>

* <span data-ttu-id="276c2-437">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-437">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="276c2-438">消費</span><span class="sxs-lookup"><span data-stu-id="276c2-438">Consumption</span></span>

* <span data-ttu-id="276c2-439">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-439">Added `marketplace` commands</span></span>
* <span data-ttu-id="276c2-440">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-440">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="276c2-441">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-441">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="276c2-442">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-442">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="276c2-443">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-443">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="276c2-444">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-444">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="276c2-445">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-445">Container</span></span>

* <span data-ttu-id="276c2-446">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-446">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="276c2-447">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-447">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="276c2-448">内線番号</span><span class="sxs-lookup"><span data-stu-id="276c2-448">Extension</span></span>

* <span data-ttu-id="276c2-449">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-449">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="276c2-450">対話</span><span class="sxs-lookup"><span data-stu-id="276c2-450">Interactive</span></span>

* <span data-ttu-id="276c2-451">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-451">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="276c2-452">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-452">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="276c2-453">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-453">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="276c2-454">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-454">Network</span></span>

* <span data-ttu-id="276c2-455">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-455">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="276c2-456">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-456">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="276c2-457">#4910</span><span class="sxs-lookup"><span data-stu-id="276c2-457">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="276c2-458">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-458">Added `ddos-protection` commands to create DDoS protection plans</span></span> 
* <span data-ttu-id="276c2-459">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="276c2-459">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="276c2-460">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-460">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="276c2-461">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-461">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="276c2-462">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-462">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="276c2-463">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-463">Profile</span></span>

* <span data-ttu-id="276c2-464">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-464">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="276c2-465">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-465">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="276c2-466">RDBMS</span><span class="sxs-lookup"><span data-stu-id="276c2-466">RDBMS</span></span>

* <span data-ttu-id="276c2-467">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-467">Added `georestore` command</span></span>
* <span data-ttu-id="276c2-468">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-468">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-469">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-469">Resource</span></span>

* <span data-ttu-id="276c2-470">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-470">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="276c2-471">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-471">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-472">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-472">SQL</span></span>

* <span data-ttu-id="276c2-473">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-473">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-474">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-474">Storage</span></span>

* <span data-ttu-id="276c2-475">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-475">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-476">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-476">VM</span></span>

* <span data-ttu-id="276c2-477">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-477">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="276c2-478">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-478">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大な変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="276c2-480">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-480">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="276c2-481">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-481">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="276c2-482">#5718</span><span class="sxs-lookup"><span data-stu-id="276c2-482">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="276c2-483">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-483">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="276c2-484">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="276c2-484">March 27, 2018</span></span>

<span data-ttu-id="276c2-485">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="276c2-485">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="276c2-486">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-486">Core</span></span>

* <span data-ttu-id="276c2-487">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="276c2-487">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-488">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-488">ACS</span></span>

* <span data-ttu-id="276c2-489">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-489">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-490">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-490">Appservice</span></span>

* <span data-ttu-id="276c2-491">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-491">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="276c2-492">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-492">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="276c2-493">Backup</span><span class="sxs-lookup"><span data-stu-id="276c2-493">Backup</span></span>

* <span data-ttu-id="276c2-494">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-494">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="276c2-495">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="276c2-495">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="276c2-496">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-496">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="276c2-497">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-497">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="276c2-498">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-498">Container</span></span>

* <span data-ttu-id="276c2-499">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-499">Added `container exec` command.</span></span> <span data-ttu-id="276c2-500">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="276c2-500">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="276c2-501">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="276c2-501">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="276c2-502">内線番号</span><span class="sxs-lookup"><span data-stu-id="276c2-502">Extension</span></span>

* <span data-ttu-id="276c2-503">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-503">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="276c2-504">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-504">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="276c2-505">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-505">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="276c2-506">対話</span><span class="sxs-lookup"><span data-stu-id="276c2-506">Interactive</span></span>

* <span data-ttu-id="276c2-507">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-507">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="276c2-508">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-508">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="276c2-509">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="276c2-509">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="276c2-510">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-510">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="276c2-511">ラボ</span><span class="sxs-lookup"><span data-stu-id="276c2-511">Lab</span></span>

* <span data-ttu-id="276c2-512">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-512">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="276c2-513">監視</span><span class="sxs-lookup"><span data-stu-id="276c2-513">Monitor</span></span>

* <span data-ttu-id="276c2-514">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="276c2-514">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="276c2-515">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="276c2-515">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="276c2-516">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="276c2-516">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="276c2-517">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-517">Network</span></span>

* <span data-ttu-id="276c2-518">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-518">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="276c2-519">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-519">Profile</span></span>

* <span data-ttu-id="276c2-520">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-520">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="276c2-521">RDBMS</span><span class="sxs-lookup"><span data-stu-id="276c2-521">RDBMS</span></span>

* <span data-ttu-id="276c2-522">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-522">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-523">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-523">Resource</span></span>

* [重大な変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="276c2-525">役割</span><span class="sxs-lookup"><span data-stu-id="276c2-525">Role</span></span>

* <span data-ttu-id="276c2-526">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-526">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="276c2-527">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-527">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="276c2-528">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-528">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="276c2-529">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-529">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="276c2-530">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-530">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-531">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-531">Storage</span></span>

* <span data-ttu-id="276c2-532">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-532">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="276c2-533">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-533">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-534">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-534">VM</span></span>

* <span data-ttu-id="276c2-535">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-535">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="276c2-536">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-536">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="276c2-537">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-537">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="276c2-538">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-538">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="276c2-539">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="276c2-539">March 13, 2018</span></span>

<span data-ttu-id="276c2-540">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="276c2-540">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="276c2-541">ACR</span><span class="sxs-lookup"><span data-stu-id="276c2-541">ACR</span></span>

* <span data-ttu-id="276c2-542">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-542">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="276c2-543">ph x="3" /&gt; コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-543">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="276c2-544">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-544">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-545">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-545">ACS</span></span>

* <span data-ttu-id="276c2-546">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-546">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="276c2-547">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-547">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="276c2-548">Advisor</span><span class="sxs-lookup"><span data-stu-id="276c2-548">Advisor</span></span>

* <span data-ttu-id="276c2-549">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-549">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="276c2-550">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-550">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="276c2-551">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-551">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span> 
* <span data-ttu-id="276c2-552">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-552">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="276c2-553">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-553">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-554">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-554">Appservice</span></span>

* <span data-ttu-id="276c2-555">を非推奨にしました `[webapp|functionapp] assign-identity`</span><span class="sxs-lookup"><span data-stu-id="276c2-555">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="276c2-556">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-556">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="276c2-557">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="276c2-557">Eventhubs</span></span>

* <span data-ttu-id="276c2-558">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="276c2-558">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="276c2-559">内線番号</span><span class="sxs-lookup"><span data-stu-id="276c2-559">Extension</span></span>

* <span data-ttu-id="276c2-560">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-560">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="276c2-561">対話</span><span class="sxs-lookup"><span data-stu-id="276c2-561">Interactive</span></span>

* <span data-ttu-id="276c2-562">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="276c2-562">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="276c2-563">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="276c2-563">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="276c2-564">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="276c2-564">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="276c2-565">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-565">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="276c2-566">監視</span><span class="sxs-lookup"><span data-stu-id="276c2-566">Monitor</span></span>

* <span data-ttu-id="276c2-567">コマンドを非推奨にしました `monitor autoscale-settings`</span><span class="sxs-lookup"><span data-stu-id="276c2-567">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="276c2-568">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-568">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="276c2-569">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-569">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="276c2-570">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-570">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="276c2-571">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-571">Network</span></span>

* <span data-ttu-id="276c2-572">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-572">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="276c2-573">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-573">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="276c2-574">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-574">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="276c2-575">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-575">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="276c2-576">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-576">Profile</span></span>

* <span data-ttu-id="276c2-577">の `--msi` パラメーターを非推奨にしました `az login`</span><span class="sxs-lookup"><span data-stu-id="276c2-577">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="276c2-578">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-578">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="276c2-579">RDBMS</span><span class="sxs-lookup"><span data-stu-id="276c2-579">RDBMS</span></span>

* <span data-ttu-id="276c2-580">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-580">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="276c2-581">Service Bus</span><span class="sxs-lookup"><span data-stu-id="276c2-581">Service Bus</span></span>

* <span data-ttu-id="276c2-582">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="276c2-582">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-583">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-583">Storage</span></span>

* <span data-ttu-id="276c2-584">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-584">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="276c2-585">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="276c2-585">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-586">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-586">VM</span></span>

* <span data-ttu-id="276c2-587">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-587">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="276c2-588">ph x="1" /&gt; および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-588">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="276c2-589">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-589">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="276c2-590">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-590">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="276c2-591">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="276c2-591">February 27, 2018</span></span>

<span data-ttu-id="276c2-592">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="276c2-592">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="276c2-593">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-593">Core</span></span>

* <span data-ttu-id="276c2-594">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="276c2-594">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="276c2-595">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-595">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="276c2-596">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-596">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-597">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-597">ACS</span></span>

* <span data-ttu-id="276c2-598">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-598">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="276c2-599">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="276c2-599">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="276c2-600">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-600">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="276c2-601">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-601">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-602">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-602">Appservice</span></span>

* <span data-ttu-id="276c2-603">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="276c2-603">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="276c2-604">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="276c2-604">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="276c2-605">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="276c2-605">Cognitive Services</span></span>

* <span data-ttu-id="276c2-606">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-606">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="276c2-607">消費</span><span class="sxs-lookup"><span data-stu-id="276c2-607">Consumption</span></span>

* <span data-ttu-id="276c2-608">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-608">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="276c2-609">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-609">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="276c2-610">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-610">Container</span></span>

* <span data-ttu-id="276c2-611">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-611">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="276c2-612">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-612">Network</span></span>

* <span data-ttu-id="276c2-613">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="276c2-613">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-614">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-614">Resource</span></span>

* <span data-ttu-id="276c2-615">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-615">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="276c2-616">役割</span><span class="sxs-lookup"><span data-stu-id="276c2-616">Role</span></span>

* <span data-ttu-id="276c2-617">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-617">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-618">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-618">SQL</span></span>

* <span data-ttu-id="276c2-619">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-619">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-620">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-620">Storage</span></span>

* <span data-ttu-id="276c2-621">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-621">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-622">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-622">VM</span></span>

* <span data-ttu-id="276c2-623">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-623">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="276c2-624">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="276c2-624">February 13, 2018</span></span>

<span data-ttu-id="276c2-625">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="276c2-625">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="276c2-626">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-626">Core</span></span>

* <span data-ttu-id="276c2-627">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-627">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-628">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-628">ACS</span></span>

* <span data-ttu-id="276c2-629">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-629">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="276c2-630">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-630">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="276c2-631">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-631">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="276c2-632">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-632">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="276c2-633">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-633">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="276c2-634">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="276c2-634">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="276c2-635">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-635">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="276c2-636">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="276c2-636">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-637">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-637">Appservice</span></span>

* <span data-ttu-id="276c2-638">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-638">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="276c2-639">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-639">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="276c2-640">CDN</span><span class="sxs-lookup"><span data-stu-id="276c2-640">CDN</span></span>

* <span data-ttu-id="276c2-641">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-641">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="276c2-642">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-642">Container</span></span>

* <span data-ttu-id="276c2-643">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-643">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="276c2-644">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-644">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="276c2-645">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="276c2-645">CosmosDB</span></span>

* <span data-ttu-id="276c2-646">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-646">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="276c2-647">内線番号</span><span class="sxs-lookup"><span data-stu-id="276c2-647">Extension</span></span>

* <span data-ttu-id="276c2-648">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-648">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="276c2-649">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-649">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="276c2-650">フィードバック</span><span class="sxs-lookup"><span data-stu-id="276c2-650">Feedback</span></span>

* <span data-ttu-id="276c2-651">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-651">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="276c2-652">対話</span><span class="sxs-lookup"><span data-stu-id="276c2-652">Interactive</span></span>

* <span data-ttu-id="276c2-653">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-653">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="276c2-654">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-654">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="276c2-655">IoT</span><span class="sxs-lookup"><span data-stu-id="276c2-655">IoT</span></span>

* <span data-ttu-id="276c2-656">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-656">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="276c2-657">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-657">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="276c2-658">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-658">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="276c2-659">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-659">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="276c2-660">監視</span><span class="sxs-lookup"><span data-stu-id="276c2-660">Monitor</span></span>

* <span data-ttu-id="276c2-661">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-661">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="276c2-662">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-662">Network</span></span>

* <span data-ttu-id="276c2-663">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-663">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="276c2-664">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-664">Profile</span></span>

* <span data-ttu-id="276c2-665">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-665">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-666">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-666">Resource</span></span>

* <span data-ttu-id="276c2-667">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-667">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="276c2-668">役割</span><span class="sxs-lookup"><span data-stu-id="276c2-668">Role</span></span>

* <span data-ttu-id="276c2-669">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-669">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-670">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-670">SQL</span></span>

* <span data-ttu-id="276c2-671">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-671">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="276c2-672">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-672">Added `sql db rename`</span></span>
* <span data-ttu-id="276c2-673">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-673">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-674">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-674">Storage</span></span>

* <span data-ttu-id="276c2-675">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-675">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-676">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-676">VM</span></span>

* <span data-ttu-id="276c2-677">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-677">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="276c2-678">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-678">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="276c2-679">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="276c2-679">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="276c2-680">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="276c2-680">January 31, 2018</span></span>

<span data-ttu-id="276c2-681">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="276c2-681">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="276c2-682">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-682">Core</span></span>

* <span data-ttu-id="276c2-683">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-683">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="276c2-684">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-684">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="276c2-685">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-685">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="276c2-686">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="276c2-686">Use `--verbose` to see</span></span>
* <span data-ttu-id="276c2-687">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="276c2-687">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-688">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-688">ACS</span></span>

* <span data-ttu-id="276c2-689">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-689">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="276c2-690">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-690">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-691">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-691">Appservice</span></span>

* <span data-ttu-id="276c2-692">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="276c2-692">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="276c2-693">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-693">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="276c2-694">CDN</span><span class="sxs-lookup"><span data-stu-id="276c2-694">CDN</span></span>

* <span data-ttu-id="276c2-695">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-695">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="276c2-696">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="276c2-696">CosmosDB</span></span>

* <span data-ttu-id="276c2-697">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-697">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="276c2-698">対話</span><span class="sxs-lookup"><span data-stu-id="276c2-698">Interactive</span></span>

* <span data-ttu-id="276c2-699">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-699">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="276c2-700">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-700">Network</span></span>

* <span data-ttu-id="276c2-701">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-701">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="276c2-702">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-702">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="276c2-703">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-703">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="276c2-704">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-704">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="276c2-705">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-705">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="276c2-706">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-706">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="276c2-707">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-707">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="276c2-708">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-708">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="276c2-709">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-709">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="276c2-710">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="276c2-710">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="276c2-711">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-711">Profile</span></span>

* <span data-ttu-id="276c2-712">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-712">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-713">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-713">Resource</span></span>

* <span data-ttu-id="276c2-714">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-714">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-715">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-715">Storage</span></span>

* <span data-ttu-id="276c2-716">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-716">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="276c2-717">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-717">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="276c2-718">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-718">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="276c2-719">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-719">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="276c2-720">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-720">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-721">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-721">VM</span></span>

* <span data-ttu-id="276c2-722">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-722">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="276c2-723">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-723">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="276c2-724">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-724">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="276c2-725">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-725">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="276c2-726">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="276c2-726">January 17, 2018</span></span>

<span data-ttu-id="276c2-727">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="276c2-727">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="276c2-728">ACR</span><span class="sxs-lookup"><span data-stu-id="276c2-728">ACR</span></span>

* <span data-ttu-id="276c2-729">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-729">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="276c2-730">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-730">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-731">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-731">ACS</span></span>

* <span data-ttu-id="276c2-732">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-732">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="276c2-733">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-733">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-734">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-734">Appservice</span></span>

* <span data-ttu-id="276c2-735">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-735">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="276c2-736">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-736">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="276c2-737">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-737">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="276c2-738">Backup</span><span class="sxs-lookup"><span data-stu-id="276c2-738">Backup</span></span>

* <span data-ttu-id="276c2-739">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-739">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="276c2-740">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-740">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="276c2-741">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-741">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="276c2-742">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-742">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="276c2-743">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-743">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="276c2-744">Batch</span><span class="sxs-lookup"><span data-stu-id="276c2-744">Batch</span></span>

* <span data-ttu-id="276c2-745">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-745">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="276c2-746">クラウド</span><span class="sxs-lookup"><span data-stu-id="276c2-746">Cloud</span></span>

* <span data-ttu-id="276c2-747">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-747">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="276c2-748">消費</span><span class="sxs-lookup"><span data-stu-id="276c2-748">Consumption</span></span>

* <span data-ttu-id="276c2-749">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-749">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="276c2-750">Event Grid</span><span class="sxs-lookup"><span data-stu-id="276c2-750">Event Grid</span></span>

* <span data-ttu-id="276c2-751">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="276c2-751">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="276c2-752">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="276c2-752">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="276c2-753">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-753">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="276c2-754">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="276c2-754">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="276c2-755">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-755">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="276c2-756">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-756">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="276c2-757">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-757">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="276c2-758">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-758">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="276c2-759">対話</span><span class="sxs-lookup"><span data-stu-id="276c2-759">Interactive</span></span>

* <span data-ttu-id="276c2-760">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="276c2-760">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="276c2-761">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-761">Fixed errors on startup</span></span>
* <span data-ttu-id="276c2-762">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-762">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="276c2-763">IoT</span><span class="sxs-lookup"><span data-stu-id="276c2-763">IoT</span></span>

* <span data-ttu-id="276c2-764">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-764">Added support for device provisioning service</span></span>
* <span data-ttu-id="276c2-765">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-765">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="276c2-766">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-766">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="276c2-767">監視</span><span class="sxs-lookup"><span data-stu-id="276c2-767">Monitor</span></span>

* <span data-ttu-id="276c2-768">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-768">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="276c2-769">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="276c2-769">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="276c2-770">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-770">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="276c2-771">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-771">Network</span></span>

* <span data-ttu-id="276c2-772">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-772">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="276c2-773">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-773">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="276c2-774">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-774">Profile</span></span>

* <span data-ttu-id="276c2-775">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-775">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="276c2-776">役割</span><span class="sxs-lookup"><span data-stu-id="276c2-776">Role</span></span>

* <span data-ttu-id="276c2-777">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-777">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="276c2-778">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="276c2-778">Service Fabric</span></span>

* <span data-ttu-id="276c2-779">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-779">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="276c2-780">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-780">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-781">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-781">VM</span></span>

* <span data-ttu-id="276c2-782">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="276c2-782">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="276c2-783">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-783">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="276c2-784">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-784">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="276c2-785">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-785">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="276c2-786">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-786">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="276c2-787">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-787">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="276c2-788">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-788">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="276c2-789">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-789">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="276c2-790">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="276c2-790">December 19, 2017</span></span>

<span data-ttu-id="276c2-791">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="276c2-791">Version 2.0.23</span></span>

* <span data-ttu-id="276c2-792">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-792">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="276c2-793">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-793">Container</span></span>

* <span data-ttu-id="276c2-794">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-794">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="276c2-795">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-795">Network</span></span>

* <span data-ttu-id="276c2-796">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-796">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="276c2-797">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-797">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-798">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-798">Storage</span></span>

* <span data-ttu-id="276c2-799">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-799">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-800">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-800">VM</span></span>

* <span data-ttu-id="276c2-801">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-801">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="276c2-802">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="276c2-802">December 5, 2017</span></span>

<span data-ttu-id="276c2-803">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="276c2-803">Version 2.0.22</span></span>

* <span data-ttu-id="276c2-804">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-804">Removed `az component` commands.</span></span> <span data-ttu-id="276c2-805">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="276c2-805">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="276c2-806">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-806">Core</span></span>
* <span data-ttu-id="276c2-807">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-807">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="276c2-808">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-808">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-809">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-809">ACS</span></span>

* <span data-ttu-id="276c2-810">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-810">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="276c2-811">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-811">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="276c2-812">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-812">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="276c2-813">Advisor</span><span class="sxs-lookup"><span data-stu-id="276c2-813">Advisor</span></span>

* <span data-ttu-id="276c2-814">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="276c2-814">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-815">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-815">Appservice</span></span>

* <span data-ttu-id="276c2-816">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-816">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="276c2-817">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-817">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="276c2-818">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-818">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="276c2-819">消費</span><span class="sxs-lookup"><span data-stu-id="276c2-819">Consumption</span></span>

* <span data-ttu-id="276c2-820">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-820">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="276c2-821">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-821">Container</span></span>

* <span data-ttu-id="276c2-822">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-822">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="276c2-823">監視</span><span class="sxs-lookup"><span data-stu-id="276c2-823">Monitor</span></span>

* <span data-ttu-id="276c2-824">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-824">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-825">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-825">Resource</span></span>

* <span data-ttu-id="276c2-826">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-826">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="276c2-827">役割</span><span class="sxs-lookup"><span data-stu-id="276c2-827">Role</span></span>

* <span data-ttu-id="276c2-828">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-828">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="276c2-829">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="276c2-829">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="276c2-830">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-830">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-831">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-831">SQL</span></span>

* <span data-ttu-id="276c2-832">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-832">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="276c2-833">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-833">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-834">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-834">VM</span></span>

* <span data-ttu-id="276c2-835">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-835">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="276c2-836">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="276c2-836">November 14, 2017</span></span>

<span data-ttu-id="276c2-837">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="276c2-837">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="276c2-838">ACR</span><span class="sxs-lookup"><span data-stu-id="276c2-838">ACR</span></span>

* <span data-ttu-id="276c2-839">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-839">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="276c2-840">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-840">ACS</span></span>

* <span data-ttu-id="276c2-841">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-841">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="276c2-842">ph x="2" /&gt; の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-842">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="276c2-843">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-843">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="276c2-844">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-844">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="276c2-845">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-845">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-846">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-846">Appservice</span></span>

* <span data-ttu-id="276c2-847">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-847">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="276c2-848">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-848">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="276c2-849">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-849">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="276c2-850">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-850">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="276c2-851">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-851">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="276c2-852">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="276c2-852">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="276c2-853">Batch</span><span class="sxs-lookup"><span data-stu-id="276c2-853">Batch</span></span>

* <span data-ttu-id="276c2-854">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-854">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="276c2-855">Batchai</span><span class="sxs-lookup"><span data-stu-id="276c2-855">Batchai</span></span>

* <span data-ttu-id="276c2-856">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-856">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="276c2-857">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-857">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="276c2-858">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-858">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="276c2-859">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-859">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="276c2-860">クラウド</span><span class="sxs-lookup"><span data-stu-id="276c2-860">Cloud</span></span>

* <span data-ttu-id="276c2-861">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-861">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="276c2-862">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-862">Container</span></span>

* <span data-ttu-id="276c2-863">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-863">Added support to open multiple ports</span></span>
* <span data-ttu-id="276c2-864">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-864">Added container group restart policy</span></span>
* <span data-ttu-id="276c2-865">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-865">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="276c2-866">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-866">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="276c2-867">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="276c2-867">Data Lake Analytics</span></span>

* <span data-ttu-id="276c2-868">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-868">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="276c2-869">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="276c2-869">Data Lake Store</span></span>

* <span data-ttu-id="276c2-870">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-870">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="276c2-871">内線番号</span><span class="sxs-lookup"><span data-stu-id="276c2-871">Extension</span></span>

* <span data-ttu-id="276c2-872">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-872">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="276c2-873">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-873">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="276c2-874">IoT</span><span class="sxs-lookup"><span data-stu-id="276c2-874">IoT</span></span>

* <span data-ttu-id="276c2-875">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-875">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="276c2-876">監視</span><span class="sxs-lookup"><span data-stu-id="276c2-876">Monitor</span></span>

* <span data-ttu-id="276c2-877">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-877">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="276c2-878">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-878">Network</span></span>

* <span data-ttu-id="276c2-879">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-879">Added support for CAA DNS records</span></span>
* <span data-ttu-id="276c2-880">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-880">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="276c2-881">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-881">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="276c2-882">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-882">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="276c2-883">Reservations</span><span class="sxs-lookup"><span data-stu-id="276c2-883">Reservations</span></span>

* <span data-ttu-id="276c2-884">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="276c2-884">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-885">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-885">Resource</span></span>

* <span data-ttu-id="276c2-886">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-886">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-887">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-887">SQL</span></span>

* <span data-ttu-id="276c2-888">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-888">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-889">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-889">Storage</span></span>

* <span data-ttu-id="276c2-890">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-890">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="276c2-891">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-891">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="276c2-892">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-892">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="276c2-893">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-893">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="276c2-894">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-894">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="276c2-895">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-895">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="276c2-896">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-896">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-897">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-897">VM</span></span>

* <span data-ttu-id="276c2-898">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-898">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="276c2-899">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-899">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="276c2-900">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-900">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="276c2-901">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-901">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="276c2-902">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-902">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="276c2-903">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="276c2-903">October 24, 2017</span></span>

<span data-ttu-id="276c2-904">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="276c2-904">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="276c2-905">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-905">Core</span></span>

* <span data-ttu-id="276c2-906">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-906">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="276c2-907">ACR</span><span class="sxs-lookup"><span data-stu-id="276c2-907">ACR</span></span>

* <span data-ttu-id="276c2-908">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-908">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="276c2-909">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-909">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="276c2-910">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-910">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-911">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-911">ACS</span></span>

* <span data-ttu-id="276c2-912">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-912">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="276c2-913">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-913">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-914">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-914">Appservice</span></span>

* <span data-ttu-id="276c2-915">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-915">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="276c2-916">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="276c2-916">Component</span></span>

* <span data-ttu-id="276c2-917">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-917">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="276c2-918">監視</span><span class="sxs-lookup"><span data-stu-id="276c2-918">Monitor</span></span>

* <span data-ttu-id="276c2-919">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-919">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-920">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-920">Resource</span></span>

* <span data-ttu-id="276c2-921">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-921">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="276c2-922">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-922">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-923">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-923">VM</span></span>

* <span data-ttu-id="276c2-924">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-924">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="276c2-925">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="276c2-925">October 9, 2017</span></span>

<span data-ttu-id="276c2-926">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="276c2-926">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="276c2-927">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-927">Core</span></span>

* <span data-ttu-id="276c2-928">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-928">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-929">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-929">Appservice</span></span>

* <span data-ttu-id="276c2-930">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-930">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="276c2-931">Batch</span><span class="sxs-lookup"><span data-stu-id="276c2-931">Batch</span></span>

* <span data-ttu-id="276c2-932">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-932">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="276c2-933">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-933">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="276c2-934">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-934">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="276c2-935">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-935">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="276c2-936">Batchai</span><span class="sxs-lookup"><span data-stu-id="276c2-936">Batchai</span></span>

* <span data-ttu-id="276c2-937">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="276c2-937">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="276c2-938">KeyVault</span><span class="sxs-lookup"><span data-stu-id="276c2-938">Keyvault</span></span>

* <span data-ttu-id="276c2-939">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-939">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="276c2-940">(#4448)</span><span class="sxs-lookup"><span data-stu-id="276c2-940">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="276c2-941">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-941">Network</span></span>

* <span data-ttu-id="276c2-942">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-942">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="276c2-943">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-943">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-944">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-944">Resource</span></span>

* <span data-ttu-id="276c2-945">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-945">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="276c2-946">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-946">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="276c2-947">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-947">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="276c2-948">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-948">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-949">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-949">Sql</span></span>

* <span data-ttu-id="276c2-950">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-950">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="276c2-951">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="276c2-951">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="276c2-952">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="276c2-952">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-953">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-953">Storage</span></span>

* <span data-ttu-id="276c2-954">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-954">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-955">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-955">Vm</span></span>

* <span data-ttu-id="276c2-956">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-956">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="276c2-957">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-957">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="276c2-958">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-958">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="276c2-959">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-959">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="276c2-960">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-960">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="276c2-961">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="276c2-961">September 22, 2017</span></span>

<span data-ttu-id="276c2-962">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="276c2-962">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-963">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-963">Resource</span></span>

* <span data-ttu-id="276c2-964">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-964">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="276c2-965">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-965">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="276c2-966">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-966">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="276c2-967">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-967">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="276c2-968">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-968">Network</span></span>

* <span data-ttu-id="276c2-969">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-969">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="276c2-970">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-970">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="276c2-971">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-971">Added `asg` application security group commands</span></span>
* <span data-ttu-id="276c2-972">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-972">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="276c2-973">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-973">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="276c2-974">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-974">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="276c2-975">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-975">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-976">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-976">Storage</span></span>

* <span data-ttu-id="276c2-977">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-977">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="276c2-978">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="276c2-978">Eventgrid</span></span>

* <span data-ttu-id="276c2-979">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-979">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-980">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-980">SQL</span></span>

* <span data-ttu-id="276c2-981">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-981">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="276c2-982">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="276c2-982">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="276c2-983">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-983">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="276c2-984">KeyVault</span><span class="sxs-lookup"><span data-stu-id="276c2-984">Keyvault</span></span>

* <span data-ttu-id="276c2-985">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-985">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-986">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-986">VM</span></span>

* <span data-ttu-id="276c2-987">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-987">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="276c2-988">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-988">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="276c2-989">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-989">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="276c2-990">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-990">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="276c2-991">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-991">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="276c2-992">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-992">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-993">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-993">ACS</span></span>

* <span data-ttu-id="276c2-994">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-994">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-995">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-995">Appservice</span></span>

* <span data-ttu-id="276c2-996">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-996">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="276c2-997">Backup</span><span class="sxs-lookup"><span data-stu-id="276c2-997">Backup</span></span>

* <span data-ttu-id="276c2-998">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="276c2-998">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="276c2-999">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="276c2-999">September 11, 2017</span></span>

<span data-ttu-id="276c2-1000">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="276c2-1000">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="276c2-1001">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-1001">Core</span></span>

* <span data-ttu-id="276c2-1002">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1002">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="276c2-1003">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1003">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-1004">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-1004">Acs</span></span>

* <span data-ttu-id="276c2-1005">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1005">Added `acs list-locations` command</span></span>
* <span data-ttu-id="276c2-1006">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1006">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-1007">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-1007">Appservice</span></span>

* <span data-ttu-id="276c2-1008">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1008">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="276c2-1009">CDN</span><span class="sxs-lookup"><span data-stu-id="276c2-1009">CDN</span></span>

* <span data-ttu-id="276c2-1010">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1010">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="276c2-1011">内線番号</span><span class="sxs-lookup"><span data-stu-id="276c2-1011">Extension</span></span>

* <span data-ttu-id="276c2-1012">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="276c2-1012">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="276c2-1013">KeyVault</span><span class="sxs-lookup"><span data-stu-id="276c2-1013">Keyvault</span></span>

* <span data-ttu-id="276c2-1014">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1014">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="276c2-1015">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-1015">Network</span></span>

* <span data-ttu-id="276c2-1016">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1016">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="276c2-1017">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1017">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="276c2-1018">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1018">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="276c2-1019">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1019">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="276c2-1020">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1020">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-1021">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-1021">Resource</span></span>

* <span data-ttu-id="276c2-1022">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="276c2-1022">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="276c2-1023">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="276c2-1023">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="276c2-1024">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="276c2-1024">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="276c2-1025">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1025">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-1026">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-1026">SQL</span></span>

* <span data-ttu-id="276c2-1027">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1027">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-1028">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-1028">VM</span></span>

* <span data-ttu-id="276c2-1029">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="276c2-1029">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="276c2-1030">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="276c2-1030">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="276c2-1031">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1031">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="276c2-1032">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="276c2-1032">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="276c2-1033">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="276c2-1033">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="276c2-1034">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="276c2-1034">August 31, 2017</span></span>

<span data-ttu-id="276c2-1035">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="276c2-1035">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="276c2-1036">KeyVault</span><span class="sxs-lookup"><span data-stu-id="276c2-1036">Keyvault</span></span>

* <span data-ttu-id="276c2-1037">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1037">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="276c2-1038">SF</span><span class="sxs-lookup"><span data-stu-id="276c2-1038">Sf</span></span>

* <span data-ttu-id="276c2-1039">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="276c2-1039">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-1040">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-1040">Storage</span></span>

* <span data-ttu-id="276c2-1041">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1041">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="276c2-1042">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="276c2-1042">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="276c2-1043">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="276c2-1043">August 28, 2017</span></span>

<span data-ttu-id="276c2-1044">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="276c2-1044">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="276c2-1045">CLI</span><span class="sxs-lookup"><span data-stu-id="276c2-1045">CLI</span></span>

* <span data-ttu-id="276c2-1046">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1046">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-1047">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-1047">ACS</span></span>

* <span data-ttu-id="276c2-1048">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1048">Corrected preview regions</span></span>
* <span data-ttu-id="276c2-1049">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1049">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="276c2-1050">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1050">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-1051">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-1051">Appservice</span></span>

* <span data-ttu-id="276c2-1052">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1052">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="276c2-1053">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1053">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="276c2-1054">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1054">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="276c2-1055">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1055">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="276c2-1056">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="276c2-1056">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="276c2-1057">IoT</span><span class="sxs-lookup"><span data-stu-id="276c2-1057">IoT</span></span>

* <span data-ttu-id="276c2-1058">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1058">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="276c2-1059">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-1059">Network</span></span>

* <span data-ttu-id="276c2-1060">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1060">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="276c2-1061">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1061">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="276c2-1062">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1062">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="276c2-1063">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1063">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="276c2-1064">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1064">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="276c2-1065">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-1065">Profile</span></span>

* <span data-ttu-id="276c2-1066">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1066">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="276c2-1067">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="276c2-1067">Service Fabric</span></span>

* <span data-ttu-id="276c2-1068">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="276c2-1068">Preview release</span></span>
* <span data-ttu-id="276c2-1069">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1069">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="276c2-1070">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1070">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="276c2-1071">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1071">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-1072">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-1072">Storage</span></span>

* <span data-ttu-id="276c2-1073">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1073">Enabled setting blob tier</span></span>
* <span data-ttu-id="276c2-1074">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1074">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="276c2-1075">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1075">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="276c2-1076">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1076">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="276c2-1077">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1077">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="276c2-1078">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="276c2-1078">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-1079">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-1079">VM</span></span>

* <span data-ttu-id="276c2-1080">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1080">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="276c2-1081">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-1081">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="276c2-1082">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1082">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="276c2-1083">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1083">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="276c2-1084">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1084">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="276c2-1085">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1085">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="276c2-1086">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="276c2-1086">August 15, 2017</span></span>

<span data-ttu-id="276c2-1087">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="276c2-1087">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-1088">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-1088">ACS</span></span>

* <span data-ttu-id="276c2-1089">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1089">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-1090">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-1090">Appservice</span></span>

* <span data-ttu-id="276c2-1091">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1091">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="276c2-1092">Event Grid</span><span class="sxs-lookup"><span data-stu-id="276c2-1092">Event Grid</span></span>

* <span data-ttu-id="276c2-1093">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1093">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="276c2-1094">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="276c2-1094">August 11, 2017</span></span>

<span data-ttu-id="276c2-1095">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="276c2-1095">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-1096">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-1096">ACS</span></span>

* <span data-ttu-id="276c2-1097">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1097">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="276c2-1098">Batch</span><span class="sxs-lookup"><span data-stu-id="276c2-1098">Batch</span></span>

* <span data-ttu-id="276c2-1099">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1099">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="276c2-1100">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1100">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="276c2-1101">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1101">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="276c2-1102">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1102">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="276c2-1103">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1103">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="276c2-1104">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1104">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="276c2-1105">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="276c2-1105">Component</span></span>

* <span data-ttu-id="276c2-1106">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1106">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="276c2-1107">コンテナー</span><span class="sxs-lookup"><span data-stu-id="276c2-1107">Container</span></span>

* <span data-ttu-id="276c2-1108">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1108">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="276c2-1109">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="276c2-1109">Data Lake Store</span></span>

* <span data-ttu-id="276c2-1110">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1110">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="276c2-1111">Event Grid</span><span class="sxs-lookup"><span data-stu-id="276c2-1111">Event Grid</span></span>

* <span data-ttu-id="276c2-1112">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="276c2-1112">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="276c2-1113">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-1113">Network</span></span>

* <span data-ttu-id="276c2-1114">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1114">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="276c2-1115">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1115">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="276c2-1116">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1116">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="276c2-1117">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1117">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="276c2-1118">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-1118">Profile</span></span>

* <span data-ttu-id="276c2-1119">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1119">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-1120">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-1120">Storage</span></span>

* <span data-ttu-id="276c2-1121">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="276c2-1121">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-1122">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-1122">VM</span></span>

* <span data-ttu-id="276c2-1123">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1123">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="276c2-1124">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1124">Exposed `list-skus` command</span></span>
* <span data-ttu-id="276c2-1125">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1125">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="276c2-1126">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="276c2-1126">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="276c2-1127">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1127">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="276c2-1128">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="276c2-1128">July 28, 2017</span></span>

<span data-ttu-id="276c2-1129">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="276c2-1129">Version 2.0.12</span></span>

* <span data-ttu-id="276c2-1130">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1130">Added container commands</span></span>
* <span data-ttu-id="276c2-1131">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1131">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="276c2-1132">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-1132">Core</span></span>

* <span data-ttu-id="276c2-1133">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="276c2-1133">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="276c2-1134">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1134">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="276c2-1135">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="276c2-1135">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="276c2-1136">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="276c2-1136">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="276c2-1137">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="276c2-1137">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="276c2-1138">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="276c2-1138">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="276c2-1139">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="276c2-1139">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="276c2-1140">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="276c2-1140">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="276c2-1141">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="276c2-1141">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="276c2-1142">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="276c2-1142">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="276c2-1143">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="276c2-1143">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="276c2-1144">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="276c2-1144">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="276c2-1145">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1145">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="276c2-1146">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1146">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="276c2-1147">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1147">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="276c2-1148">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="276c2-1148">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="276c2-1149">ACR</span><span class="sxs-lookup"><span data-stu-id="276c2-1149">ACR</span></span>

* <span data-ttu-id="276c2-1150">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1150">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="276c2-1151">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1151">Support SKU update for managed registries</span></span>
* <span data-ttu-id="276c2-1152">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1152">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="276c2-1153">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1153">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="276c2-1154">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1154">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="276c2-1155">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1155">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-1156">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-1156">ACS</span></span>

* <span data-ttu-id="276c2-1157">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1157">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-1158">Appservice</span><span class="sxs-lookup"><span data-stu-id="276c2-1158">Appservice</span></span>

* <span data-ttu-id="276c2-1159">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1159">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="276c2-1160">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1160">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="276c2-1161">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="276c2-1161">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="276c2-1162">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="276c2-1162">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="276c2-1163">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="276c2-1163">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="276c2-1164">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="276c2-1164">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="276c2-1165">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="276c2-1165">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="276c2-1166">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="276c2-1166">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="276c2-1167">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-1167">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="276c2-1168">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="276c2-1168">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="276c2-1169">Batch</span><span class="sxs-lookup"><span data-stu-id="276c2-1169">Batch</span></span>

* <span data-ttu-id="276c2-1170">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1170">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="276c2-1171">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1171">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="276c2-1172">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1172">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="276c2-1173">CDN</span><span class="sxs-lookup"><span data-stu-id="276c2-1173">CDN</span></span>

* <span data-ttu-id="276c2-1174">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1174">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="276c2-1175">クラウド</span><span class="sxs-lookup"><span data-stu-id="276c2-1175">Cloud</span></span>

* <span data-ttu-id="276c2-1176">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1176">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="276c2-1177">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="276c2-1177">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="276c2-1178">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1178">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="276c2-1179">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1179">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="276c2-1180">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1180">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="276c2-1181">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="276c2-1181">CosmosDB</span></span>

* <span data-ttu-id="276c2-1182">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1182">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="276c2-1183">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1183">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="276c2-1184">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="276c2-1184">Data Lake Analytics</span></span>

* <span data-ttu-id="276c2-1185">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1185">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="276c2-1186">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1186">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="276c2-1187">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1187">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="276c2-1188">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="276c2-1188">Data Lake Store</span></span>

* <span data-ttu-id="276c2-1189">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1189">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="276c2-1190">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1190">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="276c2-1191">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-1191">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="276c2-1192">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="276c2-1192">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="276c2-1193">対話</span><span class="sxs-lookup"><span data-stu-id="276c2-1193">Interactive</span></span>

* <span data-ttu-id="276c2-1194">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1194">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="276c2-1195">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="276c2-1195">Increased test coverage</span></span>
* <span data-ttu-id="276c2-1196">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1196">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="276c2-1197">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="276c2-1197">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="276c2-1198">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="276c2-1198">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="276c2-1199">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="276c2-1199">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="276c2-1200">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="276c2-1200">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="276c2-1201">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1201">Added `--progress` flag</span></span>
* <span data-ttu-id="276c2-1202">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1202">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="276c2-1203">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="276c2-1203">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="276c2-1204">IoT</span><span class="sxs-lookup"><span data-stu-id="276c2-1204">IoT</span></span>

* <span data-ttu-id="276c2-1205">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-1205">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="276c2-1206">(#3934)</span><span class="sxs-lookup"><span data-stu-id="276c2-1206">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="276c2-1207">Key Vault</span><span class="sxs-lookup"><span data-stu-id="276c2-1207">Key vault</span></span>

* <span data-ttu-id="276c2-1208">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-1208">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="276c2-1209">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="276c2-1209">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="276c2-1210">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="276c2-1210">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="276c2-1211">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="276c2-1211">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="276c2-1212">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="276c2-1212">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="276c2-1213">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="276c2-1213">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="276c2-1214">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-1214">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="276c2-1215">(#3307)</span><span class="sxs-lookup"><span data-stu-id="276c2-1215">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="276c2-1216">ラボ</span><span class="sxs-lookup"><span data-stu-id="276c2-1216">Lab</span></span>

* <span data-ttu-id="276c2-1217">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1217">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="276c2-1218">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1218">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="276c2-1219">監視</span><span class="sxs-lookup"><span data-stu-id="276c2-1219">Monitor</span></span>

* <span data-ttu-id="276c2-1220">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="276c2-1220">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="276c2-1221">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1221">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="276c2-1222">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1222">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="276c2-1223">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1223">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="276c2-1224">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1224">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="276c2-1225">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="276c2-1225">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="276c2-1226">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1226">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="276c2-1227">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="276c2-1227">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="276c2-1228">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1228">`location` no longer required</span></span>
  * <span data-ttu-id="276c2-1229">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="276c2-1229">Add name and ID support for target</span></span>
  * <span data-ttu-id="276c2-1230">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="276c2-1230">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="276c2-1231">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1231">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="276c2-1232">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1232">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="276c2-1233">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="276c2-1233">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="276c2-1234">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1234">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="276c2-1235">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1235">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="276c2-1236">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-1236">Network</span></span>

* <span data-ttu-id="276c2-1237">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1237">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="276c2-1238">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1238">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="276c2-1239">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1239">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="276c2-1240">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1240">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="276c2-1241">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1241">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="276c2-1242">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1242">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="276c2-1243">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1243">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="276c2-1244">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1244">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="276c2-1245">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1245">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="276c2-1246">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1246">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="276c2-1247">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1247">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="276c2-1248">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1248">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="276c2-1249">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1249">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="276c2-1250">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1250">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="276c2-1251">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1251">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="276c2-1252">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1252">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="276c2-1253">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1253">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="276c2-1254">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1254">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="276c2-1255">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1255">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="276c2-1256">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1256">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="276c2-1257">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1257">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="276c2-1258">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1258">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="276c2-1259">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1259">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="276c2-1260">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="276c2-1260">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="276c2-1261">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="276c2-1261">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="276c2-1262">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="276c2-1262">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="276c2-1263">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="276c2-1263">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="276c2-1264">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-1264">Profile</span></span>

* <span data-ttu-id="276c2-1265">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1265">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="276c2-1266">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1266">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="276c2-1267">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="276c2-1267">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="276c2-1268">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1268">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="276c2-1269">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1269">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="276c2-1270">RDBMS</span><span class="sxs-lookup"><span data-stu-id="276c2-1270">RDBMS</span></span>

* <span data-ttu-id="276c2-1271">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="276c2-1271">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="276c2-1272">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="276c2-1272">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="276c2-1273">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="276c2-1273">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="276c2-1274">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="276c2-1274">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-1275">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-1275">Resource</span></span>

* <span data-ttu-id="276c2-1276">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1276">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="276c2-1277">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1277">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="276c2-1278">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1278">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="276c2-1279">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1279">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="276c2-1280">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="276c2-1280">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="276c2-1281">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1281">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="276c2-1282">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="276c2-1282">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="276c2-1283">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1283">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="276c2-1284">役割</span><span class="sxs-lookup"><span data-stu-id="276c2-1284">Role</span></span>

* <span data-ttu-id="276c2-1285">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1285">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="276c2-1286">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="276c2-1286">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="276c2-1287">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="276c2-1287">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="276c2-1288">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="276c2-1288">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="276c2-1289">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1289">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="276c2-1290">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="276c2-1290">Service Fabric</span></span>
* <span data-ttu-id="276c2-1291">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="276c2-1291">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="276c2-1292">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="276c2-1292">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="276c2-1293">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="276c2-1293">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-1294">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-1294">SQL</span></span>

* <span data-ttu-id="276c2-1295">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1295">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="276c2-1296">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1296">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="276c2-1297">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1297">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-1298">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-1298">Storage</span></span>

* <span data-ttu-id="276c2-1299">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="276c2-1299">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="276c2-1300">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1300">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="276c2-1301">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="276c2-1301">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="276c2-1302">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="276c2-1302">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="276c2-1303">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="276c2-1303">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="276c2-1304">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="276c2-1304">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-1305">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-1305">VM</span></span>

* <span data-ttu-id="276c2-1306">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1306">Support configuring nsg</span></span>
* <span data-ttu-id="276c2-1307">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1307">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="276c2-1308">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="276c2-1308">Support managed service identities</span></span>
* <span data-ttu-id="276c2-1309">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1309">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="276c2-1310">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="276c2-1310">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="276c2-1311">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="276c2-1311">May 10, 2017</span></span>

<span data-ttu-id="276c2-1312">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="276c2-1312">Version 2.0.6</span></span>

* <span data-ttu-id="276c2-1313">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1313">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="276c2-1314">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1314">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="276c2-1315">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1315">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="276c2-1316">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1316">Include Cognitive Services module</span></span>
* <span data-ttu-id="276c2-1317">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1317">Include Service Fabric module</span></span>
* <span data-ttu-id="276c2-1318">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="276c2-1318">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="276c2-1319">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1319">Add support for CDN commands</span></span>
* <span data-ttu-id="276c2-1320">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1320">Remove Container module</span></span>
* <span data-ttu-id="276c2-1321">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="276c2-1321">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="276c2-1322">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="276c2-1322">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="276c2-1323">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-1323">Core</span></span>

* <span data-ttu-id="276c2-1324">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="276c2-1324">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="276c2-1325">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="276c2-1325">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="276c2-1326">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="276c2-1326">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="276c2-1327">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="276c2-1327">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="276c2-1328">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="276c2-1328">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="276c2-1329">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="276c2-1329">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="276c2-1330">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="276c2-1330">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="276c2-1331">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="276c2-1331">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="276c2-1332">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="276c2-1332">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="276c2-1333">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="276c2-1333">core: Improved performance</span></span>
* <span data-ttu-id="276c2-1334">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="276c2-1334">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="276c2-1335">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="276c2-1335">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-1336">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-1336">ACS</span></span>

* <span data-ttu-id="276c2-1337">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1337">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="276c2-1338">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1338">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="276c2-1339">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1339">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="276c2-1340">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="276c2-1340">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-1341">AppService</span><span class="sxs-lookup"><span data-stu-id="276c2-1341">AppService</span></span>

* <span data-ttu-id="276c2-1342">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1342">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="276c2-1343">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1343">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="276c2-1344">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="276c2-1344">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="276c2-1345">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1345">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="276c2-1346">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1346">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="276c2-1347">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="276c2-1347">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="276c2-1348">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="276c2-1348">support slot swap with preview</span></span>
* <span data-ttu-id="276c2-1349">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="276c2-1349">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="276c2-1350">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="276c2-1350">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="276c2-1351">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="276c2-1351">CosmosDB</span></span>

* <span data-ttu-id="276c2-1352">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1352">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="276c2-1353">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1353">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="276c2-1354">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1354">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="276c2-1355">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1355">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="276c2-1356">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="276c2-1356">Data Lake Analytics</span></span>

* <span data-ttu-id="276c2-1357">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1357">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="276c2-1358">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="276c2-1358">Add support for new catalog item type: package.</span></span> <span data-ttu-id="276c2-1359">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="276c2-1359">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="276c2-1360">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="276c2-1360">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="276c2-1361">テーブル</span><span class="sxs-lookup"><span data-stu-id="276c2-1361">Table</span></span>
  * <span data-ttu-id="276c2-1362">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="276c2-1362">Table valued function</span></span>
  * <span data-ttu-id="276c2-1363">表示</span><span class="sxs-lookup"><span data-stu-id="276c2-1363">View</span></span>
  * <span data-ttu-id="276c2-1364">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="276c2-1364">Table Statistics.</span></span> <span data-ttu-id="276c2-1365">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="276c2-1365">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="276c2-1366">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="276c2-1366">Data Lake Store</span></span>

* <span data-ttu-id="276c2-1367">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1367">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="276c2-1368">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="276c2-1368">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="276c2-1369">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="276c2-1369">missed help for access show.</span></span> <span data-ttu-id="276c2-1370">追加しました </span><span class="sxs-lookup"><span data-stu-id="276c2-1370">adding it.</span></span> <span data-ttu-id="276c2-1371">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="276c2-1371">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="276c2-1372">検索</span><span class="sxs-lookup"><span data-stu-id="276c2-1372">Find</span></span>

* <span data-ttu-id="276c2-1373">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1373">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="276c2-1374">KeyVault</span><span class="sxs-lookup"><span data-stu-id="276c2-1374">KeyVault</span></span>

* <span data-ttu-id="276c2-1375">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1375">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="276c2-1376">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1376">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="276c2-1377">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="276c2-1377">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="276c2-1378">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1378">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="276c2-1379">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="276c2-1379">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="276c2-1380">ラボ</span><span class="sxs-lookup"><span data-stu-id="276c2-1380">Lab</span></span>

* <span data-ttu-id="276c2-1381">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1381">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="276c2-1382">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1382">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="276c2-1383">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1383">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="276c2-1384">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1384">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="276c2-1385">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1385">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="276c2-1386">監視</span><span class="sxs-lookup"><span data-stu-id="276c2-1386">Monitor</span></span>

* <span data-ttu-id="276c2-1387">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="276c2-1387">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="276c2-1388">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="276c2-1388">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="276c2-1389">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-1389">Network</span></span>

* <span data-ttu-id="276c2-1390">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1390">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="276c2-1391">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1391">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="276c2-1392">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1392">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="276c2-1393">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1393">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="276c2-1394">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1394">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="276c2-1395">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1395">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="276c2-1396">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1396">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="276c2-1397">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1397">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="276c2-1398">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1398">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="276c2-1399">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1399">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="276c2-1400">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1400">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="276c2-1401">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1401">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="276c2-1402">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1402">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="276c2-1403">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1403">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="276c2-1404">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="276c2-1404">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="276c2-1405">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1405">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="276c2-1406">プロファイル</span><span class="sxs-lookup"><span data-stu-id="276c2-1406">Profile</span></span>

* <span data-ttu-id="276c2-1407">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="276c2-1407">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="276c2-1408">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="276c2-1408">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="276c2-1409">Redis</span><span class="sxs-lookup"><span data-stu-id="276c2-1409">Redis</span></span>

* <span data-ttu-id="276c2-1410">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1410">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="276c2-1411">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1411">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="276c2-1412">リソース</span><span class="sxs-lookup"><span data-stu-id="276c2-1412">Resource</span></span>

* <span data-ttu-id="276c2-1413">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="276c2-1413">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="276c2-1414">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="276c2-1414">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="276c2-1415">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="276c2-1415">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="276c2-1416">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="276c2-1416">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="276c2-1417">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="276c2-1417">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="276c2-1418">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="276c2-1418">Add docs for az lock update.</span></span> <span data-ttu-id="276c2-1419">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="276c2-1419">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="276c2-1420">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="276c2-1420">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="276c2-1421">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="276c2-1421">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="276c2-1422">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="276c2-1422">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="276c2-1423">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="276c2-1423">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="276c2-1424">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="276c2-1424">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="276c2-1425">役割</span><span class="sxs-lookup"><span data-stu-id="276c2-1425">Role</span></span>

* <span data-ttu-id="276c2-1426">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="276c2-1426">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="276c2-1427">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="276c2-1427">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="276c2-1428">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="276c2-1428">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="276c2-1429">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="276c2-1429">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="276c2-1430">SQL</span><span class="sxs-lookup"><span data-stu-id="276c2-1430">SQL</span></span>

* <span data-ttu-id="276c2-1431">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="276c2-1431">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="276c2-1432">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="276c2-1432">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="276c2-1433">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-1433">Storage</span></span>

* <span data-ttu-id="276c2-1434">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="276c2-1434">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="276c2-1435">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1435">Add support for incremental blob copy</span></span>
* <span data-ttu-id="276c2-1436">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1436">Add support for large block blob upload</span></span>
* <span data-ttu-id="276c2-1437">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="276c2-1437">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-1438">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-1438">VM</span></span>

* <span data-ttu-id="276c2-1439">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="276c2-1439">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="276c2-1440">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="276c2-1440">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="276c2-1441">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="276c2-1441">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="276c2-1442">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="276c2-1442">az vm/vmss disk</span></span>
  3. <span data-ttu-id="276c2-1443">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="276c2-1443">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="276c2-1444">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="276c2-1444">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="276c2-1445">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="276c2-1445">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="276c2-1446">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="276c2-1446">April 3, 2017</span></span>

<span data-ttu-id="276c2-1447">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="276c2-1447">Version 2.0.2</span></span>

<span data-ttu-id="276c2-1448">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="276c2-1448">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="276c2-1449">コア</span><span class="sxs-lookup"><span data-stu-id="276c2-1449">Core</span></span>

* <span data-ttu-id="276c2-1450">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="276c2-1450">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="276c2-1451">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="276c2-1451">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="276c2-1452">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="276c2-1452">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="276c2-1453">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="276c2-1453">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="276c2-1454">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="276c2-1454">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="276c2-1455">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="276c2-1455">Add prompting for missing template parameters.</span></span> <span data-ttu-id="276c2-1456">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="276c2-1456">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="276c2-1457">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="276c2-1457">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="276c2-1458">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="276c2-1458">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="276c2-1459">ACS</span><span class="sxs-lookup"><span data-stu-id="276c2-1459">ACS</span></span>

* <span data-ttu-id="276c2-1460">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="276c2-1460">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="276c2-1461">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="276c2-1461">Add support for ssh key password prompting.</span></span> <span data-ttu-id="276c2-1462">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="276c2-1462">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="276c2-1463">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="276c2-1463">Add support for windows clusters.</span></span> <span data-ttu-id="276c2-1464">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="276c2-1464">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="276c2-1465">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="276c2-1465">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="276c2-1466">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="276c2-1466">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="276c2-1467">AppService</span><span class="sxs-lookup"><span data-stu-id="276c2-1467">AppService</span></span>

* <span data-ttu-id="276c2-1468">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="276c2-1468">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="276c2-1469">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="276c2-1469">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="276c2-1470">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="276c2-1470">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="276c2-1471">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="276c2-1471">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="276c2-1472">DataLake</span><span class="sxs-lookup"><span data-stu-id="276c2-1472">DataLake</span></span>

* <span data-ttu-id="276c2-1473">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="276c2-1473">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="276c2-1474">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="276c2-1474">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="276c2-1475">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="276c2-1475">DocuemntDB</span></span>

* <span data-ttu-id="276c2-1476">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="276c2-1476">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="276c2-1477">VM</span><span class="sxs-lookup"><span data-stu-id="276c2-1477">VM</span></span>

* <span data-ttu-id="276c2-1478">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="276c2-1478">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="276c2-1479">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="276c2-1479">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="276c2-1480">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="276c2-1480">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="276c2-1481">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="276c2-1481">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="276c2-1482">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="276c2-1482">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="276c2-1483">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="276c2-1483">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="276c2-1484">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="276c2-1484">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="276c2-1485">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="276c2-1485">February 27, 2017</span></span>

<span data-ttu-id="276c2-1486">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="276c2-1486">Version 2.0.0</span></span>

<span data-ttu-id="276c2-1487">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="276c2-1487">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="276c2-1488">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="276c2-1488">Container Service (acs)</span></span>
- <span data-ttu-id="276c2-1489">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="276c2-1489">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="276c2-1490">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="276c2-1490">Networking</span></span>
- <span data-ttu-id="276c2-1491">Storage</span><span class="sxs-lookup"><span data-stu-id="276c2-1491">Storage</span></span>

<span data-ttu-id="276c2-1492">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="276c2-1492">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="276c2-1493">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="276c2-1493">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="276c2-1494">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="276c2-1494">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="276c2-1495">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="276c2-1495">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="276c2-1496">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="276c2-1496">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="276c2-1497">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="276c2-1497">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="276c2-1498">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="276c2-1498">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="276c2-1499">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="276c2-1499">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="276c2-1500">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="276c2-1500">Provide feedback from the command line with the `az feedback` command</span></span>

