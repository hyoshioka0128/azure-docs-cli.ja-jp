---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/06/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 51b8b8cad6d25f916006b8e68b8f300587f5d45b
ms.sourcegitcommit: 0d6b08048b5b35bf0bb3d7b91ff567adbaab2a8b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "51222567"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="62c18-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="62c18-103">Azure CLI release notes</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="62c18-104">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="62c18-104">November 6, 2018</span></span>

<span data-ttu-id="62c18-105">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="62c18-105">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="62c18-106">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-106">Core</span></span>
* <span data-ttu-id="62c18-107">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-107">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-108">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-108">ACR</span></span>
* <span data-ttu-id="62c18-109">タスク ソース トリガーのコミットおよびプル要求の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-109">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="62c18-110">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-110">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-111">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-111">ACS</span></span>
* <span data-ttu-id="62c18-112">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-112">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="62c18-113">Advisor</span><span class="sxs-lookup"><span data-stu-id="62c18-113">Advisor</span></span>
* <span data-ttu-id="62c18-114">GA リリース</span><span class="sxs-lookup"><span data-stu-id="62c18-114">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="62c18-115">AMS</span><span class="sxs-lookup"><span data-stu-id="62c18-115">AMS</span></span>
* <span data-ttu-id="62c18-116">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-116">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="62c18-117">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-117">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="62c18-118">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-118">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="62c18-119">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-119">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="62c18-120">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-120">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="62c18-121">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-121">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="62c18-122">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-122">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="62c18-123">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="62c18-123">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="62c18-124">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-124">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="62c18-125">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-125">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="62c18-126">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="62c18-126">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="62c18-127">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="62c18-127">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="62c18-128">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="62c18-128">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="62c18-129">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="62c18-129">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="62c18-130">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-130">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="62c18-131">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="62c18-131">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="62c18-132">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="62c18-132">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-133">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-133">AppService</span></span>
* <span data-ttu-id="62c18-134">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-134">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="62c18-135">構成</span><span class="sxs-lookup"><span data-stu-id="62c18-135">Configure</span></span>
* <span data-ttu-id="62c18-136">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-136">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="62c18-137">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-137">Container</span></span>
* <span data-ttu-id="62c18-138">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-138">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="62c18-139">EventHub</span><span class="sxs-lookup"><span data-stu-id="62c18-139">EventHub</span></span>
* <span data-ttu-id="62c18-140">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-140">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-141">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-141">Interactive</span></span>
* <span data-ttu-id="62c18-142">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="62c18-142">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-143">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-143">Monitor</span></span>
* <span data-ttu-id="62c18-144">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-144">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="62c18-145">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-145">Network</span></span>
* <span data-ttu-id="62c18-146">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-146">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="62c18-147">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-147">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="62c18-148">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-148">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="62c18-149">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-149">Profile</span></span>
* <span data-ttu-id="62c18-150">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-150">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="62c18-151">RDBMS</span><span class="sxs-lookup"><span data-stu-id="62c18-151">RDBMS</span></span>
* <span data-ttu-id="62c18-152">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-152">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-153">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-153">Resource</span></span>
* <span data-ttu-id="62c18-154">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-154">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="62c18-155">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-155">Role</span></span>
* <span data-ttu-id="62c18-156">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-156">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="62c18-157">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-157">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="62c18-158">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-158">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-159">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-159">Storage</span></span>
* <span data-ttu-id="62c18-160">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="62c18-160">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-161">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-161">VM</span></span>
* <span data-ttu-id="62c18-162">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-162">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="62c18-163">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-163">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="62c18-164">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-164">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="62c18-165">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-165">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="62c18-166">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="62c18-166">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="62c18-167">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-167">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="62c18-168">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="62c18-168">October 23, 2018</span></span>

<span data-ttu-id="62c18-169">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="62c18-169">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="62c18-170">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-170">Core</span></span>
* <span data-ttu-id="62c18-171">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-171">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="62c18-172">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-172">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-173">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-173">ACR</span></span>
* <span data-ttu-id="62c18-174">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-174">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="62c18-175">CDN</span><span class="sxs-lookup"><span data-stu-id="62c18-175">CDN</span></span>
* <span data-ttu-id="62c18-176">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="62c18-176">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="62c18-177">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-177">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="62c18-178">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-178">Container</span></span>
* <span data-ttu-id="62c18-179">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-179">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="62c18-180">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-180">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="62c18-181">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-181">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="62c18-182">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-182">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="62c18-183">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-183">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="62c18-184">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-184">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="62c18-185">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-185">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="62c18-186">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="62c18-186">CosmosDB</span></span>
* <span data-ttu-id="62c18-187">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-187">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-188">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-188">Interactive</span></span>
* <span data-ttu-id="62c18-189">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-189">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="62c18-190">IoT Central</span><span class="sxs-lookup"><span data-stu-id="62c18-190">IoT Central</span></span>
* <span data-ttu-id="62c18-191">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-191">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="62c18-192">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="62c18-192">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-193">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-193">Monitor</span></span>
* <span data-ttu-id="62c18-194">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="62c18-194">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="62c18-195">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-195">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="62c18-196">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-196">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="62c18-197">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-197">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="62c18-198">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-198">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="62c18-199">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-199">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="62c18-200">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="62c18-200">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="62c18-201">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-201">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="62c18-202">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-202">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="62c18-203">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-203">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="62c18-204">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-204">Network</span></span>
* <span data-ttu-id="62c18-205">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-205">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="62c18-206">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-206">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="62c18-207">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="62c18-207">ServiceBus</span></span>
* <span data-ttu-id="62c18-208">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-208">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-209">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-209">SQL</span></span>
* <span data-ttu-id="62c18-210">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-210">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-211">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-211">Storage</span></span>
* <span data-ttu-id="62c18-212">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-212">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="62c18-213">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-213">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-214">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-214">VM</span></span>
* <span data-ttu-id="62c18-215">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="62c18-215">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="62c18-216">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-216">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="62c18-217">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-217">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="62c18-218">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="62c18-218">October 16, 2018</span></span>

<span data-ttu-id="62c18-219">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="62c18-219">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-220">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-220">VM</span></span>
* <span data-ttu-id="62c18-221">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-221">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="62c18-222">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="62c18-222">October 9, 2018</span></span>

<span data-ttu-id="62c18-223">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="62c18-223">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="62c18-224">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-224">Core</span></span>
* <span data-ttu-id="62c18-225">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-225">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-226">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-226">ACR</span></span>
* <span data-ttu-id="62c18-227">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-227">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-228">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-228">ACS</span></span>
* <span data-ttu-id="62c18-229">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="62c18-229">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="62c18-230">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-230">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="62c18-231">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-231">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="62c18-232">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-232">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="62c18-233">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-233">Container</span></span>
* <span data-ttu-id="62c18-234">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-234">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="62c18-235">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-235">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="62c18-236">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="62c18-236">Event Hub</span></span>
* <span data-ttu-id="62c18-237">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-237">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="62c18-238">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-238">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="62c18-239">拡張機能</span><span class="sxs-lookup"><span data-stu-id="62c18-239">Extensions</span></span>
* <span data-ttu-id="62c18-240">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-240">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="62c18-241">HDInsight</span><span class="sxs-lookup"><span data-stu-id="62c18-241">HDInsight</span></span>
* <span data-ttu-id="62c18-242">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-242">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="62c18-243">IoT</span><span class="sxs-lookup"><span data-stu-id="62c18-243">IoT</span></span>
* <span data-ttu-id="62c18-244">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-244">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="62c18-245">KeyVault</span><span class="sxs-lookup"><span data-stu-id="62c18-245">KeyVault</span></span>
* <span data-ttu-id="62c18-246">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-246">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="62c18-247">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-247">Network</span></span>
* <span data-ttu-id="62c18-248">`network dns zone create` を修正しました: ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="62c18-248">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="62c18-249">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="62c18-249">See #6052</span></span>
* <span data-ttu-id="62c18-250">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-250">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="62c18-251">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="62c18-251">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="62c18-252">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-252">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="62c18-253">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-253">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="62c18-254">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-254">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="62c18-255">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-255">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="62c18-256">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-256">Role</span></span>
* <span data-ttu-id="62c18-257">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-257">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="62c18-258">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-258">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="62c18-259">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-259">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="62c18-260">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-260">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="62c18-261">Service Bus</span><span class="sxs-lookup"><span data-stu-id="62c18-261">Service Bus</span></span>
* <span data-ttu-id="62c18-262">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-262">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-263">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-263">VM</span></span>
* <span data-ttu-id="62c18-264">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-264">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="62c18-265">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-265">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="62c18-266">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-266">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="62c18-267">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-267">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="62c18-268">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-268">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="62c18-269">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-269">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="62c18-270">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="62c18-270">September 21, 2018</span></span>

<span data-ttu-id="62c18-271">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="62c18-271">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-272">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-272">ACR</span></span>
* <span data-ttu-id="62c18-273">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-273">Added ACR Task commands</span></span>
* <span data-ttu-id="62c18-274">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-274">Added quick run command</span></span>
* <span data-ttu-id="62c18-275">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-275">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="62c18-276">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-276">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="62c18-277">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-277">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="62c18-278">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-278">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-279">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-279">ACS</span></span>
* <span data-ttu-id="62c18-280">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-280">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="62c18-281">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-281">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-282">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-282">AppService</span></span>

* <span data-ttu-id="62c18-283">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-283">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="62c18-284">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-284">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="62c18-285">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-285">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="62c18-286">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-286">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="62c18-287">Batch</span><span class="sxs-lookup"><span data-stu-id="62c18-287">Batch</span></span>
* <span data-ttu-id="62c18-288">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-288">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="62c18-289">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-289">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="62c18-290">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-290">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="62c18-291">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-291">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="62c18-292">Batch AI</span><span class="sxs-lookup"><span data-stu-id="62c18-292">Batch AI</span></span> 
* <span data-ttu-id="62c18-293">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-293">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="62c18-294">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="62c18-294">Cognitive Services</span></span>
* <span data-ttu-id="62c18-295">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-295">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="62c18-296">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-296">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="62c18-297">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-297">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="62c18-298">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-298">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="62c18-299">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-299">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="62c18-300">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-300">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="62c18-301">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-301">Container</span></span>
* <span data-ttu-id="62c18-302">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-302">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="62c18-303">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-303">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="62c18-304">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-304">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="62c18-305">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-305">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="62c18-306">DataLake</span><span class="sxs-lookup"><span data-stu-id="62c18-306">Datalake</span></span>
* <span data-ttu-id="62c18-307">仮想ネットワーク ルール用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-307">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="62c18-308">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="62c18-308">Interactive Shell</span></span>
* <span data-ttu-id="62c18-309">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-309">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="62c18-310">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-310">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="62c18-311">IoT</span><span class="sxs-lookup"><span data-stu-id="62c18-311">IoT</span></span>
* <span data-ttu-id="62c18-312">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-312">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="62c18-313">Key Vault</span><span class="sxs-lookup"><span data-stu-id="62c18-313">Key Vault</span></span>
* <span data-ttu-id="62c18-314">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-314">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="62c18-315">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-315">Network</span></span>
* <span data-ttu-id="62c18-316">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-316">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="62c18-317">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-317">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="62c18-318">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-318">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="62c18-319">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-319">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="62c18-320">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-320">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="62c18-321">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-321">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="62c18-322">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="62c18-322">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="62c18-323">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-323">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="62c18-324">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-324">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="62c18-325">`network express-route create/update`: `--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-325">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="62c18-326">`network vnet subnet create/update`: `--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-326">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="62c18-327">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-327">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="62c18-328">`network traffic-manager profile create/update`: 監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、`--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-328">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="62c18-329">`network lb frontend-ip create/update`: プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="62c18-329">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="62c18-330">`dns record-set * create/update`: `--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-330">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="62c18-331">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-331">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="62c18-332">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-332">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="62c18-333">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-333">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="62c18-334">RDBMS</span><span class="sxs-lookup"><span data-stu-id="62c18-334">RDBMS</span></span>
* <span data-ttu-id="62c18-335">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-335">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="62c18-336">予約</span><span class="sxs-lookup"><span data-stu-id="62c18-336">Reservation</span></span>
* <span data-ttu-id="62c18-337">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-337">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="62c18-338">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-338">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="62c18-339">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="62c18-339">Manage App</span></span>
* <span data-ttu-id="62c18-340">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-340">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="62c18-341">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-341">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="62c18-342">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-342">Role</span></span>
* <span data-ttu-id="62c18-343">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-343">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="62c18-344">SignalR</span><span class="sxs-lookup"><span data-stu-id="62c18-344">SignalR</span></span>
* <span data-ttu-id="62c18-345">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-345">First release</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-346">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-346">Storage</span></span>
* <span data-ttu-id="62c18-347">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-347">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="62c18-348">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-348">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-349">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-349">VM</span></span>
* <span data-ttu-id="62c18-350">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="62c18-350">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="62c18-351">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-351">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="62c18-352">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="62c18-352">August 28, 2018</span></span>

<span data-ttu-id="62c18-353">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="62c18-353">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="62c18-354">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-354">Core</span></span>

* <span data-ttu-id="62c18-355">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-355">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="62c18-356">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-356">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-357">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-357">ACR</span></span>

* <span data-ttu-id="62c18-358">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-358">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="62c18-359">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-359">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-360">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-360">ACS</span></span>

* <span data-ttu-id="62c18-361">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-361">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="62c18-362">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-362">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-363">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-363">AppService</span></span>

* <span data-ttu-id="62c18-364">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-364">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="62c18-365">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-365">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="62c18-366">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-366">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="62c18-367">バックアップ</span><span class="sxs-lookup"><span data-stu-id="62c18-367">Backup</span></span>

* <span data-ttu-id="62c18-368">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-368">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="62c18-369">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="62c18-369">Bot Service</span></span>

* <span data-ttu-id="62c18-370">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="62c18-370">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="62c18-371">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="62c18-371">Cognitive Services</span></span>

* <span data-ttu-id="62c18-372">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-372">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="62c18-373">IoT</span><span class="sxs-lookup"><span data-stu-id="62c18-373">IoT</span></span>

* <span data-ttu-id="62c18-374">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-374">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-375">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-375">Monitor</span></span>

* <span data-ttu-id="62c18-376">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-376">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="62c18-377">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-377">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="62c18-378">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-378">Network</span></span>

* <span data-ttu-id="62c18-379">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-379">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-380">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-380">Resource</span></span>

* <span data-ttu-id="62c18-381">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-381">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-382">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-382">Storage</span></span>

* <span data-ttu-id="62c18-383">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-383">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-384">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-384">VM</span></span>

* <span data-ttu-id="62c18-385">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-385">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="62c18-386">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-386">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="62c18-387">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="62c18-387">Auguest 14, 2018</span></span>

<span data-ttu-id="62c18-388">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="62c18-388">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="62c18-389">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-389">Core</span></span>

* <span data-ttu-id="62c18-390">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-390">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="62c18-391">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-391">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="62c18-392">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="62c18-392">Telemetry</span></span>

* <span data-ttu-id="62c18-393">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-393">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-394">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-394">ACR</span></span>

* <span data-ttu-id="62c18-395">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-395">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="62c18-396">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-396">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-397">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-397">ACS</span></span>

* <span data-ttu-id="62c18-398">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-398">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="62c18-399">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-399">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="62c18-400">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-400">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="62c18-401">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-401">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="62c18-402">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-402">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="62c18-403">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-403">AppService</span></span>

* <span data-ttu-id="62c18-404">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-404">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="62c18-405">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-405">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="62c18-406">BatchAI</span><span class="sxs-lookup"><span data-stu-id="62c18-406">BatchAI</span></span>

* <span data-ttu-id="62c18-407">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-407">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="62c18-408">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-408">Container</span></span>

* <span data-ttu-id="62c18-409">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-409">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="62c18-410">IoT</span><span class="sxs-lookup"><span data-stu-id="62c18-410">IoT</span></span>

* <span data-ttu-id="62c18-411">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-411">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="62c18-412">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-412">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="62c18-413">Iot Central</span><span class="sxs-lookup"><span data-stu-id="62c18-413">Iot Central</span></span>

* <span data-ttu-id="62c18-414">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-414">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="62c18-415">KeyVault</span><span class="sxs-lookup"><span data-stu-id="62c18-415">KeyVault</span></span>


* <span data-ttu-id="62c18-416">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-416">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="62c18-417">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-417">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="62c18-418">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-418">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="62c18-419">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-419">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="62c18-420">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-420">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="62c18-421">リレー</span><span class="sxs-lookup"><span data-stu-id="62c18-421">Relay</span></span>

* <span data-ttu-id="62c18-422">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-422">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-423">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-423">Sql</span></span>

* <span data-ttu-id="62c18-424">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-424">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-425">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-425">Storage</span></span>

* <span data-ttu-id="62c18-426">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="62c18-426">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="62c18-427">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-427">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="62c18-428">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="62c18-428">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="62c18-429">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-429">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="62c18-430">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-430">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-431">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-431">VM</span></span>

* <span data-ttu-id="62c18-432">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-432">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="62c18-433">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="62c18-433">July 31, 2018</span></span>

<span data-ttu-id="62c18-434">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="62c18-434">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-435">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-435">ACR</span></span>

* <span data-ttu-id="62c18-436">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-436">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="62c18-437">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-437">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-438">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-438">ACS</span></span>

* <span data-ttu-id="62c18-439">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-439">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="62c18-440">Batch</span><span class="sxs-lookup"><span data-stu-id="62c18-440">Batch</span></span>

* <span data-ttu-id="62c18-441">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-441">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="62c18-442">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-442">Container</span></span>

* <span data-ttu-id="62c18-443">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-443">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="62c18-444">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-444">Network</span></span>

* <span data-ttu-id="62c18-445">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-445">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="62c18-446">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-446">Resource</span></span>

* <span data-ttu-id="62c18-447">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-447">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="62c18-448">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-448">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="62c18-449">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-449">Role</span></span>

* <span data-ttu-id="62c18-450">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-450">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="62c18-451">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-451">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="62c18-452">Search</span><span class="sxs-lookup"><span data-stu-id="62c18-452">Search</span></span>

* <span data-ttu-id="62c18-453">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-453">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="62c18-454">Service Bus</span><span class="sxs-lookup"><span data-stu-id="62c18-454">Service Bus</span></span>

* <span data-ttu-id="62c18-455">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-455">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="62c18-456">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-456">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="62c18-457">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="62c18-457">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="62c18-458">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="62c18-458">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-459">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-459">Storage</span></span>

* <span data-ttu-id="62c18-460">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-460">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="62c18-461">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="62c18-461">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-462">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-462">VM</span></span>

* <span data-ttu-id="62c18-463">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-463">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="62c18-464">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-464">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="62c18-465">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-465">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="62c18-466">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-466">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="62c18-467">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="62c18-467">July 18, 2018</span></span>

<span data-ttu-id="62c18-468">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="62c18-468">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="62c18-469">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-469">Core</span></span>

* <span data-ttu-id="62c18-470">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-470">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="62c18-471">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-471">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="62c18-472">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-472">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-473">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-473">ACR</span></span>

* <span data-ttu-id="62c18-474">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-474">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="62c18-475">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-475">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="62c18-476">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-476">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="62c18-477">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-477">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-478">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-478">ACS</span></span>

* <span data-ttu-id="62c18-479">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-479">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-480">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-480">AppService</span></span>

* <span data-ttu-id="62c18-481">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-481">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="62c18-482">Batch</span><span class="sxs-lookup"><span data-stu-id="62c18-482">Batch</span></span>

* <span data-ttu-id="62c18-483">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-483">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="62c18-484">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-484">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="62c18-485">Batch AI</span><span class="sxs-lookup"><span data-stu-id="62c18-485">Batch AI</span></span>

* <span data-ttu-id="62c18-486">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-486">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="62c18-487">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-487">Container</span></span>

* <span data-ttu-id="62c18-488">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-488">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="62c18-489">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-489">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="62c18-490">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-490">Network</span></span>

* <span data-ttu-id="62c18-491">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-491">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="62c18-492">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-492">Added `network nic wait`</span></span>
* <span data-ttu-id="62c18-493">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-493">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="62c18-494">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-494">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="62c18-495">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-495">Resource</span></span>

* <span data-ttu-id="62c18-496">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-496">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="62c18-497">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-497">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="62c18-498">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-498">Added `deployment wait` command</span></span>
* <span data-ttu-id="62c18-499">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-499">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-500">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-500">SQL</span></span>

* <span data-ttu-id="62c18-501">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-501">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="62c18-502">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-502">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="62c18-503">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="62c18-503">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-504">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-504">Storage</span></span>

* <span data-ttu-id="62c18-505">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-505">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-506">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-506">VM</span></span>

* <span data-ttu-id="62c18-507">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-507">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="62c18-508">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-508">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="62c18-509">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-509">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="62c18-510">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="62c18-510">July 3, 2018</span></span>

<span data-ttu-id="62c18-511">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="62c18-511">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="62c18-512">AKS</span><span class="sxs-lookup"><span data-stu-id="62c18-512">AKS</span></span>

* <span data-ttu-id="62c18-513">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-513">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="62c18-514">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="62c18-514">July 3, 2018</span></span>

<span data-ttu-id="62c18-515">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="62c18-515">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="62c18-516">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-516">Core</span></span>

* <span data-ttu-id="62c18-517">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-517">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-518">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-518">ACR</span></span>

* <span data-ttu-id="62c18-519">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-519">Added polling build status</span></span>
* <span data-ttu-id="62c18-520">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-520">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="62c18-521">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-521">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-522">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-522">ACS</span></span>

* <span data-ttu-id="62c18-523">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-523">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="62c18-524">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-524">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="62c18-525">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-525">Updated options for `aks browse` command.</span></span> <span data-ttu-id="62c18-526">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-526">Added `--listen-port` support</span></span>
* <span data-ttu-id="62c18-527">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-527">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="62c18-528">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="62c18-528">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="62c18-529">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-529">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-530">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-530">AppService</span></span>

* <span data-ttu-id="62c18-531">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-531">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="62c18-532">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-532">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="62c18-533">バックアップ</span><span class="sxs-lookup"><span data-stu-id="62c18-533">Backup</span></span>

* <span data-ttu-id="62c18-534">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-534">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="62c18-535">BatchAI</span><span class="sxs-lookup"><span data-stu-id="62c18-535">BatchAI</span></span>

* <span data-ttu-id="62c18-536">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-536">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="62c18-537">クラウド</span><span class="sxs-lookup"><span data-stu-id="62c18-537">Cloud</span></span>

* <span data-ttu-id="62c18-538">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-538">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="62c18-539">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-539">Container</span></span>

* <span data-ttu-id="62c18-540">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-540">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="62c18-541">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-541">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="62c18-542">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-542">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="62c18-543">内線番号</span><span class="sxs-lookup"><span data-stu-id="62c18-543">Extension</span></span>

* <span data-ttu-id="62c18-544">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-544">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="62c18-545">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-545">Network</span></span>

* <span data-ttu-id="62c18-546">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-546">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="62c18-547">Rdbms</span><span class="sxs-lookup"><span data-stu-id="62c18-547">Rdbms</span></span>

* <span data-ttu-id="62c18-548">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-548">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-549">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-549">Resource</span></span>

* <span data-ttu-id="62c18-550">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-550">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-551">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-551">VM</span></span>

* <span data-ttu-id="62c18-552">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-552">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="62c18-553">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="62c18-553">June 25, 2018</span></span>

<span data-ttu-id="62c18-554">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="62c18-554">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="62c18-555">CLI</span><span class="sxs-lookup"><span data-stu-id="62c18-555">CLI</span></span>

* <span data-ttu-id="62c18-556">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-556">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="62c18-557">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="62c18-557">June 19, 2018</span></span>

<span data-ttu-id="62c18-558">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="62c18-558">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="62c18-559">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-559">Core</span></span>

* <span data-ttu-id="62c18-560">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-560">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-561">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-561">ACR</span></span>

* <span data-ttu-id="62c18-562">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-562">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="62c18-563">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-563">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-564">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-564">ACS</span></span>

* <span data-ttu-id="62c18-565">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-565">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="62c18-566">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-566">Added `--update` support</span></span>
* <span data-ttu-id="62c18-567">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-567">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="62c18-568">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="62c18-568">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="62c18-569">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-569">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="62c18-570">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-570">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="62c18-571">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-571">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="62c18-572">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-572">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-573">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-573">AppService</span></span>

* <span data-ttu-id="62c18-574">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-574">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="62c18-575">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-575">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="62c18-576">Batch</span><span class="sxs-lookup"><span data-stu-id="62c18-576">Batch</span></span>

* <span data-ttu-id="62c18-577">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-577">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="62c18-578">Batch AI</span><span class="sxs-lookup"><span data-stu-id="62c18-578">Batch AI</span></span>

* <span data-ttu-id="62c18-579">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-579">Added support for workspaces.</span></span> <span data-ttu-id="62c18-580">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="62c18-580">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="62c18-581">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-581">Added support for experiments.</span></span> <span data-ttu-id="62c18-582">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="62c18-582">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="62c18-583">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-583">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="62c18-584">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-584">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="62c18-585">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="62c18-585">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="62c18-586">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-586">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="62c18-587">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="62c18-587">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="62c18-588">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="62c18-588">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="62c18-589">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-589">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="62c18-590">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="62c18-590">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="62c18-591">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-591">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="62c18-592">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="62c18-592">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="62c18-593">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-593">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="62c18-594">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="62c18-594">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="62c18-595">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-595">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="62c18-596">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-596">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="62c18-597">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-597">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="62c18-598">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-598">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="62c18-599">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-599">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="62c18-600">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-600">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="62c18-601">マップ</span><span class="sxs-lookup"><span data-stu-id="62c18-601">Maps</span></span>

* <span data-ttu-id="62c18-602">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-602">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="62c18-603">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-603">Network</span></span>

* <span data-ttu-id="62c18-604">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="62c18-604">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="62c18-605">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-605">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="62c18-606">#6502</span><span class="sxs-lookup"><span data-stu-id="62c18-606">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="62c18-607">Reservations</span><span class="sxs-lookup"><span data-stu-id="62c18-607">Reservations</span></span>

* <span data-ttu-id="62c18-608">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-608">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="62c18-609">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-609">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="62c18-610">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-610">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="62c18-611">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-611">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="62c18-612">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-612">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="62c18-613">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-613">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="62c18-614">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-614">Role</span></span>

* <span data-ttu-id="62c18-615">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-615">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-616">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-616">SQL</span></span>

* <span data-ttu-id="62c18-617">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-617">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-618">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-618">Storage</span></span>

* <span data-ttu-id="62c18-619">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="62c18-619">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-620">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-620">VM</span></span>

* <span data-ttu-id="62c18-621">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-621">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="62c18-622">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-622">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="62c18-623">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-623">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="62c18-624">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="62c18-624">June 13, 2018</span></span>

<span data-ttu-id="62c18-625">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="62c18-625">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="62c18-626">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-626">Core</span></span>

* <span data-ttu-id="62c18-627">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-627">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="62c18-628">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="62c18-628">June 13, 2018</span></span>

<span data-ttu-id="62c18-629">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="62c18-629">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="62c18-630">AKS</span><span class="sxs-lookup"><span data-stu-id="62c18-630">AKS</span></span>

* <span data-ttu-id="62c18-631">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-631">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="62c18-632">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-632">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="62c18-633">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-633">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="62c18-634">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-634">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="62c18-635">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-635">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-636">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-636">AppService</span></span>

* <span data-ttu-id="62c18-637">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-637">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="62c18-638">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="62c18-638">June 5, 2018</span></span>

<span data-ttu-id="62c18-639">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="62c18-639">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-640">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-640">Interactive</span></span>

* <span data-ttu-id="62c18-641">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-641">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="62c18-642">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="62c18-642">June 5, 2018</span></span>

<span data-ttu-id="62c18-643">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="62c18-643">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="62c18-644">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-644">Core</span></span>

* <span data-ttu-id="62c18-645">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-645">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="62c18-646">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-646">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-647">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-647">ACR</span></span>

* <span data-ttu-id="62c18-648">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-648">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="62c18-649">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-649">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="62c18-650">AKS</span><span class="sxs-lookup"><span data-stu-id="62c18-650">AKS</span></span>

* <span data-ttu-id="62c18-651">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-651">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="62c18-652">Batch</span><span class="sxs-lookup"><span data-stu-id="62c18-652">Batch</span></span>

* <span data-ttu-id="62c18-653">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-653">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="62c18-654">IoT</span><span class="sxs-lookup"><span data-stu-id="62c18-654">IOT</span></span>

* <span data-ttu-id="62c18-655">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-655">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="62c18-656">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-656">Network</span></span>

* <span data-ttu-id="62c18-657">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-657">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="62c18-658">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="62c18-658">Policy Insights</span></span>

* <span data-ttu-id="62c18-659">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-659">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="62c18-660">ARM</span><span class="sxs-lookup"><span data-stu-id="62c18-660">ARM</span></span>

* <span data-ttu-id="62c18-661">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-661">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-662">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-662">SQL</span></span>

* <span data-ttu-id="62c18-663">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-663">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="62c18-664">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-664">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="62c18-665">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-665">Storage</span></span>

* <span data-ttu-id="62c18-666">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-666">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-667">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-667">VM</span></span>

* <span data-ttu-id="62c18-668">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-668">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="62c18-669">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-669">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="62c18-670">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-670">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="62c18-671">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="62c18-671">May 22, 2018</span></span>

<span data-ttu-id="62c18-672">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="62c18-672">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="62c18-673">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-673">Core</span></span>

* <span data-ttu-id="62c18-674">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-674">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-675">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-675">ACS</span></span>

* <span data-ttu-id="62c18-676">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-676">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="62c18-677">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-677">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-678">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-678">AppService</span></span>

* <span data-ttu-id="62c18-679">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-679">Improved generic update commands</span></span>
* <span data-ttu-id="62c18-680">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-680">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="62c18-681">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-681">Container</span></span>

* <span data-ttu-id="62c18-682">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-682">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="62c18-683">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-683">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="62c18-684">内線番号</span><span class="sxs-lookup"><span data-stu-id="62c18-684">Extension</span></span>

* <span data-ttu-id="62c18-685">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-685">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-686">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-686">Interactive</span></span>

* <span data-ttu-id="62c18-687">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-687">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="62c18-688">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-688">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="62c18-689">KeyVault</span><span class="sxs-lookup"><span data-stu-id="62c18-689">KeyVault</span></span>

* <span data-ttu-id="62c18-690">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-690">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="62c18-691">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-691">Network</span></span>

* <span data-ttu-id="62c18-692">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-692">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="62c18-693">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-693">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-694">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-694">SQL</span></span>

* <span data-ttu-id="62c18-695">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-695">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="62c18-696">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-696">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="62c18-697">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-697">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="62c18-698">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-698">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="62c18-699">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-699">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="62c18-700">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="62c18-700">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="62c18-701">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="62c18-701">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="62c18-702">`edition`</span><span class="sxs-lookup"><span data-stu-id="62c18-702">`edition`.</span></span> <span data-ttu-id="62c18-703">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="62c18-703">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="62c18-704">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="62c18-704">`elasticPoolName`.</span></span> <span data-ttu-id="62c18-705">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="62c18-705">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="62c18-706">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-706">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="62c18-707">`edition`</span><span class="sxs-lookup"><span data-stu-id="62c18-707">`edition`.</span></span> <span data-ttu-id="62c18-708">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="62c18-708">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="62c18-709">`dtu`</span><span class="sxs-lookup"><span data-stu-id="62c18-709">`dtu`.</span></span> <span data-ttu-id="62c18-710">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="62c18-710">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="62c18-711">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="62c18-711">`databaseDtuMin`.</span></span> <span data-ttu-id="62c18-712">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="62c18-712">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="62c18-713">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="62c18-713">`databaseDtuMax`.</span></span> <span data-ttu-id="62c18-714">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="62c18-714">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="62c18-715">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-715">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="62c18-716">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-716">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-717">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-717">Storage</span></span>

* <span data-ttu-id="62c18-718">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-718">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="62c18-719">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-719">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-720">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-720">VM</span></span>

* <span data-ttu-id="62c18-721">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-721">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="62c18-722">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="62c18-722">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="62c18-723">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-723">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="62c18-724">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-724">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="62c18-725">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-725">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="62c18-726">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="62c18-726">May 7, 2018</span></span>

<span data-ttu-id="62c18-727">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="62c18-727">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="62c18-728">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-728">Core</span></span>

* <span data-ttu-id="62c18-729">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-729">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="62c18-730">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-730">Added limited support for positional arguments</span></span>
* <span data-ttu-id="62c18-731">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-731">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="62c18-732">#5591</span><span class="sxs-lookup"><span data-stu-id="62c18-732">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="62c18-733">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-733">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="62c18-734">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="62c18-734">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="62c18-735">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-735">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="62c18-736">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-736">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="62c18-737">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-737">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-738">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-738">ACR</span></span>

* <span data-ttu-id="62c18-739">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-739">Added ACR Build commands</span></span>
* <span data-ttu-id="62c18-740">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-740">Improved resource not found error messages</span></span>
* <span data-ttu-id="62c18-741">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-741">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="62c18-742">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-742">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="62c18-743">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-743">Improved repository commands error messages</span></span>
* <span data-ttu-id="62c18-744">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-744">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-745">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-745">ACS</span></span>

* <span data-ttu-id="62c18-746">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-746">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="62c18-747">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-747">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="62c18-748">AMS</span><span class="sxs-lookup"><span data-stu-id="62c18-748">AMS</span></span>

* <span data-ttu-id="62c18-749">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="62c18-749">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-750">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-750">Appservice</span></span>

* <span data-ttu-id="62c18-751">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-751">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="62c18-752">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-752">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="62c18-753">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-753">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="62c18-754">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-754">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="62c18-755">Batch AI</span><span class="sxs-lookup"><span data-stu-id="62c18-755">Batch AI</span></span>

* <span data-ttu-id="62c18-756">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-756">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="62c18-757">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="62c18-757">Cognitive Services</span></span>

* <span data-ttu-id="62c18-758">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-758">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="62c18-759">消費</span><span class="sxs-lookup"><span data-stu-id="62c18-759">Consumption</span></span>

* <span data-ttu-id="62c18-760">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-760">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="62c18-761">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-761">Container</span></span>

* <span data-ttu-id="62c18-762">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-762">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="62c18-763">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="62c18-763">Cosmos DB</span></span>

* <span data-ttu-id="62c18-764">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="62c18-764">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="62c18-765">DMS</span><span class="sxs-lookup"><span data-stu-id="62c18-765">DMS</span></span>

* <span data-ttu-id="62c18-766">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-766">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="62c18-767">内線番号</span><span class="sxs-lookup"><span data-stu-id="62c18-767">Extension</span></span>

* <span data-ttu-id="62c18-768">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-768">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-769">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-769">Interactive</span></span>

* <span data-ttu-id="62c18-770">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-770">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="62c18-771">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="62c18-771">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="62c18-772">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-772">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="62c18-773">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-773">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="62c18-774">ラボ</span><span class="sxs-lookup"><span data-stu-id="62c18-774">Lab</span></span>

* <span data-ttu-id="62c18-775">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-775">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="62c18-776">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-776">Network</span></span>

* <span data-ttu-id="62c18-777">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-777">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="62c18-778">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-778">Profile</span></span>

* <span data-ttu-id="62c18-779">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-779">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="62c18-780">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-780">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="62c18-781">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-781">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="62c18-782">Redis</span><span class="sxs-lookup"><span data-stu-id="62c18-782">Redis</span></span>

* <span data-ttu-id="62c18-783">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-783">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="62c18-784">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="62c18-784">Deprecated `redis list-all`.</span></span> <span data-ttu-id="62c18-785">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="62c18-785">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="62c18-786">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-786">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="62c18-787">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-787">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="62c18-788">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-788">Role</span></span>

* <span data-ttu-id="62c18-789">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-789">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-790">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-790">Storage</span></span>

* <span data-ttu-id="62c18-791">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="62c18-791">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="62c18-792">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="62c18-792">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="62c18-793">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="62c18-793">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="62c18-794">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="62c18-794">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="62c18-795">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-795">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-796">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-796">VM</span></span>

* <span data-ttu-id="62c18-797">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-797">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="62c18-798">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-798">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="62c18-799">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="62c18-799">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="62c18-800">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-800">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="62c18-801">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-801">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="62c18-802">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-802">Added write accelerator support</span></span>
* <span data-ttu-id="62c18-803">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-803">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="62c18-804">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-804">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="62c18-805">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-805">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="62c18-806">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="62c18-806">April 10, 2018</span></span>

<span data-ttu-id="62c18-807">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="62c18-807">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-808">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-808">ACR</span></span>

* <span data-ttu-id="62c18-809">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-809">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-810">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-810">ACS</span></span>

* <span data-ttu-id="62c18-811">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-811">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-812">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-812">Appservice</span></span>

* [重大な変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="62c18-814">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-814">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="62c18-815">BatchAI</span><span class="sxs-lookup"><span data-stu-id="62c18-815">BatchAI</span></span>

* <span data-ttu-id="62c18-816">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-816">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="62c18-817">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="62c18-817">Job level mounting</span></span>
  - <span data-ttu-id="62c18-818">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="62c18-818">Environment variables with secret values</span></span>
  - <span data-ttu-id="62c18-819">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="62c18-819">Performance counters settings</span></span>
  - <span data-ttu-id="62c18-820">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="62c18-820">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="62c18-821">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="62c18-821">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="62c18-822">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="62c18-822">Usage and limits reporting</span></span>
  - <span data-ttu-id="62c18-823">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="62c18-823">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="62c18-824">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="62c18-824">Support for custom images</span></span>
  - <span data-ttu-id="62c18-825">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-825">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="62c18-826">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-826">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="62c18-827">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="62c18-827">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="62c18-828">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="62c18-828">National clouds are supported</span></span>
* <span data-ttu-id="62c18-829">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-829">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="62c18-830">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-830">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="62c18-831">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-831">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="62c18-832">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-832">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="62c18-833">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="62c18-833">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="62c18-834">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="62c18-834">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="62c18-835">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-835">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="62c18-836">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-836">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="62c18-837">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="62c18-837">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="62c18-838">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-838">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="62c18-839">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="62c18-839">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="62c18-840">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="62c18-840">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="62c18-841">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-841">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="62c18-842">課金</span><span class="sxs-lookup"><span data-stu-id="62c18-842">Billing</span></span>

* <span data-ttu-id="62c18-843">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-843">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="62c18-844">消費</span><span class="sxs-lookup"><span data-stu-id="62c18-844">Consumption</span></span>

* <span data-ttu-id="62c18-845">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-845">Added `marketplace` commands</span></span>
* <span data-ttu-id="62c18-846">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-846">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="62c18-847">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-847">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="62c18-848">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-848">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="62c18-849">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-849">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="62c18-850">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-850">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="62c18-851">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-851">Container</span></span>

* <span data-ttu-id="62c18-852">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-852">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="62c18-853">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-853">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="62c18-854">内線番号</span><span class="sxs-lookup"><span data-stu-id="62c18-854">Extension</span></span>

* <span data-ttu-id="62c18-855">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-855">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-856">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-856">Interactive</span></span>

* <span data-ttu-id="62c18-857">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-857">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="62c18-858">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-858">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="62c18-859">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-859">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="62c18-860">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-860">Network</span></span>

* <span data-ttu-id="62c18-861">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-861">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="62c18-862">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-862">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="62c18-863">#4910</span><span class="sxs-lookup"><span data-stu-id="62c18-863">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="62c18-864">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-864">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="62c18-865">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="62c18-865">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="62c18-866">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-866">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="62c18-867">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-867">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="62c18-868">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-868">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="62c18-869">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-869">Profile</span></span>

* <span data-ttu-id="62c18-870">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-870">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="62c18-871">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-871">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="62c18-872">RDBMS</span><span class="sxs-lookup"><span data-stu-id="62c18-872">RDBMS</span></span>

* <span data-ttu-id="62c18-873">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-873">Added `georestore` command</span></span>
* <span data-ttu-id="62c18-874">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-874">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-875">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-875">Resource</span></span>

* <span data-ttu-id="62c18-876">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-876">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="62c18-877">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-877">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-878">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-878">SQL</span></span>

* <span data-ttu-id="62c18-879">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-879">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-880">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-880">Storage</span></span>

* <span data-ttu-id="62c18-881">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-881">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-882">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-882">VM</span></span>

* <span data-ttu-id="62c18-883">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-883">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="62c18-884">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-884">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大な変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="62c18-886">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-886">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="62c18-887">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-887">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="62c18-888">#5718</span><span class="sxs-lookup"><span data-stu-id="62c18-888">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="62c18-889">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-889">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="62c18-890">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="62c18-890">March 27, 2018</span></span>

<span data-ttu-id="62c18-891">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="62c18-891">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="62c18-892">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-892">Core</span></span>

* <span data-ttu-id="62c18-893">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="62c18-893">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-894">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-894">ACS</span></span>

* <span data-ttu-id="62c18-895">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-895">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-896">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-896">Appservice</span></span>

* <span data-ttu-id="62c18-897">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-897">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="62c18-898">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-898">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="62c18-899">バックアップ</span><span class="sxs-lookup"><span data-stu-id="62c18-899">Backup</span></span>

* <span data-ttu-id="62c18-900">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-900">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="62c18-901">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="62c18-901">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="62c18-902">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-902">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="62c18-903">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-903">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="62c18-904">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-904">Container</span></span>

* <span data-ttu-id="62c18-905">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-905">Added `container exec` command.</span></span> <span data-ttu-id="62c18-906">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="62c18-906">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="62c18-907">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="62c18-907">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="62c18-908">内線番号</span><span class="sxs-lookup"><span data-stu-id="62c18-908">Extension</span></span>

* <span data-ttu-id="62c18-909">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-909">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="62c18-910">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-910">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="62c18-911">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-911">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-912">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-912">Interactive</span></span>

* <span data-ttu-id="62c18-913">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-913">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="62c18-914">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-914">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="62c18-915">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="62c18-915">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="62c18-916">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-916">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="62c18-917">ラボ</span><span class="sxs-lookup"><span data-stu-id="62c18-917">Lab</span></span>

* <span data-ttu-id="62c18-918">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-918">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-919">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-919">Monitor</span></span>

* <span data-ttu-id="62c18-920">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="62c18-920">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="62c18-921">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="62c18-921">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="62c18-922">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="62c18-922">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="62c18-923">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-923">Network</span></span>

* <span data-ttu-id="62c18-924">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-924">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="62c18-925">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-925">Profile</span></span>

* <span data-ttu-id="62c18-926">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-926">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="62c18-927">RDBMS</span><span class="sxs-lookup"><span data-stu-id="62c18-927">RDBMS</span></span>

* <span data-ttu-id="62c18-928">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-928">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-929">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-929">Resource</span></span>

* [重大な変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="62c18-931">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-931">Role</span></span>

* <span data-ttu-id="62c18-932">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-932">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="62c18-933">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-933">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="62c18-934">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-934">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="62c18-935">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-935">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="62c18-936">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-936">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-937">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-937">Storage</span></span>

* <span data-ttu-id="62c18-938">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-938">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="62c18-939">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-939">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-940">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-940">VM</span></span>

* <span data-ttu-id="62c18-941">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-941">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="62c18-942">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-942">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="62c18-943">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-943">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="62c18-944">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-944">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="62c18-945">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="62c18-945">March 13, 2018</span></span>

<span data-ttu-id="62c18-946">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="62c18-946">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-947">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-947">ACR</span></span>

* <span data-ttu-id="62c18-948">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-948">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="62c18-949">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-949">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="62c18-950">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-950">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-951">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-951">ACS</span></span>

* <span data-ttu-id="62c18-952">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-952">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="62c18-953">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-953">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="62c18-954">Advisor</span><span class="sxs-lookup"><span data-stu-id="62c18-954">Advisor</span></span>

* <span data-ttu-id="62c18-955">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-955">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="62c18-956">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-956">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="62c18-957">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-957">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="62c18-958">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-958">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="62c18-959">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-959">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-960">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-960">Appservice</span></span>

* <span data-ttu-id="62c18-961">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-961">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="62c18-962">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-962">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="62c18-963">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="62c18-963">Eventhubs</span></span>

* <span data-ttu-id="62c18-964">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-964">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="62c18-965">内線番号</span><span class="sxs-lookup"><span data-stu-id="62c18-965">Extension</span></span>

* <span data-ttu-id="62c18-966">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-966">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-967">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-967">Interactive</span></span>

* <span data-ttu-id="62c18-968">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="62c18-968">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="62c18-969">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="62c18-969">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="62c18-970">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="62c18-970">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="62c18-971">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-971">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-972">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-972">Monitor</span></span>

* <span data-ttu-id="62c18-973">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-973">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="62c18-974">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-974">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="62c18-975">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-975">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="62c18-976">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-976">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="62c18-977">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-977">Network</span></span>

* <span data-ttu-id="62c18-978">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-978">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="62c18-979">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-979">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="62c18-980">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-980">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="62c18-981">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-981">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="62c18-982">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-982">Profile</span></span>

* <span data-ttu-id="62c18-983">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-983">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="62c18-984">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-984">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="62c18-985">RDBMS</span><span class="sxs-lookup"><span data-stu-id="62c18-985">RDBMS</span></span>

* <span data-ttu-id="62c18-986">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-986">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="62c18-987">Service Bus</span><span class="sxs-lookup"><span data-stu-id="62c18-987">Service Bus</span></span>

* <span data-ttu-id="62c18-988">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-988">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-989">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-989">Storage</span></span>

* <span data-ttu-id="62c18-990">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-990">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="62c18-991">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="62c18-991">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-992">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-992">VM</span></span>

* <span data-ttu-id="62c18-993">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-993">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="62c18-994">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-994">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="62c18-995">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-995">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="62c18-996">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-996">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="62c18-997">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="62c18-997">February 27, 2018</span></span>

<span data-ttu-id="62c18-998">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="62c18-998">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="62c18-999">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-999">Core</span></span>

* <span data-ttu-id="62c18-1000">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="62c18-1000">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="62c18-1001">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1001">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="62c18-1002">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1002">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1003">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1003">ACS</span></span>

* <span data-ttu-id="62c18-1004">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1004">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="62c18-1005">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="62c18-1005">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="62c18-1006">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1006">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="62c18-1007">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1007">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1008">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1008">Appservice</span></span>

* <span data-ttu-id="62c18-1009">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="62c18-1009">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="62c18-1010">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="62c18-1010">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="62c18-1011">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="62c18-1011">Cognitive Services</span></span>

* <span data-ttu-id="62c18-1012">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1012">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="62c18-1013">消費</span><span class="sxs-lookup"><span data-stu-id="62c18-1013">Consumption</span></span>

* <span data-ttu-id="62c18-1014">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1014">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="62c18-1015">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1015">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="62c18-1016">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-1016">Container</span></span>

* <span data-ttu-id="62c18-1017">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1017">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1018">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1018">Network</span></span>

* <span data-ttu-id="62c18-1019">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="62c18-1019">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1020">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1020">Resource</span></span>

* <span data-ttu-id="62c18-1021">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1021">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="62c18-1022">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-1022">Role</span></span>

* <span data-ttu-id="62c18-1023">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1023">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-1024">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-1024">SQL</span></span>

* <span data-ttu-id="62c18-1025">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1025">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1026">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1026">Storage</span></span>

* <span data-ttu-id="62c18-1027">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1027">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1028">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1028">VM</span></span>

* <span data-ttu-id="62c18-1029">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1029">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="62c18-1030">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1030">February 13, 2018</span></span>

<span data-ttu-id="62c18-1031">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="62c18-1031">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="62c18-1032">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-1032">Core</span></span>

* <span data-ttu-id="62c18-1033">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1033">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1034">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1034">ACS</span></span>

* <span data-ttu-id="62c18-1035">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1035">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="62c18-1036">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1036">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="62c18-1037">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1037">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="62c18-1038">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1038">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="62c18-1039">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1039">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="62c18-1040">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1040">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="62c18-1041">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1041">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="62c18-1042">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="62c18-1042">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1043">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1043">Appservice</span></span>

* <span data-ttu-id="62c18-1044">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1044">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="62c18-1045">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1045">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="62c18-1046">CDN</span><span class="sxs-lookup"><span data-stu-id="62c18-1046">CDN</span></span>

* <span data-ttu-id="62c18-1047">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1047">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="62c18-1048">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-1048">Container</span></span>

* <span data-ttu-id="62c18-1049">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1049">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="62c18-1050">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1050">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="62c18-1051">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="62c18-1051">CosmosDB</span></span>

* <span data-ttu-id="62c18-1052">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1052">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="62c18-1053">内線番号</span><span class="sxs-lookup"><span data-stu-id="62c18-1053">Extension</span></span>

* <span data-ttu-id="62c18-1054">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1054">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="62c18-1055">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1055">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="62c18-1056">フィードバック</span><span class="sxs-lookup"><span data-stu-id="62c18-1056">Feedback</span></span>

* <span data-ttu-id="62c18-1057">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1057">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-1058">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-1058">Interactive</span></span>

* <span data-ttu-id="62c18-1059">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1059">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="62c18-1060">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1060">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="62c18-1061">IoT</span><span class="sxs-lookup"><span data-stu-id="62c18-1061">IoT</span></span>

* <span data-ttu-id="62c18-1062">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1062">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="62c18-1063">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1063">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="62c18-1064">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1064">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="62c18-1065">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1065">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-1066">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-1066">Monitor</span></span>

* <span data-ttu-id="62c18-1067">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1067">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1068">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1068">Network</span></span>

* <span data-ttu-id="62c18-1069">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1069">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="62c18-1070">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-1070">Profile</span></span>

* <span data-ttu-id="62c18-1071">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1071">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1072">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1072">Resource</span></span>

* <span data-ttu-id="62c18-1073">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1073">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="62c18-1074">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-1074">Role</span></span>

* <span data-ttu-id="62c18-1075">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1075">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-1076">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-1076">SQL</span></span>

* <span data-ttu-id="62c18-1077">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1077">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="62c18-1078">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1078">Added `sql db rename`</span></span>
* <span data-ttu-id="62c18-1079">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1079">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1080">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1080">Storage</span></span>

* <span data-ttu-id="62c18-1081">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1081">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1082">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1082">VM</span></span>

* <span data-ttu-id="62c18-1083">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1083">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="62c18-1084">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1084">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="62c18-1085">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="62c18-1085">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="62c18-1086">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1086">January 31, 2018</span></span>

<span data-ttu-id="62c18-1087">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="62c18-1087">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="62c18-1088">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-1088">Core</span></span>

* <span data-ttu-id="62c18-1089">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1089">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="62c18-1090">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1090">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="62c18-1091">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1091">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="62c18-1092">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="62c18-1092">Use `--verbose` to see</span></span>
* <span data-ttu-id="62c18-1093">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="62c18-1093">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1094">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1094">ACS</span></span>

* <span data-ttu-id="62c18-1095">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1095">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="62c18-1096">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1096">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1097">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1097">Appservice</span></span>

* <span data-ttu-id="62c18-1098">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="62c18-1098">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="62c18-1099">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1099">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="62c18-1100">CDN</span><span class="sxs-lookup"><span data-stu-id="62c18-1100">CDN</span></span>

* <span data-ttu-id="62c18-1101">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1101">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="62c18-1102">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="62c18-1102">CosmosDB</span></span>

* <span data-ttu-id="62c18-1103">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1103">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-1104">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-1104">Interactive</span></span>

* <span data-ttu-id="62c18-1105">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1105">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1106">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1106">Network</span></span>

* <span data-ttu-id="62c18-1107">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1107">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="62c18-1108">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1108">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="62c18-1109">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1109">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="62c18-1110">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1110">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="62c18-1111">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1111">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="62c18-1112">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1112">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="62c18-1113">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1113">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="62c18-1114">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1114">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="62c18-1115">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1115">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="62c18-1116">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1116">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="62c18-1117">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-1117">Profile</span></span>

* <span data-ttu-id="62c18-1118">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1118">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1119">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1119">Resource</span></span>

* <span data-ttu-id="62c18-1120">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1120">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1121">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1121">Storage</span></span>

* <span data-ttu-id="62c18-1122">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1122">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="62c18-1123">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1123">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="62c18-1124">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1124">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="62c18-1125">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1125">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="62c18-1126">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1126">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1127">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1127">VM</span></span>

* <span data-ttu-id="62c18-1128">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1128">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="62c18-1129">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1129">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="62c18-1130">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1130">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="62c18-1131">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1131">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="62c18-1132">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1132">January 17, 2018</span></span>

<span data-ttu-id="62c18-1133">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="62c18-1133">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-1134">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-1134">ACR</span></span>

* <span data-ttu-id="62c18-1135">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1135">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="62c18-1136">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1136">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1137">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1137">ACS</span></span>

* <span data-ttu-id="62c18-1138">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1138">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="62c18-1139">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1139">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1140">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1140">Appservice</span></span>

* <span data-ttu-id="62c18-1141">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1141">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="62c18-1142">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1142">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="62c18-1143">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1143">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="62c18-1144">バックアップ</span><span class="sxs-lookup"><span data-stu-id="62c18-1144">Backup</span></span>

* <span data-ttu-id="62c18-1145">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1145">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="62c18-1146">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1146">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="62c18-1147">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1147">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="62c18-1148">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1148">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="62c18-1149">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1149">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="62c18-1150">Batch</span><span class="sxs-lookup"><span data-stu-id="62c18-1150">Batch</span></span>

* <span data-ttu-id="62c18-1151">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1151">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="62c18-1152">クラウド</span><span class="sxs-lookup"><span data-stu-id="62c18-1152">Cloud</span></span>

* <span data-ttu-id="62c18-1153">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1153">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="62c18-1154">消費</span><span class="sxs-lookup"><span data-stu-id="62c18-1154">Consumption</span></span>

* <span data-ttu-id="62c18-1155">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1155">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="62c18-1156">Event Grid</span><span class="sxs-lookup"><span data-stu-id="62c18-1156">Event Grid</span></span>

* <span data-ttu-id="62c18-1157">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1157">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="62c18-1158">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1158">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="62c18-1159">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1159">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="62c18-1160">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="62c18-1160">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="62c18-1161">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1161">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="62c18-1162">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1162">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="62c18-1163">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1163">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="62c18-1164">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1164">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-1165">Interactive</span><span class="sxs-lookup"><span data-stu-id="62c18-1165">Interactive</span></span>

* <span data-ttu-id="62c18-1166">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1166">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="62c18-1167">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1167">Fixed errors on startup</span></span>
* <span data-ttu-id="62c18-1168">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1168">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="62c18-1169">IoT</span><span class="sxs-lookup"><span data-stu-id="62c18-1169">IoT</span></span>

* <span data-ttu-id="62c18-1170">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1170">Added support for device provisioning service</span></span>
* <span data-ttu-id="62c18-1171">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1171">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="62c18-1172">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1172">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-1173">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-1173">Monitor</span></span>

* <span data-ttu-id="62c18-1174">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1174">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="62c18-1175">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1175">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="62c18-1176">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1176">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1177">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1177">Network</span></span>

* <span data-ttu-id="62c18-1178">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1178">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="62c18-1179">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1179">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="62c18-1180">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-1180">Profile</span></span>

* <span data-ttu-id="62c18-1181">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1181">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="62c18-1182">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-1182">Role</span></span>

* <span data-ttu-id="62c18-1183">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1183">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="62c18-1184">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="62c18-1184">Service Fabric</span></span>

* <span data-ttu-id="62c18-1185">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1185">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="62c18-1186">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1186">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1187">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1187">VM</span></span>

* <span data-ttu-id="62c18-1188">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="62c18-1188">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="62c18-1189">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1189">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="62c18-1190">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1190">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="62c18-1191">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1191">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="62c18-1192">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1192">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="62c18-1193">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1193">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="62c18-1194">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1194">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="62c18-1195">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1195">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="62c18-1196">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1196">December 19, 2017</span></span>

<span data-ttu-id="62c18-1197">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="62c18-1197">Version 2.0.23</span></span>

* <span data-ttu-id="62c18-1198">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1198">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="62c18-1199">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-1199">Container</span></span>

* <span data-ttu-id="62c18-1200">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1200">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1201">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1201">Network</span></span>

* <span data-ttu-id="62c18-1202">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1202">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="62c18-1203">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1203">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1204">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1204">Storage</span></span>

* <span data-ttu-id="62c18-1205">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1205">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1206">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1206">VM</span></span>

* <span data-ttu-id="62c18-1207">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1207">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="62c18-1208">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1208">December 5, 2017</span></span>

<span data-ttu-id="62c18-1209">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="62c18-1209">Version 2.0.22</span></span>

* <span data-ttu-id="62c18-1210">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1210">Removed `az component` commands.</span></span> <span data-ttu-id="62c18-1211">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="62c18-1211">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="62c18-1212">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-1212">Core</span></span>
* <span data-ttu-id="62c18-1213">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1213">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="62c18-1214">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1214">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1215">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1215">ACS</span></span>

* <span data-ttu-id="62c18-1216">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1216">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="62c18-1217">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1217">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="62c18-1218">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1218">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="62c18-1219">Advisor</span><span class="sxs-lookup"><span data-stu-id="62c18-1219">Advisor</span></span>

* <span data-ttu-id="62c18-1220">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-1220">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1221">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1221">Appservice</span></span>

* <span data-ttu-id="62c18-1222">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1222">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="62c18-1223">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1223">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="62c18-1224">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1224">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="62c18-1225">消費</span><span class="sxs-lookup"><span data-stu-id="62c18-1225">Consumption</span></span>

* <span data-ttu-id="62c18-1226">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1226">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="62c18-1227">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-1227">Container</span></span>

* <span data-ttu-id="62c18-1228">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1228">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-1229">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-1229">Monitor</span></span>

* <span data-ttu-id="62c18-1230">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1230">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1231">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1231">Resource</span></span>

* <span data-ttu-id="62c18-1232">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1232">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="62c18-1233">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-1233">Role</span></span>

* <span data-ttu-id="62c18-1234">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1234">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="62c18-1235">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1235">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="62c18-1236">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1236">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-1237">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-1237">SQL</span></span>

* <span data-ttu-id="62c18-1238">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1238">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="62c18-1239">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1239">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1240">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1240">VM</span></span>

* <span data-ttu-id="62c18-1241">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1241">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="62c18-1242">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1242">November 14, 2017</span></span>

<span data-ttu-id="62c18-1243">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="62c18-1243">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-1244">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-1244">ACR</span></span>

* <span data-ttu-id="62c18-1245">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1245">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="62c18-1246">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1246">ACS</span></span>

* <span data-ttu-id="62c18-1247">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1247">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="62c18-1248">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1248">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="62c18-1249">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1249">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="62c18-1250">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1250">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="62c18-1251">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1251">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1252">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1252">Appservice</span></span>

* <span data-ttu-id="62c18-1253">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1253">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="62c18-1254">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1254">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="62c18-1255">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1255">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="62c18-1256">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1256">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="62c18-1257">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1257">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="62c18-1258">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="62c18-1258">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="62c18-1259">Batch</span><span class="sxs-lookup"><span data-stu-id="62c18-1259">Batch</span></span>

* <span data-ttu-id="62c18-1260">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1260">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="62c18-1261">Batchai</span><span class="sxs-lookup"><span data-stu-id="62c18-1261">Batchai</span></span>

* <span data-ttu-id="62c18-1262">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1262">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="62c18-1263">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1263">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="62c18-1264">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1264">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="62c18-1265">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1265">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="62c18-1266">クラウド</span><span class="sxs-lookup"><span data-stu-id="62c18-1266">Cloud</span></span>

* <span data-ttu-id="62c18-1267">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1267">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="62c18-1268">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-1268">Container</span></span>

* <span data-ttu-id="62c18-1269">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1269">Added support to open multiple ports</span></span>
* <span data-ttu-id="62c18-1270">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1270">Added container group restart policy</span></span>
* <span data-ttu-id="62c18-1271">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1271">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="62c18-1272">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1272">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="62c18-1273">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="62c18-1273">Data Lake Analytics</span></span>

* <span data-ttu-id="62c18-1274">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1274">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="62c18-1275">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="62c18-1275">Data Lake Store</span></span>

* <span data-ttu-id="62c18-1276">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1276">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="62c18-1277">内線番号</span><span class="sxs-lookup"><span data-stu-id="62c18-1277">Extension</span></span>

* <span data-ttu-id="62c18-1278">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1278">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="62c18-1279">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1279">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="62c18-1280">IoT</span><span class="sxs-lookup"><span data-stu-id="62c18-1280">IoT</span></span>

* <span data-ttu-id="62c18-1281">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1281">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-1282">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-1282">Monitor</span></span>

* <span data-ttu-id="62c18-1283">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1283">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1284">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1284">Network</span></span>

* <span data-ttu-id="62c18-1285">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1285">Added support for CAA DNS records</span></span>
* <span data-ttu-id="62c18-1286">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1286">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="62c18-1287">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1287">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="62c18-1288">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1288">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="62c18-1289">Reservations</span><span class="sxs-lookup"><span data-stu-id="62c18-1289">Reservations</span></span>

* <span data-ttu-id="62c18-1290">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="62c18-1290">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1291">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1291">Resource</span></span>

* <span data-ttu-id="62c18-1292">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1292">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-1293">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-1293">SQL</span></span>

* <span data-ttu-id="62c18-1294">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1294">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1295">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1295">Storage</span></span>

* <span data-ttu-id="62c18-1296">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1296">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="62c18-1297">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1297">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="62c18-1298">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1298">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="62c18-1299">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1299">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="62c18-1300">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1300">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="62c18-1301">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1301">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="62c18-1302">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1302">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1303">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1303">VM</span></span>

* <span data-ttu-id="62c18-1304">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1304">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="62c18-1305">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1305">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="62c18-1306">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1306">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="62c18-1307">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1307">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="62c18-1308">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1308">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="62c18-1309">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1309">October 24, 2017</span></span>

<span data-ttu-id="62c18-1310">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="62c18-1310">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="62c18-1311">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-1311">Core</span></span>

* <span data-ttu-id="62c18-1312">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1312">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-1313">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-1313">ACR</span></span>

* <span data-ttu-id="62c18-1314">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1314">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="62c18-1315">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1315">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="62c18-1316">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1316">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1317">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1317">ACS</span></span>

* <span data-ttu-id="62c18-1318">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1318">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="62c18-1319">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1319">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1320">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1320">Appservice</span></span>

* <span data-ttu-id="62c18-1321">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1321">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="62c18-1322">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="62c18-1322">Component</span></span>

* <span data-ttu-id="62c18-1323">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1323">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-1324">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-1324">Monitor</span></span>

* <span data-ttu-id="62c18-1325">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1325">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1326">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1326">Resource</span></span>

* <span data-ttu-id="62c18-1327">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1327">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="62c18-1328">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1328">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1329">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1329">VM</span></span>

* <span data-ttu-id="62c18-1330">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1330">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="62c18-1331">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1331">October 9, 2017</span></span>

<span data-ttu-id="62c18-1332">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="62c18-1332">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="62c18-1333">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-1333">Core</span></span>

* <span data-ttu-id="62c18-1334">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1334">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1335">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1335">Appservice</span></span>

* <span data-ttu-id="62c18-1336">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1336">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="62c18-1337">Batch</span><span class="sxs-lookup"><span data-stu-id="62c18-1337">Batch</span></span>

* <span data-ttu-id="62c18-1338">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1338">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="62c18-1339">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1339">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="62c18-1340">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1340">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="62c18-1341">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1341">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="62c18-1342">Batchai</span><span class="sxs-lookup"><span data-stu-id="62c18-1342">Batchai</span></span>

* <span data-ttu-id="62c18-1343">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-1343">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="62c18-1344">KeyVault</span><span class="sxs-lookup"><span data-stu-id="62c18-1344">Keyvault</span></span>

* <span data-ttu-id="62c18-1345">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1345">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="62c18-1346">(#4448)</span><span class="sxs-lookup"><span data-stu-id="62c18-1346">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="62c18-1347">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1347">Network</span></span>

* <span data-ttu-id="62c18-1348">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1348">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="62c18-1349">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1349">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1350">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1350">Resource</span></span>

* <span data-ttu-id="62c18-1351">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1351">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="62c18-1352">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1352">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="62c18-1353">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1353">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="62c18-1354">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1354">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-1355">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-1355">Sql</span></span>

* <span data-ttu-id="62c18-1356">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1356">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="62c18-1357">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1357">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="62c18-1358">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1358">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1359">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1359">Storage</span></span>

* <span data-ttu-id="62c18-1360">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1360">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1361">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1361">Vm</span></span>

* <span data-ttu-id="62c18-1362">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1362">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="62c18-1363">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1363">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="62c18-1364">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1364">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="62c18-1365">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1365">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="62c18-1366">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1366">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="62c18-1367">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1367">September 22, 2017</span></span>

<span data-ttu-id="62c18-1368">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="62c18-1368">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1369">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1369">Resource</span></span>

* <span data-ttu-id="62c18-1370">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1370">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="62c18-1371">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1371">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="62c18-1372">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1372">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="62c18-1373">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1373">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1374">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1374">Network</span></span>

* <span data-ttu-id="62c18-1375">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1375">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="62c18-1376">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1376">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="62c18-1377">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1377">Added `asg` application security group commands</span></span>
* <span data-ttu-id="62c18-1378">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1378">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="62c18-1379">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1379">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="62c18-1380">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1380">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="62c18-1381">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1381">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1382">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1382">Storage</span></span>

* <span data-ttu-id="62c18-1383">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1383">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="62c18-1384">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="62c18-1384">Eventgrid</span></span>

* <span data-ttu-id="62c18-1385">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1385">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-1386">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-1386">SQL</span></span>

* <span data-ttu-id="62c18-1387">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1387">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="62c18-1388">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="62c18-1388">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="62c18-1389">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1389">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="62c18-1390">KeyVault</span><span class="sxs-lookup"><span data-stu-id="62c18-1390">Keyvault</span></span>

* <span data-ttu-id="62c18-1391">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1391">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1392">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1392">VM</span></span>

* <span data-ttu-id="62c18-1393">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1393">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="62c18-1394">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1394">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="62c18-1395">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1395">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="62c18-1396">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1396">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="62c18-1397">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1397">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="62c18-1398">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1398">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1399">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1399">ACS</span></span>

* <span data-ttu-id="62c18-1400">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1400">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1401">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1401">Appservice</span></span>

* <span data-ttu-id="62c18-1402">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1402">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="62c18-1403">バックアップ</span><span class="sxs-lookup"><span data-stu-id="62c18-1403">Backup</span></span>

* <span data-ttu-id="62c18-1404">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="62c18-1404">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="62c18-1405">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1405">September 11, 2017</span></span>

<span data-ttu-id="62c18-1406">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="62c18-1406">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="62c18-1407">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-1407">Core</span></span>

* <span data-ttu-id="62c18-1408">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1408">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="62c18-1409">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1409">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1410">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1410">Acs</span></span>

* <span data-ttu-id="62c18-1411">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1411">Added `acs list-locations` command</span></span>
* <span data-ttu-id="62c18-1412">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1412">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1413">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1413">Appservice</span></span>

* <span data-ttu-id="62c18-1414">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1414">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="62c18-1415">CDN</span><span class="sxs-lookup"><span data-stu-id="62c18-1415">CDN</span></span>

* <span data-ttu-id="62c18-1416">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1416">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="62c18-1417">内線番号</span><span class="sxs-lookup"><span data-stu-id="62c18-1417">Extension</span></span>

* <span data-ttu-id="62c18-1418">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-1418">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="62c18-1419">KeyVault</span><span class="sxs-lookup"><span data-stu-id="62c18-1419">Keyvault</span></span>

* <span data-ttu-id="62c18-1420">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1420">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1421">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1421">Network</span></span>

* <span data-ttu-id="62c18-1422">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1422">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="62c18-1423">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1423">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="62c18-1424">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1424">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="62c18-1425">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1425">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="62c18-1426">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1426">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1427">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1427">Resource</span></span>

* <span data-ttu-id="62c18-1428">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="62c18-1428">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="62c18-1429">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="62c18-1429">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="62c18-1430">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="62c18-1430">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="62c18-1431">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1431">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-1432">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-1432">SQL</span></span>

* <span data-ttu-id="62c18-1433">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1433">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1434">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1434">VM</span></span>

* <span data-ttu-id="62c18-1435">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="62c18-1435">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="62c18-1436">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="62c18-1436">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="62c18-1437">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1437">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="62c18-1438">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="62c18-1438">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="62c18-1439">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="62c18-1439">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="62c18-1440">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1440">August 31, 2017</span></span>

<span data-ttu-id="62c18-1441">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="62c18-1441">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="62c18-1442">KeyVault</span><span class="sxs-lookup"><span data-stu-id="62c18-1442">Keyvault</span></span>

* <span data-ttu-id="62c18-1443">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1443">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="62c18-1444">SF</span><span class="sxs-lookup"><span data-stu-id="62c18-1444">Sf</span></span>

* <span data-ttu-id="62c18-1445">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="62c18-1445">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1446">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1446">Storage</span></span>

* <span data-ttu-id="62c18-1447">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1447">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="62c18-1448">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="62c18-1448">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="62c18-1449">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1449">August 28, 2017</span></span>

<span data-ttu-id="62c18-1450">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="62c18-1450">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="62c18-1451">CLI</span><span class="sxs-lookup"><span data-stu-id="62c18-1451">CLI</span></span>

* <span data-ttu-id="62c18-1452">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1452">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1453">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1453">ACS</span></span>

* <span data-ttu-id="62c18-1454">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1454">Corrected preview regions</span></span>
* <span data-ttu-id="62c18-1455">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1455">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="62c18-1456">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1456">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1457">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1457">Appservice</span></span>

* <span data-ttu-id="62c18-1458">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1458">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="62c18-1459">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1459">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="62c18-1460">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1460">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="62c18-1461">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1461">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="62c18-1462">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="62c18-1462">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="62c18-1463">IoT</span><span class="sxs-lookup"><span data-stu-id="62c18-1463">IoT</span></span>

* <span data-ttu-id="62c18-1464">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1464">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1465">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1465">Network</span></span>

* <span data-ttu-id="62c18-1466">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1466">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="62c18-1467">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1467">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="62c18-1468">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1468">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="62c18-1469">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1469">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="62c18-1470">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1470">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="62c18-1471">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-1471">Profile</span></span>

* <span data-ttu-id="62c18-1472">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1472">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="62c18-1473">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="62c18-1473">Service Fabric</span></span>

* <span data-ttu-id="62c18-1474">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="62c18-1474">Preview release</span></span>
* <span data-ttu-id="62c18-1475">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1475">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="62c18-1476">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1476">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="62c18-1477">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1477">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1478">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1478">Storage</span></span>

* <span data-ttu-id="62c18-1479">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1479">Enabled setting blob tier</span></span>
* <span data-ttu-id="62c18-1480">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1480">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="62c18-1481">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1481">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="62c18-1482">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1482">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="62c18-1483">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1483">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="62c18-1484">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="62c18-1484">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1485">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1485">VM</span></span>

* <span data-ttu-id="62c18-1486">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1486">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="62c18-1487">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1487">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="62c18-1488">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1488">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="62c18-1489">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1489">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="62c18-1490">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1490">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="62c18-1491">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1491">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="62c18-1492">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1492">August 15, 2017</span></span>

<span data-ttu-id="62c18-1493">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="62c18-1493">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1494">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1494">ACS</span></span>

* <span data-ttu-id="62c18-1495">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1495">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1496">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1496">Appservice</span></span>

* <span data-ttu-id="62c18-1497">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1497">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="62c18-1498">Event Grid</span><span class="sxs-lookup"><span data-stu-id="62c18-1498">Event Grid</span></span>

* <span data-ttu-id="62c18-1499">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1499">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="62c18-1500">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1500">August 11, 2017</span></span>

<span data-ttu-id="62c18-1501">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="62c18-1501">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1502">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1502">ACS</span></span>

* <span data-ttu-id="62c18-1503">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1503">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="62c18-1504">Batch</span><span class="sxs-lookup"><span data-stu-id="62c18-1504">Batch</span></span>

* <span data-ttu-id="62c18-1505">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1505">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="62c18-1506">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1506">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="62c18-1507">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1507">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="62c18-1508">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1508">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="62c18-1509">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1509">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="62c18-1510">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1510">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="62c18-1511">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="62c18-1511">Component</span></span>

* <span data-ttu-id="62c18-1512">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1512">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="62c18-1513">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62c18-1513">Container</span></span>

* <span data-ttu-id="62c18-1514">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1514">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="62c18-1515">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="62c18-1515">Data Lake Store</span></span>

* <span data-ttu-id="62c18-1516">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1516">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="62c18-1517">Event Grid</span><span class="sxs-lookup"><span data-stu-id="62c18-1517">Event Grid</span></span>

* <span data-ttu-id="62c18-1518">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-1518">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1519">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1519">Network</span></span>

* <span data-ttu-id="62c18-1520">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1520">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="62c18-1521">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1521">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="62c18-1522">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1522">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="62c18-1523">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1523">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="62c18-1524">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-1524">Profile</span></span>

* <span data-ttu-id="62c18-1525">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1525">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1526">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1526">Storage</span></span>

* <span data-ttu-id="62c18-1527">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="62c18-1527">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1528">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1528">VM</span></span>

* <span data-ttu-id="62c18-1529">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1529">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="62c18-1530">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1530">Exposed `list-skus` command</span></span>
* <span data-ttu-id="62c18-1531">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1531">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="62c18-1532">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="62c18-1532">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="62c18-1533">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1533">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="62c18-1534">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1534">July 28, 2017</span></span>

<span data-ttu-id="62c18-1535">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="62c18-1535">Version 2.0.12</span></span>

* <span data-ttu-id="62c18-1536">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1536">Added container commands</span></span>
* <span data-ttu-id="62c18-1537">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1537">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="62c18-1538">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-1538">Core</span></span>

* <span data-ttu-id="62c18-1539">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="62c18-1539">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="62c18-1540">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1540">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="62c18-1541">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="62c18-1541">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="62c18-1542">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="62c18-1542">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="62c18-1543">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="62c18-1543">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="62c18-1544">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="62c18-1544">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="62c18-1545">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="62c18-1545">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="62c18-1546">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="62c18-1546">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="62c18-1547">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="62c18-1547">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="62c18-1548">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="62c18-1548">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="62c18-1549">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="62c18-1549">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="62c18-1550">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="62c18-1550">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="62c18-1551">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1551">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="62c18-1552">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1552">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="62c18-1553">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1553">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="62c18-1554">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="62c18-1554">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="62c18-1555">ACR</span><span class="sxs-lookup"><span data-stu-id="62c18-1555">ACR</span></span>

* <span data-ttu-id="62c18-1556">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1556">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="62c18-1557">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1557">Support SKU update for managed registries</span></span>
* <span data-ttu-id="62c18-1558">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1558">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="62c18-1559">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1559">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="62c18-1560">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1560">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="62c18-1561">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1561">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1562">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1562">ACS</span></span>

* <span data-ttu-id="62c18-1563">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1563">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1564">Appservice</span><span class="sxs-lookup"><span data-stu-id="62c18-1564">Appservice</span></span>

* <span data-ttu-id="62c18-1565">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1565">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="62c18-1566">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1566">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="62c18-1567">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="62c18-1567">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="62c18-1568">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="62c18-1568">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="62c18-1569">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="62c18-1569">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="62c18-1570">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="62c18-1570">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="62c18-1571">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="62c18-1571">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="62c18-1572">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="62c18-1572">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="62c18-1573">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1573">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="62c18-1574">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="62c18-1574">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="62c18-1575">Batch</span><span class="sxs-lookup"><span data-stu-id="62c18-1575">Batch</span></span>

* <span data-ttu-id="62c18-1576">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1576">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="62c18-1577">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1577">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="62c18-1578">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1578">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="62c18-1579">CDN</span><span class="sxs-lookup"><span data-stu-id="62c18-1579">CDN</span></span>

* <span data-ttu-id="62c18-1580">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1580">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="62c18-1581">クラウド</span><span class="sxs-lookup"><span data-stu-id="62c18-1581">Cloud</span></span>

* <span data-ttu-id="62c18-1582">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1582">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="62c18-1583">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="62c18-1583">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="62c18-1584">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1584">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="62c18-1585">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1585">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="62c18-1586">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1586">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="62c18-1587">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="62c18-1587">CosmosDB</span></span>

* <span data-ttu-id="62c18-1588">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1588">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="62c18-1589">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1589">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="62c18-1590">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="62c18-1590">Data Lake Analytics</span></span>

* <span data-ttu-id="62c18-1591">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1591">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="62c18-1592">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1592">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="62c18-1593">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1593">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="62c18-1594">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="62c18-1594">Data Lake Store</span></span>

* <span data-ttu-id="62c18-1595">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1595">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="62c18-1596">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1596">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="62c18-1597">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1597">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="62c18-1598">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="62c18-1598">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="62c18-1599">対話</span><span class="sxs-lookup"><span data-stu-id="62c18-1599">Interactive</span></span>

* <span data-ttu-id="62c18-1600">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1600">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="62c18-1601">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="62c18-1601">Increased test coverage</span></span>
* <span data-ttu-id="62c18-1602">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1602">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="62c18-1603">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="62c18-1603">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="62c18-1604">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="62c18-1604">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="62c18-1605">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="62c18-1605">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="62c18-1606">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="62c18-1606">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="62c18-1607">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1607">Added `--progress` flag</span></span>
* <span data-ttu-id="62c18-1608">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1608">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="62c18-1609">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="62c18-1609">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="62c18-1610">IoT</span><span class="sxs-lookup"><span data-stu-id="62c18-1610">IoT</span></span>

* <span data-ttu-id="62c18-1611">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1611">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="62c18-1612">(#3934)</span><span class="sxs-lookup"><span data-stu-id="62c18-1612">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="62c18-1613">Key Vault</span><span class="sxs-lookup"><span data-stu-id="62c18-1613">Key vault</span></span>

* <span data-ttu-id="62c18-1614">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1614">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="62c18-1615">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="62c18-1615">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="62c18-1616">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="62c18-1616">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="62c18-1617">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="62c18-1617">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="62c18-1618">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="62c18-1618">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="62c18-1619">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="62c18-1619">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="62c18-1620">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1620">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="62c18-1621">(#3307)</span><span class="sxs-lookup"><span data-stu-id="62c18-1621">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="62c18-1622">ラボ</span><span class="sxs-lookup"><span data-stu-id="62c18-1622">Lab</span></span>

* <span data-ttu-id="62c18-1623">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1623">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="62c18-1624">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1624">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-1625">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-1625">Monitor</span></span>

* <span data-ttu-id="62c18-1626">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="62c18-1626">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="62c18-1627">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1627">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="62c18-1628">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1628">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="62c18-1629">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1629">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="62c18-1630">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1630">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="62c18-1631">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1631">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="62c18-1632">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1632">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="62c18-1633">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="62c18-1633">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="62c18-1634">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1634">`location` no longer required</span></span>
  * <span data-ttu-id="62c18-1635">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="62c18-1635">Add name and ID support for target</span></span>
  * <span data-ttu-id="62c18-1636">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="62c18-1636">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="62c18-1637">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1637">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="62c18-1638">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1638">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="62c18-1639">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="62c18-1639">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="62c18-1640">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1640">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="62c18-1641">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1641">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1642">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1642">Network</span></span>

* <span data-ttu-id="62c18-1643">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1643">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="62c18-1644">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1644">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="62c18-1645">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1645">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="62c18-1646">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1646">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="62c18-1647">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1647">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="62c18-1648">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1648">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="62c18-1649">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1649">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="62c18-1650">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1650">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="62c18-1651">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1651">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="62c18-1652">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1652">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="62c18-1653">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1653">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="62c18-1654">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1654">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="62c18-1655">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1655">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="62c18-1656">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1656">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="62c18-1657">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1657">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="62c18-1658">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1658">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="62c18-1659">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1659">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="62c18-1660">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1660">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="62c18-1661">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1661">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="62c18-1662">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1662">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="62c18-1663">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1663">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="62c18-1664">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1664">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="62c18-1665">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1665">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="62c18-1666">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="62c18-1666">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="62c18-1667">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="62c18-1667">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="62c18-1668">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="62c18-1668">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="62c18-1669">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="62c18-1669">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="62c18-1670">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-1670">Profile</span></span>

* <span data-ttu-id="62c18-1671">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1671">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="62c18-1672">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1672">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="62c18-1673">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="62c18-1673">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="62c18-1674">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1674">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="62c18-1675">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1675">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="62c18-1676">RDBMS</span><span class="sxs-lookup"><span data-stu-id="62c18-1676">RDBMS</span></span>

* <span data-ttu-id="62c18-1677">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="62c18-1677">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="62c18-1678">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="62c18-1678">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="62c18-1679">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="62c18-1679">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="62c18-1680">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="62c18-1680">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1681">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1681">Resource</span></span>

* <span data-ttu-id="62c18-1682">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1682">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="62c18-1683">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1683">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="62c18-1684">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1684">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="62c18-1685">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1685">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="62c18-1686">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="62c18-1686">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="62c18-1687">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1687">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="62c18-1688">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="62c18-1688">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="62c18-1689">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1689">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="62c18-1690">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-1690">Role</span></span>

* <span data-ttu-id="62c18-1691">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1691">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="62c18-1692">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="62c18-1692">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="62c18-1693">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="62c18-1693">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="62c18-1694">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="62c18-1694">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="62c18-1695">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1695">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="62c18-1696">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="62c18-1696">Service Fabric</span></span>
* <span data-ttu-id="62c18-1697">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="62c18-1697">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="62c18-1698">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="62c18-1698">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="62c18-1699">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="62c18-1699">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-1700">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-1700">SQL</span></span>

* <span data-ttu-id="62c18-1701">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1701">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="62c18-1702">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1702">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="62c18-1703">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1703">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1704">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1704">Storage</span></span>

* <span data-ttu-id="62c18-1705">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="62c18-1705">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="62c18-1706">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1706">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="62c18-1707">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="62c18-1707">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="62c18-1708">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="62c18-1708">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="62c18-1709">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="62c18-1709">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="62c18-1710">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="62c18-1710">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1711">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1711">VM</span></span>

* <span data-ttu-id="62c18-1712">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1712">Support configuring nsg</span></span>
* <span data-ttu-id="62c18-1713">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1713">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="62c18-1714">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="62c18-1714">Support managed service identities</span></span>
* <span data-ttu-id="62c18-1715">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1715">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="62c18-1716">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="62c18-1716">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="62c18-1717">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1717">May 10, 2017</span></span>

<span data-ttu-id="62c18-1718">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="62c18-1718">Version 2.0.6</span></span>

* <span data-ttu-id="62c18-1719">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1719">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="62c18-1720">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1720">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="62c18-1721">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1721">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="62c18-1722">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1722">Include Cognitive Services module</span></span>
* <span data-ttu-id="62c18-1723">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1723">Include Service Fabric module</span></span>
* <span data-ttu-id="62c18-1724">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="62c18-1724">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="62c18-1725">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1725">Add support for CDN commands</span></span>
* <span data-ttu-id="62c18-1726">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1726">Remove Container module</span></span>
* <span data-ttu-id="62c18-1727">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="62c18-1727">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="62c18-1728">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="62c18-1728">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="62c18-1729">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-1729">Core</span></span>

* <span data-ttu-id="62c18-1730">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="62c18-1730">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="62c18-1731">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="62c18-1731">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="62c18-1732">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="62c18-1732">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="62c18-1733">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="62c18-1733">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="62c18-1734">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="62c18-1734">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="62c18-1735">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="62c18-1735">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="62c18-1736">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="62c18-1736">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="62c18-1737">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="62c18-1737">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="62c18-1738">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="62c18-1738">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="62c18-1739">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="62c18-1739">core: Improved performance</span></span>
* <span data-ttu-id="62c18-1740">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="62c18-1740">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="62c18-1741">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="62c18-1741">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1742">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1742">ACS</span></span>

* <span data-ttu-id="62c18-1743">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1743">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="62c18-1744">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1744">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="62c18-1745">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1745">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="62c18-1746">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="62c18-1746">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1747">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-1747">AppService</span></span>

* <span data-ttu-id="62c18-1748">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1748">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="62c18-1749">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1749">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="62c18-1750">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="62c18-1750">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="62c18-1751">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1751">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="62c18-1752">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1752">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="62c18-1753">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="62c18-1753">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="62c18-1754">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="62c18-1754">support slot swap with preview</span></span>
* <span data-ttu-id="62c18-1755">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="62c18-1755">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="62c18-1756">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="62c18-1756">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="62c18-1757">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="62c18-1757">CosmosDB</span></span>

* <span data-ttu-id="62c18-1758">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1758">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="62c18-1759">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1759">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="62c18-1760">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1760">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="62c18-1761">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1761">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="62c18-1762">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="62c18-1762">Data Lake Analytics</span></span>

* <span data-ttu-id="62c18-1763">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1763">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="62c18-1764">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1764">Add support for new catalog item type: package.</span></span> <span data-ttu-id="62c18-1765">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="62c18-1765">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="62c18-1766">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="62c18-1766">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="62c18-1767">テーブル</span><span class="sxs-lookup"><span data-stu-id="62c18-1767">Table</span></span>
  * <span data-ttu-id="62c18-1768">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="62c18-1768">Table valued function</span></span>
  * <span data-ttu-id="62c18-1769">表示</span><span class="sxs-lookup"><span data-stu-id="62c18-1769">View</span></span>
  * <span data-ttu-id="62c18-1770">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="62c18-1770">Table Statistics.</span></span> <span data-ttu-id="62c18-1771">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="62c18-1771">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="62c18-1772">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="62c18-1772">Data Lake Store</span></span>

* <span data-ttu-id="62c18-1773">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1773">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="62c18-1774">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="62c18-1774">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="62c18-1775">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="62c18-1775">missed help for access show.</span></span> <span data-ttu-id="62c18-1776">追加しました </span><span class="sxs-lookup"><span data-stu-id="62c18-1776">adding it.</span></span> <span data-ttu-id="62c18-1777">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="62c18-1777">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="62c18-1778">検索</span><span class="sxs-lookup"><span data-stu-id="62c18-1778">Find</span></span>

* <span data-ttu-id="62c18-1779">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1779">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="62c18-1780">KeyVault</span><span class="sxs-lookup"><span data-stu-id="62c18-1780">KeyVault</span></span>

* <span data-ttu-id="62c18-1781">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1781">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="62c18-1782">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1782">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="62c18-1783">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="62c18-1783">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="62c18-1784">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1784">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="62c18-1785">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="62c18-1785">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="62c18-1786">ラボ</span><span class="sxs-lookup"><span data-stu-id="62c18-1786">Lab</span></span>

* <span data-ttu-id="62c18-1787">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1787">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="62c18-1788">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1788">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="62c18-1789">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1789">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="62c18-1790">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1790">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="62c18-1791">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1791">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="62c18-1792">監視</span><span class="sxs-lookup"><span data-stu-id="62c18-1792">Monitor</span></span>

* <span data-ttu-id="62c18-1793">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="62c18-1793">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="62c18-1794">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="62c18-1794">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="62c18-1795">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1795">Network</span></span>

* <span data-ttu-id="62c18-1796">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1796">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="62c18-1797">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1797">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="62c18-1798">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1798">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="62c18-1799">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1799">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="62c18-1800">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1800">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="62c18-1801">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1801">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="62c18-1802">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1802">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="62c18-1803">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1803">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="62c18-1804">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1804">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="62c18-1805">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1805">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="62c18-1806">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1806">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="62c18-1807">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1807">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="62c18-1808">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1808">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="62c18-1809">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1809">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="62c18-1810">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="62c18-1810">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="62c18-1811">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1811">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="62c18-1812">プロファイル</span><span class="sxs-lookup"><span data-stu-id="62c18-1812">Profile</span></span>

* <span data-ttu-id="62c18-1813">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="62c18-1813">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="62c18-1814">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="62c18-1814">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="62c18-1815">Redis</span><span class="sxs-lookup"><span data-stu-id="62c18-1815">Redis</span></span>

* <span data-ttu-id="62c18-1816">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1816">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="62c18-1817">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1817">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="62c18-1818">リソース</span><span class="sxs-lookup"><span data-stu-id="62c18-1818">Resource</span></span>

* <span data-ttu-id="62c18-1819">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="62c18-1819">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="62c18-1820">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="62c18-1820">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="62c18-1821">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="62c18-1821">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="62c18-1822">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="62c18-1822">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="62c18-1823">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="62c18-1823">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="62c18-1824">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="62c18-1824">Add docs for az lock update.</span></span> <span data-ttu-id="62c18-1825">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="62c18-1825">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="62c18-1826">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="62c18-1826">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="62c18-1827">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="62c18-1827">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="62c18-1828">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="62c18-1828">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="62c18-1829">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="62c18-1829">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="62c18-1830">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="62c18-1830">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="62c18-1831">Role</span><span class="sxs-lookup"><span data-stu-id="62c18-1831">Role</span></span>

* <span data-ttu-id="62c18-1832">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="62c18-1832">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="62c18-1833">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="62c18-1833">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="62c18-1834">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="62c18-1834">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="62c18-1835">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="62c18-1835">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="62c18-1836">SQL</span><span class="sxs-lookup"><span data-stu-id="62c18-1836">SQL</span></span>

* <span data-ttu-id="62c18-1837">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="62c18-1837">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="62c18-1838">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="62c18-1838">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="62c18-1839">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1839">Storage</span></span>

* <span data-ttu-id="62c18-1840">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="62c18-1840">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="62c18-1841">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1841">Add support for incremental blob copy</span></span>
* <span data-ttu-id="62c18-1842">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1842">Add support for large block blob upload</span></span>
* <span data-ttu-id="62c18-1843">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="62c18-1843">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1844">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1844">VM</span></span>

* <span data-ttu-id="62c18-1845">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="62c18-1845">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="62c18-1846">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="62c18-1846">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="62c18-1847">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="62c18-1847">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="62c18-1848">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="62c18-1848">az vm/vmss disk</span></span>
  3. <span data-ttu-id="62c18-1849">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="62c18-1849">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="62c18-1850">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="62c18-1850">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="62c18-1851">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="62c18-1851">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="62c18-1852">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1852">April 3, 2017</span></span>

<span data-ttu-id="62c18-1853">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="62c18-1853">Version 2.0.2</span></span>

<span data-ttu-id="62c18-1854">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="62c18-1854">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="62c18-1855">コア</span><span class="sxs-lookup"><span data-stu-id="62c18-1855">Core</span></span>

* <span data-ttu-id="62c18-1856">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="62c18-1856">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="62c18-1857">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="62c18-1857">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="62c18-1858">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="62c18-1858">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="62c18-1859">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="62c18-1859">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="62c18-1860">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="62c18-1860">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="62c18-1861">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="62c18-1861">Add prompting for missing template parameters.</span></span> <span data-ttu-id="62c18-1862">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="62c18-1862">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="62c18-1863">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="62c18-1863">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="62c18-1864">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="62c18-1864">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="62c18-1865">ACS</span><span class="sxs-lookup"><span data-stu-id="62c18-1865">ACS</span></span>

* <span data-ttu-id="62c18-1866">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="62c18-1866">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="62c18-1867">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="62c18-1867">Add support for ssh key password prompting.</span></span> <span data-ttu-id="62c18-1868">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="62c18-1868">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="62c18-1869">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="62c18-1869">Add support for windows clusters.</span></span> <span data-ttu-id="62c18-1870">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="62c18-1870">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="62c18-1871">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="62c18-1871">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="62c18-1872">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="62c18-1872">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="62c18-1873">AppService</span><span class="sxs-lookup"><span data-stu-id="62c18-1873">AppService</span></span>

* <span data-ttu-id="62c18-1874">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="62c18-1874">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="62c18-1875">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="62c18-1875">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="62c18-1876">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="62c18-1876">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="62c18-1877">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="62c18-1877">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="62c18-1878">DataLake</span><span class="sxs-lookup"><span data-stu-id="62c18-1878">DataLake</span></span>

* <span data-ttu-id="62c18-1879">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-1879">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="62c18-1880">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="62c18-1880">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="62c18-1881">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="62c18-1881">DocuemntDB</span></span>

* <span data-ttu-id="62c18-1882">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="62c18-1882">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="62c18-1883">VM</span><span class="sxs-lookup"><span data-stu-id="62c18-1883">VM</span></span>

* <span data-ttu-id="62c18-1884">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="62c18-1884">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="62c18-1885">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="62c18-1885">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="62c18-1886">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="62c18-1886">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="62c18-1887">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="62c18-1887">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="62c18-1888">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="62c18-1888">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="62c18-1889">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="62c18-1889">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="62c18-1890">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="62c18-1890">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="62c18-1891">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="62c18-1891">February 27, 2017</span></span>

<span data-ttu-id="62c18-1892">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="62c18-1892">Version 2.0.0</span></span>

<span data-ttu-id="62c18-1893">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="62c18-1893">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="62c18-1894">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="62c18-1894">Container Service (acs)</span></span>
- <span data-ttu-id="62c18-1895">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="62c18-1895">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="62c18-1896">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="62c18-1896">Networking</span></span>
- <span data-ttu-id="62c18-1897">Storage</span><span class="sxs-lookup"><span data-stu-id="62c18-1897">Storage</span></span>

<span data-ttu-id="62c18-1898">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="62c18-1898">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="62c18-1899">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="62c18-1899">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="62c18-1900">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="62c18-1900">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="62c18-1901">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="62c18-1901">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="62c18-1902">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="62c18-1902">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="62c18-1903">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="62c18-1903">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="62c18-1904">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="62c18-1904">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="62c18-1905">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="62c18-1905">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="62c18-1906">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="62c18-1906">Provide feedback from the command line with the `az feedback` command</span></span>

