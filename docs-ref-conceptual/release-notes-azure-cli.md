---
title: Azure CLI 2.0 リリース ノート
description: Azure CLI 2.0 の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/27/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 0e81f5723af47242f908b854045deb7d74c50c17
ms.sourcegitcommit: b5a6296c006e3a44f66892729e47d7a967267d3e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/28/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="4c7f8-103">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="4c7f8-103">Azure CLI 2.0 release notes</span></span>

## <a name="march-27-2018"></a><span data-ttu-id="4c7f8-104">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-104">March 27, 2018</span></span>

<span data-ttu-id="4c7f8-105">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="4c7f8-105">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="4c7f8-106">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-106">Core</span></span>

* <span data-ttu-id="4c7f8-107">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-107">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-108">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-108">ACS</span></span>

* <span data-ttu-id="4c7f8-109">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-109">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-110">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-110">Appservice</span></span>

* <span data-ttu-id="4c7f8-111">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-111">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="4c7f8-112">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-112">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="4c7f8-113">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4c7f8-113">Backup</span></span>

* <span data-ttu-id="4c7f8-114">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-114">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="4c7f8-115">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-115">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="4c7f8-116">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-116">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="4c7f8-117">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-117">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="4c7f8-118">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4c7f8-118">Container</span></span>

* <span data-ttu-id="4c7f8-119">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-119">Added `container exec` command.</span></span> <span data-ttu-id="4c7f8-120">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-120">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="4c7f8-121">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-121">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="4c7f8-122">内線番号</span><span class="sxs-lookup"><span data-stu-id="4c7f8-122">Extension</span></span>

* <span data-ttu-id="4c7f8-123">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-123">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="4c7f8-124">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-124">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="4c7f8-125">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-125">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="4c7f8-126">対話</span><span class="sxs-lookup"><span data-stu-id="4c7f8-126">Interactive</span></span>

* <span data-ttu-id="4c7f8-127">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-127">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="4c7f8-128">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-128">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="4c7f8-129">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-129">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="4c7f8-130">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-130">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="4c7f8-131">ラボ</span><span class="sxs-lookup"><span data-stu-id="4c7f8-131">Lab</span></span>

* <span data-ttu-id="4c7f8-132">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-132">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="4c7f8-133">監視</span><span class="sxs-lookup"><span data-stu-id="4c7f8-133">Monitor</span></span>

* <span data-ttu-id="4c7f8-134">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-134">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="4c7f8-135">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-135">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="4c7f8-136">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-136">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-137">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-137">Network</span></span>

* <span data-ttu-id="4c7f8-138">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-138">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="4c7f8-139">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4c7f8-139">Profile</span></span>

* <span data-ttu-id="4c7f8-140">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-140">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="4c7f8-141">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-141">RDBMS</span></span>

* <span data-ttu-id="4c7f8-142">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-142">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-143">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-143">Resource</span></span>

* [重大な変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="4c7f8-145">役割</span><span class="sxs-lookup"><span data-stu-id="4c7f8-145">Role</span></span>

* <span data-ttu-id="4c7f8-146">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-146">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="4c7f8-147">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-147">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="4c7f8-148">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-148">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="4c7f8-149">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-149">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="4c7f8-150">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-150">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-151">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-151">Storage</span></span>

* <span data-ttu-id="4c7f8-152">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-152">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="4c7f8-153">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-153">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-154">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-154">VM</span></span>

* <span data-ttu-id="4c7f8-155">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-155">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="4c7f8-156">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-156">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="4c7f8-157">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-157">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="4c7f8-158">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-158">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="4c7f8-159">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-159">March 13, 2018</span></span>

<span data-ttu-id="4c7f8-160">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="4c7f8-160">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="4c7f8-161">ACR</span><span class="sxs-lookup"><span data-stu-id="4c7f8-161">ACR</span></span>

* <span data-ttu-id="4c7f8-162">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-162">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="4c7f8-163">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-163">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="4c7f8-164">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-164">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-165">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-165">ACS</span></span>

* <span data-ttu-id="4c7f8-166">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-166">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="4c7f8-167">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-167">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="4c7f8-168">Advisor</span><span class="sxs-lookup"><span data-stu-id="4c7f8-168">Advisor</span></span>

* <span data-ttu-id="4c7f8-169">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-169">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="4c7f8-170">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-170">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="4c7f8-171">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-171">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span> 
* <span data-ttu-id="4c7f8-172">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-172">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="4c7f8-173">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-173">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-174">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-174">Appservice</span></span>

* <span data-ttu-id="4c7f8-175">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-175">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="4c7f8-176">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-176">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="4c7f8-177">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="4c7f8-177">Eventhubs</span></span>

* <span data-ttu-id="4c7f8-178">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-178">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="4c7f8-179">内線番号</span><span class="sxs-lookup"><span data-stu-id="4c7f8-179">Extension</span></span>

* <span data-ttu-id="4c7f8-180">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-180">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="4c7f8-181">対話</span><span class="sxs-lookup"><span data-stu-id="4c7f8-181">Interactive</span></span>

* <span data-ttu-id="4c7f8-182">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-182">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="4c7f8-183">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="4c7f8-183">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="4c7f8-184">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="4c7f8-184">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="4c7f8-185">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-185">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="4c7f8-186">監視</span><span class="sxs-lookup"><span data-stu-id="4c7f8-186">Monitor</span></span>

* <span data-ttu-id="4c7f8-187">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-187">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="4c7f8-188">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-188">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="4c7f8-189">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-189">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="4c7f8-190">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-190">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-191">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-191">Network</span></span>

* <span data-ttu-id="4c7f8-192">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-192">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="4c7f8-193">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-193">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="4c7f8-194">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-194">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="4c7f8-195">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-195">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="4c7f8-196">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4c7f8-196">Profile</span></span>

* <span data-ttu-id="4c7f8-197">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-197">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="4c7f8-198">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-198">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="4c7f8-199">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-199">RDBMS</span></span>

* <span data-ttu-id="4c7f8-200">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-200">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="4c7f8-201">Service Bus</span><span class="sxs-lookup"><span data-stu-id="4c7f8-201">Service Bus</span></span>

* <span data-ttu-id="4c7f8-202">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-202">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-203">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-203">Storage</span></span>

* <span data-ttu-id="4c7f8-204">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-204">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="4c7f8-205">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-205">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-206">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-206">VM</span></span>

* <span data-ttu-id="4c7f8-207">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-207">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="4c7f8-208">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-208">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="4c7f8-209">非推奨にしたコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-209">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="4c7f8-210">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-210">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="4c7f8-211">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-211">February 27, 2018</span></span>

<span data-ttu-id="4c7f8-212">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="4c7f8-212">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="4c7f8-213">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-213">Core</span></span>

* <span data-ttu-id="4c7f8-214">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="4c7f8-214">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="4c7f8-215">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-215">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="4c7f8-216">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-216">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-217">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-217">ACS</span></span>

* <span data-ttu-id="4c7f8-218">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-218">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="4c7f8-219">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="4c7f8-219">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="4c7f8-220">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-220">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="4c7f8-221">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-221">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-222">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-222">Appservice</span></span>

* <span data-ttu-id="4c7f8-223">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="4c7f8-223">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="4c7f8-224">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="4c7f8-224">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="4c7f8-225">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="4c7f8-225">Cognitive Services</span></span>

* <span data-ttu-id="4c7f8-226">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-226">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="4c7f8-227">消費</span><span class="sxs-lookup"><span data-stu-id="4c7f8-227">Consumption</span></span>

* <span data-ttu-id="4c7f8-228">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-228">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="4c7f8-229">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-229">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="4c7f8-230">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4c7f8-230">Container</span></span>

* <span data-ttu-id="4c7f8-231">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-231">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-232">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-232">Network</span></span>

* <span data-ttu-id="4c7f8-233">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="4c7f8-233">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-234">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-234">Resource</span></span>

* <span data-ttu-id="4c7f8-235">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-235">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="4c7f8-236">役割</span><span class="sxs-lookup"><span data-stu-id="4c7f8-236">Role</span></span>

* <span data-ttu-id="4c7f8-237">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-237">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="4c7f8-238">SQL</span><span class="sxs-lookup"><span data-stu-id="4c7f8-238">SQL</span></span>

* <span data-ttu-id="4c7f8-239">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-239">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-240">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-240">Storage</span></span>

* <span data-ttu-id="4c7f8-241">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-241">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-242">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-242">VM</span></span>

* <span data-ttu-id="4c7f8-243">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-243">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="4c7f8-244">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-244">February 13, 2018</span></span>

<span data-ttu-id="4c7f8-245">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="4c7f8-245">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="4c7f8-246">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-246">Core</span></span>

* <span data-ttu-id="4c7f8-247">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-247">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-248">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-248">ACS</span></span>

* <span data-ttu-id="4c7f8-249">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-249">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="4c7f8-250">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-250">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="4c7f8-251">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-251">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="4c7f8-252">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-252">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="4c7f8-253">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-253">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="4c7f8-254">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-254">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="4c7f8-255">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-255">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="4c7f8-256">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-256">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-257">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-257">Appservice</span></span>

* <span data-ttu-id="4c7f8-258">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-258">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="4c7f8-259">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-259">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="4c7f8-260">CDN</span><span class="sxs-lookup"><span data-stu-id="4c7f8-260">CDN</span></span>

* <span data-ttu-id="4c7f8-261">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-261">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="4c7f8-262">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4c7f8-262">Container</span></span>

* <span data-ttu-id="4c7f8-263">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-263">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="4c7f8-264">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-264">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4c7f8-265">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4c7f8-265">CosmosDB</span></span>

* <span data-ttu-id="4c7f8-266">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-266">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="4c7f8-267">内線番号</span><span class="sxs-lookup"><span data-stu-id="4c7f8-267">Extension</span></span>

* <span data-ttu-id="4c7f8-268">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-268">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="4c7f8-269">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-269">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="4c7f8-270">フィードバック</span><span class="sxs-lookup"><span data-stu-id="4c7f8-270">Feedback</span></span>

* <span data-ttu-id="4c7f8-271">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-271">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="4c7f8-272">対話</span><span class="sxs-lookup"><span data-stu-id="4c7f8-272">Interactive</span></span>

* <span data-ttu-id="4c7f8-273">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-273">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="4c7f8-274">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-274">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="4c7f8-275">IoT</span><span class="sxs-lookup"><span data-stu-id="4c7f8-275">IoT</span></span>

* <span data-ttu-id="4c7f8-276">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-276">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="4c7f8-277">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-277">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="4c7f8-278">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-278">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="4c7f8-279">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-279">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="4c7f8-280">監視</span><span class="sxs-lookup"><span data-stu-id="4c7f8-280">Monitor</span></span>

* <span data-ttu-id="4c7f8-281">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-281">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-282">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-282">Network</span></span>

* <span data-ttu-id="4c7f8-283">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-283">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="4c7f8-284">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4c7f8-284">Profile</span></span>

* <span data-ttu-id="4c7f8-285">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-285">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-286">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-286">Resource</span></span>

* <span data-ttu-id="4c7f8-287">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-287">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="4c7f8-288">役割</span><span class="sxs-lookup"><span data-stu-id="4c7f8-288">Role</span></span>

* <span data-ttu-id="4c7f8-289">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-289">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="4c7f8-290">SQL</span><span class="sxs-lookup"><span data-stu-id="4c7f8-290">SQL</span></span>

* <span data-ttu-id="4c7f8-291">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-291">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="4c7f8-292">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-292">Added `sql db rename`</span></span>
* <span data-ttu-id="4c7f8-293">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-293">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-294">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-294">Storage</span></span>

* <span data-ttu-id="4c7f8-295">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-295">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-296">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-296">VM</span></span>

* <span data-ttu-id="4c7f8-297">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-297">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="4c7f8-298">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-298">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="4c7f8-299">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-299">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="4c7f8-300">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-300">January 31, 2018</span></span>

<span data-ttu-id="4c7f8-301">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="4c7f8-301">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="4c7f8-302">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-302">Core</span></span>

* <span data-ttu-id="4c7f8-303">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-303">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="4c7f8-304">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-304">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="4c7f8-305">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-305">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="4c7f8-306">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-306">Use `--verbose` to see</span></span>
* <span data-ttu-id="4c7f8-307">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-307">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-308">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-308">ACS</span></span>

* <span data-ttu-id="4c7f8-309">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-309">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="4c7f8-310">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-310">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-311">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-311">Appservice</span></span>

* <span data-ttu-id="4c7f8-312">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-312">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="4c7f8-313">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-313">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="4c7f8-314">CDN</span><span class="sxs-lookup"><span data-stu-id="4c7f8-314">CDN</span></span>

* <span data-ttu-id="4c7f8-315">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-315">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4c7f8-316">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4c7f8-316">CosmosDB</span></span>

* <span data-ttu-id="4c7f8-317">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-317">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="4c7f8-318">対話</span><span class="sxs-lookup"><span data-stu-id="4c7f8-318">Interactive</span></span>

* <span data-ttu-id="4c7f8-319">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-319">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-320">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-320">Network</span></span>

* <span data-ttu-id="4c7f8-321">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-321">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="4c7f8-322">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-322">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="4c7f8-323">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-323">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="4c7f8-324">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-324">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="4c7f8-325">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-325">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="4c7f8-326">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-326">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="4c7f8-327">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-327">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="4c7f8-328">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-328">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="4c7f8-329">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-329">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="4c7f8-330">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-330">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="4c7f8-331">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4c7f8-331">Profile</span></span>

* <span data-ttu-id="4c7f8-332">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-332">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-333">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-333">Resource</span></span>

* <span data-ttu-id="4c7f8-334">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-334">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-335">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-335">Storage</span></span>

* <span data-ttu-id="4c7f8-336">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-336">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="4c7f8-337">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-337">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="4c7f8-338">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-338">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="4c7f8-339">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-339">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="4c7f8-340">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-340">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-341">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-341">VM</span></span>

* <span data-ttu-id="4c7f8-342">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-342">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="4c7f8-343">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-343">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="4c7f8-344">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-344">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="4c7f8-345">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-345">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="4c7f8-346">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-346">January 17, 2018</span></span>

<span data-ttu-id="4c7f8-347">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="4c7f8-347">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="4c7f8-348">ACR</span><span class="sxs-lookup"><span data-stu-id="4c7f8-348">ACR</span></span>

* <span data-ttu-id="4c7f8-349">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-349">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="4c7f8-350">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-350">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-351">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-351">ACS</span></span>

* <span data-ttu-id="4c7f8-352">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-352">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="4c7f8-353">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-353">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-354">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-354">Appservice</span></span>

* <span data-ttu-id="4c7f8-355">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-355">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="4c7f8-356">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-356">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="4c7f8-357">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-357">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="4c7f8-358">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4c7f8-358">Backup</span></span>

* <span data-ttu-id="4c7f8-359">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-359">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="4c7f8-360">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-360">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="4c7f8-361">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-361">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="4c7f8-362">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-362">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="4c7f8-363">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-363">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="4c7f8-364">Batch</span><span class="sxs-lookup"><span data-stu-id="4c7f8-364">Batch</span></span>

* <span data-ttu-id="4c7f8-365">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-365">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="4c7f8-366">クラウド</span><span class="sxs-lookup"><span data-stu-id="4c7f8-366">Cloud</span></span>

* <span data-ttu-id="4c7f8-367">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-367">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="4c7f8-368">消費</span><span class="sxs-lookup"><span data-stu-id="4c7f8-368">Consumption</span></span>

* <span data-ttu-id="4c7f8-369">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-369">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="4c7f8-370">Event Grid</span><span class="sxs-lookup"><span data-stu-id="4c7f8-370">Event Grid</span></span>

* <span data-ttu-id="4c7f8-371">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-371">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="4c7f8-372">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-372">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="4c7f8-373">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-373">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="4c7f8-374">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="4c7f8-374">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="4c7f8-375">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-375">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="4c7f8-376">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-376">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="4c7f8-377">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-377">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="4c7f8-378">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-378">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="4c7f8-379">対話</span><span class="sxs-lookup"><span data-stu-id="4c7f8-379">Interactive</span></span>

* <span data-ttu-id="4c7f8-380">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-380">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="4c7f8-381">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-381">Fixed errors on startup</span></span>
* <span data-ttu-id="4c7f8-382">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-382">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="4c7f8-383">IoT</span><span class="sxs-lookup"><span data-stu-id="4c7f8-383">IoT</span></span>

* <span data-ttu-id="4c7f8-384">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-384">Added support for device provisioning service</span></span>
* <span data-ttu-id="4c7f8-385">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-385">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="4c7f8-386">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-386">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="4c7f8-387">監視</span><span class="sxs-lookup"><span data-stu-id="4c7f8-387">Monitor</span></span>

* <span data-ttu-id="4c7f8-388">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-388">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="4c7f8-389">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-389">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="4c7f8-390">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-390">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-391">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-391">Network</span></span>

* <span data-ttu-id="4c7f8-392">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-392">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="4c7f8-393">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-393">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="4c7f8-394">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4c7f8-394">Profile</span></span>

* <span data-ttu-id="4c7f8-395">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-395">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="4c7f8-396">役割</span><span class="sxs-lookup"><span data-stu-id="4c7f8-396">Role</span></span>

* <span data-ttu-id="4c7f8-397">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-397">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="4c7f8-398">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4c7f8-398">Service Fabric</span></span>

* <span data-ttu-id="4c7f8-399">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-399">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="4c7f8-400">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-400">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-401">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-401">VM</span></span>

* <span data-ttu-id="4c7f8-402">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="4c7f8-402">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="4c7f8-403">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-403">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="4c7f8-404">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-404">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="4c7f8-405">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-405">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="4c7f8-406">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-406">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="4c7f8-407">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-407">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="4c7f8-408">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-408">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="4c7f8-409">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-409">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="4c7f8-410">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-410">December 19, 2017</span></span>

<span data-ttu-id="4c7f8-411">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="4c7f8-411">Version 2.0.23</span></span>

* <span data-ttu-id="4c7f8-412">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-412">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="4c7f8-413">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4c7f8-413">Container</span></span>

* <span data-ttu-id="4c7f8-414">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-414">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-415">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-415">Network</span></span>

* <span data-ttu-id="4c7f8-416">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-416">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="4c7f8-417">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-417">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-418">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-418">Storage</span></span>

* <span data-ttu-id="4c7f8-419">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-419">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-420">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-420">VM</span></span>

* <span data-ttu-id="4c7f8-421">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-421">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="4c7f8-422">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-422">December 5, 2017</span></span>

<span data-ttu-id="4c7f8-423">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="4c7f8-423">Version 2.0.22</span></span>

* <span data-ttu-id="4c7f8-424">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-424">Removed `az component` commands.</span></span> <span data-ttu-id="4c7f8-425">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="4c7f8-425">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="4c7f8-426">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-426">Core</span></span>
* <span data-ttu-id="4c7f8-427">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-427">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="4c7f8-428">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-428">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-429">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-429">ACS</span></span>

* <span data-ttu-id="4c7f8-430">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-430">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="4c7f8-431">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-431">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="4c7f8-432">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-432">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="4c7f8-433">Advisor</span><span class="sxs-lookup"><span data-stu-id="4c7f8-433">Advisor</span></span>

* <span data-ttu-id="4c7f8-434">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-434">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-435">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-435">Appservice</span></span>

* <span data-ttu-id="4c7f8-436">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-436">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="4c7f8-437">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-437">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="4c7f8-438">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-438">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="4c7f8-439">消費</span><span class="sxs-lookup"><span data-stu-id="4c7f8-439">Consumption</span></span>

* <span data-ttu-id="4c7f8-440">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-440">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="4c7f8-441">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4c7f8-441">Container</span></span>

* <span data-ttu-id="4c7f8-442">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-442">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="4c7f8-443">監視</span><span class="sxs-lookup"><span data-stu-id="4c7f8-443">Monitor</span></span>

* <span data-ttu-id="4c7f8-444">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-444">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-445">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-445">Resource</span></span>

* <span data-ttu-id="4c7f8-446">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-446">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="4c7f8-447">役割</span><span class="sxs-lookup"><span data-stu-id="4c7f8-447">Role</span></span>

* <span data-ttu-id="4c7f8-448">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-448">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="4c7f8-449">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-449">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="4c7f8-450">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-450">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="4c7f8-451">SQL</span><span class="sxs-lookup"><span data-stu-id="4c7f8-451">SQL</span></span>

* <span data-ttu-id="4c7f8-452">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-452">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="4c7f8-453">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-453">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-454">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-454">VM</span></span>

* <span data-ttu-id="4c7f8-455">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-455">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="4c7f8-456">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-456">November 14, 2017</span></span>

<span data-ttu-id="4c7f8-457">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="4c7f8-457">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="4c7f8-458">ACR</span><span class="sxs-lookup"><span data-stu-id="4c7f8-458">ACR</span></span>

* <span data-ttu-id="4c7f8-459">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-459">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="4c7f8-460">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-460">ACS</span></span>

* <span data-ttu-id="4c7f8-461">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-461">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="4c7f8-462">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-462">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="4c7f8-463">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-463">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="4c7f8-464">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-464">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="4c7f8-465">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-465">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-466">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-466">Appservice</span></span>

* <span data-ttu-id="4c7f8-467">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-467">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="4c7f8-468">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-468">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="4c7f8-469">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-469">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="4c7f8-470">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-470">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="4c7f8-471">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-471">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="4c7f8-472">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-472">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="4c7f8-473">Batch</span><span class="sxs-lookup"><span data-stu-id="4c7f8-473">Batch</span></span>

* <span data-ttu-id="4c7f8-474">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-474">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="4c7f8-475">Batchai</span><span class="sxs-lookup"><span data-stu-id="4c7f8-475">Batchai</span></span>

* <span data-ttu-id="4c7f8-476">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-476">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="4c7f8-477">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-477">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="4c7f8-478">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-478">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="4c7f8-479">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-479">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="4c7f8-480">クラウド</span><span class="sxs-lookup"><span data-stu-id="4c7f8-480">Cloud</span></span>

* <span data-ttu-id="4c7f8-481">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-481">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="4c7f8-482">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4c7f8-482">Container</span></span>

* <span data-ttu-id="4c7f8-483">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-483">Added support to open multiple ports</span></span>
* <span data-ttu-id="4c7f8-484">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-484">Added container group restart policy</span></span>
* <span data-ttu-id="4c7f8-485">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-485">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="4c7f8-486">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-486">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="4c7f8-487">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="4c7f8-487">Data Lake Analytics</span></span>

* <span data-ttu-id="4c7f8-488">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-488">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="4c7f8-489">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4c7f8-489">Data Lake Store</span></span>

* <span data-ttu-id="4c7f8-490">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-490">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="4c7f8-491">内線番号</span><span class="sxs-lookup"><span data-stu-id="4c7f8-491">Extension</span></span>

* <span data-ttu-id="4c7f8-492">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-492">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="4c7f8-493">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-493">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="4c7f8-494">IoT</span><span class="sxs-lookup"><span data-stu-id="4c7f8-494">IoT</span></span>

* <span data-ttu-id="4c7f8-495">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-495">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="4c7f8-496">監視</span><span class="sxs-lookup"><span data-stu-id="4c7f8-496">Monitor</span></span>

* <span data-ttu-id="4c7f8-497">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-497">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-498">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-498">Network</span></span>

* <span data-ttu-id="4c7f8-499">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-499">Added support for CAA DNS records</span></span>
* <span data-ttu-id="4c7f8-500">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-500">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="4c7f8-501">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-501">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="4c7f8-502">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-502">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="4c7f8-503">Reservations</span><span class="sxs-lookup"><span data-stu-id="4c7f8-503">Reservations</span></span>

* <span data-ttu-id="4c7f8-504">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-504">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-505">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-505">Resource</span></span>

* <span data-ttu-id="4c7f8-506">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-506">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="4c7f8-507">SQL</span><span class="sxs-lookup"><span data-stu-id="4c7f8-507">SQL</span></span>

* <span data-ttu-id="4c7f8-508">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-508">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-509">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-509">Storage</span></span>

* <span data-ttu-id="4c7f8-510">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-510">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="4c7f8-511">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-511">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="4c7f8-512">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-512">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="4c7f8-513">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-513">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="4c7f8-514">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-514">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="4c7f8-515">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-515">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="4c7f8-516">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-516">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-517">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-517">VM</span></span>

* <span data-ttu-id="4c7f8-518">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-518">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="4c7f8-519">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-519">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="4c7f8-520">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-520">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="4c7f8-521">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-521">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="4c7f8-522">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-522">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="4c7f8-523">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-523">October 24, 2017</span></span>

<span data-ttu-id="4c7f8-524">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="4c7f8-524">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="4c7f8-525">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-525">Core</span></span>

* <span data-ttu-id="4c7f8-526">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-526">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="4c7f8-527">ACR</span><span class="sxs-lookup"><span data-stu-id="4c7f8-527">ACR</span></span>

* <span data-ttu-id="4c7f8-528">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-528">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="4c7f8-529">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-529">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="4c7f8-530">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-530">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-531">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-531">ACS</span></span>

* <span data-ttu-id="4c7f8-532">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-532">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="4c7f8-533">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-533">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-534">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-534">Appservice</span></span>

* <span data-ttu-id="4c7f8-535">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-535">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="4c7f8-536">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="4c7f8-536">Component</span></span>

* <span data-ttu-id="4c7f8-537">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-537">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="4c7f8-538">監視</span><span class="sxs-lookup"><span data-stu-id="4c7f8-538">Monitor</span></span>

* <span data-ttu-id="4c7f8-539">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-539">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-540">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-540">Resource</span></span>

* <span data-ttu-id="4c7f8-541">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-541">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="4c7f8-542">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-542">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-543">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-543">VM</span></span>

* <span data-ttu-id="4c7f8-544">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-544">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="4c7f8-545">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-545">October 9, 2017</span></span>

<span data-ttu-id="4c7f8-546">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="4c7f8-546">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="4c7f8-547">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-547">Core</span></span>

* <span data-ttu-id="4c7f8-548">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-548">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-549">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-549">Appservice</span></span>

* <span data-ttu-id="4c7f8-550">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-550">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="4c7f8-551">Batch</span><span class="sxs-lookup"><span data-stu-id="4c7f8-551">Batch</span></span>

* <span data-ttu-id="4c7f8-552">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-552">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="4c7f8-553">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-553">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="4c7f8-554">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-554">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="4c7f8-555">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-555">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="4c7f8-556">Batchai</span><span class="sxs-lookup"><span data-stu-id="4c7f8-556">Batchai</span></span>

* <span data-ttu-id="4c7f8-557">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-557">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="4c7f8-558">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4c7f8-558">Keyvault</span></span>

* <span data-ttu-id="4c7f8-559">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-559">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="4c7f8-560">(#4448)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-560">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="4c7f8-561">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-561">Network</span></span>

* <span data-ttu-id="4c7f8-562">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-562">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="4c7f8-563">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-563">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-564">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-564">Resource</span></span>

* <span data-ttu-id="4c7f8-565">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-565">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="4c7f8-566">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-566">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="4c7f8-567">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-567">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="4c7f8-568">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-568">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="4c7f8-569">SQL</span><span class="sxs-lookup"><span data-stu-id="4c7f8-569">Sql</span></span>

* <span data-ttu-id="4c7f8-570">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-570">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="4c7f8-571">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-571">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="4c7f8-572">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-572">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-573">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-573">Storage</span></span>

* <span data-ttu-id="4c7f8-574">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-574">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-575">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-575">Vm</span></span>

* <span data-ttu-id="4c7f8-576">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-576">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="4c7f8-577">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-577">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="4c7f8-578">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-578">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="4c7f8-579">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-579">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="4c7f8-580">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-580">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="4c7f8-581">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-581">September 22, 2017</span></span>

<span data-ttu-id="4c7f8-582">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="4c7f8-582">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-583">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-583">Resource</span></span>

* <span data-ttu-id="4c7f8-584">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-584">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="4c7f8-585">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-585">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="4c7f8-586">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-586">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="4c7f8-587">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-587">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-588">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-588">Network</span></span>

* <span data-ttu-id="4c7f8-589">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-589">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="4c7f8-590">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-590">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="4c7f8-591">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-591">Added `asg` application security group commands</span></span>
* <span data-ttu-id="4c7f8-592">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-592">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="4c7f8-593">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-593">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="4c7f8-594">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-594">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="4c7f8-595">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-595">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-596">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-596">Storage</span></span>

* <span data-ttu-id="4c7f8-597">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-597">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="4c7f8-598">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="4c7f8-598">Eventgrid</span></span>

* <span data-ttu-id="4c7f8-599">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-599">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="4c7f8-600">SQL</span><span class="sxs-lookup"><span data-stu-id="4c7f8-600">SQL</span></span>

* <span data-ttu-id="4c7f8-601">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-601">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="4c7f8-602">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-602">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="4c7f8-603">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-603">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="4c7f8-604">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4c7f8-604">Keyvault</span></span>

* <span data-ttu-id="4c7f8-605">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-605">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-606">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-606">VM</span></span>

* <span data-ttu-id="4c7f8-607">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-607">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="4c7f8-608">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-608">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="4c7f8-609">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-609">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="4c7f8-610">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-610">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="4c7f8-611">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-611">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="4c7f8-612">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-612">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-613">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-613">ACS</span></span>

* <span data-ttu-id="4c7f8-614">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-614">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-615">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-615">Appservice</span></span>

* <span data-ttu-id="4c7f8-616">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-616">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="4c7f8-617">バックアップ</span><span class="sxs-lookup"><span data-stu-id="4c7f8-617">Backup</span></span>

* <span data-ttu-id="4c7f8-618">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-618">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="4c7f8-619">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-619">September 11, 2017</span></span>

<span data-ttu-id="4c7f8-620">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="4c7f8-620">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="4c7f8-621">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-621">Core</span></span>

* <span data-ttu-id="4c7f8-622">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-622">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="4c7f8-623">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-623">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-624">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-624">Acs</span></span>

* <span data-ttu-id="4c7f8-625">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-625">Added `acs list-locations` command</span></span>
* <span data-ttu-id="4c7f8-626">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-626">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-627">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-627">Appservice</span></span>

* <span data-ttu-id="4c7f8-628">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-628">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="4c7f8-629">CDN</span><span class="sxs-lookup"><span data-stu-id="4c7f8-629">CDN</span></span>

* <span data-ttu-id="4c7f8-630">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-630">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="4c7f8-631">内線番号</span><span class="sxs-lookup"><span data-stu-id="4c7f8-631">Extension</span></span>

* <span data-ttu-id="4c7f8-632">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-632">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="4c7f8-633">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4c7f8-633">Keyvault</span></span>

* <span data-ttu-id="4c7f8-634">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-634">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-635">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-635">Network</span></span>

* <span data-ttu-id="4c7f8-636">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-636">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="4c7f8-637">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-637">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="4c7f8-638">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-638">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="4c7f8-639">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-639">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="4c7f8-640">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-640">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-641">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-641">Resource</span></span>

* <span data-ttu-id="4c7f8-642">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-642">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="4c7f8-643">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-643">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="4c7f8-644">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-644">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="4c7f8-645">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-645">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="4c7f8-646">SQL</span><span class="sxs-lookup"><span data-stu-id="4c7f8-646">SQL</span></span>

* <span data-ttu-id="4c7f8-647">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-647">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-648">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-648">VM</span></span>

* <span data-ttu-id="4c7f8-649">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="4c7f8-649">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="4c7f8-650">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="4c7f8-650">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="4c7f8-651">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-651">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="4c7f8-652">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="4c7f8-652">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="4c7f8-653">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="4c7f8-653">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="4c7f8-654">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-654">August 31, 2017</span></span>

<span data-ttu-id="4c7f8-655">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="4c7f8-655">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="4c7f8-656">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4c7f8-656">Keyvault</span></span>

* <span data-ttu-id="4c7f8-657">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-657">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="4c7f8-658">SF</span><span class="sxs-lookup"><span data-stu-id="4c7f8-658">Sf</span></span>

* <span data-ttu-id="4c7f8-659">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-659">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-660">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-660">Storage</span></span>

* <span data-ttu-id="4c7f8-661">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-661">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="4c7f8-662">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-662">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="4c7f8-663">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-663">August 28, 2017</span></span>

<span data-ttu-id="4c7f8-664">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="4c7f8-664">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="4c7f8-665">CLI</span><span class="sxs-lookup"><span data-stu-id="4c7f8-665">CLI</span></span>

* <span data-ttu-id="4c7f8-666">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-666">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-667">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-667">ACS</span></span>

* <span data-ttu-id="4c7f8-668">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-668">Corrected preview regions</span></span>
* <span data-ttu-id="4c7f8-669">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-669">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="4c7f8-670">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-670">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-671">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-671">Appservice</span></span>

* <span data-ttu-id="4c7f8-672">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-672">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="4c7f8-673">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-673">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="4c7f8-674">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-674">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="4c7f8-675">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-675">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="4c7f8-676">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="4c7f8-676">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="4c7f8-677">IoT</span><span class="sxs-lookup"><span data-stu-id="4c7f8-677">IoT</span></span>

* <span data-ttu-id="4c7f8-678">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-678">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-679">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-679">Network</span></span>

* <span data-ttu-id="4c7f8-680">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-680">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="4c7f8-681">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-681">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="4c7f8-682">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-682">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="4c7f8-683">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-683">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="4c7f8-684">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-684">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="4c7f8-685">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4c7f8-685">Profile</span></span>

* <span data-ttu-id="4c7f8-686">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-686">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="4c7f8-687">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4c7f8-687">Service Fabric</span></span>

* <span data-ttu-id="4c7f8-688">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-688">Preview release</span></span>
* <span data-ttu-id="4c7f8-689">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-689">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="4c7f8-690">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-690">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="4c7f8-691">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-691">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-692">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-692">Storage</span></span>

* <span data-ttu-id="4c7f8-693">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-693">Enabled setting blob tier</span></span>
* <span data-ttu-id="4c7f8-694">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-694">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="4c7f8-695">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-695">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="4c7f8-696">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-696">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="4c7f8-697">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-697">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="4c7f8-698">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="4c7f8-698">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-699">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-699">VM</span></span>

* <span data-ttu-id="4c7f8-700">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-700">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="4c7f8-701">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-701">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="4c7f8-702">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-702">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="4c7f8-703">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-703">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="4c7f8-704">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-704">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="4c7f8-705">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-705">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="4c7f8-706">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-706">August 15, 2017</span></span>

<span data-ttu-id="4c7f8-707">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="4c7f8-707">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-708">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-708">ACS</span></span>

* <span data-ttu-id="4c7f8-709">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-709">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-710">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-710">Appservice</span></span>

* <span data-ttu-id="4c7f8-711">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-711">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="4c7f8-712">Event Grid</span><span class="sxs-lookup"><span data-stu-id="4c7f8-712">Event Grid</span></span>

* <span data-ttu-id="4c7f8-713">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-713">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="4c7f8-714">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-714">August 11, 2017</span></span>

<span data-ttu-id="4c7f8-715">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="4c7f8-715">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-716">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-716">ACS</span></span>

* <span data-ttu-id="4c7f8-717">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-717">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="4c7f8-718">Batch</span><span class="sxs-lookup"><span data-stu-id="4c7f8-718">Batch</span></span>

* <span data-ttu-id="4c7f8-719">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-719">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="4c7f8-720">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-720">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="4c7f8-721">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-721">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="4c7f8-722">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-722">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="4c7f8-723">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-723">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="4c7f8-724">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-724">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="4c7f8-725">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="4c7f8-725">Component</span></span>

* <span data-ttu-id="4c7f8-726">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-726">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="4c7f8-727">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4c7f8-727">Container</span></span>

* <span data-ttu-id="4c7f8-728">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-728">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="4c7f8-729">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4c7f8-729">Data Lake Store</span></span>

* <span data-ttu-id="4c7f8-730">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-730">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="4c7f8-731">Event Grid</span><span class="sxs-lookup"><span data-stu-id="4c7f8-731">Event Grid</span></span>

* <span data-ttu-id="4c7f8-732">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-732">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-733">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-733">Network</span></span>

* <span data-ttu-id="4c7f8-734">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-734">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="4c7f8-735">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-735">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="4c7f8-736">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-736">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="4c7f8-737">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-737">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="4c7f8-738">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4c7f8-738">Profile</span></span>

* <span data-ttu-id="4c7f8-739">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-739">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-740">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-740">Storage</span></span>

* <span data-ttu-id="4c7f8-741">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-741">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-742">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-742">VM</span></span>

* <span data-ttu-id="4c7f8-743">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-743">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="4c7f8-744">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-744">Exposed `list-skus` command</span></span>
* <span data-ttu-id="4c7f8-745">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-745">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="4c7f8-746">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-746">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="4c7f8-747">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-747">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="4c7f8-748">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-748">July 28, 2017</span></span>

<span data-ttu-id="4c7f8-749">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="4c7f8-749">Version 2.0.12</span></span>

* <span data-ttu-id="4c7f8-750">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-750">Added container commands</span></span>
* <span data-ttu-id="4c7f8-751">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-751">Added billing and consumption modules</span></span>

```
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

### <a name="core"></a><span data-ttu-id="4c7f8-752">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-752">Core</span></span>

* <span data-ttu-id="4c7f8-753">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-753">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="4c7f8-754">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-754">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="4c7f8-755">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-755">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="4c7f8-756">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-756">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="4c7f8-757">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-757">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="4c7f8-758">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-758">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="4c7f8-759">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-759">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="4c7f8-760">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-760">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="4c7f8-761">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-761">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="4c7f8-762">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-762">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="4c7f8-763">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-763">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="4c7f8-764">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-764">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="4c7f8-765">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-765">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="4c7f8-766">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-766">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="4c7f8-767">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-767">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="4c7f8-768">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-768">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="4c7f8-769">ACR</span><span class="sxs-lookup"><span data-stu-id="4c7f8-769">ACR</span></span>

* <span data-ttu-id="4c7f8-770">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-770">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="4c7f8-771">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-771">Support SKU update for managed registries</span></span>
* <span data-ttu-id="4c7f8-772">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-772">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="4c7f8-773">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-773">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="4c7f8-774">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-774">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="4c7f8-775">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-775">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-776">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-776">ACS</span></span>

* <span data-ttu-id="4c7f8-777">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-777">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-778">Appservice</span><span class="sxs-lookup"><span data-stu-id="4c7f8-778">Appservice</span></span>

* <span data-ttu-id="4c7f8-779">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-779">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="4c7f8-780">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-780">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="4c7f8-781">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-781">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="4c7f8-782">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-782">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="4c7f8-783">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-783">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="4c7f8-784">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-784">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="4c7f8-785">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-785">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="4c7f8-786">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-786">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="4c7f8-787">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-787">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="4c7f8-788">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="4c7f8-788">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="4c7f8-789">Batch</span><span class="sxs-lookup"><span data-stu-id="4c7f8-789">Batch</span></span>

* <span data-ttu-id="4c7f8-790">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-790">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="4c7f8-791">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-791">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="4c7f8-792">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-792">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="4c7f8-793">CDN</span><span class="sxs-lookup"><span data-stu-id="4c7f8-793">CDN</span></span>

* <span data-ttu-id="4c7f8-794">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-794">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="4c7f8-795">クラウド</span><span class="sxs-lookup"><span data-stu-id="4c7f8-795">Cloud</span></span>

* <span data-ttu-id="4c7f8-796">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-796">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="4c7f8-797">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="4c7f8-797">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="4c7f8-798">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-798">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="4c7f8-799">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-799">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="4c7f8-800">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-800">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4c7f8-801">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4c7f8-801">CosmosDB</span></span>

* <span data-ttu-id="4c7f8-802">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-802">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="4c7f8-803">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-803">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="4c7f8-804">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="4c7f8-804">Data Lake Analytics</span></span>

* <span data-ttu-id="4c7f8-805">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-805">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="4c7f8-806">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-806">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="4c7f8-807">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-807">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="4c7f8-808">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4c7f8-808">Data Lake Store</span></span>

* <span data-ttu-id="4c7f8-809">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-809">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="4c7f8-810">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-810">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="4c7f8-811">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-811">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="4c7f8-812">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-812">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="4c7f8-813">対話</span><span class="sxs-lookup"><span data-stu-id="4c7f8-813">Interactive</span></span>

* <span data-ttu-id="4c7f8-814">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-814">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="4c7f8-815">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-815">Increased test coverage</span></span>
* <span data-ttu-id="4c7f8-816">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-816">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="4c7f8-817">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-817">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="4c7f8-818">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-818">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="4c7f8-819">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-819">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="4c7f8-820">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-820">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="4c7f8-821">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-821">Added `--progress` flag</span></span>
* <span data-ttu-id="4c7f8-822">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-822">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="4c7f8-823">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-823">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="4c7f8-824">IoT</span><span class="sxs-lookup"><span data-stu-id="4c7f8-824">IoT</span></span>

* <span data-ttu-id="4c7f8-825">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-825">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="4c7f8-826">(#3934)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-826">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="4c7f8-827">Key Vault</span><span class="sxs-lookup"><span data-stu-id="4c7f8-827">Key vault</span></span>

* <span data-ttu-id="4c7f8-828">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-828">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="4c7f8-829">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4c7f8-829">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="4c7f8-830">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4c7f8-830">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="4c7f8-831">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4c7f8-831">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="4c7f8-832">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4c7f8-832">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="4c7f8-833">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-833">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="4c7f8-834">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-834">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="4c7f8-835">(#3307)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-835">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="4c7f8-836">ラボ</span><span class="sxs-lookup"><span data-stu-id="4c7f8-836">Lab</span></span>

* <span data-ttu-id="4c7f8-837">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-837">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="4c7f8-838">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-838">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="4c7f8-839">監視</span><span class="sxs-lookup"><span data-stu-id="4c7f8-839">Monitor</span></span>

* <span data-ttu-id="4c7f8-840">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-840">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="4c7f8-841">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-841">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="4c7f8-842">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-842">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="4c7f8-843">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-843">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="4c7f8-844">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-844">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="4c7f8-845">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-845">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="4c7f8-846">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-846">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="4c7f8-847">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-847">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="4c7f8-848">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-848">`location` no longer required</span></span>
  * <span data-ttu-id="4c7f8-849">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-849">Add name and ID support for target</span></span>
  * <span data-ttu-id="4c7f8-850">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-850">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="4c7f8-851">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-851">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="4c7f8-852">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-852">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="4c7f8-853">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-853">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="4c7f8-854">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-854">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="4c7f8-855">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-855">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-856">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-856">Network</span></span>

* <span data-ttu-id="4c7f8-857">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-857">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="4c7f8-858">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-858">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="4c7f8-859">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-859">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="4c7f8-860">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-860">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="4c7f8-861">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-861">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="4c7f8-862">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-862">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="4c7f8-863">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-863">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="4c7f8-864">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-864">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="4c7f8-865">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-865">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="4c7f8-866">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-866">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="4c7f8-867">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-867">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="4c7f8-868">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-868">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="4c7f8-869">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-869">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="4c7f8-870">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-870">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="4c7f8-871">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-871">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="4c7f8-872">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-872">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="4c7f8-873">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-873">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="4c7f8-874">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-874">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="4c7f8-875">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-875">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="4c7f8-876">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-876">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="4c7f8-877">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-877">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="4c7f8-878">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-878">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="4c7f8-879">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-879">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="4c7f8-880">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-880">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="4c7f8-881">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-881">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="4c7f8-882">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-882">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="4c7f8-883">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-883">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="4c7f8-884">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4c7f8-884">Profile</span></span>

* <span data-ttu-id="4c7f8-885">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-885">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="4c7f8-886">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-886">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="4c7f8-887">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-887">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="4c7f8-888">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-888">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="4c7f8-889">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-889">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="4c7f8-890">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-890">RDBMS</span></span>

* <span data-ttu-id="4c7f8-891">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-891">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="4c7f8-892">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-892">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="4c7f8-893">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-893">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="4c7f8-894">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-894">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-895">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-895">Resource</span></span>

* <span data-ttu-id="4c7f8-896">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-896">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="4c7f8-897">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-897">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="4c7f8-898">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-898">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="4c7f8-899">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-899">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="4c7f8-900">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-900">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="4c7f8-901">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-901">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="4c7f8-902">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-902">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="4c7f8-903">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-903">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="4c7f8-904">役割</span><span class="sxs-lookup"><span data-stu-id="4c7f8-904">Role</span></span>

* <span data-ttu-id="4c7f8-905">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-905">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="4c7f8-906">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-906">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="4c7f8-907">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-907">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="4c7f8-908">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-908">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="4c7f8-909">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-909">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="4c7f8-910">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4c7f8-910">Service Fabric</span></span>
* <span data-ttu-id="4c7f8-911">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-911">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="4c7f8-912">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-912">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="4c7f8-913">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-913">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="4c7f8-914">SQL</span><span class="sxs-lookup"><span data-stu-id="4c7f8-914">SQL</span></span>

* <span data-ttu-id="4c7f8-915">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-915">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="4c7f8-916">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-916">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="4c7f8-917">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-917">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-918">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-918">Storage</span></span>

* <span data-ttu-id="4c7f8-919">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-919">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="4c7f8-920">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-920">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="4c7f8-921">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-921">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="4c7f8-922">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-922">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="4c7f8-923">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-923">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="4c7f8-924">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-924">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-925">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-925">VM</span></span>

* <span data-ttu-id="4c7f8-926">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-926">Support configuring nsg</span></span>
* <span data-ttu-id="4c7f8-927">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-927">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="4c7f8-928">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="4c7f8-928">Support managed service identities</span></span>
* <span data-ttu-id="4c7f8-929">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-929">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="4c7f8-930">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-930">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="4c7f8-931">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-931">May 10, 2017</span></span>

<span data-ttu-id="4c7f8-932">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="4c7f8-932">Version 2.0.6</span></span>

* <span data-ttu-id="4c7f8-933">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-933">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="4c7f8-934">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-934">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="4c7f8-935">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-935">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="4c7f8-936">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-936">Include Cognitive Services module</span></span>
* <span data-ttu-id="4c7f8-937">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-937">Include Service Fabric module</span></span>
* <span data-ttu-id="4c7f8-938">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-938">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="4c7f8-939">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-939">Add support for CDN commands</span></span>
* <span data-ttu-id="4c7f8-940">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-940">Remove Container module</span></span>
* <span data-ttu-id="4c7f8-941">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-941">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="4c7f8-942">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-942">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="4c7f8-943">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-943">Core</span></span>

* <span data-ttu-id="4c7f8-944">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-944">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="4c7f8-945">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-945">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="4c7f8-946">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-946">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="4c7f8-947">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-947">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="4c7f8-948">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-948">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="4c7f8-949">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-949">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="4c7f8-950">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-950">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="4c7f8-951">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-951">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="4c7f8-952">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-952">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="4c7f8-953">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="4c7f8-953">core: Improved performance</span></span>
* <span data-ttu-id="4c7f8-954">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-954">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="4c7f8-955">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-955">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-956">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-956">ACS</span></span>

* <span data-ttu-id="4c7f8-957">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-957">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="4c7f8-958">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-958">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="4c7f8-959">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-959">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="4c7f8-960">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-960">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-961">AppService</span><span class="sxs-lookup"><span data-stu-id="4c7f8-961">AppService</span></span>

* <span data-ttu-id="4c7f8-962">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-962">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="4c7f8-963">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-963">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="4c7f8-964">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-964">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="4c7f8-965">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-965">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="4c7f8-966">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-966">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="4c7f8-967">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-967">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="4c7f8-968">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="4c7f8-968">support slot swap with preview</span></span>
* <span data-ttu-id="4c7f8-969">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-969">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="4c7f8-970">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-970">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4c7f8-971">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4c7f8-971">CosmosDB</span></span>

* <span data-ttu-id="4c7f8-972">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-972">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="4c7f8-973">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-973">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="4c7f8-974">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-974">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="4c7f8-975">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-975">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="4c7f8-976">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="4c7f8-976">Data Lake Analytics</span></span>

* <span data-ttu-id="4c7f8-977">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-977">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="4c7f8-978">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-978">Add support for new catalog item type: package.</span></span> <span data-ttu-id="4c7f8-979">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-979">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="4c7f8-980">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-980">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="4c7f8-981">テーブル</span><span class="sxs-lookup"><span data-stu-id="4c7f8-981">Table</span></span>
  * <span data-ttu-id="4c7f8-982">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="4c7f8-982">Table valued function</span></span>
  * <span data-ttu-id="4c7f8-983">表示</span><span class="sxs-lookup"><span data-stu-id="4c7f8-983">View</span></span>
  * <span data-ttu-id="4c7f8-984">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-984">Table Statistics.</span></span> <span data-ttu-id="4c7f8-985">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="4c7f8-985">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="4c7f8-986">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4c7f8-986">Data Lake Store</span></span>

* <span data-ttu-id="4c7f8-987">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-987">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="4c7f8-988">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-988">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="4c7f8-989">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="4c7f8-989">missed help for access show.</span></span> <span data-ttu-id="4c7f8-990">追加しました </span><span class="sxs-lookup"><span data-stu-id="4c7f8-990">adding it.</span></span> <span data-ttu-id="4c7f8-991">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-991">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="4c7f8-992">検索</span><span class="sxs-lookup"><span data-stu-id="4c7f8-992">Find</span></span>

* <span data-ttu-id="4c7f8-993">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-993">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="4c7f8-994">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4c7f8-994">KeyVault</span></span>

* <span data-ttu-id="4c7f8-995">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-995">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="4c7f8-996">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-996">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="4c7f8-997">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-997">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="4c7f8-998">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-998">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="4c7f8-999">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-999">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="4c7f8-1000">ラボ</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1000">Lab</span></span>

* <span data-ttu-id="4c7f8-1001">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1001">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="4c7f8-1002">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1002">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="4c7f8-1003">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1003">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="4c7f8-1004">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1004">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="4c7f8-1005">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1005">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="4c7f8-1006">監視</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1006">Monitor</span></span>

* <span data-ttu-id="4c7f8-1007">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1007">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="4c7f8-1008">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1008">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="4c7f8-1009">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1009">Network</span></span>

* <span data-ttu-id="4c7f8-1010">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1010">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="4c7f8-1011">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1011">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="4c7f8-1012">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1012">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="4c7f8-1013">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1013">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="4c7f8-1014">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1014">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="4c7f8-1015">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1015">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="4c7f8-1016">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1016">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="4c7f8-1017">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1017">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="4c7f8-1018">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1018">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="4c7f8-1019">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1019">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="4c7f8-1020">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1020">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="4c7f8-1021">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1021">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="4c7f8-1022">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1022">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="4c7f8-1023">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1023">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="4c7f8-1024">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1024">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="4c7f8-1025">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1025">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="4c7f8-1026">プロファイル</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1026">Profile</span></span>

* <span data-ttu-id="4c7f8-1027">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1027">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="4c7f8-1028">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1028">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="4c7f8-1029">Redis</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1029">Redis</span></span>

* <span data-ttu-id="4c7f8-1030">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1030">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="4c7f8-1031">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1031">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="4c7f8-1032">リソース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1032">Resource</span></span>

* <span data-ttu-id="4c7f8-1033">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1033">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="4c7f8-1034">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1034">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="4c7f8-1035">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1035">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="4c7f8-1036">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="4c7f8-1036">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="4c7f8-1037">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1037">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="4c7f8-1038">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="4c7f8-1038">Add docs for az lock update.</span></span> <span data-ttu-id="4c7f8-1039">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1039">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="4c7f8-1040">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="4c7f8-1040">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="4c7f8-1041">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1041">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="4c7f8-1042">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1042">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="4c7f8-1043">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1043">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="4c7f8-1044">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1044">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="4c7f8-1045">役割</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1045">Role</span></span>

* <span data-ttu-id="4c7f8-1046">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1046">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="4c7f8-1047">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1047">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="4c7f8-1048">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1048">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="4c7f8-1049">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1049">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="4c7f8-1050">SQL</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1050">SQL</span></span>

* <span data-ttu-id="4c7f8-1051">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1051">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="4c7f8-1052">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1052">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="4c7f8-1053">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1053">Storage</span></span>

* <span data-ttu-id="4c7f8-1054">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1054">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="4c7f8-1055">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1055">Add support for incremental blob copy</span></span>
* <span data-ttu-id="4c7f8-1056">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1056">Add support for large block blob upload</span></span>
* <span data-ttu-id="4c7f8-1057">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1057">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-1058">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1058">VM</span></span>

* <span data-ttu-id="4c7f8-1059">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1059">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="4c7f8-1060">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1060">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="4c7f8-1061">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1061">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="4c7f8-1062">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1062">az vm/vmss disk</span></span>
  3. <span data-ttu-id="4c7f8-1063">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1063">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="4c7f8-1064">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1064">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="4c7f8-1065">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1065">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="4c7f8-1066">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1066">April 3, 2017</span></span>

<span data-ttu-id="4c7f8-1067">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1067">Version 2.0.2</span></span>

<span data-ttu-id="4c7f8-1068">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1068">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="4c7f8-1069">コア</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1069">Core</span></span>

* <span data-ttu-id="4c7f8-1070">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1070">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="4c7f8-1071">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1071">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="4c7f8-1072">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1072">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="4c7f8-1073">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1073">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="4c7f8-1074">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1074">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="4c7f8-1075">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="4c7f8-1075">Add prompting for missing template parameters.</span></span> <span data-ttu-id="4c7f8-1076">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1076">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="4c7f8-1077">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1077">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="4c7f8-1078">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1078">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="4c7f8-1079">ACS</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1079">ACS</span></span>

* <span data-ttu-id="4c7f8-1080">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1080">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="4c7f8-1081">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="4c7f8-1081">Add support for ssh key password prompting.</span></span> <span data-ttu-id="4c7f8-1082">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1082">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="4c7f8-1083">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="4c7f8-1083">Add support for windows clusters.</span></span> <span data-ttu-id="4c7f8-1084">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1084">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="4c7f8-1085">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="4c7f8-1085">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="4c7f8-1086">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1086">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="4c7f8-1087">AppService</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1087">AppService</span></span>

* <span data-ttu-id="4c7f8-1088">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1088">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="4c7f8-1089">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1089">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="4c7f8-1090">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1090">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="4c7f8-1091">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1091">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="4c7f8-1092">DataLake</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1092">DataLake</span></span>

* <span data-ttu-id="4c7f8-1093">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1093">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="4c7f8-1094">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1094">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="4c7f8-1095">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1095">DocuemntDB</span></span>

* <span data-ttu-id="4c7f8-1096">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1096">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="4c7f8-1097">VM</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1097">VM</span></span>

* <span data-ttu-id="4c7f8-1098">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1098">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="4c7f8-1099">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1099">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="4c7f8-1100">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1100">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="4c7f8-1101">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1101">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="4c7f8-1102">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1102">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="4c7f8-1103">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1103">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="4c7f8-1104">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1104">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="4c7f8-1105">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1105">February 27, 2017</span></span>

<span data-ttu-id="4c7f8-1106">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1106">Version 2.0.0</span></span>

<span data-ttu-id="4c7f8-1107">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1107">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="4c7f8-1108">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1108">Container Service (acs)</span></span>
- <span data-ttu-id="4c7f8-1109">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1109">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="4c7f8-1110">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1110">Networking</span></span>
- <span data-ttu-id="4c7f8-1111">Storage</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1111">Storage</span></span>

<span data-ttu-id="4c7f8-1112">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1112">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="4c7f8-1113">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1113">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="4c7f8-1114">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1114">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="4c7f8-1115">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1115">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="4c7f8-1116">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1116">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="4c7f8-1117">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1117">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="4c7f8-1118">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1118">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="4c7f8-1119">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1119">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="4c7f8-1120">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="4c7f8-1120">Provide feedback from the command line with the `az feedback` command</span></span>

