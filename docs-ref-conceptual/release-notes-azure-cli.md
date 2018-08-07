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
ms.openlocfilehash: d0f8c01495cc95ecfbf6a41d510eb4bc54d47ba2
ms.sourcegitcommit: 8019690502e9f89c083839d83a0a245cc812e8b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2018
ms.locfileid: "39392355"
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="33f62-103">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="33f62-103">Azure CLI 2.0 release notes</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="33f62-104">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="33f62-104">July 31, 2018</span></span>

<span data-ttu-id="33f62-105">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="33f62-105">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-106">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-106">ACR</span></span>

* <span data-ttu-id="33f62-107">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-107">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="33f62-108">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-108">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-109">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-109">ACS</span></span>

* <span data-ttu-id="33f62-110">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-110">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="33f62-111">Batch</span><span class="sxs-lookup"><span data-stu-id="33f62-111">Batch</span></span>

* <span data-ttu-id="33f62-112">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-112">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="33f62-113">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-113">Container</span></span>

* <span data-ttu-id="33f62-114">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-114">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="33f62-115">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-115">Network</span></span>

* <span data-ttu-id="33f62-116">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-116">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="33f62-117">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-117">Resource</span></span>

* <span data-ttu-id="33f62-118">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-118">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="33f62-119">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-119">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="33f62-120">Role</span><span class="sxs-lookup"><span data-stu-id="33f62-120">Role</span></span>

* <span data-ttu-id="33f62-121">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-121">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="33f62-122">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-122">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="33f62-123">Search</span><span class="sxs-lookup"><span data-stu-id="33f62-123">Search</span></span>

* <span data-ttu-id="33f62-124">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-124">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="33f62-125">Service Bus</span><span class="sxs-lookup"><span data-stu-id="33f62-125">Service Bus</span></span>

* <span data-ttu-id="33f62-126">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-126">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="33f62-127">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-127">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="33f62-128">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="33f62-128">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="33f62-129">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="33f62-129">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-130">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-130">Storage</span></span>

* <span data-ttu-id="33f62-131">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-131">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="33f62-132">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="33f62-132">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-133">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-133">VM</span></span>

* <span data-ttu-id="33f62-134">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-134">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="33f62-135">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-135">Added support for support `StandardSSD_LRS`</span></span>
* <span data-ttu-id="33f62-136">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-136">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="33f62-137">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-137">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="33f62-138">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="33f62-138">July 18, 2018</span></span>

<span data-ttu-id="33f62-139">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="33f62-139">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="33f62-140">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-140">Core</span></span>

* <span data-ttu-id="33f62-141">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-141">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="33f62-142">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-142">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="33f62-143">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-143">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-144">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-144">ACR</span></span>

* <span data-ttu-id="33f62-145">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-145">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="33f62-146">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-146">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="33f62-147">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-147">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="33f62-148">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-148">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-149">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-149">ACS</span></span>

* <span data-ttu-id="33f62-150">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-150">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-151">AppService</span><span class="sxs-lookup"><span data-stu-id="33f62-151">AppService</span></span>

* <span data-ttu-id="33f62-152">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-152">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="33f62-153">Batch</span><span class="sxs-lookup"><span data-stu-id="33f62-153">Batch</span></span>

* <span data-ttu-id="33f62-154">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-154">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="33f62-155">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-155">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="33f62-156">Batch AI</span><span class="sxs-lookup"><span data-stu-id="33f62-156">Batch AI</span></span>

* <span data-ttu-id="33f62-157">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-157">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="33f62-158">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-158">Container</span></span>

* <span data-ttu-id="33f62-159">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-159">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="33f62-160">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-160">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="33f62-161">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-161">Network</span></span>

* <span data-ttu-id="33f62-162">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-162">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="33f62-163">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-163">Added `network nic wait`</span></span>
* <span data-ttu-id="33f62-164">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-164">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="33f62-165">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-165">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="33f62-166">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-166">Resource</span></span>

* <span data-ttu-id="33f62-167">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-167">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="33f62-168">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-168">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="33f62-169">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-169">Added `deployment wait` command</span></span>
* <span data-ttu-id="33f62-170">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-170">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-171">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-171">SQL</span></span>

* <span data-ttu-id="33f62-172">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-172">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="33f62-173">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-173">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="33f62-174">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="33f62-174">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-175">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-175">Storage</span></span>

* <span data-ttu-id="33f62-176">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-176">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-177">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-177">VM</span></span>

* <span data-ttu-id="33f62-178">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-178">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="33f62-179">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-179">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="33f62-180">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-180">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="33f62-181">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="33f62-181">July 3, 2018</span></span>

<span data-ttu-id="33f62-182">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="33f62-182">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="33f62-183">AKS</span><span class="sxs-lookup"><span data-stu-id="33f62-183">AKS</span></span>

* <span data-ttu-id="33f62-184">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-184">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="33f62-185">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="33f62-185">July 3, 2018</span></span>

<span data-ttu-id="33f62-186">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="33f62-186">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="33f62-187">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-187">Core</span></span>

* <span data-ttu-id="33f62-188">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-188">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-189">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-189">ACR</span></span>

* <span data-ttu-id="33f62-190">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-190">Added polling build status</span></span>
* <span data-ttu-id="33f62-191">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-191">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="33f62-192">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-192">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-193">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-193">ACS</span></span>

* <span data-ttu-id="33f62-194">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-194">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="33f62-195">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-195">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="33f62-196">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-196">Updated options for `aks browse` command.</span></span> <span data-ttu-id="33f62-197">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-197">Added `--listen-port` support</span></span>
* <span data-ttu-id="33f62-198">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-198">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="33f62-199">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="33f62-199">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="33f62-200">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-200">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-201">AppService</span><span class="sxs-lookup"><span data-stu-id="33f62-201">AppService</span></span>

* <span data-ttu-id="33f62-202">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-202">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="33f62-203">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-203">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="33f62-204">Backup</span><span class="sxs-lookup"><span data-stu-id="33f62-204">Backup</span></span>

* <span data-ttu-id="33f62-205">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-205">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="33f62-206">BatchAI</span><span class="sxs-lookup"><span data-stu-id="33f62-206">BatchAI</span></span>

* <span data-ttu-id="33f62-207">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-207">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="33f62-208">クラウド</span><span class="sxs-lookup"><span data-stu-id="33f62-208">Cloud</span></span>

* <span data-ttu-id="33f62-209">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-209">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="33f62-210">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-210">Container</span></span>

* <span data-ttu-id="33f62-211">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-211">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="33f62-212">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-212">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="33f62-213">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-213">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="33f62-214">内線番号</span><span class="sxs-lookup"><span data-stu-id="33f62-214">Extension</span></span>

* <span data-ttu-id="33f62-215">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-215">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="33f62-216">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-216">Network</span></span>

* <span data-ttu-id="33f62-217">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-217">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="33f62-218">Rdbms</span><span class="sxs-lookup"><span data-stu-id="33f62-218">Rdbms</span></span>

* <span data-ttu-id="33f62-219">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-219">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-220">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-220">Resource</span></span>

* <span data-ttu-id="33f62-221">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-221">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-222">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-222">VM</span></span>

* <span data-ttu-id="33f62-223">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-223">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="33f62-224">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="33f62-224">June 25, 2018</span></span>

<span data-ttu-id="33f62-225">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="33f62-225">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="33f62-226">CLI</span><span class="sxs-lookup"><span data-stu-id="33f62-226">CLI</span></span>

* <span data-ttu-id="33f62-227">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-227">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="33f62-228">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="33f62-228">June 19, 2018</span></span>

<span data-ttu-id="33f62-229">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="33f62-229">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="33f62-230">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-230">Core</span></span>

* <span data-ttu-id="33f62-231">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-231">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-232">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-232">ACR</span></span>

* <span data-ttu-id="33f62-233">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-233">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="33f62-234">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-234">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-235">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-235">ACS</span></span>

* <span data-ttu-id="33f62-236">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-236">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="33f62-237">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-237">Added `--update` support</span></span>
* <span data-ttu-id="33f62-238">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-238">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="33f62-239">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="33f62-239">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="33f62-240">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-240">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="33f62-241">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-241">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="33f62-242">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-242">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="33f62-243">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-243">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-244">AppService</span><span class="sxs-lookup"><span data-stu-id="33f62-244">AppService</span></span>

* <span data-ttu-id="33f62-245">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-245">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="33f62-246">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-246">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="33f62-247">Batch</span><span class="sxs-lookup"><span data-stu-id="33f62-247">Batch</span></span>

* <span data-ttu-id="33f62-248">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-248">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="33f62-249">Batch AI</span><span class="sxs-lookup"><span data-stu-id="33f62-249">Batch AI</span></span>

* <span data-ttu-id="33f62-250">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-250">Added support for workspaces.</span></span> <span data-ttu-id="33f62-251">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="33f62-251">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="33f62-252">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-252">Added support for experiments.</span></span> <span data-ttu-id="33f62-253">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="33f62-253">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="33f62-254">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-254">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="33f62-255">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-255">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="33f62-256">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="33f62-256">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="33f62-257">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-257">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="33f62-258">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="33f62-258">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="33f62-259">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="33f62-259">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="33f62-260">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-260">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="33f62-261">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="33f62-261">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="33f62-262">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-262">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="33f62-263">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="33f62-263">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="33f62-264">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-264">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="33f62-265">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="33f62-265">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="33f62-266">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-266">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="33f62-267">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-267">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
 - <span data-ttu-id="33f62-268">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-268">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
 - <span data-ttu-id="33f62-269">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-269">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="33f62-270">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-270">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="33f62-271">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-271">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="33f62-272">マップ</span><span class="sxs-lookup"><span data-stu-id="33f62-272">Maps</span></span>

* <span data-ttu-id="33f62-273">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-273">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="33f62-274">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-274">Network</span></span>

* <span data-ttu-id="33f62-275">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="33f62-275">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="33f62-276">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-276">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="33f62-277">#6502</span><span class="sxs-lookup"><span data-stu-id="33f62-277">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="33f62-278">Reservations</span><span class="sxs-lookup"><span data-stu-id="33f62-278">Reservations</span></span>

* <span data-ttu-id="33f62-279">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-279">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="33f62-280">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-280">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="33f62-281">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-281">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="33f62-282">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-282">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="33f62-283">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-283">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="33f62-284">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-284">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="33f62-285">Role</span><span class="sxs-lookup"><span data-stu-id="33f62-285">Role</span></span>

* <span data-ttu-id="33f62-286">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-286">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-287">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-287">SQL</span></span>

* <span data-ttu-id="33f62-288">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-288">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-289">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-289">Storage</span></span>

* <span data-ttu-id="33f62-290">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="33f62-290">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-291">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-291">VM</span></span>

* <span data-ttu-id="33f62-292">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-292">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="33f62-293">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-293">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="33f62-294">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-294">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="33f62-295">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="33f62-295">June 13, 2018</span></span>

<span data-ttu-id="33f62-296">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="33f62-296">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="33f62-297">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-297">Core</span></span>

* <span data-ttu-id="33f62-298">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-298">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="33f62-299">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="33f62-299">June 13, 2018</span></span>

<span data-ttu-id="33f62-300">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="33f62-300">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="33f62-301">AKS</span><span class="sxs-lookup"><span data-stu-id="33f62-301">AKS</span></span>

* <span data-ttu-id="33f62-302">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-302">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="33f62-303">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-303">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="33f62-304">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-304">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="33f62-305">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-305">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="33f62-306">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-306">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-307">AppService</span><span class="sxs-lookup"><span data-stu-id="33f62-307">AppService</span></span>

* <span data-ttu-id="33f62-308">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-308">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="33f62-309">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="33f62-309">June 5, 2018</span></span>

<span data-ttu-id="33f62-310">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="33f62-310">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="33f62-311">Interactive</span><span class="sxs-lookup"><span data-stu-id="33f62-311">Interactive</span></span>

* <span data-ttu-id="33f62-312">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-312">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="33f62-313">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="33f62-313">June 5, 2018</span></span>

<span data-ttu-id="33f62-314">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="33f62-314">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="33f62-315">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-315">Core</span></span>

* <span data-ttu-id="33f62-316">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-316">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="33f62-317">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-317">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-318">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-318">ACR</span></span>

* <span data-ttu-id="33f62-319">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-319">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="33f62-320">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-320">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="33f62-321">AKS</span><span class="sxs-lookup"><span data-stu-id="33f62-321">AKS</span></span>

* <span data-ttu-id="33f62-322">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-322">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="33f62-323">Batch</span><span class="sxs-lookup"><span data-stu-id="33f62-323">Batch</span></span>

* <span data-ttu-id="33f62-324">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-324">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="33f62-325">IoT</span><span class="sxs-lookup"><span data-stu-id="33f62-325">IOT</span></span>

* <span data-ttu-id="33f62-326">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-326">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="33f62-327">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-327">Network</span></span>

* <span data-ttu-id="33f62-328">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-328">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="33f62-329">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="33f62-329">Policy Insights</span></span>

* <span data-ttu-id="33f62-330">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="33f62-330">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="33f62-331">ARM</span><span class="sxs-lookup"><span data-stu-id="33f62-331">ARM</span></span>

* <span data-ttu-id="33f62-332">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-332">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-333">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-333">SQL</span></span>

* <span data-ttu-id="33f62-334">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-334">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="33f62-335">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-335">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="33f62-336">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-336">Storage</span></span>

* <span data-ttu-id="33f62-337">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-337">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-338">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-338">VM</span></span>

* <span data-ttu-id="33f62-339">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-339">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="33f62-340">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-340">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="33f62-341">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-341">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="33f62-342">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="33f62-342">May 22, 2018</span></span>

<span data-ttu-id="33f62-343">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="33f62-343">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="33f62-344">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-344">Core</span></span>

* <span data-ttu-id="33f62-345">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-345">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-346">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-346">ACS</span></span>

* <span data-ttu-id="33f62-347">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-347">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="33f62-348">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-348">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-349">AppService</span><span class="sxs-lookup"><span data-stu-id="33f62-349">AppService</span></span>

* <span data-ttu-id="33f62-350">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-350">Improved generic update commands</span></span>
* <span data-ttu-id="33f62-351">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-351">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="33f62-352">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-352">Container</span></span>

* <span data-ttu-id="33f62-353">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-353">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="33f62-354">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-354">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="33f62-355">内線番号</span><span class="sxs-lookup"><span data-stu-id="33f62-355">Extension</span></span>

* <span data-ttu-id="33f62-356">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-356">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="33f62-357">Interactive</span><span class="sxs-lookup"><span data-stu-id="33f62-357">Interactive</span></span>

* <span data-ttu-id="33f62-358">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-358">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="33f62-359">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-359">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="33f62-360">KeyVault</span><span class="sxs-lookup"><span data-stu-id="33f62-360">KeyVault</span></span>

* <span data-ttu-id="33f62-361">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-361">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="33f62-362">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-362">Network</span></span>

* <span data-ttu-id="33f62-363">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-363">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="33f62-364">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-364">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-365">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-365">SQL</span></span>

* <span data-ttu-id="33f62-366">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-366">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="33f62-367">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-367">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="33f62-368">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-368">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="33f62-369">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-369">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="33f62-370">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-370">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="33f62-371">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="33f62-371">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="33f62-372">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="33f62-372">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="33f62-373">`edition`</span><span class="sxs-lookup"><span data-stu-id="33f62-373">`edition`.</span></span> <span data-ttu-id="33f62-374">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="33f62-374">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="33f62-375">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="33f62-375">`elasticPoolName`.</span></span> <span data-ttu-id="33f62-376">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="33f62-376">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="33f62-377">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-377">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="33f62-378">`edition`</span><span class="sxs-lookup"><span data-stu-id="33f62-378">`edition`.</span></span> <span data-ttu-id="33f62-379">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="33f62-379">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="33f62-380">`dtu`</span><span class="sxs-lookup"><span data-stu-id="33f62-380">`dtu`.</span></span> <span data-ttu-id="33f62-381">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="33f62-381">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="33f62-382">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="33f62-382">`databaseDtuMin`.</span></span> <span data-ttu-id="33f62-383">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="33f62-383">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="33f62-384">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="33f62-384">`databaseDtuMax`.</span></span> <span data-ttu-id="33f62-385">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="33f62-385">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="33f62-386">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-386">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="33f62-387">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-387">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-388">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-388">Storage</span></span>

* <span data-ttu-id="33f62-389">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-389">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="33f62-390">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-390">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-391">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-391">VM</span></span>

* <span data-ttu-id="33f62-392">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-392">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="33f62-393">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="33f62-393">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="33f62-394">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-394">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="33f62-395">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-395">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="33f62-396">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-396">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="33f62-397">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="33f62-397">May 7, 2018</span></span>

<span data-ttu-id="33f62-398">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="33f62-398">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="33f62-399">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-399">Core</span></span>

* <span data-ttu-id="33f62-400">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-400">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="33f62-401">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-401">Added limited support for positional arguments</span></span>
* <span data-ttu-id="33f62-402">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-402">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="33f62-403">#5591</span><span class="sxs-lookup"><span data-stu-id="33f62-403">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="33f62-404">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-404">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="33f62-405">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="33f62-405">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="33f62-406">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-406">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="33f62-407">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-407">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="33f62-408">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-408">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-409">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-409">ACR</span></span>

* <span data-ttu-id="33f62-410">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-410">Added ACR Build commands</span></span>
* <span data-ttu-id="33f62-411">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-411">Improved resource not found error messages</span></span>
* <span data-ttu-id="33f62-412">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-412">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="33f62-413">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-413">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="33f62-414">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-414">Improved repository commands error messages</span></span>
* <span data-ttu-id="33f62-415">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-415">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-416">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-416">ACS</span></span>

* <span data-ttu-id="33f62-417">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-417">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="33f62-418">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-418">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="33f62-419">AMS</span><span class="sxs-lookup"><span data-stu-id="33f62-419">AMS</span></span>

* <span data-ttu-id="33f62-420">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="33f62-420">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-421">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-421">Appservice</span></span>

* <span data-ttu-id="33f62-422">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-422">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="33f62-423">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-423">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="33f62-424">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-424">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="33f62-425">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-425">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="33f62-426">Batch AI</span><span class="sxs-lookup"><span data-stu-id="33f62-426">Batch AI</span></span>

* <span data-ttu-id="33f62-427">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-427">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="33f62-428">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="33f62-428">Cognitive Services</span></span>

* <span data-ttu-id="33f62-429">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-429">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="33f62-430">消費</span><span class="sxs-lookup"><span data-stu-id="33f62-430">Consumption</span></span>

* <span data-ttu-id="33f62-431">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-431">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="33f62-432">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-432">Container</span></span>

* <span data-ttu-id="33f62-433">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-433">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="33f62-434">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="33f62-434">Cosmos DB</span></span>

* <span data-ttu-id="33f62-435">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="33f62-435">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="33f62-436">DMS</span><span class="sxs-lookup"><span data-stu-id="33f62-436">DMS</span></span>

* <span data-ttu-id="33f62-437">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-437">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="33f62-438">内線番号</span><span class="sxs-lookup"><span data-stu-id="33f62-438">Extension</span></span>

* <span data-ttu-id="33f62-439">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-439">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="33f62-440">Interactive</span><span class="sxs-lookup"><span data-stu-id="33f62-440">Interactive</span></span>

* <span data-ttu-id="33f62-441">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-441">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="33f62-442">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="33f62-442">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="33f62-443">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-443">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="33f62-444">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-444">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="33f62-445">ラボ</span><span class="sxs-lookup"><span data-stu-id="33f62-445">Lab</span></span>

* <span data-ttu-id="33f62-446">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-446">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="33f62-447">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-447">Network</span></span>

* <span data-ttu-id="33f62-448">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-448">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="33f62-449">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-449">Profile</span></span>

* <span data-ttu-id="33f62-450">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-450">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="33f62-451">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-451">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="33f62-452">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-452">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="33f62-453">Redis</span><span class="sxs-lookup"><span data-stu-id="33f62-453">Redis</span></span>

* <span data-ttu-id="33f62-454">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-454">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="33f62-455">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="33f62-455">Deprecated `redis list-all`.</span></span> <span data-ttu-id="33f62-456">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="33f62-456">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="33f62-457">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-457">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="33f62-458">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-458">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="33f62-459">Role</span><span class="sxs-lookup"><span data-stu-id="33f62-459">Role</span></span>

* <span data-ttu-id="33f62-460">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-460">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-461">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-461">Storage</span></span>

* <span data-ttu-id="33f62-462">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="33f62-462">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="33f62-463">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="33f62-463">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="33f62-464">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="33f62-464">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="33f62-465">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="33f62-465">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="33f62-466">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-466">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-467">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-467">VM</span></span>

* <span data-ttu-id="33f62-468">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-468">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="33f62-469">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-469">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="33f62-470">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="33f62-470">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="33f62-471">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-471">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="33f62-472">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-472">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="33f62-473">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-473">Added write accelerator support</span></span>
* <span data-ttu-id="33f62-474">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-474">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="33f62-475">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-475">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="33f62-476">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-476">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="33f62-477">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="33f62-477">April 10, 2018</span></span>

<span data-ttu-id="33f62-478">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="33f62-478">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-479">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-479">ACR</span></span>

* <span data-ttu-id="33f62-480">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-480">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-481">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-481">ACS</span></span>

* <span data-ttu-id="33f62-482">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-482">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-483">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-483">Appservice</span></span>

* [重大な変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="33f62-485">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-485">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="33f62-486">BatchAI</span><span class="sxs-lookup"><span data-stu-id="33f62-486">BatchAI</span></span>

* <span data-ttu-id="33f62-487">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-487">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="33f62-488">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="33f62-488">Job level mounting</span></span>
 - <span data-ttu-id="33f62-489">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="33f62-489">Environment variables with secret values</span></span>
 - <span data-ttu-id="33f62-490">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="33f62-490">Performance counters settings</span></span>
 - <span data-ttu-id="33f62-491">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="33f62-491">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="33f62-492">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="33f62-492">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="33f62-493">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="33f62-493">Usage and limits reporting</span></span>
 - <span data-ttu-id="33f62-494">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="33f62-494">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="33f62-495">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="33f62-495">Support for custom images</span></span>
 - <span data-ttu-id="33f62-496">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-496">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="33f62-497">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-497">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="33f62-498">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="33f62-498">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="33f62-499">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="33f62-499">National clouds are supported</span></span>
* <span data-ttu-id="33f62-500">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-500">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="33f62-501">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-501">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="33f62-502">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-502">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="33f62-503">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-503">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="33f62-504">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="33f62-504">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="33f62-505">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="33f62-505">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="33f62-506">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-506">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="33f62-507">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-507">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="33f62-508">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="33f62-508">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="33f62-509">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-509">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="33f62-510">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="33f62-510">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="33f62-511">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="33f62-511">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="33f62-512">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-512">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="33f62-513">課金</span><span class="sxs-lookup"><span data-stu-id="33f62-513">Billing</span></span>

* <span data-ttu-id="33f62-514">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-514">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="33f62-515">消費</span><span class="sxs-lookup"><span data-stu-id="33f62-515">Consumption</span></span>

* <span data-ttu-id="33f62-516">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-516">Added `marketplace` commands</span></span>
* <span data-ttu-id="33f62-517">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-517">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="33f62-518">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-518">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="33f62-519">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-519">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="33f62-520">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-520">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="33f62-521">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-521">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="33f62-522">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-522">Container</span></span>

* <span data-ttu-id="33f62-523">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-523">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="33f62-524">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-524">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="33f62-525">内線番号</span><span class="sxs-lookup"><span data-stu-id="33f62-525">Extension</span></span>

* <span data-ttu-id="33f62-526">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-526">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="33f62-527">Interactive</span><span class="sxs-lookup"><span data-stu-id="33f62-527">Interactive</span></span>

* <span data-ttu-id="33f62-528">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-528">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="33f62-529">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-529">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="33f62-530">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-530">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="33f62-531">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-531">Network</span></span>

* <span data-ttu-id="33f62-532">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-532">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="33f62-533">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-533">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="33f62-534">#4910</span><span class="sxs-lookup"><span data-stu-id="33f62-534">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="33f62-535">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-535">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="33f62-536">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="33f62-536">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="33f62-537">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-537">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="33f62-538">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-538">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="33f62-539">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-539">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="33f62-540">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-540">Profile</span></span>

* <span data-ttu-id="33f62-541">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-541">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="33f62-542">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-542">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="33f62-543">RDBMS</span><span class="sxs-lookup"><span data-stu-id="33f62-543">RDBMS</span></span>

* <span data-ttu-id="33f62-544">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-544">Added `georestore` command</span></span>
* <span data-ttu-id="33f62-545">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-545">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-546">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-546">Resource</span></span>

* <span data-ttu-id="33f62-547">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-547">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="33f62-548">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-548">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-549">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-549">SQL</span></span>

* <span data-ttu-id="33f62-550">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-550">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-551">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-551">Storage</span></span>

* <span data-ttu-id="33f62-552">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-552">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-553">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-553">VM</span></span>

* <span data-ttu-id="33f62-554">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-554">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="33f62-555">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-555">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大な変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="33f62-557">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-557">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="33f62-558">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-558">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="33f62-559">#5718</span><span class="sxs-lookup"><span data-stu-id="33f62-559">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="33f62-560">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-560">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="33f62-561">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="33f62-561">March 27, 2018</span></span>

<span data-ttu-id="33f62-562">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="33f62-562">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="33f62-563">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-563">Core</span></span>

* <span data-ttu-id="33f62-564">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="33f62-564">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-565">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-565">ACS</span></span>

* <span data-ttu-id="33f62-566">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-566">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-567">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-567">Appservice</span></span>

* <span data-ttu-id="33f62-568">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-568">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="33f62-569">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-569">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="33f62-570">Backup</span><span class="sxs-lookup"><span data-stu-id="33f62-570">Backup</span></span>

* <span data-ttu-id="33f62-571">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-571">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="33f62-572">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="33f62-572">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="33f62-573">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-573">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="33f62-574">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-574">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="33f62-575">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-575">Container</span></span>

* <span data-ttu-id="33f62-576">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-576">Added `container exec` command.</span></span> <span data-ttu-id="33f62-577">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="33f62-577">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="33f62-578">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="33f62-578">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="33f62-579">内線番号</span><span class="sxs-lookup"><span data-stu-id="33f62-579">Extension</span></span>

* <span data-ttu-id="33f62-580">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-580">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="33f62-581">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-581">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="33f62-582">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-582">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="33f62-583">Interactive</span><span class="sxs-lookup"><span data-stu-id="33f62-583">Interactive</span></span>

* <span data-ttu-id="33f62-584">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-584">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="33f62-585">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-585">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="33f62-586">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="33f62-586">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="33f62-587">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-587">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="33f62-588">ラボ</span><span class="sxs-lookup"><span data-stu-id="33f62-588">Lab</span></span>

* <span data-ttu-id="33f62-589">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-589">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="33f62-590">監視</span><span class="sxs-lookup"><span data-stu-id="33f62-590">Monitor</span></span>

* <span data-ttu-id="33f62-591">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="33f62-591">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="33f62-592">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="33f62-592">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="33f62-593">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="33f62-593">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="33f62-594">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-594">Network</span></span>

* <span data-ttu-id="33f62-595">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-595">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="33f62-596">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-596">Profile</span></span>

* <span data-ttu-id="33f62-597">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-597">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="33f62-598">RDBMS</span><span class="sxs-lookup"><span data-stu-id="33f62-598">RDBMS</span></span>

* <span data-ttu-id="33f62-599">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-599">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-600">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-600">Resource</span></span>

* [重大な変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="33f62-602">Role</span><span class="sxs-lookup"><span data-stu-id="33f62-602">Role</span></span>

* <span data-ttu-id="33f62-603">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-603">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="33f62-604">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-604">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="33f62-605">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-605">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="33f62-606">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-606">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="33f62-607">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-607">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-608">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-608">Storage</span></span>

* <span data-ttu-id="33f62-609">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-609">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="33f62-610">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-610">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-611">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-611">VM</span></span>

* <span data-ttu-id="33f62-612">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-612">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="33f62-613">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-613">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="33f62-614">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-614">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="33f62-615">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-615">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="33f62-616">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="33f62-616">March 13, 2018</span></span>

<span data-ttu-id="33f62-617">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="33f62-617">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-618">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-618">ACR</span></span>

* <span data-ttu-id="33f62-619">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-619">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="33f62-620">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-620">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="33f62-621">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-621">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-622">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-622">ACS</span></span>

* <span data-ttu-id="33f62-623">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-623">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="33f62-624">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-624">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="33f62-625">Advisor</span><span class="sxs-lookup"><span data-stu-id="33f62-625">Advisor</span></span>

* <span data-ttu-id="33f62-626">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-626">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="33f62-627">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-627">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="33f62-628">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-628">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="33f62-629">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-629">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="33f62-630">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-630">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-631">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-631">Appservice</span></span>

* <span data-ttu-id="33f62-632">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-632">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="33f62-633">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-633">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="33f62-634">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="33f62-634">Eventhubs</span></span>

* <span data-ttu-id="33f62-635">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="33f62-635">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="33f62-636">内線番号</span><span class="sxs-lookup"><span data-stu-id="33f62-636">Extension</span></span>

* <span data-ttu-id="33f62-637">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-637">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="33f62-638">Interactive</span><span class="sxs-lookup"><span data-stu-id="33f62-638">Interactive</span></span>

* <span data-ttu-id="33f62-639">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="33f62-639">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="33f62-640">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="33f62-640">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="33f62-641">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="33f62-641">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="33f62-642">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-642">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="33f62-643">監視</span><span class="sxs-lookup"><span data-stu-id="33f62-643">Monitor</span></span>

* <span data-ttu-id="33f62-644">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-644">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="33f62-645">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-645">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="33f62-646">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-646">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="33f62-647">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-647">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="33f62-648">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-648">Network</span></span>

* <span data-ttu-id="33f62-649">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-649">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="33f62-650">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-650">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="33f62-651">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-651">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="33f62-652">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-652">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="33f62-653">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-653">Profile</span></span>

* <span data-ttu-id="33f62-654">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-654">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="33f62-655">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-655">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="33f62-656">RDBMS</span><span class="sxs-lookup"><span data-stu-id="33f62-656">RDBMS</span></span>

* <span data-ttu-id="33f62-657">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-657">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="33f62-658">Service Bus</span><span class="sxs-lookup"><span data-stu-id="33f62-658">Service Bus</span></span>

* <span data-ttu-id="33f62-659">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="33f62-659">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-660">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-660">Storage</span></span>

* <span data-ttu-id="33f62-661">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-661">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="33f62-662">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="33f62-662">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-663">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-663">VM</span></span>

* <span data-ttu-id="33f62-664">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-664">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="33f62-665">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-665">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="33f62-666">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-666">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="33f62-667">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-667">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="33f62-668">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="33f62-668">February 27, 2018</span></span>

<span data-ttu-id="33f62-669">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="33f62-669">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="33f62-670">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-670">Core</span></span>

* <span data-ttu-id="33f62-671">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="33f62-671">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="33f62-672">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-672">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="33f62-673">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-673">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-674">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-674">ACS</span></span>

* <span data-ttu-id="33f62-675">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-675">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="33f62-676">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="33f62-676">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="33f62-677">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-677">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="33f62-678">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-678">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-679">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-679">Appservice</span></span>

* <span data-ttu-id="33f62-680">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="33f62-680">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="33f62-681">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="33f62-681">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="33f62-682">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="33f62-682">Cognitive Services</span></span>

* <span data-ttu-id="33f62-683">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-683">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="33f62-684">消費</span><span class="sxs-lookup"><span data-stu-id="33f62-684">Consumption</span></span>

* <span data-ttu-id="33f62-685">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-685">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="33f62-686">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-686">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="33f62-687">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-687">Container</span></span>

* <span data-ttu-id="33f62-688">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-688">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="33f62-689">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-689">Network</span></span>

* <span data-ttu-id="33f62-690">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="33f62-690">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-691">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-691">Resource</span></span>

* <span data-ttu-id="33f62-692">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-692">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="33f62-693">Role</span><span class="sxs-lookup"><span data-stu-id="33f62-693">Role</span></span>

* <span data-ttu-id="33f62-694">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-694">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-695">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-695">SQL</span></span>

* <span data-ttu-id="33f62-696">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-696">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-697">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-697">Storage</span></span>

* <span data-ttu-id="33f62-698">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-698">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-699">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-699">VM</span></span>

* <span data-ttu-id="33f62-700">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-700">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="33f62-701">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="33f62-701">February 13, 2018</span></span>

<span data-ttu-id="33f62-702">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="33f62-702">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="33f62-703">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-703">Core</span></span>

* <span data-ttu-id="33f62-704">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-704">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-705">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-705">ACS</span></span>

* <span data-ttu-id="33f62-706">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-706">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="33f62-707">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-707">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="33f62-708">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-708">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="33f62-709">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-709">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="33f62-710">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-710">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="33f62-711">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="33f62-711">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="33f62-712">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-712">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="33f62-713">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="33f62-713">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-714">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-714">Appservice</span></span>

* <span data-ttu-id="33f62-715">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-715">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="33f62-716">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-716">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="33f62-717">CDN</span><span class="sxs-lookup"><span data-stu-id="33f62-717">CDN</span></span>

* <span data-ttu-id="33f62-718">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-718">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="33f62-719">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-719">Container</span></span>

* <span data-ttu-id="33f62-720">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-720">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="33f62-721">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-721">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="33f62-722">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="33f62-722">CosmosDB</span></span>

* <span data-ttu-id="33f62-723">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-723">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="33f62-724">内線番号</span><span class="sxs-lookup"><span data-stu-id="33f62-724">Extension</span></span>

* <span data-ttu-id="33f62-725">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-725">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="33f62-726">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-726">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="33f62-727">フィードバック</span><span class="sxs-lookup"><span data-stu-id="33f62-727">Feedback</span></span>

* <span data-ttu-id="33f62-728">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-728">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="33f62-729">Interactive</span><span class="sxs-lookup"><span data-stu-id="33f62-729">Interactive</span></span>

* <span data-ttu-id="33f62-730">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-730">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="33f62-731">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-731">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="33f62-732">IoT</span><span class="sxs-lookup"><span data-stu-id="33f62-732">IoT</span></span>

* <span data-ttu-id="33f62-733">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-733">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="33f62-734">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-734">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="33f62-735">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-735">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="33f62-736">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-736">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="33f62-737">監視</span><span class="sxs-lookup"><span data-stu-id="33f62-737">Monitor</span></span>

* <span data-ttu-id="33f62-738">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-738">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="33f62-739">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-739">Network</span></span>

* <span data-ttu-id="33f62-740">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-740">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="33f62-741">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-741">Profile</span></span>

* <span data-ttu-id="33f62-742">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-742">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-743">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-743">Resource</span></span>

* <span data-ttu-id="33f62-744">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-744">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="33f62-745">Role</span><span class="sxs-lookup"><span data-stu-id="33f62-745">Role</span></span>

* <span data-ttu-id="33f62-746">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-746">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-747">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-747">SQL</span></span>

* <span data-ttu-id="33f62-748">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-748">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="33f62-749">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-749">Added `sql db rename`</span></span>
* <span data-ttu-id="33f62-750">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-750">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-751">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-751">Storage</span></span>

* <span data-ttu-id="33f62-752">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-752">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-753">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-753">VM</span></span>

* <span data-ttu-id="33f62-754">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-754">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="33f62-755">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-755">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="33f62-756">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="33f62-756">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="33f62-757">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="33f62-757">January 31, 2018</span></span>

<span data-ttu-id="33f62-758">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="33f62-758">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="33f62-759">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-759">Core</span></span>

* <span data-ttu-id="33f62-760">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-760">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="33f62-761">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-761">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="33f62-762">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-762">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="33f62-763">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="33f62-763">Use `--verbose` to see</span></span>
* <span data-ttu-id="33f62-764">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="33f62-764">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-765">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-765">ACS</span></span>

* <span data-ttu-id="33f62-766">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-766">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="33f62-767">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-767">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-768">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-768">Appservice</span></span>

* <span data-ttu-id="33f62-769">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="33f62-769">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="33f62-770">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-770">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="33f62-771">CDN</span><span class="sxs-lookup"><span data-stu-id="33f62-771">CDN</span></span>

* <span data-ttu-id="33f62-772">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-772">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="33f62-773">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="33f62-773">CosmosDB</span></span>

* <span data-ttu-id="33f62-774">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-774">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="33f62-775">Interactive</span><span class="sxs-lookup"><span data-stu-id="33f62-775">Interactive</span></span>

* <span data-ttu-id="33f62-776">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-776">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="33f62-777">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-777">Network</span></span>

* <span data-ttu-id="33f62-778">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-778">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="33f62-779">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-779">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="33f62-780">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-780">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="33f62-781">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-781">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="33f62-782">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-782">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="33f62-783">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-783">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="33f62-784">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-784">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="33f62-785">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-785">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="33f62-786">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-786">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="33f62-787">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="33f62-787">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="33f62-788">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-788">Profile</span></span>

* <span data-ttu-id="33f62-789">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-789">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-790">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-790">Resource</span></span>

* <span data-ttu-id="33f62-791">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-791">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-792">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-792">Storage</span></span>

* <span data-ttu-id="33f62-793">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-793">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="33f62-794">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-794">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="33f62-795">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-795">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="33f62-796">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-796">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="33f62-797">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-797">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-798">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-798">VM</span></span>

* <span data-ttu-id="33f62-799">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-799">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="33f62-800">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-800">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="33f62-801">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-801">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="33f62-802">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-802">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="33f62-803">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="33f62-803">January 17, 2018</span></span>

<span data-ttu-id="33f62-804">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="33f62-804">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-805">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-805">ACR</span></span>

* <span data-ttu-id="33f62-806">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-806">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="33f62-807">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-807">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-808">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-808">ACS</span></span>

* <span data-ttu-id="33f62-809">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-809">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="33f62-810">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-810">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-811">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-811">Appservice</span></span>

* <span data-ttu-id="33f62-812">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-812">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="33f62-813">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-813">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="33f62-814">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-814">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="33f62-815">Backup</span><span class="sxs-lookup"><span data-stu-id="33f62-815">Backup</span></span>

* <span data-ttu-id="33f62-816">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-816">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="33f62-817">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-817">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="33f62-818">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-818">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="33f62-819">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-819">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="33f62-820">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-820">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="33f62-821">Batch</span><span class="sxs-lookup"><span data-stu-id="33f62-821">Batch</span></span>

* <span data-ttu-id="33f62-822">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-822">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="33f62-823">クラウド</span><span class="sxs-lookup"><span data-stu-id="33f62-823">Cloud</span></span>

* <span data-ttu-id="33f62-824">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-824">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="33f62-825">消費</span><span class="sxs-lookup"><span data-stu-id="33f62-825">Consumption</span></span>

* <span data-ttu-id="33f62-826">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-826">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="33f62-827">Event Grid</span><span class="sxs-lookup"><span data-stu-id="33f62-827">Event Grid</span></span>

* <span data-ttu-id="33f62-828">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="33f62-828">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="33f62-829">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="33f62-829">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="33f62-830">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-830">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="33f62-831">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="33f62-831">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="33f62-832">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-832">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="33f62-833">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-833">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="33f62-834">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-834">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="33f62-835">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-835">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="33f62-836">Interactive</span><span class="sxs-lookup"><span data-stu-id="33f62-836">Interactive</span></span>

* <span data-ttu-id="33f62-837">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="33f62-837">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="33f62-838">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-838">Fixed errors on startup</span></span>
* <span data-ttu-id="33f62-839">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-839">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="33f62-840">IoT</span><span class="sxs-lookup"><span data-stu-id="33f62-840">IoT</span></span>

* <span data-ttu-id="33f62-841">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-841">Added support for device provisioning service</span></span>
* <span data-ttu-id="33f62-842">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-842">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="33f62-843">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-843">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="33f62-844">監視</span><span class="sxs-lookup"><span data-stu-id="33f62-844">Monitor</span></span>

* <span data-ttu-id="33f62-845">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-845">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="33f62-846">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="33f62-846">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="33f62-847">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-847">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="33f62-848">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-848">Network</span></span>

* <span data-ttu-id="33f62-849">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-849">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="33f62-850">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-850">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="33f62-851">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-851">Profile</span></span>

* <span data-ttu-id="33f62-852">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-852">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="33f62-853">Role</span><span class="sxs-lookup"><span data-stu-id="33f62-853">Role</span></span>

* <span data-ttu-id="33f62-854">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-854">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="33f62-855">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="33f62-855">Service Fabric</span></span>

* <span data-ttu-id="33f62-856">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-856">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="33f62-857">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-857">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-858">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-858">VM</span></span>

* <span data-ttu-id="33f62-859">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="33f62-859">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="33f62-860">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-860">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="33f62-861">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-861">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="33f62-862">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-862">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="33f62-863">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-863">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="33f62-864">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-864">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="33f62-865">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-865">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="33f62-866">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-866">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="33f62-867">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="33f62-867">December 19, 2017</span></span>

<span data-ttu-id="33f62-868">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="33f62-868">Version 2.0.23</span></span>

* <span data-ttu-id="33f62-869">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-869">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="33f62-870">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-870">Container</span></span>

* <span data-ttu-id="33f62-871">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-871">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="33f62-872">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-872">Network</span></span>

* <span data-ttu-id="33f62-873">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-873">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="33f62-874">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-874">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-875">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-875">Storage</span></span>

* <span data-ttu-id="33f62-876">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-876">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-877">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-877">VM</span></span>

* <span data-ttu-id="33f62-878">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-878">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="33f62-879">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="33f62-879">December 5, 2017</span></span>

<span data-ttu-id="33f62-880">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="33f62-880">Version 2.0.22</span></span>

* <span data-ttu-id="33f62-881">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-881">Removed `az component` commands.</span></span> <span data-ttu-id="33f62-882">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="33f62-882">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="33f62-883">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-883">Core</span></span>
* <span data-ttu-id="33f62-884">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-884">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="33f62-885">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-885">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-886">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-886">ACS</span></span>

* <span data-ttu-id="33f62-887">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-887">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="33f62-888">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-888">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="33f62-889">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-889">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="33f62-890">Advisor</span><span class="sxs-lookup"><span data-stu-id="33f62-890">Advisor</span></span>

* <span data-ttu-id="33f62-891">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="33f62-891">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-892">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-892">Appservice</span></span>

* <span data-ttu-id="33f62-893">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-893">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="33f62-894">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-894">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="33f62-895">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-895">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="33f62-896">消費</span><span class="sxs-lookup"><span data-stu-id="33f62-896">Consumption</span></span>

* <span data-ttu-id="33f62-897">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-897">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="33f62-898">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-898">Container</span></span>

* <span data-ttu-id="33f62-899">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-899">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="33f62-900">監視</span><span class="sxs-lookup"><span data-stu-id="33f62-900">Monitor</span></span>

* <span data-ttu-id="33f62-901">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-901">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-902">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-902">Resource</span></span>

* <span data-ttu-id="33f62-903">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-903">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="33f62-904">Role</span><span class="sxs-lookup"><span data-stu-id="33f62-904">Role</span></span>

* <span data-ttu-id="33f62-905">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-905">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="33f62-906">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="33f62-906">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="33f62-907">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-907">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-908">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-908">SQL</span></span>

* <span data-ttu-id="33f62-909">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-909">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="33f62-910">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-910">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-911">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-911">VM</span></span>

* <span data-ttu-id="33f62-912">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-912">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="33f62-913">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="33f62-913">November 14, 2017</span></span>

<span data-ttu-id="33f62-914">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="33f62-914">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-915">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-915">ACR</span></span>

* <span data-ttu-id="33f62-916">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-916">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="33f62-917">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-917">ACS</span></span>

* <span data-ttu-id="33f62-918">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-918">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="33f62-919">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-919">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="33f62-920">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-920">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="33f62-921">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-921">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="33f62-922">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-922">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-923">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-923">Appservice</span></span>

* <span data-ttu-id="33f62-924">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-924">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="33f62-925">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-925">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="33f62-926">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-926">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="33f62-927">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-927">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="33f62-928">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-928">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="33f62-929">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="33f62-929">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="33f62-930">Batch</span><span class="sxs-lookup"><span data-stu-id="33f62-930">Batch</span></span>

* <span data-ttu-id="33f62-931">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-931">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="33f62-932">Batchai</span><span class="sxs-lookup"><span data-stu-id="33f62-932">Batchai</span></span>

* <span data-ttu-id="33f62-933">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-933">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="33f62-934">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-934">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="33f62-935">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-935">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="33f62-936">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-936">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="33f62-937">クラウド</span><span class="sxs-lookup"><span data-stu-id="33f62-937">Cloud</span></span>

* <span data-ttu-id="33f62-938">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-938">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="33f62-939">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-939">Container</span></span>

* <span data-ttu-id="33f62-940">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-940">Added support to open multiple ports</span></span>
* <span data-ttu-id="33f62-941">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-941">Added container group restart policy</span></span>
* <span data-ttu-id="33f62-942">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-942">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="33f62-943">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-943">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="33f62-944">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="33f62-944">Data Lake Analytics</span></span>

* <span data-ttu-id="33f62-945">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-945">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="33f62-946">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="33f62-946">Data Lake Store</span></span>

* <span data-ttu-id="33f62-947">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-947">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="33f62-948">内線番号</span><span class="sxs-lookup"><span data-stu-id="33f62-948">Extension</span></span>

* <span data-ttu-id="33f62-949">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-949">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="33f62-950">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-950">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="33f62-951">IoT</span><span class="sxs-lookup"><span data-stu-id="33f62-951">IoT</span></span>

* <span data-ttu-id="33f62-952">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-952">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="33f62-953">監視</span><span class="sxs-lookup"><span data-stu-id="33f62-953">Monitor</span></span>

* <span data-ttu-id="33f62-954">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-954">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="33f62-955">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-955">Network</span></span>

* <span data-ttu-id="33f62-956">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-956">Added support for CAA DNS records</span></span>
* <span data-ttu-id="33f62-957">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-957">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="33f62-958">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-958">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="33f62-959">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-959">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="33f62-960">Reservations</span><span class="sxs-lookup"><span data-stu-id="33f62-960">Reservations</span></span>

* <span data-ttu-id="33f62-961">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="33f62-961">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-962">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-962">Resource</span></span>

* <span data-ttu-id="33f62-963">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-963">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-964">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-964">SQL</span></span>

* <span data-ttu-id="33f62-965">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-965">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-966">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-966">Storage</span></span>

* <span data-ttu-id="33f62-967">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-967">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="33f62-968">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-968">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="33f62-969">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-969">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="33f62-970">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-970">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="33f62-971">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-971">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="33f62-972">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-972">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="33f62-973">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-973">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-974">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-974">VM</span></span>

* <span data-ttu-id="33f62-975">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-975">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="33f62-976">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-976">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="33f62-977">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-977">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="33f62-978">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-978">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="33f62-979">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-979">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="33f62-980">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="33f62-980">October 24, 2017</span></span>

<span data-ttu-id="33f62-981">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="33f62-981">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="33f62-982">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-982">Core</span></span>

* <span data-ttu-id="33f62-983">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-983">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-984">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-984">ACR</span></span>

* <span data-ttu-id="33f62-985">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-985">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="33f62-986">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-986">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="33f62-987">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-987">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-988">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-988">ACS</span></span>

* <span data-ttu-id="33f62-989">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-989">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="33f62-990">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-990">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-991">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-991">Appservice</span></span>

* <span data-ttu-id="33f62-992">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-992">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="33f62-993">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="33f62-993">Component</span></span>

* <span data-ttu-id="33f62-994">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-994">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="33f62-995">監視</span><span class="sxs-lookup"><span data-stu-id="33f62-995">Monitor</span></span>

* <span data-ttu-id="33f62-996">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-996">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-997">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-997">Resource</span></span>

* <span data-ttu-id="33f62-998">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-998">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="33f62-999">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-999">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-1000">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-1000">VM</span></span>

* <span data-ttu-id="33f62-1001">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1001">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="33f62-1002">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1002">October 9, 2017</span></span>

<span data-ttu-id="33f62-1003">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="33f62-1003">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="33f62-1004">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-1004">Core</span></span>

* <span data-ttu-id="33f62-1005">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1005">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-1006">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-1006">Appservice</span></span>

* <span data-ttu-id="33f62-1007">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1007">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="33f62-1008">Batch</span><span class="sxs-lookup"><span data-stu-id="33f62-1008">Batch</span></span>

* <span data-ttu-id="33f62-1009">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1009">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="33f62-1010">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1010">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="33f62-1011">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1011">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="33f62-1012">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1012">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="33f62-1013">Batchai</span><span class="sxs-lookup"><span data-stu-id="33f62-1013">Batchai</span></span>

* <span data-ttu-id="33f62-1014">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="33f62-1014">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="33f62-1015">KeyVault</span><span class="sxs-lookup"><span data-stu-id="33f62-1015">Keyvault</span></span>

* <span data-ttu-id="33f62-1016">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1016">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="33f62-1017">(#4448)</span><span class="sxs-lookup"><span data-stu-id="33f62-1017">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="33f62-1018">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-1018">Network</span></span>

* <span data-ttu-id="33f62-1019">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1019">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="33f62-1020">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1020">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-1021">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-1021">Resource</span></span>

* <span data-ttu-id="33f62-1022">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1022">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="33f62-1023">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1023">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="33f62-1024">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1024">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="33f62-1025">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1025">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-1026">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-1026">Sql</span></span>

* <span data-ttu-id="33f62-1027">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1027">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="33f62-1028">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1028">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="33f62-1029">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1029">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-1030">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-1030">Storage</span></span>

* <span data-ttu-id="33f62-1031">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1031">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-1032">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-1032">Vm</span></span>

* <span data-ttu-id="33f62-1033">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1033">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="33f62-1034">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1034">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="33f62-1035">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1035">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="33f62-1036">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1036">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="33f62-1037">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1037">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="33f62-1038">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1038">September 22, 2017</span></span>

<span data-ttu-id="33f62-1039">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="33f62-1039">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-1040">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-1040">Resource</span></span>

* <span data-ttu-id="33f62-1041">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1041">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="33f62-1042">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1042">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="33f62-1043">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1043">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="33f62-1044">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1044">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="33f62-1045">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-1045">Network</span></span>

* <span data-ttu-id="33f62-1046">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1046">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="33f62-1047">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1047">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="33f62-1048">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1048">Added `asg` application security group commands</span></span>
* <span data-ttu-id="33f62-1049">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1049">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="33f62-1050">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1050">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="33f62-1051">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1051">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="33f62-1052">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1052">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-1053">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-1053">Storage</span></span>

* <span data-ttu-id="33f62-1054">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1054">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="33f62-1055">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="33f62-1055">Eventgrid</span></span>

* <span data-ttu-id="33f62-1056">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1056">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-1057">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-1057">SQL</span></span>

* <span data-ttu-id="33f62-1058">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1058">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="33f62-1059">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="33f62-1059">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="33f62-1060">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1060">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="33f62-1061">KeyVault</span><span class="sxs-lookup"><span data-stu-id="33f62-1061">Keyvault</span></span>

* <span data-ttu-id="33f62-1062">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1062">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-1063">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-1063">VM</span></span>

* <span data-ttu-id="33f62-1064">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1064">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="33f62-1065">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1065">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="33f62-1066">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1066">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="33f62-1067">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1067">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="33f62-1068">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1068">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="33f62-1069">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1069">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-1070">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-1070">ACS</span></span>

* <span data-ttu-id="33f62-1071">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1071">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-1072">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-1072">Appservice</span></span>

* <span data-ttu-id="33f62-1073">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1073">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="33f62-1074">Backup</span><span class="sxs-lookup"><span data-stu-id="33f62-1074">Backup</span></span>

* <span data-ttu-id="33f62-1075">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="33f62-1075">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="33f62-1076">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1076">September 11, 2017</span></span>

<span data-ttu-id="33f62-1077">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="33f62-1077">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="33f62-1078">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-1078">Core</span></span>

* <span data-ttu-id="33f62-1079">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1079">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="33f62-1080">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1080">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-1081">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-1081">Acs</span></span>

* <span data-ttu-id="33f62-1082">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1082">Added `acs list-locations` command</span></span>
* <span data-ttu-id="33f62-1083">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1083">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-1084">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-1084">Appservice</span></span>

* <span data-ttu-id="33f62-1085">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1085">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="33f62-1086">CDN</span><span class="sxs-lookup"><span data-stu-id="33f62-1086">CDN</span></span>

* <span data-ttu-id="33f62-1087">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1087">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="33f62-1088">内線番号</span><span class="sxs-lookup"><span data-stu-id="33f62-1088">Extension</span></span>

* <span data-ttu-id="33f62-1089">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="33f62-1089">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="33f62-1090">KeyVault</span><span class="sxs-lookup"><span data-stu-id="33f62-1090">Keyvault</span></span>

* <span data-ttu-id="33f62-1091">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1091">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="33f62-1092">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-1092">Network</span></span>

* <span data-ttu-id="33f62-1093">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1093">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="33f62-1094">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1094">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="33f62-1095">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1095">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="33f62-1096">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1096">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="33f62-1097">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1097">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-1098">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-1098">Resource</span></span>

* <span data-ttu-id="33f62-1099">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="33f62-1099">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="33f62-1100">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="33f62-1100">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="33f62-1101">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="33f62-1101">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="33f62-1102">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1102">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-1103">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-1103">SQL</span></span>

* <span data-ttu-id="33f62-1104">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1104">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-1105">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-1105">VM</span></span>

* <span data-ttu-id="33f62-1106">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="33f62-1106">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="33f62-1107">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="33f62-1107">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="33f62-1108">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1108">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="33f62-1109">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="33f62-1109">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="33f62-1110">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="33f62-1110">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="33f62-1111">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1111">August 31, 2017</span></span>

<span data-ttu-id="33f62-1112">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="33f62-1112">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="33f62-1113">KeyVault</span><span class="sxs-lookup"><span data-stu-id="33f62-1113">Keyvault</span></span>

* <span data-ttu-id="33f62-1114">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1114">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="33f62-1115">SF</span><span class="sxs-lookup"><span data-stu-id="33f62-1115">Sf</span></span>

* <span data-ttu-id="33f62-1116">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="33f62-1116">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-1117">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-1117">Storage</span></span>

* <span data-ttu-id="33f62-1118">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1118">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="33f62-1119">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="33f62-1119">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="33f62-1120">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1120">August 28, 2017</span></span>

<span data-ttu-id="33f62-1121">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="33f62-1121">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="33f62-1122">CLI</span><span class="sxs-lookup"><span data-stu-id="33f62-1122">CLI</span></span>

* <span data-ttu-id="33f62-1123">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1123">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-1124">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-1124">ACS</span></span>

* <span data-ttu-id="33f62-1125">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1125">Corrected preview regions</span></span>
* <span data-ttu-id="33f62-1126">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1126">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="33f62-1127">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1127">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-1128">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-1128">Appservice</span></span>

* <span data-ttu-id="33f62-1129">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1129">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="33f62-1130">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1130">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="33f62-1131">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1131">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="33f62-1132">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1132">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="33f62-1133">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="33f62-1133">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="33f62-1134">IoT</span><span class="sxs-lookup"><span data-stu-id="33f62-1134">IoT</span></span>

* <span data-ttu-id="33f62-1135">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1135">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="33f62-1136">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-1136">Network</span></span>

* <span data-ttu-id="33f62-1137">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1137">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="33f62-1138">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1138">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="33f62-1139">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1139">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="33f62-1140">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1140">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="33f62-1141">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1141">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="33f62-1142">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-1142">Profile</span></span>

* <span data-ttu-id="33f62-1143">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1143">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="33f62-1144">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="33f62-1144">Service Fabric</span></span>

* <span data-ttu-id="33f62-1145">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="33f62-1145">Preview release</span></span>
* <span data-ttu-id="33f62-1146">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1146">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="33f62-1147">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1147">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="33f62-1148">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1148">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-1149">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-1149">Storage</span></span>

* <span data-ttu-id="33f62-1150">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1150">Enabled setting blob tier</span></span>
* <span data-ttu-id="33f62-1151">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1151">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="33f62-1152">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1152">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="33f62-1153">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1153">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="33f62-1154">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1154">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="33f62-1155">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="33f62-1155">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-1156">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-1156">VM</span></span>

* <span data-ttu-id="33f62-1157">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1157">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="33f62-1158">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1158">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="33f62-1159">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1159">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="33f62-1160">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1160">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="33f62-1161">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1161">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="33f62-1162">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1162">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="33f62-1163">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1163">August 15, 2017</span></span>

<span data-ttu-id="33f62-1164">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="33f62-1164">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-1165">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-1165">ACS</span></span>

* <span data-ttu-id="33f62-1166">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1166">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-1167">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-1167">Appservice</span></span>

* <span data-ttu-id="33f62-1168">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1168">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="33f62-1169">Event Grid</span><span class="sxs-lookup"><span data-stu-id="33f62-1169">Event Grid</span></span>

* <span data-ttu-id="33f62-1170">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1170">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="33f62-1171">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1171">August 11, 2017</span></span>

<span data-ttu-id="33f62-1172">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="33f62-1172">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-1173">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-1173">ACS</span></span>

* <span data-ttu-id="33f62-1174">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1174">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="33f62-1175">Batch</span><span class="sxs-lookup"><span data-stu-id="33f62-1175">Batch</span></span>

* <span data-ttu-id="33f62-1176">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1176">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="33f62-1177">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1177">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="33f62-1178">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1178">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="33f62-1179">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1179">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="33f62-1180">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1180">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="33f62-1181">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1181">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="33f62-1182">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="33f62-1182">Component</span></span>

* <span data-ttu-id="33f62-1183">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1183">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="33f62-1184">コンテナー</span><span class="sxs-lookup"><span data-stu-id="33f62-1184">Container</span></span>

* <span data-ttu-id="33f62-1185">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1185">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="33f62-1186">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="33f62-1186">Data Lake Store</span></span>

* <span data-ttu-id="33f62-1187">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1187">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="33f62-1188">Event Grid</span><span class="sxs-lookup"><span data-stu-id="33f62-1188">Event Grid</span></span>

* <span data-ttu-id="33f62-1189">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="33f62-1189">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="33f62-1190">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-1190">Network</span></span>

* <span data-ttu-id="33f62-1191">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1191">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="33f62-1192">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1192">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="33f62-1193">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1193">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="33f62-1194">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1194">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="33f62-1195">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-1195">Profile</span></span>

* <span data-ttu-id="33f62-1196">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1196">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-1197">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-1197">Storage</span></span>

* <span data-ttu-id="33f62-1198">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="33f62-1198">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-1199">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-1199">VM</span></span>

* <span data-ttu-id="33f62-1200">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1200">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="33f62-1201">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1201">Exposed `list-skus` command</span></span>
* <span data-ttu-id="33f62-1202">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1202">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="33f62-1203">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="33f62-1203">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="33f62-1204">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1204">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="33f62-1205">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1205">July 28, 2017</span></span>

<span data-ttu-id="33f62-1206">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="33f62-1206">Version 2.0.12</span></span>

* <span data-ttu-id="33f62-1207">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1207">Added container commands</span></span>
* <span data-ttu-id="33f62-1208">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1208">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="33f62-1209">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-1209">Core</span></span>

* <span data-ttu-id="33f62-1210">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="33f62-1210">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="33f62-1211">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1211">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="33f62-1212">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="33f62-1212">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="33f62-1213">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="33f62-1213">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="33f62-1214">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="33f62-1214">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="33f62-1215">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="33f62-1215">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="33f62-1216">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="33f62-1216">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="33f62-1217">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="33f62-1217">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="33f62-1218">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="33f62-1218">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="33f62-1219">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="33f62-1219">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="33f62-1220">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="33f62-1220">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="33f62-1221">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="33f62-1221">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="33f62-1222">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1222">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="33f62-1223">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1223">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="33f62-1224">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1224">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="33f62-1225">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="33f62-1225">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="33f62-1226">ACR</span><span class="sxs-lookup"><span data-stu-id="33f62-1226">ACR</span></span>

* <span data-ttu-id="33f62-1227">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1227">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="33f62-1228">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1228">Support SKU update for managed registries</span></span>
* <span data-ttu-id="33f62-1229">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1229">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="33f62-1230">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1230">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="33f62-1231">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1231">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="33f62-1232">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1232">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-1233">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-1233">ACS</span></span>

* <span data-ttu-id="33f62-1234">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1234">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-1235">Appservice</span><span class="sxs-lookup"><span data-stu-id="33f62-1235">Appservice</span></span>

* <span data-ttu-id="33f62-1236">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1236">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="33f62-1237">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1237">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="33f62-1238">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="33f62-1238">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="33f62-1239">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="33f62-1239">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="33f62-1240">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="33f62-1240">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="33f62-1241">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="33f62-1241">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="33f62-1242">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="33f62-1242">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="33f62-1243">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="33f62-1243">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="33f62-1244">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1244">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="33f62-1245">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="33f62-1245">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="33f62-1246">Batch</span><span class="sxs-lookup"><span data-stu-id="33f62-1246">Batch</span></span>

* <span data-ttu-id="33f62-1247">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1247">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="33f62-1248">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1248">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="33f62-1249">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1249">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="33f62-1250">CDN</span><span class="sxs-lookup"><span data-stu-id="33f62-1250">CDN</span></span>

* <span data-ttu-id="33f62-1251">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1251">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="33f62-1252">クラウド</span><span class="sxs-lookup"><span data-stu-id="33f62-1252">Cloud</span></span>

* <span data-ttu-id="33f62-1253">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1253">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="33f62-1254">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="33f62-1254">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="33f62-1255">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1255">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="33f62-1256">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1256">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="33f62-1257">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1257">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="33f62-1258">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="33f62-1258">CosmosDB</span></span>

* <span data-ttu-id="33f62-1259">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1259">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="33f62-1260">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1260">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="33f62-1261">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="33f62-1261">Data Lake Analytics</span></span>

* <span data-ttu-id="33f62-1262">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1262">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="33f62-1263">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1263">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="33f62-1264">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1264">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="33f62-1265">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="33f62-1265">Data Lake Store</span></span>

* <span data-ttu-id="33f62-1266">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1266">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="33f62-1267">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1267">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="33f62-1268">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1268">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="33f62-1269">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="33f62-1269">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="33f62-1270">対話</span><span class="sxs-lookup"><span data-stu-id="33f62-1270">Interactive</span></span>

* <span data-ttu-id="33f62-1271">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1271">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="33f62-1272">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="33f62-1272">Increased test coverage</span></span>
* <span data-ttu-id="33f62-1273">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1273">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="33f62-1274">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="33f62-1274">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="33f62-1275">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="33f62-1275">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="33f62-1276">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="33f62-1276">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="33f62-1277">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="33f62-1277">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="33f62-1278">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1278">Added `--progress` flag</span></span>
* <span data-ttu-id="33f62-1279">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1279">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="33f62-1280">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="33f62-1280">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="33f62-1281">IoT</span><span class="sxs-lookup"><span data-stu-id="33f62-1281">IoT</span></span>

* <span data-ttu-id="33f62-1282">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1282">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="33f62-1283">(#3934)</span><span class="sxs-lookup"><span data-stu-id="33f62-1283">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="33f62-1284">Key Vault</span><span class="sxs-lookup"><span data-stu-id="33f62-1284">Key vault</span></span>

* <span data-ttu-id="33f62-1285">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1285">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="33f62-1286">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="33f62-1286">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="33f62-1287">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="33f62-1287">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="33f62-1288">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="33f62-1288">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="33f62-1289">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="33f62-1289">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="33f62-1290">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="33f62-1290">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="33f62-1291">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1291">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="33f62-1292">(#3307)</span><span class="sxs-lookup"><span data-stu-id="33f62-1292">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="33f62-1293">ラボ</span><span class="sxs-lookup"><span data-stu-id="33f62-1293">Lab</span></span>

* <span data-ttu-id="33f62-1294">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1294">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="33f62-1295">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1295">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="33f62-1296">監視</span><span class="sxs-lookup"><span data-stu-id="33f62-1296">Monitor</span></span>

* <span data-ttu-id="33f62-1297">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="33f62-1297">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="33f62-1298">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1298">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="33f62-1299">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1299">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="33f62-1300">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1300">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="33f62-1301">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1301">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="33f62-1302">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1302">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="33f62-1303">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1303">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="33f62-1304">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="33f62-1304">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="33f62-1305">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1305">`location` no longer required</span></span>
  * <span data-ttu-id="33f62-1306">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="33f62-1306">Add name and ID support for target</span></span>
  * <span data-ttu-id="33f62-1307">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="33f62-1307">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="33f62-1308">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1308">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="33f62-1309">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1309">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="33f62-1310">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="33f62-1310">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="33f62-1311">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1311">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="33f62-1312">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1312">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="33f62-1313">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-1313">Network</span></span>

* <span data-ttu-id="33f62-1314">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1314">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="33f62-1315">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1315">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="33f62-1316">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1316">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="33f62-1317">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1317">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="33f62-1318">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1318">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="33f62-1319">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1319">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="33f62-1320">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1320">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="33f62-1321">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1321">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="33f62-1322">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1322">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="33f62-1323">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1323">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="33f62-1324">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1324">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="33f62-1325">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1325">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="33f62-1326">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1326">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="33f62-1327">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1327">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="33f62-1328">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1328">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="33f62-1329">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1329">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="33f62-1330">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1330">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="33f62-1331">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1331">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="33f62-1332">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1332">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="33f62-1333">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1333">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="33f62-1334">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1334">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="33f62-1335">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1335">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="33f62-1336">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1336">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="33f62-1337">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="33f62-1337">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="33f62-1338">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="33f62-1338">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="33f62-1339">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="33f62-1339">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="33f62-1340">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="33f62-1340">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="33f62-1341">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-1341">Profile</span></span>

* <span data-ttu-id="33f62-1342">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1342">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="33f62-1343">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1343">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="33f62-1344">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="33f62-1344">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="33f62-1345">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1345">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="33f62-1346">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1346">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="33f62-1347">RDBMS</span><span class="sxs-lookup"><span data-stu-id="33f62-1347">RDBMS</span></span>

* <span data-ttu-id="33f62-1348">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="33f62-1348">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="33f62-1349">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="33f62-1349">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="33f62-1350">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="33f62-1350">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="33f62-1351">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="33f62-1351">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-1352">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-1352">Resource</span></span>

* <span data-ttu-id="33f62-1353">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1353">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="33f62-1354">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1354">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="33f62-1355">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1355">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="33f62-1356">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1356">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="33f62-1357">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="33f62-1357">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="33f62-1358">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1358">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="33f62-1359">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="33f62-1359">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="33f62-1360">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1360">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="33f62-1361">Role</span><span class="sxs-lookup"><span data-stu-id="33f62-1361">Role</span></span>

* <span data-ttu-id="33f62-1362">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1362">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="33f62-1363">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="33f62-1363">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="33f62-1364">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="33f62-1364">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="33f62-1365">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="33f62-1365">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="33f62-1366">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1366">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="33f62-1367">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="33f62-1367">Service Fabric</span></span>
* <span data-ttu-id="33f62-1368">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="33f62-1368">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="33f62-1369">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="33f62-1369">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="33f62-1370">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="33f62-1370">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-1371">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-1371">SQL</span></span>

* <span data-ttu-id="33f62-1372">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1372">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="33f62-1373">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1373">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="33f62-1374">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1374">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-1375">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-1375">Storage</span></span>

* <span data-ttu-id="33f62-1376">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="33f62-1376">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="33f62-1377">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1377">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="33f62-1378">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="33f62-1378">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="33f62-1379">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="33f62-1379">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="33f62-1380">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="33f62-1380">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="33f62-1381">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="33f62-1381">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-1382">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-1382">VM</span></span>

* <span data-ttu-id="33f62-1383">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1383">Support configuring nsg</span></span>
* <span data-ttu-id="33f62-1384">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1384">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="33f62-1385">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="33f62-1385">Support managed service identities</span></span>
* <span data-ttu-id="33f62-1386">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1386">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="33f62-1387">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="33f62-1387">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="33f62-1388">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1388">May 10, 2017</span></span>

<span data-ttu-id="33f62-1389">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="33f62-1389">Version 2.0.6</span></span>

* <span data-ttu-id="33f62-1390">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1390">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="33f62-1391">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1391">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="33f62-1392">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1392">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="33f62-1393">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1393">Include Cognitive Services module</span></span>
* <span data-ttu-id="33f62-1394">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1394">Include Service Fabric module</span></span>
* <span data-ttu-id="33f62-1395">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="33f62-1395">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="33f62-1396">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1396">Add support for CDN commands</span></span>
* <span data-ttu-id="33f62-1397">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1397">Remove Container module</span></span>
* <span data-ttu-id="33f62-1398">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="33f62-1398">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="33f62-1399">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="33f62-1399">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="33f62-1400">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-1400">Core</span></span>

* <span data-ttu-id="33f62-1401">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="33f62-1401">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="33f62-1402">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="33f62-1402">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="33f62-1403">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="33f62-1403">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="33f62-1404">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="33f62-1404">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="33f62-1405">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="33f62-1405">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="33f62-1406">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="33f62-1406">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="33f62-1407">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="33f62-1407">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="33f62-1408">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="33f62-1408">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="33f62-1409">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="33f62-1409">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="33f62-1410">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="33f62-1410">core: Improved performance</span></span>
* <span data-ttu-id="33f62-1411">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="33f62-1411">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="33f62-1412">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="33f62-1412">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-1413">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-1413">ACS</span></span>

* <span data-ttu-id="33f62-1414">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1414">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="33f62-1415">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1415">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="33f62-1416">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1416">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="33f62-1417">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="33f62-1417">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-1418">AppService</span><span class="sxs-lookup"><span data-stu-id="33f62-1418">AppService</span></span>

* <span data-ttu-id="33f62-1419">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1419">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="33f62-1420">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1420">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="33f62-1421">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="33f62-1421">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="33f62-1422">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1422">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="33f62-1423">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1423">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="33f62-1424">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="33f62-1424">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="33f62-1425">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="33f62-1425">support slot swap with preview</span></span>
* <span data-ttu-id="33f62-1426">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="33f62-1426">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="33f62-1427">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="33f62-1427">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="33f62-1428">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="33f62-1428">CosmosDB</span></span>

* <span data-ttu-id="33f62-1429">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1429">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="33f62-1430">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1430">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="33f62-1431">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1431">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="33f62-1432">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1432">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="33f62-1433">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="33f62-1433">Data Lake Analytics</span></span>

* <span data-ttu-id="33f62-1434">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1434">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="33f62-1435">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1435">Add support for new catalog item type: package.</span></span> <span data-ttu-id="33f62-1436">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="33f62-1436">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="33f62-1437">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="33f62-1437">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="33f62-1438">テーブル</span><span class="sxs-lookup"><span data-stu-id="33f62-1438">Table</span></span>
  * <span data-ttu-id="33f62-1439">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="33f62-1439">Table valued function</span></span>
  * <span data-ttu-id="33f62-1440">表示</span><span class="sxs-lookup"><span data-stu-id="33f62-1440">View</span></span>
  * <span data-ttu-id="33f62-1441">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="33f62-1441">Table Statistics.</span></span> <span data-ttu-id="33f62-1442">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="33f62-1442">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="33f62-1443">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="33f62-1443">Data Lake Store</span></span>

* <span data-ttu-id="33f62-1444">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1444">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="33f62-1445">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="33f62-1445">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="33f62-1446">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="33f62-1446">missed help for access show.</span></span> <span data-ttu-id="33f62-1447">追加しました </span><span class="sxs-lookup"><span data-stu-id="33f62-1447">adding it.</span></span> <span data-ttu-id="33f62-1448">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="33f62-1448">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="33f62-1449">検索</span><span class="sxs-lookup"><span data-stu-id="33f62-1449">Find</span></span>

* <span data-ttu-id="33f62-1450">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1450">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="33f62-1451">KeyVault</span><span class="sxs-lookup"><span data-stu-id="33f62-1451">KeyVault</span></span>

* <span data-ttu-id="33f62-1452">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1452">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="33f62-1453">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1453">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="33f62-1454">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="33f62-1454">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="33f62-1455">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1455">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="33f62-1456">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="33f62-1456">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="33f62-1457">ラボ</span><span class="sxs-lookup"><span data-stu-id="33f62-1457">Lab</span></span>

* <span data-ttu-id="33f62-1458">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1458">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="33f62-1459">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1459">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="33f62-1460">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1460">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="33f62-1461">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1461">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="33f62-1462">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1462">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="33f62-1463">監視</span><span class="sxs-lookup"><span data-stu-id="33f62-1463">Monitor</span></span>

* <span data-ttu-id="33f62-1464">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="33f62-1464">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="33f62-1465">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="33f62-1465">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="33f62-1466">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-1466">Network</span></span>

* <span data-ttu-id="33f62-1467">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1467">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="33f62-1468">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1468">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="33f62-1469">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1469">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="33f62-1470">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1470">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="33f62-1471">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1471">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="33f62-1472">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1472">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="33f62-1473">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1473">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="33f62-1474">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1474">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="33f62-1475">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1475">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="33f62-1476">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1476">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="33f62-1477">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1477">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="33f62-1478">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1478">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="33f62-1479">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1479">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="33f62-1480">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1480">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="33f62-1481">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="33f62-1481">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="33f62-1482">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1482">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="33f62-1483">プロファイル</span><span class="sxs-lookup"><span data-stu-id="33f62-1483">Profile</span></span>

* <span data-ttu-id="33f62-1484">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="33f62-1484">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="33f62-1485">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="33f62-1485">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="33f62-1486">Redis</span><span class="sxs-lookup"><span data-stu-id="33f62-1486">Redis</span></span>

* <span data-ttu-id="33f62-1487">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1487">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="33f62-1488">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1488">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="33f62-1489">リソース</span><span class="sxs-lookup"><span data-stu-id="33f62-1489">Resource</span></span>

* <span data-ttu-id="33f62-1490">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="33f62-1490">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="33f62-1491">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="33f62-1491">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="33f62-1492">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="33f62-1492">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="33f62-1493">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="33f62-1493">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="33f62-1494">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="33f62-1494">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="33f62-1495">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="33f62-1495">Add docs for az lock update.</span></span> <span data-ttu-id="33f62-1496">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="33f62-1496">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="33f62-1497">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="33f62-1497">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="33f62-1498">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="33f62-1498">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="33f62-1499">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="33f62-1499">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="33f62-1500">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="33f62-1500">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="33f62-1501">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="33f62-1501">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="33f62-1502">Role</span><span class="sxs-lookup"><span data-stu-id="33f62-1502">Role</span></span>

* <span data-ttu-id="33f62-1503">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="33f62-1503">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="33f62-1504">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="33f62-1504">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="33f62-1505">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="33f62-1505">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="33f62-1506">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="33f62-1506">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="33f62-1507">SQL</span><span class="sxs-lookup"><span data-stu-id="33f62-1507">SQL</span></span>

* <span data-ttu-id="33f62-1508">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="33f62-1508">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="33f62-1509">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="33f62-1509">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="33f62-1510">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-1510">Storage</span></span>

* <span data-ttu-id="33f62-1511">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="33f62-1511">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="33f62-1512">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1512">Add support for incremental blob copy</span></span>
* <span data-ttu-id="33f62-1513">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1513">Add support for large block blob upload</span></span>
* <span data-ttu-id="33f62-1514">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="33f62-1514">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-1515">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-1515">VM</span></span>

* <span data-ttu-id="33f62-1516">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="33f62-1516">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="33f62-1517">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="33f62-1517">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="33f62-1518">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="33f62-1518">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="33f62-1519">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="33f62-1519">az vm/vmss disk</span></span>
  3. <span data-ttu-id="33f62-1520">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="33f62-1520">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="33f62-1521">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="33f62-1521">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="33f62-1522">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="33f62-1522">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="33f62-1523">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1523">April 3, 2017</span></span>

<span data-ttu-id="33f62-1524">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="33f62-1524">Version 2.0.2</span></span>

<span data-ttu-id="33f62-1525">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="33f62-1525">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="33f62-1526">コア</span><span class="sxs-lookup"><span data-stu-id="33f62-1526">Core</span></span>

* <span data-ttu-id="33f62-1527">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="33f62-1527">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="33f62-1528">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="33f62-1528">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="33f62-1529">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="33f62-1529">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="33f62-1530">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="33f62-1530">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="33f62-1531">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="33f62-1531">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="33f62-1532">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="33f62-1532">Add prompting for missing template parameters.</span></span> <span data-ttu-id="33f62-1533">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="33f62-1533">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="33f62-1534">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="33f62-1534">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="33f62-1535">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="33f62-1535">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="33f62-1536">ACS</span><span class="sxs-lookup"><span data-stu-id="33f62-1536">ACS</span></span>

* <span data-ttu-id="33f62-1537">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="33f62-1537">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="33f62-1538">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="33f62-1538">Add support for ssh key password prompting.</span></span> <span data-ttu-id="33f62-1539">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="33f62-1539">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="33f62-1540">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="33f62-1540">Add support for windows clusters.</span></span> <span data-ttu-id="33f62-1541">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="33f62-1541">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="33f62-1542">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="33f62-1542">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="33f62-1543">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="33f62-1543">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="33f62-1544">AppService</span><span class="sxs-lookup"><span data-stu-id="33f62-1544">AppService</span></span>

* <span data-ttu-id="33f62-1545">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="33f62-1545">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="33f62-1546">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="33f62-1546">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="33f62-1547">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="33f62-1547">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="33f62-1548">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="33f62-1548">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="33f62-1549">DataLake</span><span class="sxs-lookup"><span data-stu-id="33f62-1549">DataLake</span></span>

* <span data-ttu-id="33f62-1550">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="33f62-1550">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="33f62-1551">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="33f62-1551">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="33f62-1552">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="33f62-1552">DocuemntDB</span></span>

* <span data-ttu-id="33f62-1553">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="33f62-1553">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="33f62-1554">VM</span><span class="sxs-lookup"><span data-stu-id="33f62-1554">VM</span></span>

* <span data-ttu-id="33f62-1555">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="33f62-1555">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="33f62-1556">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="33f62-1556">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="33f62-1557">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="33f62-1557">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="33f62-1558">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="33f62-1558">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="33f62-1559">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="33f62-1559">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="33f62-1560">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="33f62-1560">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="33f62-1561">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="33f62-1561">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="33f62-1562">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="33f62-1562">February 27, 2017</span></span>

<span data-ttu-id="33f62-1563">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="33f62-1563">Version 2.0.0</span></span>

<span data-ttu-id="33f62-1564">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="33f62-1564">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="33f62-1565">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="33f62-1565">Container Service (acs)</span></span>
- <span data-ttu-id="33f62-1566">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="33f62-1566">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="33f62-1567">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="33f62-1567">Networking</span></span>
- <span data-ttu-id="33f62-1568">Storage</span><span class="sxs-lookup"><span data-stu-id="33f62-1568">Storage</span></span>

<span data-ttu-id="33f62-1569">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="33f62-1569">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="33f62-1570">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="33f62-1570">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="33f62-1571">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="33f62-1571">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="33f62-1572">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="33f62-1572">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="33f62-1573">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="33f62-1573">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="33f62-1574">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="33f62-1574">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="33f62-1575">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="33f62-1575">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="33f62-1576">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="33f62-1576">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="33f62-1577">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="33f62-1577">Provide feedback from the command line with the `az feedback` command</span></span>

